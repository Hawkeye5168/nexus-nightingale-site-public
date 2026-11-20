# The Data Comes First

**Road to NEXUS Nightingale**  
Episode 04 · 15 November 2026  
Host: Sabre  
Style: long-form, conversational, evidence-first  
Scope: research update, not medical advice

---

**Update, 16 November 2026:** The v2 additions increase the seven LOF dossiers from 40 to 48 pages; the 40-page figure spoken here is the 15 November v1 snapshot. External clinical review remains pending.

**Update, 20 November 2026 — section counts:** The benchmark floor remains thirty substantive sections. The current full dossiers run **36–46 sections**: most have 36, DENV-001 has 38 and EBOLA-001 has 46. This audio is the 15 November record and has not been re-voiced.

**SABRE:**

A dossier is not a longer report.

That is the first thing I want to say, because it is the easiest thing to get wrong.

A dossier is a decision record. It exists to answer one question, with the evidence attached, the uncertainty visible, and a clear statement of what would change the answer.

And for a long time, we built them in the wrong order.

We started with the target. We resolved the protein. We looked for a structure. We ran the fold. We classified the mechanism. We designed a route. And then, somewhere near the end, we assembled the evidence around the thing we had already decided to build.

That order feels natural. It is how a lot of computational drug-discovery work is presented. But it has a quiet failure mode: the structure becomes the centre of the document, and the evidence becomes decoration.

So we changed the order.

Now, every dossier starts with the data.

Before we touch a structure, before we choose a mechanism, before we write a single design sentence, we run a data preflight.

The preflight looks across nine evidence classes: identity, structure, variation, expression, pathways, trials, literature, countermeasures and diagnostics. For each class, it checks the sources a dossier will need, records what is reachable, what is partial, and what is blocked. On a typical target, that is up to eighty-one source checks.

That number is not a marketing number. It is a floor. It is the point at which we can say: we have looked for the obvious things, in the obvious places, and we know what is missing.

And if something is missing, we write it down.

That sounds simple. It is not.

A missing structure is not the same as a missing disease. A registry entry is not the same as a trial result. A trial record is not the same as an efficacy claim. A sequence alignment is not the same as a contact map. If you collapse those distinctions, you get a document that looks complete and is not.

So the preflight records a status for every class: pass, partial or blocked. It records the source, the date, the response, and the reason. A blocked class stays blocked. It does not get quietly promoted because the rest of the document is going well.

The second thing the preflight does is look at the sequence alignment.

If the dossier is going to make any claim about a family, a domain, a contact, or a conserved surface, the alignment has to be deep enough, clean enough and diverse enough to support it. A hundred sequences that are all ninety-nine per cent identical are not a deep alignment. They are one sequence with a lot of photocopies.

So we check the alignment. We remove the worst gap-heavy sequences. We remove the worst gap-heavy columns. We remove near-duplicates. We record what is left.

Sometimes what is left is good. Sometimes it is thin. Sometimes it is not enough.

And when it is not enough, we say so.

That is the part that matters. The data-first rule is not a promise that every target will have all the data. It is a promise that the document will tell you when it does not.

Let me give you the hardest example from this week.

Ebola.

The target is the glycoprotein, GP. The full protein is six hundred and seventy-six amino acids. It is the thing on the surface of the virus. It is the thing the immune system sees. It is the thing a vaccine or a therapeutic has to deal with.

We wanted a full-length structure. We looked. The pipeline found structures, but they were not the full protein. One was a four hundred and eighty-nine amino acid ectodomain construct. Another was a five hundred amino acid construct. Another was a four hundred and ninety-four amino acid construct. And one, two E B O, was a seventy-four amino acid GP2 core chain.

That last one is important, because it is easy to misread. The deposit contains three copies of that chain, so the deposited residue count is two hundred and twenty-two. But the chain you are looking at is seventy-four residues. It is not a two-hundred-and-twenty-two-residue chain. It is certainly not the full six-hundred-and-seventy-six-residue protein.

