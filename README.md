 <h1 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398145-00822b00-dcc9-11eb-9519-6b724eb81b52.png">
  <br />
  Linear Algebra Guide
</h1>

#### The purpose of this guide is to give you an introduction to the mathematical operations that we can perform on vectors and matrices and to give you a feel of the power of linear algebra. A lot of complex problems in science, business, and technology can be described in terms of vectors and matrices so it's important that people understand how it all works.

**Note: You can easily convert this markdown file to a PDF in [VSCode](https://code.visualstudio.com/) using this handy extension [Markdown PDF](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf).**

# Table of Contents

1. [Linear Algebra Learning Resources](https://github.com/mikeroyal/Linear-Algebra-Guide#Linear-Algebra-Learning-Resources)

2. [Defintions](https://github.com/mikeroyal/Linear-Algebra-Guide#Defintions)

    - [i. Vector operations](https://github.com/mikeroyal/Linear-Algebra-Guide#vector-operations)
    - [ii. Matrix operations](https://github.com/mikeroyal/Linear-Algebra-Guide#matrix-operations)
    - [iii. Matrix-vector product](https://github.com/mikeroyal/Linear-Algebra-Guide#matrix-vector-product)
    - [iv. Linear transformations](https://github.com/mikeroyal/Linear-Algebra-Guide#linear-transformations)
    - [ v. Fundamental vector spaces](https://github.com/mikeroyal/Linear-Algebra-Guide#)

3. [Computational Linear Algebra](https://github.com/mikeroyal/Linear-Algebra-Guide#Computational-Linear-Algebra)

    - [i. Solving systems of equations](https://github.com/mikeroyal/Linear-Algebra-Guide#solving-systems-of-equations)
    - [ii. Systems of equations as matrix equations](https://github.com/mikeroyal/Linear-Algebra-Guide#systems-of-equations-as-matrix-equations)

4. [Computing the Inverse of a Matrix](https://github.com/mikeroyal/Linear-Algebra-Guide#Computing-the-Inverse-of-a-Matrix)

    - [i. Using row operations](https://github.com/mikeroyal/Linear-Algebra-Guide#using-row-operations)
    - [ii. Using elementary matrices](https://github.com/mikeroyal/Linear-Algebra-Guide#using-elementary-matrices)
    - [iii. Transpose of a Matrix](https://github.com/mikeroyal/Linear-Algebra-Guide#transpose-of-a-matrix)

5. [Other Linear Topics](https://github.com/mikeroyal/Linear-Algebra-Guide#Other-Linear-Topics)

    - [i. Basis](https://github.com/mikeroyal/Linear-Algebra-Guide#basis)
    - [ii. Matrix representations of linear transformations](https://github.com/mikeroyal/Linear-Algebra-Guide#matrix-representations-of-linear-transformations)
    - [iii. Dimension and Basis for Vector Spaces](https://github.com/mikeroyal/Linear-Algebra-Guide#dimension-and-basis-for-vector-spaces)
    - [iv. Row space, columns space, and rank of a matrix](https://github.com/mikeroyal/Linear-Algebra-Guide#row-space-columns-space-and-rank-of-a-matrix)
    - [v. Invertible matrix theorem](https://github.com/mikeroyal/Linear-Algebra-Guide#invertible-matrix-theorem)
    - [vi. Determinants](https://github.com/mikeroyal/Linear-Algebra-Guide#determinants)
    - [vii. Eigenvalues and eigenvectors](https://github.com/mikeroyal/Linear-Algebra-Guide#eigenvalues-and-eigenvectors)
    - [viii. Linear Regression](https://github.com/mikeroyal/Linear-Algebra-Guide#linear-regression)

6. [MATLAB](https://github.com/mikeroyal/Linear-Algebra-Guide#MATLAB)

 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398150-037d1b80-dcc9-11eb-81a4-d7ab8aa49041.png">
  <br />
</p>

# Linear Algebra Learning Resources
[Back to the Top](https://github.com/mikeroyal/Linear-Algebra-Guide#table-of-contents)

[Linear algebra](https://en.wikipedia.org/wiki/Linear_algebra) is the math of vectors and matrices. The only prerequisite for this guide is a basic understanding of high school math concepts like numbers, variables, equations, and the fundamental arithmetic operations on real numbers: addition (denoted +), subtraction (denoted −), multiplication (denoted implicitly), and division (fractions). Also, you should also be familiar with functions that take real numbers as inputs and give real numbers as outputs, f : R → R.

[Linear Algebra - Online Courses | Harvard University](https://online-learning.harvard.edu/course/linear-algebra)

[Linear Algebra | MIT Open Learning Library](https://openlearninglibrary.mit.edu/courses/course-v1:OCW+18.06SC+2T2019/about)

[Linear Algebra - Khan Academy](https://www.khanacademy.org/math/linear-algebra)

[Top Linear Algebra Courses on Coursera](https://www.coursera.org/courses?query=linear%20algebra)

[Mathematics for Machine Learning: Linear Algebra on Coursera](https://www.coursera.org/learn/linear-algebra-machine-learning)

[Top Linear Algebra Courses on Udemy](https://www.udemy.com/topic/linear-algebra/)

[Learn Linear Algebra with Online Courses and Classes on edX](https://www.edx.org/learn/linear-algebra)

[The Math of Data Science: Linear Algebra Course on edX](https://www.edx.org/course/math-of-data-science-linear-algebra)

[Linear Algebra Full Course for Beginners to Experts - YouTube](Linear Algebra Full Course for Beginners to Experts - YouTube)

[Linear Algebra in Twenty Five Lectures | UC Davis](https://www.math.ucdavis.edu/~linear/linear.pdf)

[Linear Algebra | UC San Diego Extension](https://extension.ucsd.edu/courses-and-programs/linear-algebra-1)

[Linear Algebra for Machine Learning | UC San Diego Extension](https://extension.ucsd.edu/courses-and-programs/linear-algebra-for-machine-learning)

[Introduction to Linear Algebra, Interactive Online Video | Wolfram](http://www.wolfram.com/wolfram-u/introduction-to-linear-algebra/)

[Linear Algebra Resources | Dartmouth](https://math.dartmouth.edu/~trs/linear-algebra-resources.php)

#  Defintions
[Back to the Top](https://github.com/mikeroyal/Linear-Algebra-Guide#table-of-contents)

### i. Vector operations

We now define the math operations for vectors. The operations we can perform on vectors ~u = (u1, u2, u3) and ~v = (v1, v2, v3) are: addition, subtraction, scaling, norm (length), dot product, and cross product:

The dot product and the cross product of two vectors can also be described in terms of the angle θ between the two vectors. The formula for the dot
product of the vectors is ~u · ~v = k~ukk~vk cos θ. We say two vectors ~u and ~v are orthogonal if the angle between them is 90◦. The dot product of orthogonal vectors is zero: ~u · ~v = k~ukk~vk cos(90◦) = 0. The norm of the cross product is given by k~u×~vk = k~ukk~vk sin θ. The cross product is not commutative: ~u ×~v 6= ~v × ~u, in fact ~u ×~v = −~v × ~u.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398163-26a7cb00-dcc9-11eb-9b70-3452d50762c5.png">
  <br />
</p>

**Vector Operations. Source: [slideserve](https://www.slideserve.com/krystal/streaming-simd-extension-sse)**

<p align="center">
 <img src="(https://user-images.githubusercontent.com/45159366/124398165-28718e80-dcc9-11eb-9fab-258fc4b6ab96.png">
  <br />
</p>

**Vector Operations. Source: [pinterest](https://www.pinterest.com/pin/41799102767414798/)**

### ii. Matrix operations

We denote by A the matrix as a whole and refer to its entries as aij .The mathematical operations defined for matrices are the following:

• determinant (denoted det(A) or |A|)
Note that the matrix product is not a commutative operation: AB 6= BA.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398167-2ad3e880-dcc9-11eb-9455-9b0c3c6171cd.png">
  <br />
</p>

**Matrix Operations. Source: [SDSU Physics](https://sdsu-physics.org/math/pages/435_LA_ch2.html)**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398169-2c051580-dcc9-11eb-934a-71c691325062.png">
  <br />
</p>

**Check for modules that allow Matrix Operations. Source: [DPS Concepts](https://dspconcepts.com/forums/audio-weaver-designer/347-check-modules-allow-matrix-operations)**

### iii. Matrix-vector product

The matrix-vector product is an important special case of the matrixmatrix product.

There are two fundamentally different yet equivalent ways to interpret the matrix-vector product. In the column picture, (C), the multiplication of the
matrix A by the vector ~x produces a linear combination of the columns of the matrix: ~y = A~x = x1A[:,1] + x2A[:,2], where A[:,1] and A[:,2] are the first and second columns of the matrix A. In the row picture, (R), multiplication of the matrix A by the vector ~x produces a column vector with coefficients equal to the dot products of rows of the matrix with the vector ~x.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398176-36bfaa80-dcc9-11eb-82c9-641f9ddd8563.png">
  <br />
</p>

**Matrix-vector product. Source: [wikimedia](https://commons.wikimedia.org/wiki/File:Matrix_vector_product_qtl1.svg)**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398178-38896e00-dcc9-11eb-94c4-2b2fa7499989.png">
  <br />
</p>

**Matrix-vector Product. Source: [mathisfun](https://www.mathsisfun.com/algebra/scalar-vector-matrix.html)**

### iv. Linear transformations

The matrix-vector product is used to define the notion of a linear transformation, which is one of the key notions in the study of linear algebra. Multiplication by a matrix A ∈ R m×n can be thought of as computing a linear transformation TA that takes n-vectors as inputs and produces m-vectors as outputs:

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398182-3fb07c00-dcc9-11eb-815a-d31e591fe218.png">
  <br />
</p>

**Linear Transformations. Source:[slideserve](https://www.slideserve.com/hall-cobb/chap-6-linear-transformations)**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398184-40e1a900-dcc9-11eb-90e9-36031124610f.png">
  <br />
</p>

**Elementary matrices for linear transformations in R^2. Source:[](https://www.quora.com/What-is-a-linear-transformation)**

### v. Fundamental vector spaces

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398197-4fc85b80-dcc9-11eb-9abc-3741bda9b63e.png">
  <br />
</p>

**Fundamental theorem of linear algebra for Vector Spaces. Source: [wikimedia](https://en.wikipedia.org/wiki/Fundamental_theorem_of_linear_algebra)**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398199-50f98880-dcc9-11eb-8fd0-994dc48f62d6.png">
  <br />
</p>

**Fundamental theorem of linear algebra. Source: [wolfram](https://mathworld.wolfram.com/FundamentalTheoremofLinearAlgebra.html)**

# Computational Linear Algebra
[Back to the Top](https://github.com/mikeroyal/Linear-Algebra-Guide#table-of-contents)

### i. Solving systems of equations

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398355-307dfe00-dcca-11eb-8668-ba037de5aca5.png">
  <br />
</p>

**System of Linear Equations by Graphing. Source: [slideshare](https://www.slideshare.net/JITENDRATHAKOR/systems-of-linear-equations-43550732)**

### ii. Systems of equations as matrix equations

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398360-34118500-dcca-11eb-94eb-81ee66a9dc8a.png">
  <br />
</p>

**Systems of equations as matrix equations. Source: [mathisfun](https://www.mathsisfun.com/algebra/systems-linear-equations-matrices.html?ref=binfind.com%2Fweb)**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398358-3247c180-dcca-11eb-967c-992764686a0d.png">
  <br />
</p>

**Matrix Equations and Systems of Linear Equations. Source: [ppt-online](https://ppt-online.org/241576)**


# Computing the Inverse of a Matrix
[Back to the Top](https://github.com/mikeroyal/Linear-Algebra-Guide#table-of-contents)

In this section we’ll look at several different approaches for computing the inverse of a matrix. The matrix inverse is unique so no matter which
method we use to find the inverse, we’ll always obtain the same answer.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398409-71761280-dcca-11eb-9add-d105af886569.png">
  <br />
</p>

**Inverse of 2x2 Matrix. Source: [pinterest](https://www.pinterest.com/pin/375276581446966518/)**

### i. Using row operations

One approach for computing the inverse is to use the Gauss–Jordan elimination procedure.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398532-0c6eec80-dccb-11eb-9c82-6a65916fa43a.png">
  <br />
</p>

**Elementray row operations. Source: [YouTube](http://www.youtube.com/watch?v=DH2JSYx52nk)**

### ii. Using elementary matrices

Every row operation we perform on a matrix is equivalent to a leftmultiplication by an elementary matrix.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398426-83f04c00-dcca-11eb-8dde-54deedff30f7.png">
  <br />
</p>

**Elementary Matrices. Source: [SDSU Physics](http://sdsu-physics.org/math/pages/435_LA_ch2.html)**

### iii. Transpose of a Matrix

Finding the inverse of a matrix is to use the Transpose method.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398574-34f6e680-dccb-11eb-8112-ca77aad96004.png">
  <br />
</p>

**Transpose of a Matrix. Source:[slideserve](https://www.slideserve.com/jaimin/matrix-inverse-and-transpose)**

# Other Linear Topics
[Back to the Top](https://github.com/mikeroyal/Linear-Algebra-Guide#table-of-contents)

In this section discuss a number of other important topics of linear algebra.

### i. Basis

Intuitively, a basis is any set of vectors that can be used as a coordinate system for a vector space. You are certainly familiar with the standard basis for the xy-plane that is made up of two orthogonal axes: the x-axis and the y-axis.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398635-a040b880-dccb-11eb-8d5f-0e6ec65b742d.png">
  <br />
</p>

**Basis. Source: [wikimedia](https://en.wikipedia.org/wiki/Basis_(linear_algebra))**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398636-a171e580-dccb-11eb-8a40-8e6a9e24b6af.png">
  <br />
</p>

**Change of Basis. Source: [wikimedia](https://en.wikipedia.org/wiki/Change_of_basis)**

### ii. Matrix representations of linear transformations

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398653-b9e20000-dccb-11eb-8985-1d203f52f131.png">
  <br />
</p>

**Matrix representations of linear transformations. Source:[slideserve](https://www.slideserve.com/sylvie/two-dimensional-geometric-transformations)**

### iii. Dimension and Basis for Vector Spaces

The dimension of a vector space is defined as the number of vectors in a basis for that vector space. Consider the following vector space S = span{(1, 0, 0),(0, 1, 0),(1, 1, 0)}. Seeing that the space is described by three vectors, we might think that S is 3-dimensional. This is not the case, however, since the three vectors are not linearly independent so they don’t form a basis for S. Two vectors are sufficient to describe any vector in S; we can write S = span{(1, 0, 0),(0, 1, 0)}, and we see these two vectors are linearly independent so they form a basis and dim(S) = 2. There is a general procedure for finding a basis for a vector space. Suppose you are given a description of a vector space in terms of m vectors V = span{~v1, ~v2, . . . , ~vm} and you are asked to find a basis for V and the dimension of V. To find a basis for V, you must find a set of linearly independent vectors that span V. We can use the Gauss–Jordan elimination procedure to accomplish this task. Write the vectors ~vi as the rows of a matrix M. The vector space V corresponds to the row space of the matrix M. Next, use row operations to find the reduced row echelon form (RREF) of the matrix M. Since row operations do not change the row space of the matrix, the row space of reduced row echelon form of the matrix M is the same as the row space of the original set of vectors. The nonzero rows in the RREF of the matrix form a basis for vector space V and the numbers of nonzero rows is the dimension of V.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398664-c5352b80-dccb-11eb-866e-61808bcf953d.png">
  <br />
</p>

**Basis and Dimension. Source: [sliderserve](https://www.slideserve.com/kalil/chapter-3-vector-space)**

### iv. Row space, columns space, and rank of a matrix

Recall the fundamental vector spaces for matrices that we defined in Section II-E: the column space C(A), the null space N (A), and the row space R(A). A standard linear algebra exam question is to give you a certain matrix A and ask you to find the dimension and a basis for each of its fundamental spaces. In the previous section we described a procedure based on Gauss–Jordan elimination which can be used “distill” a set of linearly independent vectors which form a basis for the row space R(A). We will now illustrate this procedure with an example, and also show how to use the RREF of the matrix A to find bases for C(A) and N (A).

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398677-d67e3800-dccb-11eb-8052-dfd1b01920fd.png">
  <br />
</p>

**Row space and Column space. Source: [slideshare](https://www.slideshare.net/VishveshJasani/row-space-column-space-null-space-rank-nullity)**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398679-d8e09200-dccb-11eb-8707-e340933063d4.png">
  <br />
</p>

**Row space and Column space. Source:[slideshare](http://www.slideshare.net/RonakMachhi/null-space-rank-and-nullity-theorem)**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398681-d9792880-dccb-11eb-8c6f-0c483cf860a4.png">
  <br />
</p>

**Rank and Nullity. Source: [slideshare](https://www.slideshare.net/VishveshJasani/row-space-column-space-null-space-rank-nullity)**

### v. Invertible matrix theorem

There is an important distinction between matrices that are invertible and those that are not as formalized by the following theorem. Theorem. For an n×n matrix A, the following statements are equivalent:

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398692-e6961780-dccb-11eb-98d9-dae7199a6365.png">
  <br />
</p>

**Invertible Matrix theorem. Source: [SDSU Physics](https://sdsu-physics.org/math/pages/435_LA_ch2.html)**

### vi. Determinants

The determinant of a matrix, denoted det(A) or |A|, is a special way to combine the entries of a matrix that serves to check if a matrix is invertible or not.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398703-f9105100-dccb-11eb-8d4e-e6db343304ec.png">
  <br />
</p>

**Determinant of a Square Matrix. Source:[stackexchange](https://math.stackexchange.com/questions/1354148/proving-the-formula-for-finding-the-determinant-of-a-square-matrix)**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398705-fa417e00-dccb-11eb-8d1f-0cbf01d77f3d.png">
  <br />
</p>

**Determinant of matrix. Source: [onlinemathlearning](https://www.onlinemathlearning.com/matrix-determinants.html)**

### vii. Eigenvalues and eigenvectors

The set of eigenvectors of a matrix is a special set of input vectors for which the action of the matrix is described as a simple scaling. When a matrix is multiplied by one of its eigenvectors the output is the same eigenvector multiplied by a constant A~eλ = λ~eλ. The constant λ is called an eigenvalue of A.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398717-03cae600-dccc-11eb-86f2-72a816b9231a.png">
  <br />
</p>

**Generalized EigenVectors. Source: [YouTube](https://www.youtube.com/watch?v=xyhaYHGZN-w)**

### viii. Linear Regression

[Linear regression](https://en.wikipedia.org/wiki/Linear_regression) is an approach to model the relationship between two variables by fitting a linear equation to observed data. One variable is considered to be an explanatory variable, and the other is considered to be a dependent variable.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/124398722-0af1f400-dccc-11eb-9ac7-1de7c6e43ff5.png">
  <br />
</p>

**Multiple Linear Regression. Source: [Medium](https://medium.com/@subarna.lamsal1/multiple-linear-regression-sklearn-and-statsmodels-798750747755)**

# MATLAB
[Back to the Top](https://github.com/mikeroyal/Linear-Algebra-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/94306473-de809e80-ff27-11ea-924b-0a6947ae38bc.png">
  <br />
</p>

## MATLAB Learning Resources

[MATLAB](https://www.mathworks.com/products/matlab.html) is a programming language that does numerical computing such as expressing matrix and array mathematics directly.

[MATLAB Documentation](https://www.mathworks.com/help/matlab/)

[Getting Started with MATLAB ](https://www.mathworks.com/help/matlab/getting-started-with-matlab.html)

[MATLAB and Simulink Training from MATLAB Academy](https://matlabacademy.mathworks.com)

[MathWorks Certification Program](https://www.mathworks.com/services/training/certification.html)

[MATLAB Online Courses from Udemy](https://www.udemy.com/topic/matlab/)

[MATLAB Online Courses from Coursera](https://www.coursera.org/courses?query=matlab)

[MATLAB Online Courses from edX](https://www.edx.org/learn/matlab)

[Building a MATLAB GUI](https://www.mathworks.com/discovery/matlab-gui.html)

[MATLAB Style Guidelines 2.0](https://www.mathworks.com/matlabcentral/fileexchange/46056-matlab-style-guidelines-2-0)

[Setting Up Git Source Control with MATLAB & Simulink](https://www.mathworks.com/help/matlab/matlab_prog/set-up-git-source-control.html)

[Pull, Push and Fetch Files with Git with MATLAB & Simulink](https://www.mathworks.com/help/matlab/matlab_prog/push-and-fetch-with-git.html)

[Create New Repository with MATLAB & Simulink](https://www.mathworks.com/help/matlab/matlab_prog/add-folder-to-source-control.html)

[PRMLT](http://prml.github.io/) is Matlab code for machine learning algorithms in the PRML book.

## MATLAB Tools

[MATLAB Online](https://matlab.mathworks.com) allows to users to uilitize MATLAB and Simulink through a web browser such as Google Chrome.

[Simulink](https://www.mathworks.com/products/simulink.html) is a block diagram environment for Model-Based Design. It supports simulation, automatic code generation, and continuous testing of embedded systems.

[MATLAB Schemer](https://github.com/scottclowe/matlab-schemer) is a MATLAB package makes it easy to change the color scheme (theme) of the MATLAB display and GUI.

[LRSLibrary](https://github.com/andrewssobral/lrslibrary) is a Low-Rank and Sparse Tools for Background Modeling and Subtraction in Videos. The library was designed for moving object detection in videos, but it can be also used for other computer vision and machine learning problems.

[Robotics Toolbox for MATLAB](https://www.mathworks.com/products/robotics.html) provides a toolbox that brings robotics specific functionality(designing, simulating, and testing manipulators, mobile robots, and humanoid robots) to MATLAB, exploiting the native capabilities of MATLAB (linear algebra, portability, graphics). The toolbox also supports mobile robots with functions for robot motion models (bicycle), path planning algorithms (bug, distance transform, D*, PRM), kinodynamic planning (lattice, RRT), localization (EKF, particle filter), map building (EKF) and simultaneous localization and mapping (EKF), and a Simulink model a of non-holonomic vehicle. The Toolbox also including a detailed Simulink model for a quadrotor flying robot.

[SEA-MAT](https://sea-mat.github.io/sea-mat/) is a collaborative effort to organize and distribute Matlab tools for the Oceanographic Community.

[Gramm](https://github.com/piermorel/gramm) is a complete data visualization toolbox for Matlab. It provides an easy to use and high-level interface to produce publication-quality plots of complex data with varied statistical visualizations. Gramm is inspired by R's ggplot2 library.

[hctsa](https://hctsa-users.gitbook.io/hctsa-manual) is a software package for running highly comparative time-series analysis using Matlab.

[Plotly](https://plot.ly/matlab/) is a Graphing Library for MATLAB.

[YALMIP](https://yalmip.github.io/) is a MATLAB toolbox for optimization modeling.

[GNU Octave](https://www.gnu.org/software/octave/) is a high-level interpreted language, primarily intended for numerical computations. It provides capabilities for the numerical solution of linear and nonlinear problems, and for performing other numerical experiments. It also provides extensive graphics capabilities for data visualization and manipulation.


## Contribute

- [x] If would you like to contribute to this guide simply make a [Pull Request](https://github.com/mikeroyal/Linear-Algebra-Guide/pulls).


## License
[Back to the Top](https://github.com/mikeroyal/Linear-Algebra-Guide#table-of-contents)

Distributed under the [Creative Commons Attribution 4.0 International (CC BY 4.0) Public License](https://creativecommons.org/licenses/by/4.0/).
