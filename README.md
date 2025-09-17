Amplifex 🧬
Instant PCR primer design & publication-ready DNA feature maps in three A4 pages – straight from Google Colab.
https://colab.research.google.com/github/YOUR_USERNAME/amplifex/blob/main/amplifex.ipynb
https://opensource.org/licenses/MIT
https://www.python.org/downloads/

What Amplifex does
Analyses any DNA sequence (plain text or FASTA) in seconds:
global composition (%GC, base counts)
homopolymer runs ≥ 5 nt
di-, tri-, tetra-nucleotide SSRs
palindromic hairpins (ΔG < −3 kcal/mol)
low-complexity windows (Shannon entropy < 1.2 bits)

Designs optimal PCR primers:
scans first/last 200 nt by default
filters length (18–25 nt), GC 40–60 %, Tm 60 ± 2 °C (Wallace)
penalises hairpins, self-dimers, long homopolymer runs
returns 5 highest-scoring non-interacting pairs

Exports three 300-dpi A4 PNG pages:
Page 1 – summary table + full-colour sequence map with obstacle legend
Page 2 – publication-quality charts (base pie, GC gauge, feature pie, base bar)
Page 3 – primer pair table (sequence, position, length, GC %, Tm, score, amplicon length)

Downloads:
individual PNG
all PNGs in ZIP
merged PDF

One-click run (zero installation)
Click the blue “Open in Colab” badge above.
Paste your DNA sequence when prompted.
Choose what to download – done.

Algorithms & thresholds
Table
Copy
Parameter	Value
Primer length	18 – 25 nt
Annealing temp (Wallace)	60 ± 2 °C
GC content	40 – 60 %
Max homopolymer run	≤ 4 nt
Max hairpin stem	≤ 3 bp
Max primer-dimer overlap	≤ 5 bp
SSR thresholds	di 4, tri 3, tetra 3 copies
Palindrome ΔG cut-off	< −3 kcal/mol
Low-complexity entropy	< 1.2 bits (20-mer window)

Folder structure
Copy
amplifex/
├─ amplifex.ipynb      # single notebook (full code)
├─ requirements.txt    # frozen dependencies (optional)
├─ LICENSE             # MIT
└─ README.md           # this file

Local usage (optional)
bash
Copy
git clone https://github.com/YOUR_USERNAME/amplifex.git
cd amplifex
pip install -r requirements.txt
jupyter notebook amplifex.ipynb

Run every cell – behaviour identical to Colab.

Citation
If you use Amplifex in a publication, please cite:
Hassan, M. S. Amplifex: quick PCR primer design & feature maps. GitHub https://github.com/YOUR_USERNAME/amplifex

License
MIT © 2025 Muhammad Sohaib Hassan – see LICENSE for details.