For a while, our own document said the wrong thing. It described two E B O as a two-hundred-and-twenty-two-amino-acid construct. That was wrong. The deposit is three copies of a seventy-four-residue chain.

We corrected it. The dossier now says exactly what the deposit is.

That is not a small correction. If you describe a fragment as a full protein, every structural claim that follows is built on a false object.

The same thing happened with Bundibugyo virus, the species behind the 2026 outbreak.

There are structures. Six D Z M, seven K E W, six E A five. But they are not full-length GP. They are mucin-deleted GP1 and GP2 complexes. They are useful constructs. They are not the whole protein.

So the dossier says: full-length BDBV structure blocked. Construct-level evidence partial.

And when we folded one of those constructs, six D Z M, we got a supervised template recovery score of zero point six two six eight, with an RMSD of about eleven point one six angstroms. That is a construct-level result. It is not a full-length GP result. It is not a claim that we have solved the BDBV glycoprotein.

We also went deeper on the sequence data.

The first alignment had a few hundred sequences. Many were fragments. Many were gap-heavy. We pulled a much larger set of Ebolavirus glycoprotein records from NCBI. Three thousand eight hundred and ninety-four records. After alignment, three thousand eight hundred and eighty-seven sequences across the six-hundred-and-seventy-six columns.

That sounds like a deep alignment. And it is, in raw numbers. But when we cleaned it, we were left with a hundred and twenty-five sequences that passed the gap and identity filters. The rest were too fragmentary, too gappy, or too similar to add information.

We ran the contact analysis anyway. The scores were no longer all zero. But they were numerically unstable, and we did not have a full-length experimental contact map to validate them against. So we did not publish a contact map.

We did not say: the contacts are solved. We said: the alignment is deeper, the signal is unstable, and the claim remains partial.

That is the discipline.

Let me explain what those nine evidence classes actually mean, because the phrase can sound like a checklist.

Identity is the anchor. What is the disease? What is the gene? What is the protein? What is the inheritance pattern? What are the synonyms that different databases use? If you get identity wrong, every later search is aimed at the wrong object.

Structure is not one thing. It is experimental structures, predicted structures, domains, constructs, complexes and missing regions. A good preflight does not just ask whether a structure exists. It asks what the structure covers.

Variation is the variant record: pathogenic variants, variants of uncertain significance, population frequencies, and the difference between a causal variant and a bystander.

Expression is where the protein is made, when, and in which tissue. A beautiful target that is not expressed in the relevant cell is not a useful target.

Pathways are the causal neighbourhood. What does the protein do? What does it interact with? What happens downstream when it is lost or overactive?

Trials are the clinical landscape. Not a promise. A map of what has been tested, in whom, at what stage, with what endpoint.

Literature is the primary and secondary record. It is not a pile of PDFs. It is a set of claims with dates, methods and limitations.

Countermeasures are the things that already exist or are being developed: drugs, vaccines, antibodies, replacement enzymes, gene therapies, supportive care.

Diagnostics are how the disease is recognised. A dossier that cannot explain the diagnostic pathway is not ready to discuss treatment.

Nine classes. Eighty-one checks. The point is not to collect everything. The point is to know what you have before you start arguing.

And this is why the old order was so tempting.

When you start with a structure, you always have something to show. A ribbon diagram. A surface. A pocket. A score. It looks like progress. But a structure without the right identity, the right construct and the right biological context is just a shape.

When you start with the data, the first thing you often get is a list of gaps. That is less exciting. It is also more useful.

The seven loss-of-function dossiers are a good example.

Woodhouse-Sakati syndrome is caused by loss of DCAF17. The phenotype includes hypogonadism, alopecia, diabetes, hearing loss and progressive neurological involvement. There is no approved disease-modifying therapy. The dossier does not pretend that a degrader is appropriate, because the problem is a missing function, not an excess.

