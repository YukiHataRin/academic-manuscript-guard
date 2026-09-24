# Scientific figures and hybrid reconstruction

Use for manuscript figure work requested by the user. Preserve the selected visual direction while checking scientific meaning against the actual method, code and recorded evidence. A visually convincing generated diagram is a design reference, not a source of scientific facts.

## Choose the appropriate representation

- **Measured results:** use the recorded dataset or experiment outputs and deterministic plotting tools. Preserve selection rules, units, reference populations, aggregation and uncertainty. Generated images must not fabricate curves, distributions, trajectories, comparisons or experimental observations.
- **Method and concept illustrations:** generated pictorial assets may depict schematic anatomy, materials or processes. Distinguish these illustrations from measured results and actual dataset examples in the caption/body or an appropriate figure note.
- **Editable diagrams:** native SVG/TikZ or another vector format works for labels, boxes and connections. When the user requests generated illustrations plus vector annotations, retain the illustrations; do not replace every pictorial asset with generic vector icons or stick figures merely for convenience.
- **Existing source figures:** preserve provenance and inspect usage rights before reusing third-party material. A citation alone does not establish permission. Dataset examples and generated illustrations need distinct source records.

Read the available image-generation skill before using its tools. Follow its supported edit, reference-image and save-path workflow. Use the available PDF skill when producing or editing a PDF deliverable. These are conditional capabilities, not dependencies of ordinary prose review. If a capability is unavailable, report that limit and continue independent work; do not silently substitute a different generation service.

## Generated design → editable hybrid figure

For requests such as “generate a labelled Nature-style draft, then rebuild its text and boxes in SVG,” use this sequence:

1. **Map the content first.** Extract the real modules, input/output data, condition paths, tensor dimensions when useful, losses, frozen/trainable components and train/inference boundary. Record consequential unknowns instead of inventing connections. Take terminology from the current implementation/manuscript, not abandoned proposals.
2. **Generate a labelled design concept.** Provide labels in the user's chosen language and a concise style specification. A restrained scientific-journal aesthetic may use white space, a limited palette and thin outlines; it does not require a journal logo or imply affiliation. Keep this concept as a versioned reference.
3. **Compare it region by region.** Separate acceptable visual choices from factual errors. Check modules, arrow directions, correction types, loss names and training responsibility. Preserve attractive composition and pictorial style where compatible with the evidence; correct the meaning even if the design must change.
4. **Prepare reusable illustration assets.** With the image tool, obtain individual assets or an illustration-only underlay retaining the chosen style. Remove raster labels, panel borders and main connector arrows that will be rebuilt. Correct misleading pictorial content too: replacing a rotation label with “translation” is insufficient if the picture still depicts a rotation. Inspect the returned image rather than assuming it obeyed the prompt.
5. **Compose the hybrid SVG.** Keep headings, labels, formulas when supported, boxes, main connectors and legends as editable vector objects. Keep the approved generated or dataset illustrations as image layers. Native SVG `text` remains editable; converting text to outlines should be a separate optional export. A raster background covered by a new SVG label is not a clean reconstruction if old lettering remains visible.
6. **Preserve portability.** Embed the approved image assets in the SVG or ship a clearly linked asset folder. Use SVG viewports/clipping for asset placement when suitable; avoid clipping relevant body parts or pictorial details. Keep the source SVG, assets, generation prompt and build procedure. Do not leave manuscript references pointing only to a transient generation location.
7. **Render and compare.** Inspect the hybrid next to the concept, then against the scientific source. Check both full size and intended printed size. If the renderer loses fonts, arrowheads, dashes or clipping, change or repair the rendering path; do not deliver its damaged output as equivalent to the SVG. Export a PNG preview and a PDF when requested. A PDF containing bitmap illustrations and vector text is a hybrid PDF, not a fully vector figure.
8. **Integrate within scope.** If insertion into the manuscript is requested, add the figure, caption, body introduction and semantic label, then compile and inspect the resulting pages. If the user asked for a design exercise or preview, deliver that artifact and retain the existing manuscript figure until replacement is requested. Do not create an extra approval gate for insertion already authorized by the user.

A labelled concept and a clean underlay serve different purposes. Save both when needed to show the design progression, but distinguish the final reviewed figure from discarded or inaccurate concepts. Do not regenerate a useful concept merely to repeat a step already completed in the session.

## Scientific checks that affect the drawing

Check the actual source rather than enforcing any particular architecture:

- Does a branch read the final output, an intermediate state, or noisy input? A misplaced wire changes the claimed method.
- Is a module learned, frozen, differentiable but parameter-free, or a fixed inference solver? Differentiability alone does not mean that a module has trainable parameters.
- Does a correction change rotation, translation, both, or a specified subset? The illustration and text must agree.
- Do a forward-data arrow, conditioning arrow and gradient arrow mean different things? Show their direction and legend clearly, and keep connections off text and important image details.
- Are the depicted objectives the implemented losses? Avoid replacing a specific distribution objective with generic claims such as “physical realism loss.”
- Does a solver check feasibility or establish optimality? Do not label a feasible output as globally optimal or physically executable without evidence.
- Are a frequency range, joint set or reference mask used for training different from evaluation? Keep those distinctions in the appropriate panel or body text.
- Is a single illustrative case being presented as population evidence? Preserve its selection rule and scope. A generated dancer does not demonstrate empirical improvement.

Simplification is acceptable when it preserves the reader's understanding. An overview may omit secondary paths; explain material omitted dependencies in its introduction or refer to the detailed diagram. Do not preserve a confusing connection solely to match the generated reference.

## Caption, introduction and numbering

- Follow the user's language choices for the manuscript, captions, figure labels, and explanations. These may use different languages when requested. If unspecified, preserve the existing document's conventions; do not infer a required language from examples in this skill. Address font support through suitable fonts and rendering rather than silently changing the language.
- Use a short caption stating the subject. Put the reading order, axes, symbols, units, reference lines, selection conditions, observations and interpretation in the body as needed. Avoid duplicating the full caption in prose or adding text only to increase page count.
- Explain the figure where it supports the argument. Keep schematic illustrations, measured results, inference interventions and retrained ablations distinct in their descriptions.
- In LaTeX, use `\caption`, a semantic `\label` after it, and `\ref` in prose. Reuse the manuscript's chapter-based numbering. If absent and requested, configure numbering for the actual document class: an `article` thesis may use sections as chapters, whereas `report`/`book` use chapters. Do not hard-code “Figure 3.1” into artwork or captions.
- Check the compiled figure list and references. Inspect readability, image scaling, floating placement, legends, cropping and page breaks. Preview-only figure files do not mean figures have been inserted into the manuscript.

## Deliver and report

Preserve a concise provenance record: source evidence or asset origin, prompts for generated material, which layers are vector versus raster, factual corrections to the concept, and the checks actually performed. Keep production history in the figure source record rather than narrating it in the thesis; retain disclosures necessary to identify schematic or generated content.

Link the editable source and requested export. State whether the manuscript was updated or the result is a preview. Apply the skill's scientific-fidelity and manuscript-voice review to new captions and introductions, with reviewer agents when available and permitted. Do not claim that visual QA verifies the underlying experiment or guarantees publication acceptance.
