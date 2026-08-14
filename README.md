# renovate-config

Preset Renovate partage de RN20. Il porte la politique de mise a jour des
dependances pour tous les repos de l'organisation web-rn20 et du compte
JulienMassonnat : passe hebdomadaire (nuit de dimanche a lundi, heure de
Paris), delai de 7 jours avant d'adopter une version publiee (protection
supply chain), automerge limite aux patchs de prod et aux minor/patch des
devDependencies quand la CI est verte, majeures sur approbation via le
Dependency Dashboard, jamais d'automerge sur next/react/prisma.

Pour abonner un repo, ajouter a sa racine un fichier renovate.json contenant
`{"extends": ["github>web-rn20/renovate-config"]}`. Prerequis : l'app Mend
Renovate doit etre installee par un admin sur l'organisation et le compte
(https://github.com/apps/renovate), et le repo doit avoir au moins un check
CI (sans check vert, Renovate ne merge rien tout seul, par construction).
Toute evolution de la politique se fait ici, en un commit, pour tout le parc.
