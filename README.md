# Spin-Informed EGNN

The intersection of machine learning and quantum physics has opened new frontiers in the study of
complex many-body systems. In recent years, Graph Neural Networks (GNNs) have emerged as a
powerful tool for modeling physical systems, owing to their natural ability to represent relational data.
Indeed atoms, molecules and spin lattices all lend themselves perfectly to a graph-based description.
A particularly compelling extension of this framework is the class of Equivariant Graph Neural
Networks (EGNNs), which incorporate the symmetries of three-dimensional Euclidean space
directly into the network architecture, ensuring that predictions remain consistent under rotations,
reflections and translations of the input.

Despite their success in classical atomistic simulations and molecular property prediction, standard
EGNNs were not designed to account for the quantum state of the particles they represent. In quantum
many-body systems, the physical properties of a node depend not only on its position and classical
attributes, but also on the full quantum mechanical state it occupies, information that is typically
discarded in classical graph representations.

In this work, we address this limitation by introducing Spin-Informed Equivariant Graph Neural
Networks (SI-EGNNs), an architecture that augments traditional EGNNs with an encoding of
the initial quantum state. Each node in the graph is endowed with a representation of its spin
state, parameterized via the Bloch vector, allowing the network to incorporate quantum mechanical
information while preserving the equivariance properties essential for physical consistency.

To validate this approach on a concrete and practically relevant problem, we apply SI-EGNNs to the
prediction of the coherence time T2 of Nitrogen-Vacancy (NV) centers in diamond. NV centers are
point defects in the diamond lattice that have attracted significant attention as solid-state quantum bits
(qubits), due to their long coherence times at room temperature, optical addressability, and potential
for quantum sensing and quantum information processing. The decoherence of an NV center
spin is primarily driven by the surrounding bath of 13C nuclear spins and substitutional nitrogen
(P1) defects, making T2 a quantity that depends sensitively on both the spatial configuration and the
quantum state of the spin environment: precisely the setting our architecture is designed to handle.
