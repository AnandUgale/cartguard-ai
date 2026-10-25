# Third-party components

CartGuard application source is MIT licensed. Dependencies retain their own licenses in `node_modules` and the lockfile records exact versions.

- Transformers.js: Hugging Face, Apache-2.0, https://github.com/huggingface/transformers.js
- all-MiniLM-L6-v2: Sentence Transformers, Apache-2.0, https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2
- ONNX conversion: Xenova, Apache-2.0, https://huggingface.co/Xenova/all-MiniLM-L6-v2, revision `751bff37182d3f1213fa05d7196b954e230abad9`. Four unmodified pinned assets are bundled in `models/minilm/` for local-only execution. Their Apache-2.0 license, attribution/provenance and checked SHA-256 manifest are included there; they are not relicensed as MIT application code. See linked model cards for training provenance and limitations.
- ONNX Runtime and other transitive packages: see the respective installed package license files. No third-party retailer catalog, private imagery or commercial product data is used.

PayPal is a trademark of its owner. This prototype is not affiliated with or endorsed by PayPal. Its REST adapter is permanently restricted to the sandbox endpoint.
