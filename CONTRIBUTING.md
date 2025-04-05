# Contributing to Boot Firmware

Thank you for your interest in contributing to the Boot Firmware repository! This project is critical for ensuring secure boot functionality across a wide range of SoCs. To maintain high standards and ensure security, please follow these guidelines when contributing.

## Getting Started

1. **Understand the Project**: Familiarize yourself with the repository structure, purpose of the firmware, licensing and redistribution conditions of the firmware.
2. **Security First**: Contributions must prioritize security and follow best practices for secure boot implementations.

## Contribution Process

1. Contribution is via mailing list <boot-firmware@vger.kernel.org>. Send the binaries using git send-email or send a git pull request
2. Commit message should include information about the source of the firmware and sha512sum of the files being added.
3. See README.md for folder hierarchy, make sure to add `WHENCE` and `LICENSE` files
4. All submissions should provide proof of authenticity of the firmware. 

## Providing authenticity of the firmware
Given that these firmwares maybe part of secure boot chain, its important that this repository only host legitimate versions of the firmwares. 
Thus, contributors are required to provide some proof of authenticity of the firwmares by:
1. Pointing to a URL of website hoisting the firmware and its License. Such websites should use secure protocol like https:// and clearly show how they are assosicated with vendor of the SoC, board or the product.
2. Your commit **must** contain a `Signed-Off-By:` from someone authoritative on the licensing of the firmware in question (i.e. from within the company that owns the code).
3. Submissions should be signed with GPG keys (Both pull request and direct git send-email submissions). This helps maintainers verify that the firmwares are indeed from intended legitimate source. See Linux kernel PGP [guide](https://docs.kernel.org/process/maintainer-pgp-guide.html) on how setup such keys and sign a submission. This step is optional if authors can satisfy first condition above.

## Security Guidelines

- **Do not introduce hardcoded keys or secrets**.
- Its almost impossible for anyone to delete the firmwares once released in public (either on mailing list or public git hosting), so authors need to ensure the firmwares being submitted are redistributable and are not subject to any non-disclosure clauses.
-  Don't send any `CONFIDENTIALITY STATEMENT` in your e-mail, patch or request. Otherwise your firmware _will never be accepted_.


## Reporting Issues

If you discover a bug or security vulnerability, please report it responsibly:
- Report issues to maintainers privately and don't disclose directly on the mailing lists.

## Licensing

By contributing, you agree that the firmwares are redistributable under appropriate licenses.

Thank you for helping make this project secure and reliable!