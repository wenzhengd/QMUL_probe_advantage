# Available Skills

## check_latex
Command:
bash scripts/check_latex.sh

Purpose:
- Compile LaTeX
- Detect undefined references
- Report math-mode errors

Use when:
- User asks to verify LaTeX correctness
- User requests PDF build or error fixing

---

## verify_equations
Command:
python scripts/verify_equations.py

Purpose:
- Symbolically re-derive equations
- Check consistency between sections

Use when:
- User asks to validate derivations
- User doubts correctness of equations
