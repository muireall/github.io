+++
title = "Wave mechanics in periodic media"
date = 2022-01-01
description = "Comparisons between solid-state crystals and photonic crystals, from Photonic Crystals: Molding the Flow of Light"
+++
<!-- pedagogy, analogy, what's weird about quantum mechanics, steven g johnson -->
[Photonic Crystals: Molding the Flow of Light](http://ab-initio.mit.edu/book/) is one of my favorite undergraduate-level textbooks. (PDF freely available.)

Below I reproduce its appendix tabulating the comparisons between quantum mechanics and electromagnetism that the authors make throughout the book. If you're familiar with one but not the other, you might find it interesting. If you want something more technical, try ["Notes on the algebraic structure of wave equations"](https://math.mit.edu/~stevenj/18.369/wave-equations.pdf) from Steven G. Johnson (one of the textbook authors, as it happens, though [better known for other work](https://en.wikipedia.org/wiki/Steven_G._Johnson)). Otherwise, it's relevant to a few subjects where I like to collect concrete, real-world cases for study—pedagogy, extended analogy, what is or isn't weird about quantum mechanics.

(I also wanted to experiment with typesetting for my new site here.)

<!-- more -->

___

### Appendix A

#### Comparisons with Quantum Mechanics

<span style="font-variant:small-caps;">Throughout the text</span>, especially in chapters 2 and 3, we make several comparisons between our formalism and the equations of quantum mechanics and solid-state physics. In this appendix, we present an extensive listing of these comparisons. It will hopefully serve as both a brief summary of the phenomena surrounding photonic crystals, and a way to relate them to (perhaps) familiar concepts in other fields.

The heart of the subject of photonic crystals is the propagation of electromagnetic waves in a periodic dielectric medium. In a sense, quantum mechanics is also the study of wave propagation, although the waves are a bit more abstract. At the atomic scale, particles (like the electron) begin to display wavelike properties, including interference and nonlocalization. The function that contains the information about the particle obeys the Schrödinger equation, which bears some resemblance to a familiar wave equation.

It therefore comes as no surprise that the study of quantum mechanics in a periodic potential contains direct parallels to our study of electromagnetism in a periodic dielectric. Since the quantum mechanics of periodic potentials is the basic theory of solid-state physics, the field of photonic crystals can also inherit some of the theorems and terminology of solid-state physics, in slightly modified form. Table 1 lists some of these correspondences.

 <table class="propTable">
  <tr>
    <th>Table 1</th>
    <th>Quantum mechanics in a periodic potential (crystal)</th>
    <th>Electromagnetism in a periodic dielectric (photonic crystal)</th>
  </tr>
  <tr>
    <td>What is the "key function" that contains all of the information?</td>
    <td>The scalar wave function, {% katex() %} \Psi(\mathbf{r},t). {% end %}</td>
    <td>The magnetic vector field {% katex() %} \mathbf{H}(\mathbf{r}, t). {% end %}</td>
  </tr>
  <tr>
    <td>How do we separate the time dependence of the function from the spatial dependence?</td>
    <td>Expand in a set of energy eigenstates: {% katex(block="true") %} \Psi(\mathbf{r},t)= \Sigma_E c_E \Psi_E(\mathbf{r})e^{-iEt/\hbar}. {% end %}</td>
    <td>Expand in a set of harmonic modes (frequency eigenstates): {% katex(block="true") %}  \mathbf{H}(\mathbf{r},t) = \Sigma_\omega c_\omega \mathbf{H}_\omega(\mathbf{r})e^{-i\omega t}.{% end %}</td>
  </tr>
  <tr>
    <td>What is the "master equation" that determines the eigenstates of the system?</td>
    <td>The Schrödinger equation: {% katex(block=true) %} \begin{aligned}\left[ -\frac{\hbar}{2m} \nabla^2 + V(\mathbf{r})\right] &\Psi_E(\mathbf{r}) =\\ E &\Psi_E(\mathbf{r}).\end{aligned} {% end %}</td>
    <td>The Maxwell equations: {% katex(block=true) %}\begin{aligned} \nabla~\times~\frac{1}{\varepsilon(\mathbf{r})} \nabla \times &\mathbf{H}_\omega(\mathbf{r}) = \\ \frac{\omega^2}{c^2} &\mathbf{H}_\omega(\mathbf{r}). \end{aligned}{% end %}</td>
  </tr>
  <tr>
    <td>Are there any other conditions on the key function?</td>
    <td>Yes, the scalar field must be normalizable.</td>
    <td>Yes, the vector field must be both normalizable and transverse: {% katex() %} \nabla~\cdot~\mathbf{H} = 0 .{% end %}</td>
  </tr>
  <tr>
    <td>Where does the periodicity of the system enter?</td>
    <td>The potential: {% katex() %}\\ V(\mathbf{r}) = V(\mathbf{r}~+~\mathbf{R}), \\\textrm{for all }\textrm{lattice vectors } \mathbf{R}. {% end %}</td>
    <td>The dielectric function: {% katex() %} \\\varepsilon(\mathbf{r}) = \varepsilon(\mathbf{r}~+~\mathbf{R}),\\ \textrm{for all lattice vectors } \mathbf{R}. {% end %}</td>
  </tr>
  <tr>
    <td>Is there any interaction between normal modes?</td>
    <td>Yes, there is an electron-electron repulsive interaction that makes large-scale computation difficult.</td>
    <td>In the linear regime, electromagnetic modes do not interact, and can be calculated independently.</td>
  </tr>
  <tr>
    <td>What important properties do the normal modes have in common?</td>
    <td>Eigenstates with different energies are orthogonal, have real eigenvalues, and can be found through a variational principle.</td>
    <td>Modes with different frequencies are orthogonal, have <em>nonnegative</em> real eigenvalues, and can be found through a variational principle.</td>
  </tr>
  <tr>
    <td>What are the properties of the master equation that guarantee these properties of normal modes?</td>
    <td>The Hamiltonian, {% katex() %} \hat{H}\textrm{,} {% end %} is a linear Hermitian operator.</td>
    <td>The Maxwell operator, {% katex() %} \hat{\Theta}\textrm{,} {% end %} is a linear positive-semidefinite Hermitian operator.</td>
  </tr>
  <tr>
    <td>What is the variational theorem that is used to determine the normal modes and frequencies?</td>
    <td>{% katex() %} E_\mathrm{var} = \frac{(\Psi, \hat{H}, \Psi)}{(\Psi, \Psi)} \textrm{ is minimized}\\ \textrm{when }\Psi\textrm{ is an eigenstate of }\hat{H}.{% end %}</td>
    <td>{% katex() %} U_\mathrm{var} = \frac{(\mathbf{H}, \hat{\Theta}, \mathbf{H})}{(\mathbf{H}, \mathbf{H})} \textrm{ is minimized}\\\textrm{when }\mathbf{H}\textrm{ is an eigenstate of }\hat{\Theta}. {% end %}</td>
  </tr>
  <tr>
    <td>What is the heuristic that goes along with the variational theorem?</td>
    <td>The wave function concentrates in potential wells, without oscillating too fast, while remaining orthogonal to lower-energy states.</td>
    <td>The electromagnetic fields concentrate their energy in high-ɛ regions, without oscillating too fast, while remaining orthogonal to lower-frequency modes.</td>
  </tr>
  <tr>
    <td>What is the physical energy of the system?</td>
    <td>The eigenvalue {% katex() %} E {% end %} of the Hamiltonian.</td>
    <td>The time-average electromagnetic energy: 
    {% katex(block="true") %} U = \frac{1}{4} \int\!\!\!\mathrm{d}^3\!\mathbf{r}\; ɛ|\mathbf{E}|^2 + \mu_0 |\mathbf{H}|^2. {% end %}</td>
  </tr>
  <tr>
    <td>Is there a natural length scale to the system?</td>
    <td>Usually. Physical constants such as the Bohr radius set the length scale.</td>
    <td>No. Solutions are generally scale-free.</td>
  </tr>
  <tr>
    <td>What is the mathematical statement that says "{% katex() %} \hat{A} {% end %} is a symmetry of the system"?</td>
    <td>{% katex() %} \hat{A} {% end %} commutes with the Hamiltonian: {% katex() %} [\hat{A}, \hat{H}] = 0. {% end %}</td>
    <td>{% katex() %} \hat{A} {% end %} commutes with the Maxwell operator: {% katex() %} [\hat{A}, \hat{\Theta}] = 0. {% end %}</p></td>
  </tr>
  <tr>
    <td>How do we use the symmetries of a system to classify the eigenstates?</td>
    <td colspan="2" style="text-align:center">Distinguish them by how they transform under a  symmetry operation {% katex() %} \hat A. {% end %}</td>
  </tr>
  <tr>
    <td>If a system has discrete translational symmetry (as a crystal does), then how can the modes be classified?</td>
    <td>By wave vector {% katex() %} \mathbf{k}. {% end %} Write the wave function in Bloch form: {% katex() %} \Psi_\mathbf{k}(\mathbf{r}) = u_\mathbf{k}e^{i\mathbf{k}\cdot\mathbf{r}}. {% end %}</td>
    <td>By wave vector {% katex() %} \mathbf{k}. {% end %} Write the harmonic modes in Bloch form: {% katex() %} \mathbf{H}_\mathbf{k}(\mathbf{r}) = u_\mathbf{k}e^{i\mathbf{k}\cdot\mathbf{r}}. {% end %}</td>
  </tr>
  <tr>
    <td>What are the nonredundant values for the wave vector {% katex() %} \mathbf{k}\textrm{?}{% end %}</td>
    <td colspan="2" style="text-align:center">They lie in the irreducible Brillouin zone in reciprocal space.</td>
  </tr>
  <tr>
    <td>What do we mean by the term "band structure"?</td>
    <td>The functions {% katex() %} E_n(\mathbf{k}), {% end %} a set of continuous functions that specify the energies of the eigenstates.</td>
    <td>The functions {% katex() %} \omega_n(\mathbf{k}), {% end %} a set of continuous functions that specify the frequencies of the harmonic modes.</td>
  </tr>
  <tr>
    <td>What is the physical origin<sup class="sidenote-widget"><a href="#note1"">a
  </a>
</sup> of the band structure?</td>
    <td>The electron wave scatters coherently from the different potential regions.<sup class="sidenote-widget"><a href="#note1"">a</td>
    <td>The electromagnetic fields scatter coherently at the interfaces between different dielectric regions.{% note() %} Maybe rather the origin "from a causal perspective"? {% end %} </td>
  </tr>
  <tr>
    <td>What property characterizes a "gap" in the band structure?</td>
    <td>Within that range of energies, there are no propagating electron states, regardless of wave vector.</td>
    <td>Within that range of frequencies, there are no propagating electromagnetic modes, regardless of wave vector or polarization.{% note() %} Gaps only for specific polarizations or propagation directions are still interesting, so sometimes you hear the special name "complete band gap" for this case. {% end %}</td>
  </tr>
  <tr>
    <td>What are the terms for the bands that are immediately above and below a gap?</td>
    <td>The band above the gap is the <em>conduction band</em>. The band below the gap is the <em>valence band</em>.</td>
    <td>The band above the gap is the <em>air band</em>. The band below the gap is the <em>dielectric band</em>.</td>
  </tr>
  <tr>
    <td>How are defects introduced into the system?</td>
    <td>By adding foreign atoms to the crystal, thereby breaking the translational symmetry of the atomic potential.</td>
    <td>By changing the dielectric constant at particular locations, thereby breaking the translational symmetry of the dielectric function.</td>
  </tr>
  <tr>
    <td>What is a possible result of introducing a defect?</td>
    <td>It may create an allowed state within a band gap, thereby permitting a localized <em>electron state</em> to exist in the vicinity of the defect.</td>
    <td>It may create an allowed state within a band gap, thereby permitting a localized <em>electromagnetic mode</em> to exist in the vicinity of the defect.</td>
  </tr>
  <tr>
    <td>How do we classify different types of defects?</td>
    <td><em>Donor atoms</em> pull states from the conduction band down into the gap.
        <em>Acceptor atoms</em> push states from the valence band up into the gap.
</td>
    <td><em>Dielectric defects</em> pull states from the air band down into the gap.
    <em>Air defects</em> push states from the dielectric band up into the gap.</td>
  </tr>
  <tr>
    <td>In short, why is studying the physics of the system important?</td>
    <td>We can tailor the <em>electronic</em> properties of materials to our needs. </td>
    <td>We can tailor the <em>optical</em> properties of materials to our needs.</td>
  </tr>
</table> 