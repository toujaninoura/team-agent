# team-agent

Systeme multi-agents PO + BA pour creer le backlog GitHub.

## Structure
team-agent/
  po-agent/
    CLAUDE.md          <- Agent Product Owner
  ba-agent/
    CLAUDE.md          <- Agent Business Analyst
  shared/
    conversation.json  <- Communication entre agents
  po-memory.json       <- Memoire persistante PO
  ba-memory.json       <- Memoire persistante BA
  README.md

## Comment utiliser
1. Ouvrir po-agent/ dans VS Code
2. Lancer Claude Code (etoile)
3. Coller le CDC
4. Le PO analyse et lance le BA automatiquement
5. Suivre la conversation PO <-> BA dans le chat
6. Valider le backlog quand demande
7. Issues creees automatiquement sur GitHub

## Flux de communication
waiting
  -> po_vision_ready    (PO a analyse le CDC)
  -> ba_questions_ready (BA a pose ses questions)
  -> po_answers_ready   (PO a repondu)
  -> ba_issues_proposed (BA a propose les issues)
  -> po_review_done     (PO a review)
  -> ba_backlog_final   (BA a finalise)
  -> user_approved      (User a valide)
  -> issues_created     (Issues sur GitHub)
