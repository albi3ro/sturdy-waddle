+++
title = "The Berry Phase"
weight = 1
+++


The first person, Berry, to create a connection in condensed matter physics did so purely from a physics standpoint.  Only from discussions with Berry did Barry Simon make the jump from the physics formulas to the mathematical notions of parallel transport on a fiber bundle.

Here I replicate Berry's derivation.

Let's start with Schrodiner's equation, where the Hamiltonian depends on a set of parameters $\mathbf{R}(t)$ that we can manipulate in time.
$$
  H(\mathbf{R}(t))|\Psi(t)\rangle = i \hbar \frac{d}{dt} |\Psi(t) \rangle
$$

Next, we use the adiabatic theorem and assume that the parameters $\mathbf{R}(t)$ change slowly enough that we are always in an instantaneous eigenstate.  This holds as long as the frequency with which the Hamiltonian changes is much less than the energy between eigenstates.

Once we apply this approximation, we can break the rate of change for an eigenstate into the standard phase evolution and a slower evolution due to the evolution of the parameters.  All the while, this still is an eigenstate.
$$
  E\_n(\mathbf{R}(t)) | n(\mathbf{R}(t)) \rangle
  =
  \hbar \left( \frac{d}{dt} \theta (t) \right) | n(\mathbf{R}(t)) \rangle
  +i \hbar \frac{d}{dt} |n(\mathbf{R}(t)) \rangle
$$
We multiply by corresponding bra to get this formula in a more convenient form,
$$
  E\_n(\mathbf{R}(t))=  \hbar \left( \frac{d}{dt}\theta(t) \right)  + i \hbar \langle n(\mathbf{R}(t)) | \frac{d}{dt} | n(\mathbf{R}(t)) \rangle
$$
And now integrate the phase over time.
$$
  \theta(t)=
  \frac{1}{\hbar} \int\_{0}^{t}E (\mathbf{R}(t^{\prime}))dt^{\prime}-  i \int\_{0}^{t} \langle n(\mathbf{R}(t^{\prime})) | \frac{d}{d t^{\prime}} | n(\mathbf{R}(t^{\prime})) \rangle dt^{\prime}
$$
The first integral is the same time evolution phase we see all the time, but the second term, we can do something with that. Let's rewrite,
$$
  \gamma
  =i \int\_{0}^{t\_{end}} \langle n(\mathbf{R}(t^{\prime})) | \nabla\_{\mathbf{R}}  | n(\mathbf{R}(t^{\prime})) \rangle \cdot \frac{d \mathbf{R}}{d t^{\prime}} dt^{\prime}
  $$
  $$
  =i \int\_{C} \langle n(\mathbf{R}) | \nabla\_{\mathbf{R}} | n(\mathbf{R}) \rangle \cdot d \mathbf{R}
$$
From that equation we can extract
$$
  A^{R^i} = \langle n(\mathbf{R}) | \nabla\_{\mathbf{R}}  | n(\mathbf{R}) \rangle 
  \qquad \qquad \gamma= i \int_C A^{R^i} \cdot dR^i
$$
