# ClaudeBLDSkill
> **Status**: VALIDATED

**Cost**: B + D×L = 20 + 9×0.575 = 25.178

---

## Structure

```
structure ClaudeBLDSkill

B workflow: write_bld | run_parse | run_cost | iterate
  write_bld -> articulate_formally, not_prose, file(<name>.bld)
  run_parse -> bld_parse, see_structure, verify_articulation
  run_cost -> bld_cost, measure_alignment, check_DxL
  iterate -> refine_articulation, match_reality
B question: q1_partition | q2_connection | q3_repetition
  q1_partition -> ask("Where does behavior partition?"), find(B)
  q2_connection -> ask("What connects to what?"), find(L)
  q3_repetition -> ask("What repeats?"), find(D)
B primitive: boundary | link | dimension
  boundary -> topological, invariant_under_D, local_scope
  link -> geometric, scales_with_D, can_span_distance
  dimension -> multiplier_on_L, not_on_B
B tool: parse | cost | doc | run | compile
  parse -> see_structure, normalize, verify
  cost -> measure_alignment, B_plus_DxL
  doc -> generate_documentation, bld_all_the_way_down
  run -> execute, traverse
  compile -> binary, optimize
B epistemic: validated | derived | mechanism | exploratory | foundational
  validated -> empirical_tests_pass, quantitative_metrics
  derived -> mathematical_proof, follows_from_BLD
  mechanism -> structure_identified, values_TBD
  exploratory -> hypothesis, needs_testing
  foundational -> core_definition, axiomatic

L workflow_seq: write_bld -> run_parse -> run_cost -> iterate (deps=1, sequential=true)
L apply_questions: system -> structure (deps=1)
L extract_B: system -> boundaries (deps=0)
L extract_L: system -> links (deps=0)
L extract_D: system -> dimensions (deps=0)
L validate: hypothesis -> evidence (deps=1)
L compensate: L -> B_deficiency (deps=1, direction=forward_only)
L load_domain: question -> domain (uses=domains/*.bld, deps=0)

D domains: N [parallel, lazy]
D questions: 3 [sequential]
D primitives: 3 [parallel]

returns: StructuralAnalysis
```

## Boundaries (B)

| Boundary | Partitions | Properties |
|----------|------------|------------|
| workflow | write_bld \| run_parse \| run_cost \| iterate | topological |
| question | q1_partition \| q2_connection \| q3_repetition | topological |
| primitive | boundary \| link \| dimension | topological |
| tool | parse \| cost \| doc \| run \| compile | topological |
| epistemic | validated \| derived \| mechanism \| exploratory \| foundational | topological |

## Links (L)

| Link | Source | Target | deps | Attributes |
|------|--------|--------|------|------------|
| workflow_seq | write_bld | run_parse -> run_cost -> iterate | 1 | sequential=true |
| apply_questions | system | structure | 1 |  |
| extract_B | system | boundaries | 0 |  |
| extract_L | system | links | 0 |  |
| extract_D | system | dimensions | 0 |  |
| validate | hypothesis | evidence | 1 |  |
| compensate | L | B_deficiency | 1 | direction=forward_only |
| load_domain | question | domain | 0 | uses=domains/*.bld |

## Dimensions (D)

| Dimension | Extent | Properties |
|-----------|--------|------------|
| domains | N | parallel, lazy |
| questions | 3 | sequential |
| primitives | 3 | parallel |

## Returns

`StructuralAnalysis`

