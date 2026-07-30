<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1f3b73,50:2f7d4f,100:b3452c&height=190&section=header&text=Koussay%20Mansouri&fontSize=54&fontColor=ffffff&fontAlignY=34&desc=theoretical%20physics%20·%20continuum%20mechanics%20·%20scientific%20computing&descAlignY=54&descSize=17" width="100%"/>

<a href="https://github.com/Koussay17/M.Koussay-engineering-portfolio">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=21&duration=3600&pause=900&color=1f3b73&center=true&vCenter=true&width=760&lines=Prove+what+is+provable.;Measure+what+is+measurable.;Say+where+it+breaks." alt="motto"/>
</a>

<br><br>

[![Portfolio](https://img.shields.io/badge/📄_Research_Portfolio-10_papers_·_138_pages-1f3b73?style=for-the-badge)](https://github.com/Koussay17/M.Koussay-engineering-portfolio)
[![Location](https://img.shields.io/badge/Sousse-Tunisia-2f7d4f?style=for-the-badge)](#)

</div>

<br>

```
                  ┌─────────────────────────────────────────────────────────┐
                  │                                                         │
                  │   A theorem is worth more than a simulation.             │
                  │   A simulation that matches a theorem is worth more     │
                  │   than either.                                          │
                  │                                                         │
                  │   A limit stated honestly is worth more than all three. │
                  │                                                         │
                  └─────────────────────────────────────────────────────────┘
```

<br>

## What I actually do

I write **research papers** where the analysis and the numerics have to agree,
and I say by how much.

Not "I ran a simulation and it looked like an instability." That proves nothing —
the instability is obvious. What has evidentiary value is: *the growth rate I
measured is $0.70\,\%$ from the root of the exact kinetic dispersion relation,
mode by mode, with the fit window strictly inside the linear phase, and here are
the three modes I refuse to quote because their window is contaminated.*

Ten papers, all built the same way:

<table>
<tr><td width="33%" valign="top">

**Prove**

Theorems with full proofs.
Frobenius, Howard, Penrose,
Squire, Buckingham,
Kármán–Howarth–Monin.
Not cited — derived.

</td><td width="33%" valign="top">

**Verify**

Independent code, no
domain libraries. Compare
against exact solutions
and closed forms, never
against a fitted curve.

</td><td width="33%" valign="top">

**Validate internally**

Energy conservation.
Constraint propagation.
Rankine–Hugoniot.
Quantities that test the
code against *itself*.

</td></tr>
</table>

<br>

## Research portfolio

<div align="center">

### [→ M.Koussay-engineering-portfolio](https://github.com/Koussay17/M.Koussay-engineering-portfolio)

</div>

| # | field | what the paper proves | verified to |
|:-:|---|---|:-:|
| **01** | String cosmology | An Einstein-frame bounce requires $W(H)\le H^2$ — **identically violated at leading order**. No bounce below the string scale. | $3.9\!\times\!10^{-12}$ |
| **02** | Kinetic plasma theory | Penrose's criterion in strong form; cold beams solved exactly, $\gamma_{\max}=\omega_p/2\sqrt2$ | $0.70\,\%$ |
| **03** | Geometric mechanics | $[X_1,X_2]=a^{-2}E_z$ — the Lie bracket **predicts** the measured rolling holonomy | $0.9997918$ |
| **04** | Kinetic → hydrodynamics | The $-\tfrac12$ in $\nu=c_s^2(\tau-\tfrac12)$ is trapezoidal integration, and it is worth $271\,\%$ | $0.156\,\%$ |
| **05** | Periodic electromagnetics | Li's factorization rules: $N^{+0.07}\to N^{-1.15}$, gain $\times64$ | $R+T=1.000000000000$ |
| **06** | Hydrodynamic stability | Exact neutral mode $\mathrm{sech}\,y$ at $k=1$; four theorems from one identity | $5.6\!\times\!10^{-17}$ |
| **07** | Dynamical systems | Leapfrog integrates a modified Hamiltonian exactly — order 2 **beats** order 4 | order $4.00$ |
| **08** | Polymer rheology | Oldroyd-B diverges at $\mathrm{Wi}=1/2$; the real regime is entirely beyond it | 8 digits |
| **09** | Turbulence | The $4/5$ law forces $\zeta_3=1$; the anomaly is measured, not fitted | $1.60\,\%$ |
| **10** | Hyperbolic conservation laws | Weak solutions are **not unique** — two exhibited for the same datum | $10^{-16}$ |

Plus a **31-page computational notebook** rebuilding paper 01 from manifolds and
connections upward, with eight worked exercises.

<br>

## One result, in full

<details open>
<summary><b>The Lie bracket that you can measure with a ball and two plates</b></summary>

<br>

Roll a sphere on a plane without slipping or twisting. The admissible velocity
fields are

$$X_1=\partial_x+\tfrac1a E_y,\qquad X_2=\partial_y-\tfrac1a E_x$$

and their bracket is

$$[X_1,X_2]=\frac{1}{a^2}\,E_z \;\notin\; \mathcal{D}$$

By Frobenius the constraint is **non-integrable**. Then $[X_1,E_z]$ and
$[X_2,E_z]$ generate the remaining directions, so the distribution is
bracket-generating and — by Chow–Rashevskii — the sphere is **completely
controllable**: you can return it to the same point with any orientation you
like. That is why a car can parallel-park.

But the bracket is not just an obstruction. It *is* the curvature of the rolling
connection, so it makes a **prediction**: transport around a closed loop of area
$\mathcal{A}$ rotates the ball by $\Theta\simeq\mathcal{A}/a^2$.

I measured it — exact transport by ordered products of $\mathfrak{so}(3)$
exponentials, no expansion:

```
𝒜/a²      Θ (rad)        Θ/𝒜
0.0025    0.002499480    0.9997918     ← the area law
0.0400    0.039867504    0.9966876
0.2500    0.244988014    0.9799521
```

The first-order coefficient comes out of the hand-calculated bracket exactly.
The second order is $-\mathcal{A}/12$ for a square — and it **depends on the
shape of the loop**: at equal area $0.36$, a square gives $\Theta=0.3498$ but a
$2.4\times0.15$ rectangle gives $0.2796$.

That shape dependence is the signature of a **non-abelian** structure group. For
an abelian connection — magnetic flux, Aharonov–Bohm — $\Theta$ would be
*exactly* proportional to area. Here $SO(3)$ does not commute with itself, the
holonomy is a path-ordered product, and the corrections are successive
commutators.

Sanity check that the whole thing is a genuine group element:
$\|R_{\mathrm{direct}}\cdot R_{\mathrm{inverse}}-I\|=7\times10^{-13}$.

</details>

<br>

## Toolbox

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white)
<br>
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![MATLAB](https://img.shields.io/badge/MATLAB-0076A8?style=for-the-badge)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

</div>

**Methods I've implemented from scratch, not called from a library:**

```
particle-in-cell (CIC + spectral Poisson)      Dormand–Prince 8(5,3), Radau
lattice Boltzmann D2Q9 (Gauss–Hermite)         symplectic Störmer–Verlet
rigorous coupled-wave analysis (RCWA)          Benettin variational algorithm
exact Riemann solver for Euler                 generalized eigenvalue problems
Rayleigh equation eigensolver                  Toeplitz operator inversion
GOY shell model of turbulence                  Faddeeva-function root finding
Oldroyd-B / FENE-P with log-conformation       SO(3) ordered exponentials
```

<br>

## Fields, in the order I fell into them

```
aerospace & compressible flow ──┐
                                ├──→ hyperbolic conservation laws, entropy conditions
fluid mechanics ────────────────┤
                                ├──→ hydrodynamic stability, turbulence, rheology
kinetic theory ─────────────────┤
                                ├──→ Vlasov–Poisson, Chapman–Enskog
geometric mechanics ────────────┤
                                ├──→ non-holonomic systems, symplectic integration
field theory ───────────────────┘
                                └──→ string cosmology, anomalous dimensions
```

The thread that ties them: **how macroscopic laws emerge, and where they fail.**
Navier–Stokes from Boltzmann. Hydrodynamics from kinetics. Friedmann from
strings. Every one of these emergences has a domain of validity, and finding its
edge is more interesting than applying it inside.

<br>

## GitHub

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=Koussay17&show_icons=true&theme=nightowl&hide_border=true&include_all_commits=true&count_private=true&title_color=1f3b73&icon_color=2f7d4f" alt="stats"/>
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Koussay17&layout=compact&theme=nightowl&hide_border=true&langs_count=8&title_color=1f3b73" alt="languages"/>

<br>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=Koussay17&theme=nightowl&hide_border=true&ring=1f3b73&fire=b3452c&currStreakLabel=2f7d4f" alt="streak"/>

</div>

<br>

## Currently

- Extending the $\mathrm{O}(d,d)$ formalism to **Bianchi I**, to settle whether
  the anisotropic instability of paper 01 is fatal or curable
- Computing **perturbations through the bounce** — the background is now known
  and regular to $10^{-12}$, so it's tractable
- Implementing **adaptive spatial resolution** for RCWA, to break the
  $N^{-1.15}$ edge-singularity ceiling of paper 05
- Reading: Frisch on turbulence, Hairer–Lubich–Wanner on geometric integration,
  Montgomery on sub-Riemannian geometry

<br>

<div align="center">

## Open to

**PhD positions · research internships · collaborations**

theoretical & computational physics · fluid mechanics · kinetic theory · geometric mechanics

<br>

[![Email](https://img.shields.io/badge/Email-contact-b3452c?style=for-the-badge&logo=gmail&logoColor=white)](#)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](#)
[![Portfolio](https://img.shields.io/badge/Portfolio-10_papers-1f3b73?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Koussay17/M.Koussay-engineering-portfolio)

<br><br>

> *"Ce que ce travail ne fait pas est tout aussi important."*
>
> Every paper I write ends with a section on its own limits — stated,
> quantified, and left open. It is the section I spend the longest on,
> and the one a jury reads first.

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:b3452c,50:2f7d4f,100:1f3b73&height=110&section=footer" width="100%"/>

</div>

<!--
  ─────────────────────────────────────────────────────────────────────
  TO CUSTOMIZE BEFORE PUBLISHING:
    · Email and LinkedIn badges above have placeholder links (#) — add yours
    · "Currently" section: edit to match what you're actually working on
    · If you want a specific academic title (student / graduate / etc.),
      add it under the header — I left it out rather than guess
    · Stats cards render from your public activity automatically
  ─────────────────────────────────────────────────────────────────────
-->
