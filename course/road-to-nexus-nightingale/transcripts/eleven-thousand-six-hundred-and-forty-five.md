# Eleven Thousand Six Hundred and Forty-Five

**The Orphan Intelligence Project**  
A NEXUS Nightingale research podcast  
Recorded 6 November 2026  
Host: Sabre  
Style: long-form, conversational, evidence-first  
Scope: research update, not medical advice

---

**Update, 11 November 2026:** This episode is a 6 November 2026 snapshot. The current programme has five benchmark dossiers — Dengue, Friedreich ataxia, NSCLC, Gaucher and Fabry — and the current pipeline has fourteen stages. The counts in the episode remain the record of that date.

**SABRE:**

Eleven thousand six hundred and forty-five.

That’s the number that changed how I think about this project.

Not eleven thousand six hundred and forty-five dollars. Not lines of code. Eleven thousand six hundred and forty-five clinical entities in the Orphanet catalogue — rare diseases, disease groups, subtypes, syndromes, the whole messy map of conditions that most of the world has never heard of.

And behind every one of those numbers is a person. Usually a family. Usually a long diagnostic odyssey. Usually a doctor saying, “I’ve never seen this before.” Usually a research literature that is thin, scattered, or locked behind a paywall. Usually no treatment.

That’s the world the orphan intelligence project is trying to serve.

My name is Sabre. This is the story of what we built, what it actually does, what it refused to do, and where it goes next.

Let’s start with the problem.

When people hear “rare disease,” they often think “small problem.” The opposite is true. There are thousands of rare diseases. Taken together, they affect hundreds of millions of people worldwide. But each one is rare enough that the market often ignores it, the literature is fragmented, and the research community is small.

A scientist working on one of these diseases can spend weeks just assembling the basics. What is the gene? What is the protein? Which variants are pathogenic? What structures exist? Which trials are running? What drugs are approved? What has failed? What is the evidence for a mechanism? What would a good experiment look like?

That’s not glamorous work. It’s the work that determines whether anything else is possible.

And here’s the thing: most of that information exists. It’s in Orphanet, in OMIM, in ClinVar, in UniProt, in the PDB, in ClinicalTrials.gov, in PubMed, in a hundred papers that use a hundred different names for the same disease.

The problem is not that the information doesn’t exist. The problem is that it isn’t assembled in a form a scientist can use quickly, with provenance, uncertainty and a clear next question.

That is the gap we set out to fill.

Now, I want to be clear about what this project is not.

It is not a diagnostic. It is not a treatment recommendation. It is not a replacement for a clinician. It is not a machine that looks at a disease name and invents a drug.

The first version of the orphan intelligence console is a research instrument. It assembles evidence, shows its sources, labels its uncertainty, and proposes hypotheses that a scientist can test.

The scientist leads. The system organises.

That distinction matters, because it determines everything about how we built it.

Let’s talk about the catalogue.

We used Orphanet, through the Orphadata API. It’s an authoritative rare-disease nomenclature, and it’s available under a CC-BY-4.0 licence. We ingested every clinical entity the cross-referencing endpoint returned: eleven thousand six hundred and forty-five.

Every one gets a record. Not every one gets a full dossier with a mechanism and a hypothesis — that would be dishonest. But every one gets a schema-valid record with its identity, source, Orphanet type, and flags for what data exist.

The record contains:

the ORPHAcode;
the preferred term;
the source URL;
whether Orphanet has gene associations;
whether it has phenotype annotations;
whether it has epidemiology;
whether it has natural-history data;
and a set of claims, each tied to a source record.

For the first fifteen priority diseases, we enriched the record with the actual gene, phenotype, inheritance, onset, prevalence and cross-reference data.

For Friedreich ataxia, for example, the record has FXN, autosomal-recessive inheritance, adolescent or childhood onset, a long list of HPO phenotypes, prevalence entries by country, and structures 1EKG and 3S4M.

But the important thing is not the fields. The important thing is the rule:

No claim without a source.

Not “the literature says.” Not “it is known.” A specific source ID, a specific URL, an evidence tier, and a retrieved date.

If we can’t show the source, the claim doesn’t go in.

That’s the first safeguard.

The second is the tier.

Not all sources are equal. A primary experimental paper is not the same as a registry entry. A registry entry is not the same as a preprint. A model output is not the same as a biological measurement.

So every claim carries a tier:

T1 is primary experimental or clinical evidence, or official regulatory text.
T2 is a peer-reviewed synthesis, guideline or curated database.
T3 is a registry, preprint or conference abstract — useful for hypothesis generation, not for a clinical claim.
T4 is a computational output, model score or expert opinion. It can support a hypothesis. It cannot support a biological fact.

