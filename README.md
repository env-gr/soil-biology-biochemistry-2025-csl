# soil-biology-biochemistry-2025-csl
Zotero CSL style for Soil Biology &amp; Biochemistry (SBB), updated to match the 2025 Guide for Authors.


### 1. In-text citations

* **Author–date format** with parentheses:
  `... (Georgiou et al., 2022; Lavallee et al., 2020)`
* **et al. rule:**

  * 3 or more authors → `FirstAuthor et al., 2022` (always, including first mention).
* **Multiple citations in one group:**

  * Separated by `;` and ordered by **year, then author**.
* **Locators (pages, figures, etc.)**

  * Appended after the year, e.g. `(Smith et al., 2020, p. 10)` if you use a locator.

---

### 2. Author names

* Initials are rendered **without spaces**:

  * `Bradford, M.A., Keiser, A.D., Davies, C.A.`
  * Not `M. A.` but `M.A.`
* **Particles** (e.g., *van der*, *de*, etc.) are handled by CSL’s normal name logic:

  * If Zotero is filled correctly (family vs. given vs. non-dropping particle), the style preserves lowercase particles in both citations and bibliography.

---

### 3. Sorting rules

* **In-text citation cluster:**

  * Sorted by year (ascending), then by short author string.
* **Reference list:**

  * Sorted by:

    1. Author (family name, then initials)
    2. Year (ascending: 1999, 2000a, 2000b, 2001, …)
    3. Title (for ties)
* Automatic year suffixes (**a, b, c**) if same author and year exist.

---

### 4. Journal articles (the main target)

Output pattern:

```text
Author, A.B., Author, C.D., 2023. Title of the article. Journal Name 159, 108302. doi:10.xxxx/...
```

* **Journal title:**

  * Uses the **full title as entered in Zotero**, in italics.
  * No automatic abbreviation or capitalization change.
* **Article title:**

  * Printed exactly as in Zotero (so **sentence case must be done in Zotero**).
* **Volume and pages / article number:**

  * Printed as `Volume, PageOrArticleNumber`
  * If you store an article number (e.g. `108302`) in the **Pages** field in Zotero, it will appear correctly as `159, 108302`.
* **DOI:**

  * Printed as `doi:10.xxxx/...` (no `https://doi.org/` prefix).

---

### 5. Book chapters / conference papers

Pattern:

```text
Author, A.B., 2010. Chapter title. In: Editor, C.D. (Ed.), Book Title. Publisher, Place, pp. 281–304. doi:...
```

* Adds `In:` + editors in SBB style: `Editor, A.B. (Ed.)` or `(Eds.)`.
* Book title not italicized in the CSL above (can be tuned), publisher and place after a period.
* Pages printed as `pp. 281–304` (if page field is filled).

---

### 6. Books / reports

Pattern:

```text
Author, A.B., 2010. Book Title, 2nd ed. Publisher, Place. doi:...
```

* Supports **edition**: numeric editions become `2nd ed.`, etc.
* Publisher and place are grouped as `Publisher, Place`.

---

### 7. Theses

Pattern:

```text
Author, A.B., 2015. Thesis title. PhD thesis. University, City.
```

* The exact wording (e.g. *PhD thesis*) comes from Zotero’s **Genre/Type** fields.
* Institution and place taken from the publisher fields.

---

### 8. Access information

* **Preferred:** DOI.

  * If DOI is present → prints `doi:10.xxxx/...`.
* **Fallback:** URL + accessed date, e.g.:

```text
URL https://...
(accessed 3 Mar 2025).
```

---

### 9. Layout of the reference list

* **Hanging indent** enabled.
* **Single-spaced** within entries, no extra blank line between entries.
* Final period at the end of each reference.

---

### 10. What the style deliberately does *not* change

These are **left to your Zotero data** (so you keep full control):

* **Sentence case vs. Title Case** of titles → whatever you type in Zotero is printed.
* **Hyphens and special characters** (`mineral-associated`, en-dash `–` vs. hyphen `-`) → exactly as in Zotero.
* **Acronyms / technical terms** (MEMS, NMR, DFT, etc.) → capitalization is preserved from Zotero.

So the workflow is:

1. Clean and standardize titles, hyphens, acronyms in Zotero.
2. Let this CSL style handle **structure, punctuation, ordering, and DOI formatting** to match SBB 2025 requirements.
