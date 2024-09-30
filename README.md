# Frank M. Bass (1967) model of product growth
Bass model of product growth is based on Everett Rogers' diffusion of innovation theory (for an overview, see Rogers, 1995). The model describes the continuous process of product adoption where the installed base as proportion of potential users, $F(t)$, is a function of the coefficient of innovation, $p$, and coefficient of immitation, $q$, as a differential equation:

$$ dF/dt = p(1-F) + q(1-F)F $$

# System dynamics version of Bass diffusion model of product growth

The system dynamics (SD) version of the Bass diffusion model of product growth is shown n Figure 1. 

![image](https://github.com/user-attachments/assets/8169bb0f-563e-4ab2-bb42-49bce8db29cd)

Figure 1. Stella version of Bass model

$$ Adoption(t) = Innovation(t) +  Imitation(t) $$

$$Imitation(t) = \textit{Coefficient of Imitation} \cdot \textit{Potential Users} \cdot Users  (Users+\textit{Potential Users})$$

$$ \textbf{greatest} $$

Coefficient_of_Imitation = .5

Coefficient_of_Innovation = 0.05

F = Users/Initial_Potential_Users


 


    UNITS: Dimensionless

    UNITS: Users/Month
Initial_Potential_Users = 5E6
    UNITS: Users
Innovation = Coefficient_of_Innovation* Potential_Users
    UNITS: Users/Month
Potential_Users(t) = Potential_Users(t - dt) + ( - Adoption) * dt
    INIT Potential_Users = Initial_Potential_Users
    UNITS: Users
Users(t) = Users(t - dt) + (Adoption) * dt
    INIT Users = 0
    UNITS: Users


![image](https://github.com/user-attachments/assets/a9cea467-e133-41e7-9887-484a9e98f695)

Figure 2. Innovation and immitation over time

![image](https://github.com/user-attachments/assets/f03e5734-8156-480b-9d79-196ccb371f13)

Figure 3. Installed user base, $F(t)$, as proportion of potential users 

# References 

Bass, F. M. (1967). A new product growth for model consumer durables. *Management Science, 15*(5), 215-227. 

Bass, F. M. (2004). Comments on “A new product growth for model consumer durables”. *Management Science, 50*(12), 1833-1840. 

Rogers, E. M. (1995). *Diffusion of innovation (4th ed.).* The Free Press. 

Sterman, J. D. (2000). *Business dynamics: Systems thinking and modeling for a complex world.* Irwin McGraw-Hill. 