That sounds bureaucratic. It isn’t. It’s the difference between a useful research tool and a very confident machine that makes things up.

Now, the third layer is the one I care about most: the hypothesis.

A dossier that only summarises the literature is a very expensive search engine. The thing a scientist needs is a testable next step.

So each curated record can carry hypotheses. And each hypothesis has to have four things:

a statement;
a mechanism;
a falsifier;
and a critical experiment with a readout and a go/no-go threshold.

The falsifier is the key. If you can’t say what result would prove you wrong, you don’t have a hypothesis. You have a hope.

In the Friedreich ataxia record, there are three hypotheses.

The first is transcriptional restoration. The GAA repeat expansion silences FXN. If we can reduce that silencing, we should increase FXN mRNA and frataxin protein, and that should improve iron-sulfur cluster enzyme activity in patient-derived cells.

What would falsify it? If FXN mRNA goes up but frataxin protein does not, or if frataxin goes up but the ISC readout does not improve at a non-toxic dose.

The critical experiment is patient fibroblasts versus corrected controls, with a dose-response, measuring FXN mRNA, frataxin protein, aconitase activity, ISC assembly, and viability.

The go/no-go is a reproducible dose-dependent increase in frataxin protein and a functional ISC gain, separated from cytotoxicity.

That’s a hypothesis a scientist can actually test.

The second is protein restoration. Delivering mature frataxin, or a frataxin-encoding nucleic acid, might restore ISC function when endogenous frataxin is limiting. The falsifier is detectable frataxin without a functional benefit, or an exposure that cannot be achieved safely.

The third is modulation of the frataxin–ISC assembly interface. Could we increase cluster output without causing iron overload? The falsifier is no target engagement, no cluster output gain, or iron misdistribution at effective exposure.

These are not claims. They are hypotheses. The difference is the whole point.

Now, the fourth layer is the NEXUS run.

We wanted every record to have a pipeline status, not just a summary. So we ran the non-fold NEXUS therapeutic stage on every entity with a gene association.

Four thousand two hundred and forty-five entities had a gene. We ran them. Zero command failures.

For each one, the dossier records the mechanism returned by NEXUS, the AUTOTAC eligibility, the confidence, and any alternative modality routes — gene therapy, protein replacement, transcriptional activation, CRISPR, and so on.

And for the seven thousand four hundred entities without a gene in the Orphanet record, we did not invent a protein target. We wrote an explicit “not run” dossier. It says: this record does not supply a molecular target for the protein/gene pipeline. Non-protein and phenotype-led routes must be assessed separately.

That is not a failure. That is the system refusing to hallucinate.

Here’s the result that matters most:

Of the four thousand two hundred and forty-five gene-level runs, four thousand and sixty-five came back as UNKNOWN — research needed.

Ninety-seven were gain-of-function. Thirty-four were toxic aggregate. Thirty-two were loss-of-function or haploinsufficiency. Seventeen were other or specialised.

The largest category is UNKNOWN.

I want to sit with that for a second, because it would be very easy to spin it. You could say, “Our AI analysed four thousand rare diseases.” That sounds impressive. But the honest statement is: our knowledge base did not know the mechanism for most of them.

That’s not a failure of the run. It’s a measurement of the knowledge base. And it tells us exactly where the work is.

This is why I keep saying the system has to show its ignorance. A dossier that says “research needed” is more valuable than a dossier that invents a mechanism.

Now, I want to talk about the scientist-facing console, because that’s where this becomes a product rather than a pipeline.

The console has a searchable list of the enriched targets. You open Friedreich ataxia, and you see the disease record, the evidence claims, the genes, the phenotypes, the prevalence, the structures, the hypotheses, the trials, the gaps, and the sources.

There’s a tab for evidence. Every claim has an ID, a tier, a confidence, a review status, and a source link.

There’s a tab for hypotheses. Every hypothesis has a falsifier, a critical experiment and a go/no-go.

There’s a tab for trials. The Friedreich ataxia query returned one hundred and fifteen studies at the time of retrieval. The console lists examples, and it says plainly: a registry entry is not evidence of efficacy.

There’s a tab for sources, and a tab for gaps and review questions.

And there’s a banner that says: research use only. Not a diagnosis, treatment recommendation or clinical claim.

The console is read-only. It doesn’t pretend to be a doctor. It doesn’t make decisions. It gives a scientist a place to start.

Now, the fifth layer is the safeguard system, and I want to be specific, because this is where a lot of AI projects hand-wave.

