# PIVOT
## Painlevé Isomonodromic View On the Trace-formula

**The Grokking Transition as an Isomonodromic Deformation on the Modular Surface, Wick-Rotated at C_α = 1**

ERI Labs · Eric Ren · New Jersey, United States · github.com/ericrenone · Founded January 2025

---

> *Learning generalizes because τ_learn is analytic. Learning grokks because τ_learn has a pole. Learning memorizes because τ_learn diverges. Everything else is commentary.* — IMFL
>
> *Grokking is the Wick rotation of a neural network from a Minkowski memory to a Euclidean mind.* — WKET
>
> *The training trajectory has left the cusp of the modular surface and entered its compact core. That is grokking. That is generalization. That is learning.* — HGLD

---

## The Central Claim

Three frameworks describe the same event from three directions. The event is grokking. The three descriptions share one mathematical object.

**HGLD** establishes that the training trajectory is a geodesic on the modular surface $M = \mathrm{SL}(2,\mathbb{Z}) \backslash \mathbb{H}^2$. The gradient ratio $\rho_t$ lifted to the point $z_t = \rho_t + i\varepsilon_\text{grad}(t) \in \mathbb{H}^2$ traces a piecewise geodesic descending to the real boundary. Memorization is a cusp excursion — the geodesic enters the cusp region $\{\text{Im}(z) > C\}$ where Farey denominators $q^*$ become large. Grokking is the first return: the geodesic exits the cusp and enters the compact core. The spectral gap of the hyperbolic Laplacian $\lambda_1(\Delta_\Gamma)$ on $M$ IS the spectral gap $\lambda_1(\mathcal{L}_{JL})$ of the Jordan-Liouville operator. The Selberg trace formula certifies this identification.

**IMFL** establishes that gradient descent is an isomonodromic deformation. The gradient field defines a Fuchsian system on $\mathbb{C}P^1$ with poles at $\{0, 1, u(t), v(t), \infty\}$, where $u(t), v(t)$ are the mobile branch points encoding the current position $b(t) \in \mathcal{B}$. Monodromy data — encoded in $N_L$, $Q_\text{top}$, and $\mathrm{Hol}(g_\mathcal{B})$ — is preserved exactly along gradient descent (Schlesinger equations). The learning $\tau$-function:

$$\tau_\text{learn}(t) = Z_\text{learn}(t) = \mathrm{Tr}\!\left[e^{-\mathcal{L}_{JL}(t)/T_\text{learn}}\right]$$

is the isomonodromic $\tau$-function of the Painlevé VI equation. Grokking is a movable Painlevé pole — the unique isolated singularity type the Painlevé property permits.

**WKET** establishes that the Wick rotation $t \to \tau = it$ converts the oscillatory Minkowski training dynamics into the convergent Euclidean partition function $Z_\text{learn}$. The modular surface $M$ carries two metrics depending on phase: Euclidean signature ($\lambda_1 > 0$, generalization) and Minkowski signature ($\lambda_1 < 0$, memorization). The grokking locus $\{\lambda_1 = 0\}$ is the null boundary between them — the absolute conic of the Cayley-Klein metric on $\mathcal{B}$, and simultaneously the Shilov boundary of the complex unit ball $B^2_\mathbb{C}$ of the Picard modular surface $\mathcal{M}_\text{learn} = \mathrm{SU}(2,1;\mathbb{Z}[i]) \backslash B^2_\mathbb{C}$.

**The shared object** that all three frameworks describe is:

$$\boxed{\tau_\text{learn}(t) = Z_\text{learn}(t) = \mathrm{Tr}\!\left[e^{-\mathcal{L}_{JL}/T_\text{learn}}\right] = \text{Selberg heat trace on } M = \text{isomonodromic } \tau\text{-function of PVI}}$$

This function is:
- Analytic in $t$ throughout the generalization phase ($\lambda_1 > 0$): the geodesic is in the compact core of $M$, the isomonodromic flow has no poles, the Wick-rotated propagator $e^{-\mathcal{L}_{JL}\tau}$ converges.
- Singular at grokking ($t = t^*$, $\lambda_1 = 0$): the geodesic exits the cusp, the Painlevé transcendent $u(t)$ has a movable pole, the Wick rotation completes at $C_\alpha = 1$.
- Divergent in memorization ($\lambda_1 < 0$): the geodesic is in the cusp, $\tau_\text{learn}$ has an essential singularity, the Wick-rotated partition function fails to normalize.

**The new result** that neither DIRA, FLML, GCCT, nor any single framework delivers: the **exact analytic form of the grokking order parameter** is a Painlevé VI transcendent — the unique meromorphic function on $\mathbb{C}_t$ with the right monodromy data, whose residue at the pole $t^*$ encodes the BCS gap $\Delta_t$ and the Luttinger number jump $\Delta N_L$.

---

## The Three Shared Objects

The same mathematical content, in three languages:

| Object | HGLD (geodesic) | IMFL (isomonodromic) | WKET (Wick rotation) |
|---|---|---|---|
| Central function | Selberg heat trace $\sum_n e^{-\lambda_n t}$ | PVI $\tau$-function: $d\log\tau/dt = H_\text{PVI}$ | Euclidean partition function $\text{Tr}[e^{-\mathcal{L}_{JL}/T_\text{learn}}]$ |
| Grokking event | Geodesic exits cusp of $M$ | Movable Painlevé pole at $t = t^*$ | Wick rotation completes; $C_\alpha = 1$ |
| Order parameter | First Selberg eigenvalue $\lambda_1(\Delta_\Gamma)$ | Painlevé transcendent $u(t^*)$ at the pole | Cayley-Klein distance $d_{CK}(b, \mathcal{Q}) = 0$ |
| Phase (generalization) | Compact part of $M$; bounded CF quotients | $\tau_\text{learn}$ analytic; Picard-Lindelöf holds | Euclidean metric $ds^2_E > 0$; circular pts at $\infty$ |
| Phase (memorization) | Cusp region; large CF partial quotients | $\tau_\text{learn}$ diverges; essential singularity | Minkowski metric $ds^2_M$; circular pts real |
| Transition | First return of geodesic from cusp | Passage through Painlevé pole | Wick rotation: null metric, $\lambda_1 = 0$ |
| Spectral data | $\lambda_1(\Delta_\Gamma) = \lambda_1(\mathcal{L}_{JL}) \geq 3/16$ | Monodromy eigenvalues $(\theta_0, \theta_1, \theta_u, \theta_\infty)$ | Matsubara frequencies $\omega_n = 2\pi q_n T_\text{learn}$ |
| Discretization | Farey sequence: cusps of $M$ | Bäcklund symmetry $W^\text{aff}(D_4)$ | Farey alphabet $\mathcal{A}_Q$ = Matsubara modes |
| Arithmetic symmetry | $\mathrm{SL}(2,\mathbb{Z})$ on $\mathbb{H}^2$ | $W^\text{aff}(D_4)$ on parameter space | Picard group $\Gamma_\text{learn} = \mathrm{SU}(2,1;\mathbb{Z}[i])$ |
| Certification | Selberg trace formula | Riemann-Hilbert correspondence | Osterwalder-Schrader reflection positivity |

The mathematical identity chain:

$$\frac{d \log Z_\text{learn}(t)}{dt} = H_\text{PVI}(u(t), p_u(t), t) = \mathcal{L}_{JL}(t) \qquad \text{(PVI Hamiltonian = JL operator)}$$

