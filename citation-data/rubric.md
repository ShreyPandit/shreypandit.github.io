# Citation impact rubric (EB1-oriented)

Goal: rate how substantively each citing paper engages with / depends on Shrey Pandit's work.

## HIGH — "builds on / needs the work"
The citing paper *uses* the work as a load-bearing component:
- Evaluates its models/methods ON the benchmark or dataset (FaithEval, MedHallu, CodeUpdateArena, Hard2Verify, ContextualBench...), reporting numbers on it.
- Uses the released dataset/model/method/code as an ingredient of their system (trains on it, builds atop the pipeline, extends the benchmark, uses the model as baseline system they modify).
- Explicitly states their work is motivated by / a direct extension of the cited paper's findings (e.g., "following Pandit et al., we...", "we adopt the X protocol of...").
- Dedicates a section/table/substantial analysis to the work.

## MEDIUM — "substantive engagement"
- Direct comparison: discusses the work individually (not just in a grouped list), contrasts their approach with it, positions against it, discusses its findings or limitations in ≥1 dedicated sentence.
- Uses conclusions of the work to justify a design decision.
- Included as one of several baselines/benchmarks with individual discussion but not central.

## LOW — "background mention"
- Grouped citation in related work among several works, one mention, no individual discussion.
- Citing only for a general claim ("hallucination is a problem [1,2,3]").

## Verification requirements (0-hallucination policy)
Every row in the final workbook must have:
1. Citing-paper title + identifier (arXiv ID / DOI / URL) confirmed by at least one search hit.
2. The exact phrase: verbatim sentence(s) from the citing paper's indexed full text containing the reference to the cited work. If full text is not indexed/retrievable, the phrase cell says "Full text not indexed — citation confirmed via <source>" — NEVER an invented phrase.
3. An independent verification pass: quote re-found by searching a distinctive fragment of it; verdict recorded (VERIFIED / UNVERIFIED-REMOVED / METADATA-ONLY).

## Honest-coverage policy
Google Scholar reports 393 total citations (user's table, 2026-08-24). Google Scholar, Semantic Scholar,
OpenAlex and arXiv APIs are all blocked by this environment's egress policy; the only channel is a
web-search index. Coverage per paper = citations we could actually discover and verify through that
index. The workbook's Summary tab reports found/GS-count per paper explicitly, and the per-tab notes
name what could not be retrieved. No row is fabricated to close the gap.
