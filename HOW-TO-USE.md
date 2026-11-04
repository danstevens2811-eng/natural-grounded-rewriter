# Using Natural Grounded Rewriter 2.1

## Applications that support SKILL.md folders

Import or copy the `natural-grounded-rewriter` folder using your application's supported skill mechanism. Its entrypoint is `SKILL.md`. Keep its references, evaluation resources, and agents folder together. Do not upload only the entrypoint if the host cannot retrieve the linked references.

On compatible hosts, the description enables automatic discovery for relevant requests; the optional Codex metadata permits implicit invocation. Auto-discovery depends on the host. You can explicitly request: “Use natural-grounded-rewriter to rewrite the following text.”

## Other LLM interfaces

Use `PORTABLE-LLM-INSTRUCTIONS.md` as project/custom instructions when the host permits its length. Alternatively, attach it and explicitly say: “Use the attached Natural Grounded Rewriter instructions for this task.” Then provide the source and any audience, purpose, voice, length, and output-format requirements.

For an API, the same file can be placed in the application's supported instruction message, with the writing task and source supplied separately in the user message. This is a prompt-based skill, not executable program code; it requires no Python runtime or external service.

If your host has a smaller instruction limit, attach the file as a reference and tell the model to read and apply it. If it cannot access attachments or fit the instructions in context, this package cannot guarantee full execution there. Do not silently trim required rules and call the shortened prompt equivalent.

## Example invocation

Use Natural Grounded Rewriter. Rewrite the text below for a professional audience, preserving all facts, qualifications, citations, and links. Keep my original voice and return only the revised text.

[Paste source text here.]

## Preservation and status

The original Version 2.1 document is preserved byte-for-byte in `natural-grounded-rewriter/references/version-2.1-original.md`. The standalone prompt also contains its exact bytes between explicit markers. The folder references are verbatim section extracts with line endings normalized. Added entrypoint and usage material provide execution and routing only.

`package-manifest.json` records SHA-256 digests and the section mapping. Packaging validation is separate from behavioral testing. No rewriting-quality score, detector guarantee, or universal automatic activation is claimed. This delivery does not install anything in an application.
