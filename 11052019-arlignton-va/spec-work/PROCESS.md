# Proposed Extensions

OGC APIs are designed to be modular. We expect new requirements will emerge with use and new features will be proposed to address those requirements. Development and validation of these new features is a community effort. Supporting that effort are two tools; a process for tracking the maturity of a proposed addition, and a means to publish the current baseline of a proposed new feature. 

## Draft Features

New features will be introduced as draft extensions. By introducing new features this way we enable them to be  designed, documented and then implemented by tools that are interested in the feature, without putting the burden of implementation on all tooling. If the feature is successfully implemented and it has demonstrable value, it will become a candidate for inclusion in a future release of the specification.

Most new features can be defined in JSON Schema or through OpenAPI extensions. These Draft Feature extensions are identified by the ``x-ogc-draft-`` prefix and can only be used where existing extensions are permitted. This ensures no existing tooling will affected by the introduction of the draft feature. If the feature is deemed appropriate for inclusion in the OGC baseline, the ``x-OGC-draft-`` prefix will be removed. Tooling that supports draft features should plan for the future removal  of the prefix.

Draft features will be documented as GitHub issues and labeled with the ``draft-feature`` label and will be initially labelled as ``draft:proposal``. When the proposal is considered sufficiently stable for pilot implementation, it will be labeled ``draft:pilot``.

If during the development of a draft feature, it is determined that the feature needs to change in a way that may break existing draft implementations, the extension name itself may be versioned with a version suffix. e.g. ``-v2``. When a draft feature becomes part of a future update to the specification any version suffix will be removed.

Draft features that are deemed not appropriate for inclusion MUST be marked with the ``draft:abandoned`` label.

Draft-features that are considered suitably specified and have had successful pilot implementations will be marked with the ``draft:graduated`` label.

Not all future new features will be introduced in this way. Some new features impact the specification in ways that cannot be encapsulated in an extension. However, where a new feature can be introduced in this way, it should be.

## Publishing Draft Features

Draft Features are matured and validated through community efforts. This requires that there is a authoritative published description of the current version of each draft feature. The following procedures govern the creation and maintenance of those descriptions.

. The definitions of a draft feature should be avalable under the ``spec-work`` directory on the GitHub site.
. The definition of each draft feature shall reside in a subdirectory of ``spec-work``. That subdirectory shall have a name indicative of the nature of the draft feature.
. This definition shall provide an exact description of the changes to the contents of the specification required to support the new feature. That description should include a extract of each section of the specification which is impacted by the proposal with all proposed modifications applied. 
. Each draft feature shall be described in a description document using the template provided by the 0000_proposal-template.md file.
. The draft feature description documents shall reside in the ``spec-work`` directory

A proposed extension to OpenAPI to support alternative schema has been included as an example.




