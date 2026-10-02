# Bolt.new vs. AI Studio Comparison

Bolt.new and AI Studio were both considered for the F-06 exportable skill summary. The same project context and F-06 instruction were used for the comparison.

Bolt.new produced an implementation of F-06. The implementation was preserved in `delegated/bolt-001.zip` before review. It added the export summary interface and summary-generation logic while continuing to use the existing Worker/D1 evidence-log architecture. The delegated output was then inspected against the acceptance criteria, security checks, dependencies, and design standards. Manual testing confirmed that all four F-06 EARS rows passed. The review also identified a tooling issue with the original npm test script, which was corrected, and an AC-10 automated test was added.

AI Studio was also attempted using the same F-06 context and instruction, but it returned `Request contains an invalid argument` before producing an implementation. A minimal test request also returned the same error. Because no AI Studio implementation was generated, an implementation-level comparison of its code, dependencies, storage, styling, or security patterns was not possible.

Therefore, the comparison is limited to the observed delegation results: Bolt.new produced a reviewable implementation that could be tested and corrected, while AI Studio did not produce an implementation during the attempted comparison. No conclusion is made about AI Studio's code quality because there was no AI Studio code to evaluate.
