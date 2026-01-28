---
title: Mathematical notation in RFCs
docname: draft-rossi-mathinrfcs-00
venue:
  group: RSWG
  type: Editorial Stream Working Group
  mail: rswg@rfc-editor.org
  arch: https://mailarchive.ietf.org/arch/browse/rswg/
  github: "alexisannerossi/id-mathinrfcs"
  latest: "https://github.com/alexisannerossi/id-mathinrfcs/edit/main/draft-rossi-mathinrfcs-00.md"
stand_alone: true
v: 3
ipr: trust200902
kw: Internet-Draft
cat: info
submissionType: editorial
keyword:
 - HTML
author:
  -
    ins: A. Rossi
    name: Alexis Rossi
    organization: RFC Series Consulting Editor
    email: rsce@rfc-editor.org
  -
    ins: M. Thomson
    name: Martin Thomson
    organization:
    email: mt@lowentropy.net
  -
    ins: L. Eggert
    name: Lars Eggert
    organization:
    email: lars@eggert.org

normative:


informative:
  RFC9720:
  WAI:
    author:
      org: W3C
    title: W3C Accessibility Standards Overview
    target: https://www.w3.org/WAI/standards-guidelines/

--- abstract

This document defines policy and allows new technology for the representation of mathematical notation in RFCXML and relevant publication formats. After implementation of this policy, mathematical notation in RFCXML and the HTML publication format will no longer be accepted in Unicode or Scalable Vector Graphics (SVGs).

--- middle

# Introduction

This document allows new technology for the representation of mathematical notation in RFCXML and relevant publication formats defined in {{RFC9720}}. This document also defines policy requirements for the inclusion of mathematical content.

Mathematical notation in RFCs replaces existing practices for conveying mathematical content.  Inline ASCII and Unicode text or ASCII art and Scalable Vector Graphics (SVGs) can be replaced by native support for content that solely contains math. In HTML, native support can then be used in place of such crude alternatives; see {{guidance}} for more on this. Other publication formats may use the best solution available for displaying math. This document specifically removes support for displaying math in Unicode or SVG figures in the HTML publication format as these are not adequately accessible to all readers.

The RFC Publication Center (RPC) is responsible for tooling and implementation decisions regarding this policy. We expect the adoption of this policy to require changes and adaptation during implementation in early documents using this technology.

# Policy Requirements

* Mathematical notation should appear correctly in RFCXML, HTML and PDF publication formats, as well as any future publication formats that can support it. The RPC will determine how to best represent math in the Text publication format.
* Mathematical notation should support both “inline” and “block” form.  "Inline" refers to notation that is used as part of text (like this x) and "block" form refers to equations that might be referenced in the same way that a figure is.
* It must be possible to reference “block” form equations from the text in a way that clearly distinguishes them from references to figures (or other elements that can be referenced, such as citations). In academic writing, figures are usually referenced as “Fig. n” while equations are referenced as “Eq. n”.
* In the "block" form, equations must use the chosen math format.  ASCII art or SVG renderings of math must not be used in any format except for the Text publication format, as noted.  Incidental use of math in figures can still use textual or SVG alternatives, provided that any math content is not normatively relevant.
* Major desktop and mobile browsers must be capable of natively rendering the mathematical notation correctly in the HTML publication format.
* The chosen implementation should allow representation of both the meaning and the formatting of the mathematical content.
* Accessibility should be supported for readers of the HTML publication format who rely on various devices, software, and visual presentations (e.g. braille readers, screen readers, enlarging, and text formatting). The RPC will refer to the W3C Accessibility Guidelines {{WAI}} when making decisions regarding accessibility.

The RPC is authorized to make decisions about the representation of mathematical notation for both technical and editorial reasons in order to ensure that published RFCs meet the above policy and to provide consistency across the RFC series. The RPC must document their decisions in a public place, and all changes to tooling or implementation decisions must be widely communicated to the RFC author community using mailing lists or other means.


# Implementation Guidance {#guidance}

The RPC is expected to solicit community input before making decisions and to publicly explain their reasoning.

Documentation produced by the RPC should describe what technical and editorial constraints apply to the HTML publication format and CSS files.
That guidance should include updates to style guides to provide advice on how to decide when math forms are to be preferred over ASCII or Unicode workarounds that have been historically used in the series.
It is expected that native math support would be preferred in most cases, except for the simplest cases or to specifically support text renderings.

Where possible, implementation decisions should focus on specifying what is disallowed, rather than attempting to specify exactly what is allowed. These decisions should also consider the authoring process as a significant factor in implementation.

The RPC should periodically review and revise their practices.

# Security Considerations

This document has no security considerations.


# IANA Considerations

This document has no IANA actions.

# Acknowledgements

This document has greatly benefited from the input of Carsten Bormann who provided significant input on the early draft versions of this document.

--- back