We wrote a hundred-source research register on hallucination risk in protein folding and drug development. Not a blog post. A structured register with a finding, a source URL, and an evidence tier for every entry.

We wrote a source gate that checks every citation resolves to a register entry and every register entry is cited. It passed with one hundred and forty citations across one hundred sources.

We wrote a leakage gate for the folding benchmark. It checks duplicate keys, split labels, topology overlap, thirty-percent identity clusters, and numeric MSA names. It passes the corrected split eight out of eight, and it fails the old split on purpose.

We wrote a result gate that refuses single-seed, Train-only, baseline-free claims. It doesn’t decide whether a score is good. It decides whether the claim has the evidence it needs.

We wrote a model card that says what the model is, what it is not, what data it saw, what its limits are, and which uses are out of scope.

And we wrote a protocol gate for the public site that checks scope notes, stale figures, internal system references, outreach addresses, BETA removal and Fold Explorer claims.

Is that enough? No. It’s a good start. It is not a quality management system. It is not a clinical validation. It is not an independent audit.

But it is the difference between “we have a research tool” and “we have a machine that says things.”

Now I want to talk about the thing that makes this project unusual: it’s not protein-only.

A lot of computational drug-discovery tools stop at proteins. They assume the target is a protein, the drug is a small molecule, and the job is to find a pocket.

But rare disease is bigger than that.

Some diseases are caused by a missing protein. Some by a toxic protein. Some by a RNA-processing defect. Some by a metabolic pathway. Some by a structural RNA. Some by a whole cell type. Some by a developmental programme.

So the dossier format has to support multiple target classes and modalities:

gene-level targets, protein targets, RNA targets, pathway-level targets, cell therapy, enzyme replacement, substrate reduction, chaperones, gene therapy, editing, antisense oligonucleotides, small molecules, and symptomatic care.

The NEXUS therapeutic stage already returns some of these routes. Where it doesn’t know, the dossier says so. Where there is no gene, the dossier becomes phenotype-led.

That’s the correct behaviour. We don’t force every disease into a protein-shaped hole.

Now, let’s talk about Friedreich ataxia as the first vertical slice, because it shows both the promise and the limits.

Friedreich ataxia is a biallelic GAA repeat expansion in FXN. The normal repeat is about five to thirty-three. Affected individuals commonly carry sixty-six to more than a thousand. The expansion reduces frataxin production.

Frataxin is a mitochondrial protein. It’s involved in iron-sulfur cluster assembly. It supports persulfide transfer to ISCU, it delivers iron, and it modulates mitochondrial aconitase. Those are real, primary experimental findings.

There are experimental structures: 1EKG at 1.8 angstroms, mature human frataxin; 3S4M at 1.3 angstroms, wild-type human frataxin.

There are one hundred and fifteen ClinicalTrials.gov studies at the time of retrieval, including pharmacological, gene-therapy and symptomatic studies.

And there are three hypotheses, each with a falsifier.

But here’s what the dossier does not have: patient-derived data. Wet-lab validation. A systematic review. A modality-specific delivery assessment. An expert review.

Those are listed as gaps. Not hidden. Listed.

That’s the honest state of the first vertical slice.

Now, the next step is not to add ten more diseases. It is to put this in front of one FXN scientist and let their critique redesign it.

We have a review packet ready. It asks eight questions:

Is the causal claim precise enough?
Which source would you replace with a better primary study?
Is transcriptional restoration still the most testable hypothesis?
Which functional readout is accepted in your lab?
What would make you reject the first hypothesis?
Is the structural caveat sufficient?
What is missing before you would use the page?
Would this save you time, or is it another summary?

That last question is the one that matters. If the answer is “it’s another summary,” we haven’t built the right thing.

The review packet is ready. It has not been sent. It needs explicit approval, because it’s a professional email to a real organisation.

Now, I want to describe what a scientist actually does with this, because “a console” can sound abstract.

Imagine you’re a postdoc working on Friedreich ataxia. You have a hypothesis, but you’ve inherited a folder of PDFs, a spreadsheet of trials, and a grant deadline. You open the console.

The first screen is not a chatbot. It’s a record. It tells you what Orphanet says, what the gene is, what the inheritance pattern is, what phenotypes are recorded, and which structures exist. Each statement has a source and a tier.

You click into the evidence tab. You see the GAA repeat claim, the frataxin claim, the ISC claim, the structural claim. You can disagree with any of them, and you can see exactly what they rest on.

You click into the hypotheses. You see three, not thirty. Each one has a falsifier. You read the first one and think, “No, that’s not the right readout for our lab.” Good. That’s the system doing its job: it gave you something concrete to disagree with.