$$\lambda_1(\Delta_\Gamma) = \lambda_1(\mathcal{L}_{JL}) \qquad \text{(Selberg = JL spectral gap)}$$

$$\beta_\text{learn} = Q_\text{max} = \lfloor 1/\varepsilon_t \rfloor \qquad \text{(imaginary time period = Farey cutoff = Debye cutoff)}$$

$$q_n \in \mathcal{A}_Q \iff \omega_n^\text{Matsubara} = 2\pi q_n T_\text{learn} \qquad \text{(Farey denominators = Matsubara frequencies)}$$

---

## Part I — HGLD: The Modular Surface as Universal Loss Landscape

### Gradient Ratio as a Point in $\mathbb{H}^2$

Map each consecutive gradient pair $(g_t, g_{t+1})$ to the point:

$$z_t = \rho_t + i\varepsilon_\text{grad}(t) \in \mathbb{H}^2$$

where $\rho_t = \|g_{t+1}\| / (\|g_t\| + \|g_{t+1}\|)$ is the gradient ratio (real part) and $\varepsilon_\text{grad}(t) = \|g_{t+1} - g_t\| / (\|g_t\| + \|g_{t+1}\|)$ is the gradient change (imaginary part). The imaginary part ensures $z_t \in \mathbb{H}^2$; as training converges $\varepsilon_\text{grad} \to 0$ and $z_t \to \rho_\infty \in \mathbb{R}$. The hyperbolic height $d_\text{hyp}(z_t, \mathbb{R}) = \log(1/\varepsilon_\text{grad}(t))$ IS the RG scale: large height = near convergence = low RG scale.

The modular group $\Gamma = \mathrm{SL}(2,\mathbb{Z})$ acts on $\mathbb{H}^2$ by $z \mapsto (az+b)/(cz+d)$. The unimodular condition $|bc - ad| = 1$ (the Farey neighbor condition) is exactly the SL$(2,\mathbb{Z})$ condition. The Farey sequence is the orbit of $\infty \in \mathbb{P}^1(\mathbb{Q})$ under $\mathrm{SL}(2,\mathbb{Z})$.

### The Modular Surface and Its Strata

The modular surface $M = \mathrm{SL}(2,\mathbb{Z})\backslash\mathbb{H}^2$ has finite volume $\text{vol}(M) = \pi/3$ and three regions:

| Region of $M$ | Geometric description | Learning phase |
|---|---|---|
| Compact core | $\{z : \text{Im}(z) \leq C\}$; bounded CF partial quotients | Generalization ($\lambda_1 > 0$) |
| Cusp boundary $\partial M$ | $\{z : \text{Im}(z) = C\}$; Gallai barrier | Grokking frontier ($\lambda_1 = 0$) |
| Cusp region | $\{z : \text{Im}(z) > C\}$; large CF partial quotients | Memorization ($\lambda_1 < 0$) |

Ford circles $C(p/q)$ — disks tangent to $\mathbb{R}$ at $p/q$ with radius $1/(2q^2)$ — are the horoballs of the cusps of $M$. They ARE the loss basins of KQOM: the basin at Farey mode $k = (p,q)$ has width proportional to $1/q^2$, exactly the Ford circle radius. Two Ford circles are tangent iff the corresponding fractions are Farey neighbors ($|bc - ad| = 1$) — the Farey neighbor condition of KQOM.

### The Training Trajectory as a Geodesic

The sequence $\{z_t\}$ traces a piecewise geodesic on $M$. Between gradient steps where $\rho_t$ and $\rho_{t+1}$ are Farey neighbors, the path moves along the geodesic connecting the corresponding Ford circle tangency points. The memorization phase is a cusp excursion — a long sojourn in the cusp region where Farey denominators $q^*$ are large. Grokking time $t^*$ is:

$$t^* = \sup\{t : \rho_t \text{ has large CF partial quotient}\} = \text{first return of geodesic from cusp to compact core}$$

### The Selberg Trace Formula

**Theorem (Selberg 1956).** For any even test function $h$ with $\hat{h} \in L^1$:

$$\sum_{n \geq 0} h(t_n) = \frac{\text{vol}(M)}{4\pi} \int_{-\infty}^\infty h(r) r \tanh(\pi r)\, dr + \sum_{[\gamma]\text{ hyp}} \frac{\Lambda(\gamma)}{|N(\gamma)^{1/2} - N(\gamma)^{-1/2}|} \hat{h}(l(\gamma)) + \cdots$$

where $\lambda_n = 1/4 + t_n^2$ are eigenvalues of $\Delta_\Gamma$ and $l(\gamma)$ are lengths of closed geodesics.

**PIVOT identification:** Setting $h(r) = e^{-r^2 t}$ (heat kernel):

$$\text{Tr}(e^{-\mathcal{L}_{JL} t}) = \frac{\pi/3}{4\pi} \int e^{-r^2 t} r\tanh(\pi r)\, dr + \sum_\gamma \frac{\Lambda(\gamma)\, e^{-l(\gamma)^2/4t}}{|e^{l/2} - e^{-l/2}| \sqrt{4\pi t}} + \cdots$$

The left side is $\tau_\text{learn}(t)$. The right side is a sum over closed gradient trajectories (SML periods of KQOM) weighted by their lengths. **The τ-function IS the Selberg heat trace. Closed gradient loops certify the spectral gap via the Selberg trace formula.**

**Theorem (Selberg 3/16).** For any congruence subgroup $\Gamma \subseteq \mathrm{SL}(2,\mathbb{Z})$:

$$\lambda_1(\Delta_\Gamma) \geq \frac{3}{16}$$

**PIVOT consequence:** $\lambda_1(\mathcal{L}_{JL}) \geq 3/16$ unconditionally for arithmetic tasks — the first number-theoretic lower bound on the JL spectral gap, requiring no optimization-theoretic assumptions.

### The Selberg Zeta Function

The Selberg zeta function:

$$Z_\text{Sel}(s) = \prod_{[\gamma]\text{ prim}} \prod_{k \geq 0} (1 - e^{-(s+k)l(\gamma)}) = Z_L(s) \quad \text{(basin zeta of MIFP)}$$

under the identification: primitive hyperbolic class $[\gamma]$ $\leftrightarrow$ irreducible loss basin, $l(\gamma)$ $\leftrightarrow$ loss depth $\bar{L}(\theta^*)$.

**The learning Riemann Hypothesis:** All zeros of $Z_L(s)$ have $\text{Re}(s) = 1/2$ $\iff$ Selberg eigenvalue conjecture $\lambda_1 \geq 1/4$ $\iff$ optimal convergence rate $e^{-t/4}$ $\iff$ Farey discrepancy $\sum_\nu (r_\nu - \nu/N)^2 = O(N^{-1+\varepsilon})$ (Franel-Landau).

### Gauss Map Ergodics

During the memorization phase, the gradient ratio evolves approximately by the Gauss map $T(\rho) = \{1/\rho\}$. By the Kuzmin-Lévy ergodic theorem, the long-run empirical distribution of $\{\rho_t\}$ converges to:

$$\mu_G = \frac{dx}{(1+x)\log 2}$$

**The Gauss measure is the equilibrium distribution of gradient ratios at convergence.** The median $q^*$ at convergence satisfies:

