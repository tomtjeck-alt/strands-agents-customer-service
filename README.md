# Agent de service client avec Strands Agents (AWS Bedrock)

Série de 4 modules qui construisent pas à pas un agent de service client (recherche client, historique de commandes, remboursements) avec le SDK [Strands Agents](https://strandsagents.com) sur Amazon Bedrock.

| Module | Sujet |
|--------|-------|
| [01-agent-loop-tools](samples/01-agent-loop-tools) | Boucle agent + outils (`lookup_customer`, `get_order_history`, `process_refund`) |
| [02-hooks](samples/02-hooks) | Hooks sur le cycle de vie de l'agent |
| [03-skills-steering](samples/03-skills-steering) | Skills (SKILL.md) et steering handlers |
| [04-session-managers](samples/04-session-managers) | Persistance des sessions |

## Lancer

Python 3.10+, identifiants AWS avec accès à Bedrock.

```bash
cd samples/01-agent-loop-tools
pip install -r requirements.txt
jupyter lab   # ou ouvrir le notebook dans VS Code
```

Chaque module a aussi un `chat.py` pour discuter avec l'agent en ligne de commande.

Les données clients et commandes sont fictives.