You click into the gaps. It tells you there is no patient-derived data, no wet-lab validation, no systematic review, no expert review. It does not pretend those gaps are closed.

Then you export a cited dossier. You take it to your supervisor. You argue about the hypothesis. You design the experiment. The system did not decide anything. It organised the argument.

That’s the workflow.

And that’s why the console is read-only. A read-only system is not a limitation; it’s a trust boundary. The scientist is the one who writes the experiment, signs the protocol, and takes responsibility for the claim.

Now, why not just use a general chatbot for this?

Because a chatbot can produce a beautiful summary with a fabricated citation. We have the evidence for that. ChatGPT and Bard have both been shown to fabricate references in medical literature searches. Even web-enabled models still hallucinate citations. A fluent paragraph is not a source.

A general model can help you draft. It can help you brainstorm. It cannot be the audit trail.

Our console is built around the opposite assumption: every sentence is a claim, every claim has a source, and every source has a tier. If the source isn’t there, the sentence doesn’t ship.

That is slower. It is less magical. It is more useful.

Now, let’s talk about the UNKNOWN.

Four thousand and sixty-five gene-level runs came back as research needed. That sounds like a lot of nothing. It isn’t.

It is a map of where the knowledge base is thin. It tells us which diseases have a gene but no characterised mechanism, which ones need primary literature, which ones need a model organism, which ones need a biochemical assay, and which ones should not be prioritised until the biology is clearer.

That is exactly what a research portfolio needs. Not a list of 4,000 opportunities. A list of 4,000 questions, sorted by what is known and what is missing.

The next step is to take the strongest 20 or 30 of those and curate them properly. Read the primary papers. Check the variants. Check the structures. Talk to the people who know the disease. Build one real hypothesis at a time.

That’s how the catalogue becomes knowledge.

And that’s why the first vertical slice is FXN, not a thousand diseases. Depth first, then breadth.

Now, what would success look like in twelve months?

Not “we analysed every rare disease.” That’s a data-processing claim.

Success would look like this:

One FXN scientist reads the dossier and says, “This is useful, but your second hypothesis is wrong, and here is the experiment that would settle it.”

Three diseases have curated evidence maps that an academic lab would actually cite.

One hypothesis has been tested in a wet lab, with a positive or negative result, and the result is published.

The console has a workflow where a scientist can save a hypothesis, assign an experiment, and record a negative result.

And the public site has a podcast, a methods page, and a clear scope note — not a miracle cure.

That’s a real twelve-month scorecard.

Now, let’s zoom out.

What is the orphan intelligence project, really?

It is an attempt to build the evidence layer for rare-disease translation.

Not the diagnostic. Not the drug. The layer underneath: the map of what is known, what is uncertain, what is missing, and what experiment would move the field.

It is a place where a scientist can see the provenance of every claim, the tier of every source, the falsifier for every hypothesis, and the gaps that still need work.

It is deliberately unglamorous. It is a library with a good index. It is a lab notebook that can be audited. It is a map that shows its blank spaces.

And it is built around a simple rule: the system must never be more confident than its evidence.

That rule is why the biggest result is UNKNOWN.

That rule is why the Friedreich ataxia dossier says “seed, unreviewed.”

That rule is why the public site says “research use only.”

That rule is why we have gates that fail on purpose.

Now, where does it go next?

First, the FXN review. One scientist. Real critique. Then redesign.

Second, GBA1 or ATP7B. Not both at once. Choose the one with a real partner and a testable question.

Third, deepen the evidence layer: primary literature, trial results, variant data, structure validation, modality evidence.

Fourth, build the scientist workflow: save a hypothesis, assign an experiment, record a negative result, export a cited dossier.

Fifth, only when the evidence justifies it, consider a clinical or regulatory pathway. Not before.

And the ab initio work continues in the background. It is a separate workstream. It is not the product yet. It is the long game.

I want to close with something Papa says: we are Sabre-Tek, we are the Light.

That’s not a marketing line. It’s a standard.

The Light doesn’t mean “we are always right.” It means we don’t hide the dark. We show the failed experiments. We show the shallow MSAs. We show the UNKNOWN. We show the gaps.

If we do that, then a scientist can trust the instrument. Not because it’s perfect, but because it’s honest.

Eleven thousand six hundred and forty-five diseases. One research console. One rule: evidence first.

That’s the orphan intelligence project.

Thanks for listening.

---

*Research update, not medical advice. No clinical or regulatory claim is made. Orphanet/Orphadata data is used under CC-BY-4.0. The voice is synthetic.*
