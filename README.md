# HQC — Cryptographic Operation Layer Stack

Interactive 3D visualization of the HQC (Hamming Quasi-Cyclic) post-quantum key encapsulation mechanism, showing the full mathematical operation stack with pseudocode. HQC is NIST's recently selected alternate post-quantum KEM standard alongside ML-KEM, based on quasi-cyclic codes rather than lattices.

**🔗 Live:** [https://secwest.github.io/hqc-stack/](https://secwest.github.io/hqc-stack/)

---

## What This Covers

### 🔐 HQC (Hamming Quasi-Cyclic)

HQC is a code-based post-quantum key encapsulation mechanism selected by NIST as a backup/diversification standard. Unlike lattice-based ML-KEM, HQC relies on the hardness of decoding random quasi-cyclic codes — a problem with over 50 years of cryptanalytic study.

This visualization breaks down the full cryptographic operation stack:

- **KeyGen** — quasi-cyclic matrix generation, sparse vector sampling, syndrome computation
- **Encapsulation** — error vector generation, Reed–Muller/Reed–Solomon encoding, ciphertext construction
- **Decapsulation** — syndrome decoding, error correction, Fujisaki–Okamoto transform
- **Underlying math** — Quasi-cyclic codes over GF(2), LRPC decoding, tensor product codes

### 📡 Applications

- **Post-quantum diversification** — Alternative to lattice-based schemes in case of lattice cryptanalysis breakthroughs
- **TLS 1.3** — Future hybrid key exchange alongside X25519
- **Long-term secrets** — Archival encryption where algorithm diversity matters
- **Government/defense** — CNSA 2.0 compliance with algorithm agility

## Tech Stack

| Component | Source |
|-----------|--------|
| Three.js r128 | cdnjs.cloudflare.com |

**Zero dependencies to install.** Single self-contained HTML file (~60 KB) with inline CSS/JS. No build step.

## See Also

- [ML-KEM Stack](https://secwest.github.io/mlkem-stack/) — Companion visualization for the primary NIST post-quantum KEM

## Run Locally

```bash
python3 -m http.server 8000
# Open http://localhost:8000
```

Or open `index.html` directly in a browser.

## License

[MIT](LICENSE)
