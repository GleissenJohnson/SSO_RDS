# SSO_RDS
Activer le SSO sur RDS


Aller dans le fichier config de notre site dans C:\Windows\Web\RDWeb\Pages

![image](https://github.com/GleissenJohnson/SSO_RDS/assets/115966414/7b73776e-2147-4711-a3ad-ec8d3d86a22e)


Dans le fichier, chercher la ligne "<authentication mode="Windows"/>" et décommenter les balises HTML "--> et <!--"

![image](https://github.com/GleissenJohnson/SSO_RDS/assets/115966414/852630e4-6882-4871-801b-4120a2d8a5d4)


Désactiver la ligne "<authentication mode="Forms">...</authentication>"

![image](https://github.com/GleissenJohnson/SSO_RDS/assets/115966414/89b3339e-5783-4859-b5b1-cce45c537b89)

Dans <system.webServer>, commenter le module runAllManagedModules + security

![image](https://github.com/GleissenJohnson/SSO_RDS/assets/115966414/977db10a-d53e-4f96-8db1-55905e1024d9)


Dans IIS : aller dans "RDweb" => "Authentification"

![image](https://github.com/GleissenJohnson/SSO_RDS/assets/115966414/a490627d-b8c1-4c8a-bdc5-ee4369d602dc)

Activer la Windows Authentification  et activer l'extended Protection dans les paramètres avancés, puis désactiver l'Anonymous Authentification

![image](https://github.com/GleissenJohnson/SSO_RDS/assets/115966414/64696232-b791-4d09-a413-5399135c0273)


Le SSO est désormais activé sur RD Web Access.
