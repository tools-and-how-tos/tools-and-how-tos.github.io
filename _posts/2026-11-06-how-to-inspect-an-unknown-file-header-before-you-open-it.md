---
layout: post
title: "How to Inspect an Unknown File Header Before You Open It"
description: "Use a quick file-header inspection to spot a mismatched or unknown file type before opening an unexpected attachment."
date: 2026-11-06 07:32:00 +0000
categories: [tools, how-to]
tags: [file-inspection, developer-tools, security, browser-tools]
canonical_url: ""
image: "/assets/img/posts/2026-11-06-how-to-inspect-an-unknown-file-header-before-you-open-it/cover-3ff8bd4f3a1b.webp"
---

# How to Inspect an Unknown File Header Before You Open It

An unexpected attachment called `invoice.pdf` is not proof that it is a PDF. Before I open an unknown file, I inspect its first bytes, compare them with the format I expect, and stop if the evidence disagrees. A header check will not declare a file safe—but it is a fast, low-ceremony way to catch a mislabeled or simply unfamiliar file before the wrong application gets a chance to interpret it.

For a quick local look, [Tiny Online Tools’ Hex Viewer](https://tiny-online.tools/developer-tools/hex-viewer) shows offset addresses, hexadecimal bytes, and an ASCII column in the browser. It also reports common file types from magic bytes. That makes it useful for an *inspection* step; it is not a malware verdict.

![Magnifier examining a file header and simple evidence cards](/assets/img/posts/2026-11-06-how-to-inspect-an-unknown-file-header-before-you-open-it/image-01-df6abc55af2f.webp)

## What a file header can—and cannot—tell you

Many binary formats begin with a recognizable identifier, often called a magic number or file signature. A PDF normally begins with `%PDF-`; a PNG begins with the eight-byte PNG signature; a ZIP-based file begins with `PK`. Those patterns are clues about the container or format, not a promise about intent, safety, or what an application will do with it.

That distinction matters. Someone can rename an executable, a malformed file can imitate an expected header, and a valid container can still hold content you do not want to trust. Treat the extension as a label and the header as one independent piece of evidence.

If the file is a normal business artifact from a known sender and the header agrees with the expected format, you have reduced one kind of surprise. If it disagrees—or you cannot explain what you see—pause and use the organization’s normal review or security path.

## The two-minute header check

1. **Keep the original untouched.** Work from a copy if you need to investigate. Do not rename the only copy just to make it open.
2. **Start with the expected format.** Ask what the file is supposed to be: PDF, image, spreadsheet, archive, or something else. This gives you a claim to test rather than a pile of bytes to stare at.
3. **Inspect the opening bytes locally.** Open the file in the [Hex Viewer](https://tiny-online.tools/developer-tools/hex-viewer). Look at offset `00000000`, the very beginning of the file. Keep the byte display and ASCII column visible; the latter occasionally exposes a readable format marker.
4. **Compare, do not guess.** Match the first bytes against the format’s official specification or reliable documentation. The [IANA media-type registry](https://www.iana.org/assignments/media-types/media-types.xhtml) is useful when you are checking a claimed content type, but it does not replace a format specification.
5. **Choose a path.** Agreement means “continue with ordinary caution”; disagreement means “verify through a safer channel”; an unfamiliar or garbled result means “stop and escalate.”

## A small decision card for unexpected files

| What you find | Practical next step | What not to conclude |
| --- | --- | --- |
| Extension and header match the expected type | Confirm sender/context, then use the appropriate viewer | “It is definitely safe” |
| Header names another common format | Ask the sender to confirm or obtain a fresh copy | “The file is malicious” |
| Header is missing, odd, or unreadable | Preserve it and route it to your normal security/review process | “A converter will fix it” |
| File opens only after changing its extension | Stop and verify the intended format first | “The extension was the only problem” |

![Decision matrix for inspect verify or stop paths](/assets/img/posts/2026-11-06-how-to-inspect-an-unknown-file-header-before-you-open-it/image-02-e5b1b744419a.webp)

## Make the comparison repeatable

The useful habit is writing down one small receipt: claimed name, expected type, first-byte observation, source of the reference signature, and the decision. That is enough to make a support handoff or a later re-check less speculative.

For example, a supplier sends `catalog-export.pdf`, but the first bytes do not look like a PDF header. The right next move is not trying three PDF readers. It is requesting a clean export through the supplier’s established channel. Conversely, a product team that is validating source media can pair this inspection with a [camera RAW format support check](https://tools-and-how-tos.github.io/2026/11/04/how-to-test-camera-raw-format-support-before-a-browser-upload-launch/) before it commits to an upload workflow.

This same evidence-first habit helps elsewhere. Use a [suspicious email-header check](https://tools-and-how-tos.github.io/2026/11/01/how-to-check-a-suspicious-email-header-without-clicking-anything/) to understand delivery context, keep a [product photo export checklist](https://tools-and-how-tos.github.io/2026/11/01/a-practical-product-photo-export-checklist-for-shopify-listings/) for expected output, and use a [Framer responsive-export receipt](https://tools-and-how-tos.github.io/2026/11/05/framer-responsive-export-qa-a-breakpoint-receipt-you-can-hand-off/) when the problem is proving a release rather than opening a mystery file. The shared idea is simple: compare the artifact to an explicit expectation before handing it to the next tool.

## Where this workflow fails

A header check is deliberately narrow. It will not inspect encrypted content, establish provenance, validate a digital signature, find every embedded object, or replace endpoint protection and sandboxing. It is also not a reason to upload a sensitive file to an unfamiliar service.

Use it when the question is “does this look like the kind of file I was told it is?” Use dedicated security tooling and team policy when the question is “is it safe?” Those are different jobs.

![Comparing file-header patterns before opening a file](/assets/img/posts/2026-11-06-how-to-inspect-an-unknown-file-header-before-you-open-it/image-03-98ff20c3c779.webp)

## Make the first check cheap

Bookmark the [local Hex Viewer](https://tiny-online.tools/developer-tools/hex-viewer) for the next attachment whose extension does not earn your trust. Check the opening bytes, document the result, and let a mismatch change your next action. That two-minute pause is much cheaper than confidently opening the wrong thing.
