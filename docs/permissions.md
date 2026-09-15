# Component license review

Reviewed on 16 September 2026 for European Vanilla+ v1.0.0. Redux sources are pinned to [`e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a`](https://github.com/ShadowOne333/Metroid-Fusion-Redux/tree/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a).

## Result / Esito

Redux expressly declares its project GPLv3. The original European integration and tools are offered under GPL-3.0-only. However, the reviewed public sources do not independently establish the original authors' grants for every included third-party component. This review therefore does not establish complete permission coverage for public redistribution of the combined patch.

Redux dichiara espressamente la GPLv3 per il progetto; l'integrazione europea originale e gli strumenti sono distribuiti sotto GPL-3.0-only. Non sono però emersi permessi autonomi e chiari di tutti gli autori dei contributi inclusi. La verifica non consente quindi di dichiarare chiarita ogni autorizzazione per la ridistribuzione pubblica della patch completa. Per Piggy Chan! esiste una risposta favorevole al lavoro specifico di ShadowOne333, ma non una licenza esplicita per il riuso da parte di terzi.

Missing public evidence is not proof that an author prohibited reuse, that no private permission exists, or that Redux's GPL declaration is invalid. This is a record of the evidence found, not legal clearance. Attribution and downloadable source are not, by themselves, permission grants.

## Included components

“Redux GPLv3” below means an express project-level offer permitting copying, modification and distribution under its terms. “Unresolved” means no independent original-author grant covering downstream modification and redistribution was located.

| Component | Author / provenance | Modification and redistribution evidence |
| --- | --- | --- |
| Color Palette Improvement, including its suit palettes | Piggy Chan!, [original patch 8122](https://www.romhacking.net/hacks/8122/) | Unresolved. Original package has no license or reuse grant. Favorable forum response to Shadow's port does not state general downstream terms. |
| European palette address map / port | ShadowOne333, [EU source](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/ColorImprovement/color_improvement_eur.asm) | Redux GPLv3 for the project and Shadow's contribution. This is not independent evidence of Piggy's grant for the imported palette material. |
| Fast Text | SpineShark, [source block](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L114-L126) | Redux GPLv3; original-author grant unresolved. |
| Faster Door Transitions | Jumzhu, [original resource](https://metroidconstruction.com/resource.php?id=414) | Original page has no explicit reuse terms. Redux GPLv3 for the later source; original-author grant unresolved. |
| Odd-distance door-transition correction | Upstream credit: somerando(caauyjdp), [source](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_door_transitions.asm) | Redux GPLv3; original-author grant unresolved. |
| Faster Elevators | interdpth, [source](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/faster_elevators.asm) | Redux GPLv3; original-author grant unresolved. |
| New European Start-to-skip intro hook | Bruc3Dev573; behavior referenced from Redux and yohann's research | Original local implementation under GPL-3.0-only; modification and redistribution permitted under that license. The Japanese binary hook was not copied. |

The separate [Better Suits Colours patch 7473](https://www.romhacking.net/hacks/7473/) is not included. Its terms cannot establish permission for patch 8122.

## Piggy Chan!: original package and forum

The [author's project thread](https://www.romhacking.net/forum/index.php?action=printpage;topic=37317.0) identifies the Fusion release as patch 8122 on 7 October 2023. The original release page was inaccessible during this review. Its package was recovered from a [public mirror of the August 2024 RHDN export](https://mir.natalie.ee/vgm/dustinodellofficial/rhdn_20240801.zip) using byte ranges, without downloading the full collection.

Relevant export members:

- `hacks/gba/patches/[8122]Metroid Fusion Color Improvement.zip`
- `hacks/gba/patches/8122readme.txt`

The recovered inner ZIP contains only `Metroid Fusion Color Improvement.ips` (25,355 bytes) and `readme.txt` (1,187 bytes). The internal readme is byte-identical to the separate export readme. No license file or permission grant appears in either member. The readme states:

> This patch is in no way affiliated with the "Special Edition" hack, or the "Better Suit Colors" hack, both of which make various changes to the game's visuals.

It targets `Metroid Fusion (USA, Australia)` and says:

> It will not work with other versions of the game. A patch for the EU version of the game may happen in the future.

This describes technical compatibility and an author's plan, not permission to make or distribute a port.

Recovered-file SHA-256 values:

```text
Patch ZIP: 88600467c42323d9927a370f57185c20627c4a49091d9ecf06cdbf410b283535
readme:    a272e21781da614727c6e5b7e675d4c88686d6ec6ee74ebb1182aeee058e00d5
IPS:       760b01db94cdcbf943d944e6348c7a33a282f31245b4cab3c77b7bd6d4c7c67e
```

[Internet Archive's export metadata](https://archive.org/metadata/romhacking.net-20240801) records `rhdn_20240801.zip` as 12,573,450,015 bytes, matching the mirror's listed size. The full mirror was not hashed; identity with the official full-archive checksum is not asserted.

The forum provides additional evidence that must not be omitted:

- On 4 September 2025 Shadow asked to use the Zero Mission patch as a base, then separately asked about porting Fusion.
- On 6 September Piggy replied, “Hello, I would be flattered if you used it as a base for your own work!” The next paragraph begins, “As for the Fusion patch, I still plan on porting it to the EU version of the game, but I can make no promises on anything more than that.” The scope of the first sentence should not be presented as an unambiguous Fusion-specific downstream license.
- After Shadow announced his completed disassembly and ports in November, Piggy replied on 21 November: “Wow, that is amazing, Shadow!” This supports favorable awareness of Shadow's work, but states no transferable license, relicensing authority or downstream redistribution terms.

The EU source credits both authors and imports palette blobs derived from Piggy's patch. Shadow's address map does not remove that underlying provenance. A clear Fusion-specific grant covering downstream modification, redistribution and GPL-compatible use would resolve the remaining uncertainty.

## QoL contributions

### Fast Text

The source says `By SpineShark`. Shadow introduced it in commit [`3a7261b`](https://github.com/ShadowOne333/Metroid-Fusion-Redux/commit/3a7261b8bc435aed63cb71c3342137fb75ae7d9f), “Add Fast Text hack by SpineShark”. No separate author-controlled archive, license or public permission statement was located. The express terms found are Redux's project-level GPL declaration.

### Faster Door Transitions and correction

The [archived original Jumzhu resource page](https://web.archive.org/web/20240205201918id_/https://metroidconstruction.com/resource.php?id=414) identifies the author, release date of 30 August 2018 and a bare IPS download. It says “Speeds up door transitions dramatically.” It displays no license or explicit modification/redistribution grant. The IPS itself was not inspected in this licensing review.

The Redux source separately says `Following fixes by somerando(caauyjdp)`. Both the original door code and correction were present in Shadow's [initial source import](https://github.com/ShadowOne333/Metroid-Fusion-Redux/commit/44222baffb477b379f4e961d14381351b371b82c). No independent permission statement from either credited author was located.

### Faster Elevators

The source says `Original code by interdpth, ported to MF_J by ShadowOne333`, introduced in commit [`e41e779`](https://github.com/ShadowOne333/Metroid-Fusion-Redux/commit/e41e7797b2d7d35d6b64f3e8b178ffdb31c109c4). The checked [archived interdpth resource listing](https://web.archive.org/web/20240205201555id_/https://metroidconstruction.com/resources.php?search=author%3Ainterdpth) lists only an unrelated Crocomire resource. [GBATroid-patches](https://github.com/interdpth/GBATroid-patches) supplies neither elevator code nor a license. No original elevator grant was located.

A [separate MARS elevator implementation](https://github.com/MetroidAdvRandomizerSystem/mars-fusion-asm/blob/3cb7ffb4b711aeed8c14d5067e996d0fa0df5301/src/qol/fast-elevators.s) has an explicit MPL-2.0 notice and a later GPLv3 history. It is not the provenance used for this release and does not establish interdpth's permission. No implementation was replaced during this review.

## European intro hook

The [Japanese Redux reference](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/code/misc.asm#L4-L6) is covered by Redux's project declaration. Redux credits yohann for finding the enabling value; no separate yohann grant was located.

The released European hook is a new implementation, not a copy of that Japanese instruction. Its assembly is included in `patches/vanilla-plus-eu.json` in the corresponding-source archive, and its original code is licensed as stated in [NOTICE](../NOTICE). Research or an abstract behavior is not treated here as copied code merely because a separate author license was not found.

The [MIT-licensed metroidret/mf decompilation](https://github.com/metroidret/mf/blob/b17cfedb4d886c59ee23f3e402bc26b249b59f17/LICENSE) was a technical reference for native game behavior, not the source of a copied intro-skip implementation. Its license is not presented as permission for unrelated Redux contributions. No identity between its credited YohannDR and Redux's yohann is assumed.

## Confirmed Redux declaration and obligations

The [pinned Redux README](https://github.com/ShadowOne333/Metroid-Fusion-Redux/blob/e7da0d65bb3186e6ed2a5ec02d9602213bf3c79a/ReadMe.md#license) states:

> Metroid Fusion Redux is a project licensed under the terms of the GPLv3, which means that you are given legal permission to copy, distribute and/or modify this project, as long as:
>
> 1. The source for the available modified project is shared and also available to the public without exception.
> 2. The modified project subjects itself different naming convention, to differentiate it from the main and licensed Metroid Fusion Redux project.
>
> You can find a copy of the license in the LICENSE file.

The complete [GPLv3 text](Metroid-Fusion-Redux-LICENSE.txt) and [upstream README](Metroid-Fusion-Redux-README.txt) are preserved verbatim. Relevant GPL obligations include retaining applicable copyright, license and warranty notices (§4), marking modifications and their date and licensing covered modified work under the GPL (§5), and providing Corresponding Source through an applicable §6 method when distributing non-source form. The quoted public-source and distinct-name wording comes from the Redux README and is preserved as written.

Vanilla+ uses a different name, records the September 2026 European modifications in NOTICE, and supplies its specification, assembly and build tools in the standalone source archive beside the IPS. These measures address packaging and source access; they do not independently resolve the original-author evidence gaps. When offering a public release, ensure the corresponding source is accessible to its recipients and account for the upstream README's public-source wording.

## Remaining questions and limits

Before describing all included contributions as cleared for public redistribution, obtain or locate documented terms covering Piggy Chan!, SpineShark, Jumzhu, somerando(caauyjdp) and interdpth. Evidence could come from original author notices or documented permissions held by Redux; the absence of a separate license file does not rule those out. Any grant must cover the actual material and intended modification/redistribution, including compatibility with the combined project's license. An independently written replacement would be a separate implementation change, not a result of this documentation review.

Current RHDN download pages and Metroid Construction resources returned access errors; the review used the recovered RHDN package, accessible forum, archived resource pages, pinned Redux sources and public commit/issue history. No relevant public contributor assent was located in the checked history. These searches cannot exclude private or unindexed agreements. No authors were contacted.

No permission discussed here grants rights to distribute Nintendo's game ROM or unrelated game content. No ROM is included. The report does not decide whether another legal basis applies to a particular contribution.
