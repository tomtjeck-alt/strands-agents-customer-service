# Agent de service client avec Strands Agents (AWS Bedrock)

Série de 7 modules qui construisent pas à pas un agent de service client (recherche client, historique de commandes, remboursements) avec le SDK [Strands Agents](https://strandsagents.com) sur Amazon Bedrock.

| Module | Sujet |
|--------|-------|
| [01-agent-loop-tools](samples/01-agent-loop-tools) | Boucle agent + outils (`lookup_customer`, `get_order_history`, `process_refund`) |
| [02-hooks](samples/02-hooks) | Hooks sur le cycle de vie de l'agent |
| [03-skills-steering](samples/03-skills-steering) | Skills (SKILL.md) et steering handlers |
| [04-session-managers](samples/04-session-managers) | Persistance des sessions |
| [05-deploy](samples/05-deploy) | Déploiement sur Amazon Bedrock AgentCore (CDK) |
| [06-multi-agent](samples/06-multi-agent) | Délégation entre plusieurs agents |
| [07-evals](samples/07-evals) | Évaluation de l'agent |

Le dossier [shared](samples/shared) contient les outils communs.

## Rapport détaillé

📘 **[Lire le rapport complet, niveau débutant, avec captures d'écran](docs/RAPPORT.md)**

## Lancer

Python 3.10+, identifiants AWS avec accès à Bedrock.

```bash
cd samples/01-agent-loop-tools
pip install -r requirements.txt
jupyter lab   # ou ouvrir le notebook dans VS Code
```

Chaque module a aussi un `chat.py` pour discuter avec l'agent en ligne de commande.

Pour le module 5, remplacez `<VOTRE_ID_COMPTE_AWS>` dans `MonAgent/agentcore/aws-targets.json` et `<VOTRE_AGENT_ARN>` dans le notebook par vos propres valeurs (`agentcore status` affiche l'ARN).

Les données clients et commandes sont fictives.