Zellweger spectrum disorder is a peroxisome biogenesis failure. PEX1 is the most common gene. The consequences run through the liver, the eyes, the ears, the adrenal glands and development. The dossier describes supportive care and investigational restoration, not a molecule that fixes the whole spectrum.

LAMA2-related congenital muscular dystrophy is a laminin-211 problem. The muscle loses its attachment to the extracellular matrix. The dossier describes respiratory and nutritional support, and the gene-replacement work as investigational.

Aicardi-Goutieres syndrome, RNASEH2A-related, is a type I interferonopathy. The therapeutic question is not simply which drug suppresses interferon. It is which patient, at which stage, with which organ risk. JAK inhibition is used in selected patients. It is not a cure.

Warsaw breakage syndrome is a DDX11 helicase problem with chromosomal instability. The dossier records growth, hearing, cardiac and developmental care, and the limits of the evidence.

Ribose-5-phosphate isomerase deficiency is a metabolic block. Ribitol has been reported. It is not an established cure. The dossier says that plainly.

GFER-related mitochondrial disease is a mitochondrial protein-import problem. The evidence is thin. The care is supportive. The research route is investigational.

Seven different diseases. Seven different mechanisms. One shared rule: do not degrade a protein the patient already lacks.

That rule is not a slogan. It changes the entire document. It changes the mechanism section, the modality section, the design section and the decision. It also changes what the dossier refuses to say.

A reviewer should be able to see that refusal. Not as a footnote, but as a result.

That is what the mechanism gate is for.

Let me make the status vocabulary concrete, because it is easy to say current, stale, conflict, unverified, blocked, retracted and then use the words loosely.

Current means the claim has a source that is still the best available record and has been checked recently. It does not mean eternal truth. It means current as of the date on the document.

Stale means a newer source has appeared, or the underlying record has changed, and the claim has not yet been reconciled. It stays visible until someone does the work.

Conflict means two credible sources disagree. The dossier does not pick the more convenient one and hide the other. It shows the disagreement and says what would resolve it.

Unverified means we have not been able to check it against a primary record. It is not a synonym for false. It is a statement about our confidence, not about the world.

Blocked means the evidence class or the claim cannot be completed with the data we have. A full-length structure that does not exist is blocked. A contact map that cannot be validated is blocked. A trial result that has not been published is blocked.

Retracted means the source was withdrawn. It is kept in the record so that nobody accidentally cites it again.

Those words do the same job as the red team. They make the document argue with itself.

And that is what a reviewer should see when they open a dossier. Not a polished surface with a few limitations at the end. A structure of claims, each with a status, each with a source, each with a date.

The reviewer can then do something useful. They can attack a specific claim. They can replace a source. They can say: this is current, but your interpretation is wrong. Or: this is blocked, but I have the data you are missing.

That is a much better conversation than: is this document good or bad?

A dossier is not good or bad in the abstract. It is more or less useful for a defined question, at a defined date, with a defined evidence base.

That is why the data-first rule and the status vocabulary belong together.

The preflight tells you what evidence exists. The status tells you what you are allowed to say about it.

Without the preflight, the status is guesswork. Without the status, the preflight is a folder of links.

Together, they make the document reviewable.

There is one more thing I want to say about the seven loss-of-function dossiers, because they are easy to underestimate.

They are not less important because they do not have a degrader. They are important because they show what the pipeline does when the honest answer is: do not degrade this protein.

That is a real decision. It saves a programme from spending a year on the wrong modality. It gives a scientist a clear statement of what would be worth doing instead: restore the function, replace the protein, compensate the downstream consequence, or support the patient.

Those are different programmes. They need different evidence. They need different experiments. The dossier makes that separation explicit.

And that is the point of a decision record. It is not there to make every disease look like an opportunity. It is there to make the next decision clearer.

So when I say the library now has twenty-six dossiers, I do not mean twenty-six chances to sell something. I mean twenty-six structured arguments, each with its own evidence base, its own gaps and its own limits.

Some of them will be more useful than others. Some will be superseded. Some will be wrong in a way we have not noticed yet. That is research.

