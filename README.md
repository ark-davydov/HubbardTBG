# HubardTBG


This repositry contains the four-band and twelve-band Hubbard
models for twisted bilayer graphene at the magic angle 1.05 degree.

The tight-binding part of the model is writtein into *_tb.dat  files with Wannier90 format for such files, described in page 92, section 8.1 of the user_guide_Wannier90.pdf

The Hubabrd parameters U_ij (R) are writtein into UR*.dat files with the following format:
 -first line in the file gives the number of lattice vectors nR, follwed by the number of orbitals nb
  next data is split into nR blocks, at each block:
 -the first line gives the lattice coordinates of lattice vector R
 -followed by nb x nb lines:
        i,j, real(U_ij),imag(U_ij) at this R
 -block is terminated by an empty line

Finally, orbital centers right after the wannierization are writtein into wannier*_centres.xyz file, in which cartesian coordinates after 'X' are the actaual final orbital coordinates, and coordinates after 'Xx' are initial ones (should be ignored).

These however are not exactly in the symmetric Wyckoff positions due to the large size of orbitals and other numberical reasons. Therefore, we also write coordinates adjusted to Wyckoff postions into wannier*_centres_adjusted.xyz, where both lattice and cartesian components are written, and z-component ignored, as we deal with 2D model.