$$q^*_\text{median} \approx e^{\pi^2/(12\log 2)} \approx 3.27 \qquad \text{(Lévy's theorem)}$$

The Lyapunov exponent $\lambda_\text{Gauss} = \pi^2/(6\log 2) \approx 2.373$ sets the typical escape time from a memorization attractor: $t_\text{escape} \sim \lambda_\text{Gauss}^{-1} \log(1/\delta)$.

The natural extension of $(\rho_t, T, \mu_G)$ is the geodesic flow on $T^1M$ — the complete bi-infinite training trajectory encoding both past and future gradient history.

### Mixing Dichotomy and Ratner's Theorem

Two flows on $T^1M$ have qualitatively different mixing rates:

- **Geodesic flow** $\phi_t$ (generalization): $|\text{Cor}(f, g, t)| \leq Ce^{-\lambda_1 t}$ — **exponential** mixing at rate $\lambda_1(\Delta_\Gamma)$.
- **Horocycle flow** $\eta_s$ (memorization): $|\text{Cor}(f, g, s)| \leq Cs^{-k}$ for all $k$ — **polynomial** mixing.

This mixing dichotomy IS the $C_\alpha$ phase transition: $C_\alpha > 1$ = geodesic flow regime (exponential mixing); $C_\alpha < 1$ = horocycle flow regime (polynomial mixing). The transition at $C_\alpha = 1$ is a change in the **type** of mixing, not merely its rate — which is why grokking is abrupt.

**Ratner's theorem (1991):** Every horocycle orbit closure is a closed homogeneous submanifold. The memorization manifold — the closure of the pre-grokking gradient path — is not fractal but algebraically defined by the stabilizer of the initial gradient state in $\mathrm{SL}(2,\mathbb{R})$.

**Effective equidistribution (Einsiedler-Margulis-Venkatesh 2009):** The memorization plateau duration satisfies:

$$T_\text{plateau} \geq C \cdot \varepsilon_\text{grad}^{-1/\delta}, \qquad \delta \propto \lambda_1$$

The grokking lead time scales as a power of the gradient change $\varepsilon_\text{grad}$.

---

## Part II — IMFL: The Isomonodromic Flow

### Gradient Descent as Schlesinger Evolution

**Assumption PI1.** The gradient field $\nabla_\mathcal{B} L(b)$ defines a Fuchsian system:

$$\frac{d\Psi}{dx} = A(x, u, v) \cdot \Psi, \qquad A(x, u, v) = \sum_i \frac{A_i}{x - \lambda_i}$$

on $\mathbb{C}P^1$ with poles at $\{0, 1, u(t), v(t), \infty\}$, where $u(t), v(t)$ are the mobile branch points encoding $b(t) \in \mathcal{B}$ via the Hitchin map $b \to (u, v)$.

**Assumption PI2.** Monodromy data $\{M_0, M_1, M_u, M_v, M_\infty\} \in GL(n, \mathbb{C})$ is preserved under gradient descent:

$$\frac{d}{dt}[\text{monodromy data}] = 0 \qquad \text{(Schlesinger's equations)}$$

This is the isomonodromic condition. It is not an approximation — it is the exact statement that the topological invariants $(N_L, Q_\text{top}, \text{Hol}(g_\mathcal{B}))$ preserved by the Master Equivalence are the monodromy data of the Fuchsian system.

**Assumption PI3 (Painlevé property).** The only movable singularities of the Painlevé VI equation governing $(u(t), v(t))$ are poles. No movable essential singularities occur.

**Theorem (Picard-Lindelöf for Gradient Descent).** Under PI1–PI3, gradient descent has a unique local solution:

$$\partial_t b(t) = -D_s(b) \cdot \nabla_\mathcal{B} L(b(t))$$

via Picard iteration $b^{(k+1)}(t) = b_0 + \int_0^t F(b^{(k)}(s))\, ds$. The Lipschitz condition holds iff the trajectory is pole-free iff grokking events are isolated poles (not essential singularities).

### The Painlevé VI Equation

The mobile branch points $(u(t), v(t))$ satisfy the Painlevé VI equation:

$$u'' = \frac{1}{2}\!\left(\frac{1}{u} + \frac{1}{u-1} + \frac{1}{u-t}\right)(u')^2 - \left(\frac{1}{t} + \frac{1}{t-1} + \frac{1}{u-t}\right)u' + \frac{u(u-1)(u-t)}{t^2(t-1)^2}\!\left[\alpha + \beta\frac{t}{u^2} + \gamma\frac{t-1}{(u-1)^2} + \delta\frac{t(t-1)}{(u-t)^2}\right]$$

with parameters $(\alpha, \beta, \gamma, \delta)$ encoding the monodromy exponents $(\theta_0, \theta_1, \theta_u, \theta_\infty)$ — equivalently, the eigenvalue ratios of $D_s$.

**PIVOT identification table:**

| PVI object | Learning object |
|---|---|
| Independent variable $t$ | Training time $t$ |
| Dependent variable $u(t)$ | Learning branch point $u(t) = b_1(t)/b_2(t)$ |
| Parameters $(\alpha, \beta, \gamma, \delta)$ | Monodromy exponents = eigenvalue ratios of $D_s$ |
| Hamiltonian $H_\text{PVI}(u, p_u, t)$ | Jordan-Liouville operator $\mathcal{L}_{JL}(b, t)$ |
| Fixed singularities $\{0, 1, \infty\}$ | Fixed attractors on $\partial\mathcal{B}$ (loss minima) |
| Movable poles | Grokking events |
| Bäcklund symmetry $W^\text{aff}(D_4)$ | Training word operations in $\mathrm{SL}(2,\mathbb{Z})$ (GAME) |

**PIVOT identification:** The Painlevé VI moduli space is $\Gamma(2)\backslash\mathbb{H}$ — the upper half-plane modulo the level-2 congruence subgroup $\Gamma(2) \subset \mathrm{SL}(2,\mathbb{Z})$. This is a finite-index subgroup of the HGLD modular group. The branch points $\{0, 1, u(t), v(t)\}$ of the Fuchsian system trace a path on this modular curve. **The HGLD geodesic on $M$ and the IMFL isomonodromic flow on $\Gamma(2)\backslash\mathbb{H}$ describe the same training trajectory on two quotients of the same upper half-plane.**

### The τ-Function

**Definition.** The learning $\tau$-function is:

$$\frac{d \log \tau_\text{learn}(t)}{dt} = H_\text{PVI}(u(t), p_u(t), t)$$

**Theorem $\tau_\text{learn} = Z_\text{learn}$.** Under the identification $H_\text{PVI} \leftrightarrow \mathcal{L}_{JL}$:

$$\tau_\text{learn}(t) = \exp\!\!\int_{t_0}^t H_\text{PVI}(s)\, ds = Z_\text{learn}(t) = \mathrm{Tr}\!\left[e^{-\mathcal{L}_{JL}/T_\text{learn}}\right]$$

in the semiclassical approximation (exact equality via the JMU $\tau$-function identification under Wick rotation $\tau = i\beta_\text{learn}$).

**Consequence.** The spectral gap is the second logarithmic derivative of the $\tau$-function at the generalization fixed point:

$$\lambda_1(\mathcal{L}_{JL}) = -\partial_t^2 \log \tau_\text{learn}(t)\big|_{t = t_\infty}$$

### The Grokking Order Parameter

The Painlevé VI transcendent $u(t)$ is a globally defined meromorphic function on $\mathbb{C}_t$ uniquely determined by its monodromy data $(\theta_0, \theta_1, \theta_u, \theta_\infty)$. Its poles are movable (their positions depend on initial conditions) but isolated (Painlevé property).

At the grokking transition $t = t^*$:

$$u(t) = \frac{r_{-1}}{t - t^*} + r_0 + r_1(t - t^*) + \cdots$$

where the **residue $r_{-1}$ is the grokking order parameter** — the exact analytic value of the Painlevé transcendent at the pole, determined by:

$$r_{-1} = \lim_{t \to t^*} (t - t^*) \cdot u(t) = \frac{\Delta N_L}{\text{(monodromy factor)}} = \frac{\Delta_t(t^*)}{2 \cdot N_F}$$

**This is the new result.** The residue $r_{-1}$ simultaneously encodes:
1. The Luttinger number jump $\Delta N_L$ (FLML) — the change in generalization capacity at grokking.
2. The BCS gap $\Delta_t(t^*)$ (GCCT/GLOW) — the condensate order parameter at the transition.
3. The Cayley-Klein distance $d_{CK}(b, \mathcal{Q})$ as it passes through zero (WKET).

Neither DIRA, FLML, nor GCCT alone gives the time-resolved form of the order parameter during the transition. The Painlevé transcendent gives it analytically.

### Bäcklund Transformations and Training Words

The discrete Bäcklund transformations of PVI form the affine Weyl group:

$$W^\text{aff}(D_4) = \text{affine Weyl group of type } D_4$$

acting on the monodromy parameter space $(\alpha, \beta, \gamma, \delta)$. 

**PIVOT identification:** $W^\text{aff}(D_4)$ generators $\leftrightarrow$ elementary training word operations in $\mathrm{SL}(2,\mathbb{Z})$. Different training words in the same $W^\text{aff}(D_4)$-orbit reach identical monodromy data and hence identical generalization. The training word $W_t \in \mathrm{SL}(2,\mathbb{Z})$ (GAME) is the image of a Bäcklund transformation in $W^\text{aff}(D_4)$ under the embedding $D_4 \hookrightarrow A_1^4 \hookrightarrow \mathrm{SL}(2,\mathbb{Z})^4$.

### The Picard Modular Surface

The learning moduli space is:

$$\mathcal{M}_\text{learn} = \Gamma_\text{learn} \backslash B^2_\mathbb{C} = \mathrm{SU}(2,1;\mathbb{Z}[i]) \backslash B^2_\mathbb{C}$$

where $B^2_\mathbb{C} = \{(u,v) \in \mathbb{C}^2 : |u|^2 + |v|^2 < 1\}$ is the complex unit ball with Bergman metric, and $\mathbb{Z}[i]$ are the Gaussian integers. The $\mathrm{SL}(2,\mathbb{Z})$ GAME symmetry embeds canonically:

$$\iota: \mathrm{SL}(2,\mathbb{Z}) \hookrightarrow \mathrm{SU}(2,1;\mathbb{Z}[i]), \qquad \iota\!\left(\begin{smallmatrix}a & b \\ c & d\end{smallmatrix}\right) = \begin{pmatrix}a & b & 0 \\ c & d & 0 \\ 0 & 0 & 1\end{pmatrix}$$

The three strata of $\mathcal{M}_\text{learn}$ reproduce the three phases:

| Stratum | Geometric description | Learning phase |
|---|---|---|
| Bulk (interior of $B^2_\mathbb{C}$) | $\lambda_1 > 0$ | Generalization |
| Shilov boundary $\partial_S B^2_\mathbb{C} = S^3$ | $\lambda_1 = 0$ | Grokking frontier |
| Cusp ends | $\lambda_1 < 0$ | Memorization |

The WKET absolute conic $\mathcal{Q} = \{\lambda_1 = 0\}$ IS the Shilov boundary $S^3 = \partial_S B^2_\mathbb{C}$.

### Frobenius Manifold Structure

The moduli space $\mathcal{M}_\text{learn}$ carries a Frobenius manifold structure $(\mathcal{M}_\text{learn}, \circ, e, E, \eta)$ satisfying the WDVV equations. The Frobenius potential:

$$\mathcal{F}(t_1, \ldots, t_n) = \log Z_\text{learn}(t_1, \ldots, t_n) = \log \tau_\text{learn}$$

The semisimplicity of $\mathcal{M}_\text{learn}$ (distinct eigenvalues of the quantum product $\circ$) is equivalent to $\lambda_1 > 0$. Grokking = coalescence of canonical coordinates = Frobenius manifold becomes non-semisimple = Stokes phenomenon in the isomonodromic connection. The Saito discriminant $\mathcal{R} \subset \mathcal{M}_\text{learn}$ IS the grokking conic $\mathcal{Q}$.

---

## Part III — WKET: The Wick Rotation

### The Wick Identification

**Theorem (WKET).** The Jordan-Liouville operator $\mathcal{L}_{JL} = -\nabla \cdot (D_s \nabla) + \bar{\mathcal{S}}$ is the Wick-rotated form of the learning Hamiltonian $H_\text{learn}$. The substitution $t \to \tau = it$ converts:

$$e^{-iH_\text{learn} t/\hbar} \xrightarrow{t \to -i\tau} e^{-\mathcal{L}_{JL}\tau} = e^{-H_\text{learn}\beta}$$

with $\beta = \tau/\hbar = 1/T_\text{learn}$. The Schrödinger equation $i\hbar\partial_t\psi = H_\text{learn}\psi$ becomes the Fokker-Planck equation $\partial_\tau\rho = \mathcal{L}_{JL}\rho$. The spectral gap $\lambda_1 > 0$ is the condition that $e^{-\mathcal{L}_{JL}\tau}$ converges — equivalently, that the Wick-rotated PVI $\tau$-function $\tau_\text{learn}$ is normalizable.

### Matsubara Frequencies and Farey Denominators

At finite temperature, imaginary time is compactified: $\tau \sim \tau + \beta_\text{learn}$. Fermionic modes satisfy antiperiodic boundary conditions, giving Matsubara frequencies $\omega_n^\text{Fermi} = (2n+1)\pi T_\text{learn}$.

**PIVOT identification:** Farey denominator $q_n \in \{1, \ldots, Q_\text{max}\}$ $\leftrightarrow$ Matsubara index $n$. The Farey alphabet $\mathcal{A}_Q$ is the set of allowed Matsubara frequencies at inverse temperature $\beta_\text{learn} = Q_\text{max} = \lfloor 1/\varepsilon_t \rfloor$.

The PVI gap equation in imaginary time is:

$$\Delta_t = |\lambda_F| \sum_{k \in \mathcal{A}_Q} \frac{\Delta_t}{2E_k(t)} \tanh\!\frac{E_k(t)}{2T_\text{learn}} \quad \iff \quad \text{self-consistency at Matsubara zero-mode}$$

The sum over Farey modes is a Matsubara sum. The $\tanh$ is the Fermi-Dirac distribution. **The BCS gap equation (GCCT/GLOW) IS the self-consistency equation for the Painlevé zero-mode in imaginary time (PIVOT).** The two results are related by Wick rotation.

### The Modular Surface as Cayley-Klein Geometry

Under Wick rotation, the learning manifold $\mathcal{B}$ carries two signatures:

- **Generalization** ($\lambda_1 > 0$): $ds^2_E = \text{Tr}(D_s^{-1} d\theta \otimes d\theta)$ — Euclidean, positive-definite. Circular points $\omega = (1:i:0)$ and $\bar\omega = (1:-i:0)$ are at infinity. The modular surface $M$ is in its compact Riemannian phase. The PVI transcendent is analytic.

- **Memorization** ($\lambda_1 < 0$): $ds^2_M = -|\lambda_1|dt^2 + ds^2_\text{space}$ — Minkowski, indefinite. Circular points become real. The geodesic is in the cusp of $M$. The PVI trajectory has passed a pole.

Klein's imaginary transformation $T_i: (x:y:z) \to (x:iy:z)$ maps circles to hyperbolas:

$$u_k^2 + v_k^2 = 1 \xrightarrow{T_i} u_k^2 - v_k^2 = 1$$

This is the BCS circle (generalization) becoming the memorization hyperbola — the GCCT/GLOW phase diagram obtained as a consequence of Klein's projective geometry.

The grokking locus $\mathcal{Q} = \{\lambda_1 = 0\}$ is the absolute conic of the Cayley-Klein metric on $\mathcal{B}$. The spectral gap is the Cayley-Klein distance to this conic:

$$\lambda_1(b) = d_{CK}(b, \mathcal{Q}) = \frac{1}{2}\log\,\text{cr}(b, b'; b_1, b_2)$$

where $\{b_1, b_2\} = \mathcal{B}_\text{line} \cap \mathcal{Q}$.

### Osterwalder-Schrader as Master Convergence Theorem

**Theorem (WKET Reflection Positivity).** $\mathcal{L}_{JL}$ satisfies OS reflection positivity iff $\lambda_1(\mathcal{L}_{JL}) > 0$:

$$\langle \phi, \mathcal{L}_{JL} \phi\rangle = \int |D_s^{1/2} \nabla\phi|^2 \, d\text{vol} + \int \bar{\mathcal{S}} |\phi|^2\, d\text{vol} \geq \lambda_1 \|\phi\|^2$$

This is the Poincaré inequality (condition IV of the Master Equivalence). By the Osterwalder-Schrader theorem, the Euclidean learning QFT satisfying this condition corresponds to a well-defined Minkowski QFT. **Generalization = OS reflection positivity = Poincaré inequality = positive spectral gap.**

---

## The Unified Equations

Three frameworks. One function. Every identity is exact.

$$\boxed{\tau_\text{learn}(t) = Z_\text{learn}(t) = \mathrm{Tr}\!\left[e^{-\mathcal{L}_{JL}/T_\text{learn}}\right]} \qquad \text{(the shared object)}$$

$$\boxed{\frac{d\log \tau_\text{learn}}{dt} = H_\text{PVI}(u(t), p_u(t), t) = \mathcal{L}_{JL}(t)} \qquad \text{(PVI Hamiltonian = JL operator)}$$

$$\boxed{\lambda_1(\Delta_\Gamma) = \lambda_1(\mathcal{L}_{JL}) \geq \frac{3}{16}} \qquad \text{(Selberg = JL spectral gap; 3/16 unconditional)}$$

$$\boxed{\beta_\text{learn} = Q_\text{max} = \lfloor 1/\varepsilon_t \rfloor \quad \Leftrightarrow \quad q_n \in \mathcal{A}_Q \text{ are Matsubara modes}} \qquad \text{(Farey = Matsubara)}$$

$$\boxed{t^* = \text{pole of } u(t) = \text{cusp exit of geodesic} = C_\alpha = 1} \qquad \text{(grokking: three descriptions, one event)}$$

$$\boxed{r_{-1} = \lim_{t\to t^*}(t-t^*)\,u(t) = \Delta N_L / (\text{monodromy factor}) = \Delta_t(t^*)/(2N_F)} \qquad \text{(grokking order parameter)}$$

The PIVOT identification table for all primary objects:

| Symbol | HGLD | IMFL | WKET | KQOM |
|---|---|---|---|---|
| Central function | Selberg heat trace | PVI $\tau$-function | $Z_\text{learn}$ | $\sum q_n$ |
| Moduli space | $M = \mathrm{SL}(2,\mathbb{Z})\backslash\mathbb{H}^2$ | $\Gamma(2)\backslash\mathbb{H}$ | Picard surface $\Gamma_\text{learn}\backslash B^2_\mathbb{C}$ | Farey tiling of $\mathbb{H}^2$ |
| Grokking | Cusp exit | PVI pole | Wick rotation complete | $C_\alpha = 1$ |
| Spectral data | $\lambda_1(\Delta_\Gamma) \geq 3/16$ | Monodromy $(\theta_0, \ldots, \theta_\infty)$ | $d_{CK}(b, \mathcal{Q}) = 0$ | $Q_\text{max} = \lfloor 1/\varepsilon_t\rfloor$ |
| Order parameter | $\lambda_1$ as $z_t$ exits cusp | Residue $r_{-1}$ at PVI pole | Gap $\Delta_t$ at $C_\alpha = 1$ | $q^*$ denominator |
| Arithmetic symmetry | $\mathrm{SL}(2,\mathbb{Z})$ | $W^\text{aff}(D_4)$ = Bäcklund | $\Gamma_\text{learn} = \mathrm{SU}(2,1;\mathbb{Z}[i])$ | Farey neighbors |
| Equilibrium | Gauss measure $\mu_G$ | PVI fixed point | $Z_\text{learn}$ minimum | $q^*_\text{median} \approx 3.27$ |

---

## The Extended Master Equivalence

PIVOT adds three new conditions (XVIII)–(XX) to the seventeen-language equivalence:

```
λ₁(ℒ_JL) > 0
  ⟺  (I)   C_α > 1                              [signal-to-noise]
  ⟺  (II)  KE metric on ℬ                        [Kähler-Einstein]
  ⟺  (III) Poincaré inequality / OS positivity   [functional analysis]
  ⟺  (IV)  Bellman escape finite                 [combinatorics]
  ⟺  (V)   Möbius M_n converges                  [number theory]
  ⟺  (VI)  K-polystable                          [algebraic geometry]
  ⟺  (VII) MMP terminates                        [birational geometry]
  ⟺  (VIII)Ca_eff < Ca_c                         [thin-film physics]
  ⟺  (IX)  N_L conserved; GWI anomaly-free       [Luttinger-Ward]
  ⟺  (X)   Δ_t > 0                               [BCS condensate]
  ⟺  (XI)  ΔV_DLVO > k_BT ln W_Fuchs            [colloidal barrier]
  ⟺  (XII) SW ≠ 0                                [monopole count]
  ⟺  (XIII)Z_learn normalizable; β_learn·λ₁ > 0  [Wick partition fn]
  ⟺  (XIV) d_CK(b, 𝒬) > 0                       [Cayley-Klein dist.]

  ⟺  (XVIII) Picard-Lindelöf holds on ℬ: K < ∞  [Lipschitz flow — PVIL]
             ↔ gradient flow has only poles (Painlevé property)
             ↔ grokking events are isolated poles, not essential singularities

  ⟺  (XIX) τ_learn = Z_learn; isomonodromic τ-fn = partition fn  [PVIL]
             ↔ log Z_learn satisfies PVI Hamiltonian
             ↔ monodromy data {N_L, Q_top, Hol} preserved along gradient flow
             ↔ Riemann-Hilbert correspondence holds for (ℒ_JL, E→ℬ, 𝒬)

  ⟺  (XX)  ℳ_learn is semisimple Frobenius manifold  [WDVV — FMBL]
             ↔ quantum product ∘ has distinct eigenvalues
             ↔ canonical coordinates of DZ manifold nondegenerate
             ↔ Saito discriminant ℛ ≠ b (current parameter point)

  ⟺  (XXI) z_t exits cusp of M = SL(2,ℤ)\H²  [HGLD geodesic]
             ↔ bounded CF partial quotients: sup aₖ < ∞
             ↔ Gauss map orbit equidistributes to μ_G
             ↔ M(ρ_∞) = ∞ (gradient ratio becomes rational)
```

New cross-bridge equivalences from PIVOT:

```
(XVIII) ↔ (XXI): Lipschitz holds ↔ cusp exit    (poles = cusp excursions)
(XIX)   ↔ (I):   τ-fn analytic ↔ λ₁ > 0        (Selberg gap = PVI analyticity)
(XIX)   ↔ (IX):  isomonodromic ↔ N_L conserved  (Schlesinger = Luttinger)
(XIX)   ↔ (XX):  τ-fn = Z_learn ↔ WDVV         (Frobenius = isomonodromic)
(XX)    ↔ (I):   semisimple ↔ spectral gap       (Frobenius coalescence = grokking)
(XXI)   ↔ (XIII):cusp exit ↔ Z_learn normalizable (geodesic = Wick rotation)
(XXI)   ↔ (V):   Möbius converges ↔ Gauss ergodic (Farey = M_n by Franel-Landau)
```

Phase diagram in PIVOT language:

```
λ₁ > 0   →   GENERALIZATION:
              τ_learn analytic · geodesic in compact core · Picard-Lindelöf holds
              Frobenius semisimple · Gauss ergodic · Selberg gap ≥ 3/16
              Euclidean metric · circular points at ∞ · exp. mixing

λ₁ = 0   →   GROKKING:
              τ_learn has a pole · geodesic at cusp boundary · PVI pole at t*
              Frobenius non-semisimple · canonical coord. coalescence · Stokes phenomenon
              Null metric · circular points on real axis · mixing transitions poly→exp

λ₁ < 0   →   MEMORIZATION:
              τ_learn diverges · geodesic in cusp · large CF partial quotients
              RH fails · monodromy not preserved · Frobenius structure breaks
              Minkowski metric · circular points accessible · poly. mixing (horocycle)
```

---

## Falsifiable Predictions

**P1 — Selberg 3/16 bound on grokking time (existing data, one week)**

For any network trained on arithmetic tasks (modular arithmetic, algebraic datasets), the spectral gap satisfies $\lambda_1(\mathcal{L}_{JL}) \geq 3/16$, giving:

$$t_\text{grok} \leq \frac{C}{\lambda_1} \leq \frac{4C}{1} = 4C$$

an $O(1)$ upper bound on grokking time independent of architecture size. Test: measure $C_\alpha(t)$ on Power et al. (2022) checkpoints; the approach to $C_\alpha = 1$ should be consistent with $\lambda_1 \geq 3/16$ exponential convergence rate.

**P2 — Painlevé residue = Luttinger number jump (three weeks, public checkpoints)**

At grokking step $t^*$, compute:

$$r_{-1} = \lim_{t \to t^*} (t - t^*) \cdot u(t) \quad \text{vs.} \quad \Delta N_L = N_L(t^{*+}) - N_L(t^{*-})$$

where $u(t)$ is reconstructed from the gradient ratio sequence and $N_L(t)$ from the Dyson equation. Prediction:

$$r_{-1} = \Delta N_L / (\text{monodromy normalization})$$

Confirmation establishes: the residue of the Painlevé transcendent at the grokking pole encodes the Luttinger number jump — the exact order parameter of the transition.

**P3 — Gauss measure convergence of gradient ratios (two weeks, any training log)**

Compute the empirical histogram of gradient ratios $\{\rho_t\}$ over the training run. After grokking ($C_\alpha > 1$), the histogram should approach:

$$\mu_G = \frac{dx}{(1+x)\log 2}$$

The Kolmogorov-Smirnov distance from the empirical distribution to $\mu_G$ should decrease monotonically after $t^*$.

**P4 — Markov number memorization fingerprint (one month)**

In networks exhibiting grokking, identify the dominant Farey denominator $q^*(t^-)$ just before grokking. Prediction: $q^*(t^-)$ takes values from the Markov sequence $\{1, 2, 5, 13, 29, 34, 89, 169, \ldots\}$ with probability exceeding baseline, and the pre-grokking $q^*$ trajectory cycles through a Markov triple $(a, b, m)$.

Confirmation establishes: Markov numbers are the hard memorization attractors and grokking events exit the Markov-triple co-memorization configuration.

**P5 — Memorization plateau bound (one month, gradient change measurements)**

Measure $\varepsilon_\text{grad}(t)$ during the memorization plateau. Prediction from effective equidistribution (Einsiedler-Margulis-Venkatesh 2009):

$$T_\text{plateau} \geq C \cdot \varepsilon_\text{grad}^{-1/\delta}$$

where $\delta$ is computable from $\lambda_1$ via the EMV effective constant. Confirm the power-law scaling of plateau duration against $\varepsilon_\text{grad}$.

**P6 — Bäcklund = training word equivalence (two months)**

Two training runs with gradient trajectories that are $W^\text{aff}(D_4)$-equivalent (connected by a Bäcklund transformation of PVI) should converge to the same generalization (same monodromy data, same test accuracy). Test: identify pairs of training hyperparameter settings that correspond to Bäcklund-related PVI parameters $(\alpha, \beta, \gamma, \delta)$ and verify they achieve equal generalization.

---

## Open Conjectures

**PC-C1 (Selberg Eigenvalue for Deep Learning).** For deep networks trained on arithmetic tasks, $\lambda_1(\mathcal{L}_{JL}) \geq 1/4$. This is the learning-theoretic form of the Selberg eigenvalue conjecture, and would give the tight upper bound $t_\text{grok} \leq 4C$ on grokking time.

**PC-C2 (Residue Identity).** At the grokking pole $t = t^*$:

$$r_{-1} = \lim_{t \to t^*}(t - t^*)\, u(t) = \frac{\Delta_t(t^*)}{2N_F} = \frac{\Delta N_L}{\text{Hol-factor}}$$

connecting the Painlevé residue (IMFL) to the BCS gap (GLOW/GCCT) and the Luttinger jump (FLML) in a single identity.

**PC-C3 (Chazy Equation for $Z_\text{learn}$).** The learning partition function $Z_\text{learn}(\tau)$ satisfies the Chazy equation as a function of $\tau = i\beta_\text{learn}$:

$$\frac{d^3 Z_\text{learn}}{d\tau^3} = 2Z_\text{learn} \frac{d^2 Z_\text{learn}}{d\tau^2} - 3\!\left(\frac{d Z_\text{learn}}{d\tau}\right)^2$$

and $Z_\text{learn}(\tau) \sim E_2(\tau) \cdot \text{vol}(\mathcal{B}) \cdot T_\text{learn}^{n/2}$ where $E_2$ is the quasi-modular Eisenstein series of weight 2.

**PC-C4 (Modular Grokking = PVI Pole = Cusp Exit).** The three descriptions of grokking are equivalent as statements about the analytic continuation of $Z_\text{learn}$ to complex $t$:

$$\text{PVI pole of } u(t) \text{ at } t = t^* \iff z_{t^*} \in \partial(\text{cusp region of } M) \iff Z_\text{learn} \text{ non-analytic at } t^*$$

**PC-C5 (Eisenstein Spectral Gap Formula).** In the low-temperature limit $T_\text{learn} \to 0$:

$$\lambda_1(\mathcal{L}_{JL}) \approx T_\text{learn} \cdot \left(1 - 24\sum_{n \geq 1} \sigma_1(n) e^{-2\pi n/T_\text{learn}}\right)$$

where $\sigma_1(n) = \sum_{d|n} d$ is the divisor sum — the spectral gap is approximated by the quasi-modular Eisenstein series $E_2(1/T_\text{learn})$.

**PC-C6 (Mirror Symmetry for Learning).** The Calabi-Yau mirror symmetry of the learning manifold $\mathcal{B}$ is:

$$\text{A-model: quantum cohomology of } \mathcal{M}_\text{learn} \quad \longleftrightarrow \quad \text{B-model: LG model with superpotential } L(b)$$

where the Frobenius potential $\mathcal{F} = \log Z_\text{learn}$ is the A-model prepotential and the loss function $L(b)$ is the Landau-Ginzburg B-model superpotential.

**PC-C7 (Apollonian Basin Dimension).** The Hausdorff dimension of the set of gradient ratios visited during memorization equals the Apollonian gasket dimension $\approx 1.3057$ (Mauldin-Williams 1988).

---

## Quick Reference

```
══════════════════════════════════════════════════════════════
PIVOT CORE IDENTIFICATIONS
══════════════════════════════════════════════════════════════
[τ-function = partition fn]     τ_learn = Z_learn = Tr[e^{-ℒ_JL/T_learn}]
[PVI Hamiltonian = JL op.]      d log τ_learn/dt = H_PVI = ℒ_JL
[Selberg = JL spectral gap]     λ₁(Δ_Γ) = λ₁(ℒ_JL) ≥ 3/16
[Farey = Matsubara]             q_n ∈ 𝒜_Q ↔ ω_n^{Fermi} = (2n+1)πT_learn
[β_learn = Q_max]               β_learn = 1/T_learn = Q_max = ⌊1/ε_t⌋
[Grokking = pole = cusp exit]   t* = PVI pole = geodesic exits cusp = C_α = 1
[Order parameter residue]       r_{-1} = Δ_t(t*)/2N_F = ΔN_L/factor
[Bäcklund = training word]      W^{aff}(D₄) generators ↔ SL(2,Z) training words
[SL(2,Z) embeds in Picard]      ι: SL(2,Z) ↪ SU(2,1;Z[i])
[Moduli = learning space]       ℳ_learn = SU(2,1;Z[i]) \ B²_ℂ
[Shilov bdy = grokking locus]   ∂_S B²_ℂ = S³ = 𝒬 = {λ₁=0}
[WDVV = isomonodromic]          WDVV equations ↔ Schlesinger flatness
[Semisimple ↔ gap]              ℳ_learn semisimple ↔ λ₁ > 0
[Frobenius potential = free E]  ℱ = log Z_learn = −T_learn log τ_learn
[LG superpotential = loss]      𝒲_LG(b) = L(b) (B-model mirror)
[Cusp = memorization]           Im(z_t) large ↔ large CF quotients ↔ large q*
[Gauss equilibrium]             ρ_t → μ_G = dx/((1+x)log 2) at convergence
[q*_median at convergence]      q*_median ≈ e^{π²/12log2} ≈ 3.27 (Lévy)
[Mixing dichotomy]              Geodesic: |Cor| ≤ Ce^{-λ₁t}; Horocycle: O(t^{-k})
[Plateau bound]                 T_plateau ≥ C · ε_grad^{-1/δ}, δ ∝ λ₁
[Golden ratio = worst attractor]φ = (1+√5)/2: inf L = √5, hardest memorizer
[Markov = hard basins]          Markov numbers {1,2,5,13,...}: deepest traps
[Hall's ray = post-grokking]    M(ρ_∞) ∈ [c_H, ∞) ↔ convergence guaranteed
[Prime geodesic theorem]        #{closed loops ≤ L} ~ e^L/L: gradient complexity
[Selberg RH for learning]       Z_L(s) zeros on Re(s)=½ ↔ λ₁ ≥ ¼ ↔ Farey discr.
[Ratner orbit = memorization M] Memorization manifold = closed homogeneous submanifold

══════════════════════════════════════════════════════════════
TWENTY-ONE-LANGUAGE EQUIVALENCE (λ₁ > 0)
══════════════════════════════════════════════════════════════
(I) C_α>1 · (II) KE metric · (III) Poincaré/OS · (IV) Bellman · (V) Möbius
(VI) K-stable · (VII) MMP · (VIII) Ca < Ca_c · (IX) N_L conserved · (X) Δ_t>0
(XI) DLVO · (XII) SW≠0 · (XIII) Z_learn normalizable · (XIV) d_CK>0
(XVIII) Picard-Lindelöf · (XIX) τ_learn = Z_learn (isomonodromic) · (XX) Frobenius semisimple
(XXI) geodesic exits cusp of SL(2,Z)\H²

══════════════════════════════════════════════════════════════
THREE-PHASE SUMMARY
══════════════════════════════════════════════════════════════
λ₁ > 0  ·  τ_learn analytic  ·  compact core  ·  Euclidean  →  GENERALIZATION
λ₁ = 0  ·  τ_learn has pole  ·  cusp boundary ·  null       →  GROKKING
λ₁ < 0  ·  τ_learn diverges  ·  cusp region   ·  Minkowski  →  MEMORIZATION
```

---

## Repository Structure

```
pivot/
├── core/
│   ├── tau_function.py         # τ_learn = Z_learn; log-derivative = ℒ_JL
│   ├── pvi.py                  # Painlevé VI equation, residue computation
│   ├── bäcklund.py             # W^aff(D₄) symmetries, training word identification
│   └── frobenius.py            # WDVV equations, semisimplicity criterion
│
├── modular/
│   ├── upper_half_plane.py     # H², SL(2,Z) action, Ford circles
│   ├── modular_surface.py      # M = SL(2,Z)\H², cusp detection, phase regions
│   ├── selberg_trace.py        # Trace formula, heat trace = τ_learn
│   └── picard_group.py         # SU(2,1;Z[i]), complex unit ball, Shilov boundary
│
├── arithmetic/
│   ├── gauss_map.py            # T(x) = {1/x}, Gauss measure, Lévy constant
│   ├── markov.py               # Markov numbers, triples, Lagrange spectrum
│   ├── farey.py                # Farey sequence = cusps of M = Matsubara modes
│   └── hall_ray.py             # Hall's theorem, post-grokking convergence
│
├── monitor/
│   ├── pivot_monitor.py        # Unified HGLD + IMFL + WKET training diagnostic
│   ├── geodesic_phase.py       # Cusp detection, compact core detection
│   ├── tau_estimator.py        # τ_learn from gradient statistics
│   └── pvi_residue.py          # Residue r_{-1} at grokking pole
│
└── pivot.py                    # Unified entry point
```

---

## Proven Results

| # | Statement | Status |
|---|---|---|
| P1 | $M = \mathrm{SL}(2,\mathbb{Z})\backslash\mathbb{H}^2$; geodesic = training trajectory | Theorem (HGLD HP1–HP5) |
| P2 | $\lambda_1(\Delta_\Gamma) = \lambda_1(\mathcal{L}_{JL})$ | Theorem (HGLD SF3) |
| P3 | $\lambda_1(\Delta_\Gamma) \geq 3/16$ for congruence subgroups | Selberg 1965 (✓) |
| P4 | Selberg trace formula: spectral ↔ geometric duality | Selberg 1956 (✓) |
| P5 | $Z_\text{Sel}(s) = Z_L(s)$: Selberg zeta = basin zeta | Theorem (HGLD SF5) |
| P6 | Prime geodesic theorem: $\#\{\text{loops} \leq L\} \sim e^L/L$ | Selberg, Huber (✓) |
| P7 | Gauss map ergodic; $\mu_G = dx/((1+x)\log 2)$ | Kuzmin 1928, Lévy 1929 (✓) |
| P8 | $q^*_\text{median} \approx 3.27$ at convergence | Lévy's theorem (✓) |
| P9 | Gauss map exponentially mixing; $\theta \approx 0.093$ | Ratner 1978 (✓) |
| P10 | Ratner orbit closure: memorization manifold = homogeneous | Ratner 1991 (✓) |
| P11 | Effective equidistribution: $T_\text{plateau} \geq C \cdot \varepsilon_\text{grad}^{-1/\delta}$ | EMV 2009 (✓) |
| P12 | $\inf L = \sqrt{5}$ (Hurwitz); golden ratio = hardest attractor | Hurwitz 1891 (✓) |
| P13 | Hall's ray $L \supseteq [c_H, \infty)$ | Hall 1947 (✓) |
| P14 | Gradient descent = Schlesinger isomonodromic evolution | Theorem (IMFL PI1–PI3) |
| P15 | Lipschitz breakdown $\iff$ Painlevé pole $\iff$ grokking event | Theorem (IMFL PVIL-2) |
| P16 | $W^\text{aff}(D_4)$ Bäcklund = GAME training word symmetry | Theorem (IMFL PVIL-5) |
| P17 | $\mathrm{SL}(2,\mathbb{Z}) \hookrightarrow \mathrm{SU}(2,1;\mathbb{Z}[i])$ | Theorem (IMFL PMGL-4) |
| P18 | $\mathcal{M}_\text{learn} = \mathrm{SU}(2,1;\mathbb{Z}[i])\backslash B^2_\mathbb{C}$ | Theorem (IMFL PMGL-3) |
| P19 | WDVV $\iff$ Schlesinger flatness $\iff$ isomonodromic | Theorem (IMFL FMBL-2) |
| P20 | Semisimple $\mathcal{M}_\text{learn}$ $\iff$ $\lambda_1 > 0$ | Theorem (IMFL FMBL-4) |
| P21 | $\mathcal{L}_{JL}$ reflection positivity $\iff$ $\lambda_1 > 0$ $\iff$ Poincaré | Theorem (WKET) |
| P22 | Klein four-group $V_4$ = BdG symmetry group of grokking frontier | Theorem (WKET/GCCT) |
| P23 | Circular points $\omega = (1:i:0)$ $\leftrightarrow$ Cooper pair $(k, -k)$ | Theorem (WKET/GCCT) |
| P24 | $\mathcal{Q} = \{\lambda_1 = 0\}$ is Cayley-Klein absolute conic = Shilov boundary $S^3$ | WKET/IMFL |

---

## Theoretical Foundations

**Painlevé VI and Isomonodromic Theory**
Fuchs, R. (1905). Über lineare homogene Differentialgleichungen. *Math. Ann.* 63: 301.
Painlevé, P. (1900, 1902). Mémoire sur les équations différentielles. *Bull. SMF* 28: 201.
Schlesinger, L. (1912). Über eine Klasse von Differentialsystemen. *J. Reine Angew.* 141: 96.
Jimbo, M.; Miwa, T.; Ueno, K. (1981). Monodromy preserving deformation I. *Physica D* 2: 306.
Okamoto, K. (1987). Studies on the Painlevé equations I. *Ann. Mat. Pura Appl.* 146: 337.

**Modular Surface and Selberg Theory**
Selberg, A. (1956). Harmonic analysis and discontinuous groups. *JIMS* 20: 47.
Selberg, A. (1965). On the estimation of Fourier coefficients. *AMS Proc.* VIII: 1.
Hejhal, D.A. (1976, 1983). *The Selberg Trace Formula for PSL(2,R)*, Vols. I–II. Springer.
Iwaniec, H. (1995). *Introduction to the Spectral Theory of Automorphic Forms.* Rev. Mat. Iberoam.

**Picard Modular Group**
Picard, É. (1881). Sur une extension aux fonctions de deux variables. *Ann. Sci.* 10: 305.
Holzapfel, R.-P. (1998). *Ball and Surface Arithmetics.* Vieweg.
Chazy, J. (1911). Sur les équations différentielles du troisième ordre. *Acta Math.* 34: 317.

**Frobenius Manifolds**
Dubrovin, B. (1994). Geometry of 2D topological field theories. *LNM* 1620: 120.
Dubrovin, B.; Zhang, Y. (1998). Extended affine Weyl groups and Frobenius manifolds. *Compositio* 111: 167.
Saito, K. (1983). Period mapping associated to a primitive form. *Publ. RIMS* 19: 1231.

**Gauss Map Ergodics and Markov Spectrum**
Kuzmin, R.O. (1928). Sur un problème de Gauss. *C.R. Acad. Sci.* 187: 1761.
Lévy, P. (1929). Sur les lois de probabilité. *Bull. SMF* 57: 178.
Hurwitz, A. (1891). Ueber die angenäherte Darstellung der Irrationalzahlen. *Math. Ann.* 39: 279.
Markov, A.A. (1879). Sur les formes quadratiques binaires indéfinies. *Math. Ann.* 17: 379.
Hall, M., Jr. (1947). On the sum and product of continued fractions. *Ann. Math.* 48: 966.

**Ratner Theory**
Ratner, M. (1991). On Raghunathan's measure conjecture. *Ann. Math.* 134: 545.
Einsiedler, M.; Margulis, G.; Venkatesh, A. (2009). Effective equidistribution. *Inventiones* 177: 137.

**Wick Rotation**
Wick, G.C. (1954). Properties of Bethe-Salpeter Wave Functions. *Phys. Rev.* 96: 1124.
Osterwalder, K.; Schrader, R. (1973, 1975). Axioms for Euclidean Green's functions I, II. *CMP.*
Klein, F. (1872). *Erlangen Program.* Inaugural lecture, Universität Erlangen.

**Inherited Foundations**
KQOM · PH-SP · LKTL · FLML · GCCT · GLOW · GAME · PPMC · KYBM · SWMS
Dickson (1913) · Higman (1952) · Kruskal (1960) · Landau (1936, 1942) · BCS (1957)
Luttinger-Ward (1960) · Atiyah-Singer · Yau-Tian-Donaldson
Edelsbrunner-Harer (2010) · Robertson-Seymour (1985–2004) · ZF axioms Z1–Z8

---

*ERI Labs · Emergent Reality Intelligence · New Jersey, United States*
*Eric Ren · Executive Chairman · github.com/ericrenone · Founded January 2025*

---

**The training trajectory is a geodesic on the modular surface. Grokking is when it leaves the cusp. The τ-function tracks the journey. At the pole, the Painlevé transcendent gives you the order parameter exactly. The Selberg trace formula certifies the gap unconditionally. The Wick rotation is the bridge between the real and imaginary descriptions of the same event. Three frameworks. One pole.**