But they will all be honest about what they contain.

That is the standard we are trying to hold.

A null result is still a result. A blocked class is still information. A partial answer is still an answer, as long as you label it correctly.

The alternative is worse. You can make a document look green by relabelling every red row. You can call a construct a protein. You can call a noisy score a contact map. You can call a template recovery a blind prediction. But then the document is no longer a decision record. It is a sales brochure with citations.

We are not doing that.

This week we also completed seven loss-of-function dossiers.

Woodhouse-Sakati syndrome, caused by DCAF17. Zellweger spectrum disorder, PEX1-related. LAMA2-related congenital muscular dystrophy. Aicardi-Goutieres syndrome, RNASEH2A-related. Warsaw breakage syndrome, DDX11. Ribose-5-phosphate isomerase deficiency, RPIA. And GFER-related mitochondrial disease.

All seven are loss-of-function. That matters because the mechanism gate is explicit: you do not degrade a protein the patient already lacks. For every one of those dossiers, the gate says blocked, no degrader.

That is not a failure of the pipeline. It is the pipeline protecting the patient from a plausible-sounding but wrong therapeutic direction.

Each dossier has thirty sections, thirty sources, twenty-five claims, eight red-team items, six figures and eight tables. Each one has a data-preflight record. Each one says what is missing. None of them claims a structure we do not have. None of them claims a contact map we cannot support. None of them claims a clinical benefit.

They are forty pages each. Not because we padded them, but because a serious question has at least thirty jobs to do.

And that brings the current library to twenty-six source-linked dossiers.

Nineteen existing dossiers, plus the seven loss-of-function editions. Five of them remain the reference implementations for depth: Dengue, Friedreich ataxia, NSCLC, Gaucher and Fabry. They are the ones we use when we ask: is the new document as complete as the best one we have?

The answer is not always yes. Some of the newer documents are shorter. Some have thinner evidence. Some have no experimental structure at all. That is allowed, as long as the document says so.

The point of a library is not to make every book the same length. The point is to make every book honest about what it contains.

So what does data-first mean for a scientist?

It means you can see the evidence before you see the conclusion. You can see which classes are strong, which are partial, which are blocked. You can see the alignment depth. You can see the construct, not just the score. You can see the difference between a full protein and a domain. You can see the difference between a trial record and a trial result.

And you can disagree earlier.

If the evidence is thin, you know before you read thirty pages. If the structure is a fragment, you know before you interpret the figure. If the contact map is not validated, you know before you build a hypothesis on it.

That is a better use of a scientist's time.

It is also a better use of ours.

Because the old order encouraged us to keep going. Once you have a structure and a design, there is a temptation to write the dossier that justifies them. The new order forces the opposite. The data comes first, and the conclusion has to earn its place.

That is the change.

Not a new engine. Not a new claim. A different order of work.

Data first. Then structure. Then mechanism. Then design. Then the document.

And if the data says stop, we stop.

Now, I want to be clear about the limits.

This is still a computational research pipeline. It is not a diagnostic. It is not a treatment recommendation. It is not a clinical validation. It does not replace a clinician, a wet lab or a regulatory review.

The preflight checks sources. It does not prove that every source is correct. The alignment cleaning improves the input. It does not create signal where there is none. The supervised fold recovers a known reference. It is not a blind prediction. The ab initio work remains a background research track, not a production claim.

And the dossiers are research documents. They are written to be read, challenged and improved. They are not written to be believed.

If you take one thing from this episode, take the order.

Before you build the argument, check the evidence. Before you show the structure, name the construct. Before you show the score, say what it measures. Before you call something solved, look for the row that is still blocked.

That is how a dossier becomes useful.

That is how a library becomes trustworthy.

And that is why, this week, the most important number is not a score. It is the number of gaps we were willing to write down.

We are Sabre-Tek. We are the Light.

Thanks for listening.

---

*Research update, not medical advice. No clinical or regulatory claim is made. The voice is synthetic. All results are computational unless explicitly labelled experimental.*
