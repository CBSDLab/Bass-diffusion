# Frank M. Bass (1967) model of product growth
Bass model of product growth is based on Everett Rogers' diffusion of innovation theory (for an overview, see Rogers, 1995). The model describes the continuous process of product adoption where the installed base as proportion of potential users, $F(t)$, is a function of the coefficient of innovation, $p$, and coefficient of immitation, $q$, as a differential equation:

$$ dF/dt = p(1-F) + q(1-F)F $$

# System dynamics version of Bass diffusion model of product growth

The system dynamics (SD) version of the Bass diffusion model of product growth is shown n Figure 1. 

![image](https://github.com/user-attachments/assets/8169bb0f-563e-4ab2-bb42-49bce8db29cd)

**Figure 1.** Stella version of Bass model

1. $` Users(t) = \int_0^{u} Adoption(t)dt `$
2. Adoption(t) = Innovation(t) +  Imitation(t)
3. Innovation(t) = \textit{Coefficient of Innovation(t)} * Potential_Users(t)
4. Imitation(t) = Coefficient_of_Imitation(t) * Potential_Users(t) * Users / (Users + Potential_Users)
5. Coefficient_of_Imitation = 0.5
6. Coefficient_of_Innovation = 0.05
7. Initial_Potential_Users = 5E6
8. F = Users(t)/Initial_Potential_Users

![image](https://github.com/user-attachments/assets/a9cea467-e133-41e7-9887-484a9e98f695)

Figure 2 shows the plots from simulating the model from 0 to 24 months using the equations above with a $DT=1/64$ months. Figure 3 shows the calculated proportion as proportion of users over time. 

**Figure 2.** Innovation and immitation over time

![image](https://github.com/user-attachments/assets/f03e5734-8156-480b-9d79-196ccb371f13)

**Figure 3.** Installed user base, $F(t)$, as proportion of potential users 

Frank Bass extended the model to consider multiple generations of an innovation (Bass, 2004) and John Sterman (2000) presents a version of the Bass diffusion model as an alternative to SIR models of diffusion that addresses some of the limitations in the SI and SIR models of diffusion.

# References 

Bass, F. M. (1967). A new product growth for model consumer durables. *Management Science, 15*(5), 215-227. 

Bass, F. M. (2004). Comments on “A new product growth for model consumer durables”. *Management Science, 50*(12), 1833-1840. 

Rogers, E. M. (1995). *Diffusion of innovation (4th ed.).* The Free Press. 

Sterman, J. D. (2000). *Business dynamics: Systems thinking and modeling for a complex world.* Irwin McGraw-Hill. 






