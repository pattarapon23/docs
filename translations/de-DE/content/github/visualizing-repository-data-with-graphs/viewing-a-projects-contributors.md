---
title: Mitwirkende eines Projekts anzeigen
intro: 'You can see who contributed commits to a repository{% if currentVersion == "free-pro-team@latest" %} and its dependencies{% endif %}.'
redirect_from:
  - /articles/i-don-t-see-myself-in-the-contributions-graph/
  - /articles/viewing-contribution-activity-in-a-repository/
  - /articles/viewing-a-projects-contributors
product: '{% data reusables.gated-features.repository-insights %}'
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

### Informationen zu Mitarbeitern

Im Mitarbeiterdiagramm kannst Du die Top 100 der Mitarbeiter an einem Repository anzeigen{% if enterpriseServerVersions contains currentVersion %}, darunter auch die Commit-Co-Autoren{% endif %}. Merge- und leere Commits werden für dieses Diagramm nicht als Beiträge gezählt.

{% if currentVersion == "free-pro-team@latest" %}
Darüber hinaus kannst Du eine Liste der Personen anzeigen, die Beiträge zu den Python-Abhängigkeiten des Projekts geliefert haben. Rufe `https://github.com/REPO-OWNER/REPO-NAME/community_contributors` auf, um auf diese Liste der Community-Mitarbeiter zuzugreifen.
{% endif %}

### Auf das Mitarbeiterdiagramm zugreifen

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.accessing-repository-graphs %}
3. Klicke auf der linken Seitenleiste auf **Contributors** (Mitarbeiter). ![Registerkarte „Contributors“ (Mitarbeiter)](/assets/images/help/graphs/contributors_tab.png)
4. Wenn Du optional Mitarbeiter während eines bestimmten Zeitraums anzeigen möchtest, klicke und ziehe solange, bis der gewünschte Zeitraum ausgewählt ist. ![Ausgewählter Zeitraum im Mitarbeiterdiagramm](/assets/images/help/graphs/repo_contributors_click_drag_graph.png)

### Fehlerbehebung bei Mitarbeitern

Aus den folgenden Gründen wirst Du möglicherweise im Mitarbeiterdiagramm eines Repositorys nicht angezeigt:
- Du zählst nicht zu den Top-100-Mitarbeitern.
- Deine Commits wurden nicht in den Standardbranch zusammengeführt.
- Die von Dir zum Erstellen der Commits verwendete E-Mail-Adresse wurde Deinem {% data variables.product.product_name %}-Konto nicht hinzugefügt.

{% tip %}

**Tip:** To list all commit contributors in a repository, see "[Repositories](/v3/repos/#list-contributors)."

{% endtip %}

Wenn alle Deine Commits in Nicht-Standardbranches des Repository sind, wirst Du im Mitarbeiterdiagramm nicht aufgeführt. So sind Commits auf dem Branch `gh-pages` im Diagramm nur dann enthalten, wenn `gh-pages` der Standardbranch des Repositorys ist. Damit Deine Commits in den Standardbranch zusammengeführt werden, kannst Du einen Pull Request erstellen. Weitere Informationen findest Du unter „[Informationen zu Pull Requests](/articles/about-pull-requests).“

Wenn die von Dir zum Erstellen der Commits verwendete E-Mail-Adresse Deinem {% data variables.product.product_name %}-Konto nicht hinzugefügt wurde, werden Deine Commits nicht mit Deinem Konto verknüpft, und Du wirst im Mitarbeiterdiagramm nicht angezeigt. Weitere Informationen findest Du unter „[Deine E-Mail-Adresse für Commits festlegen](/articles/setting-your-commit-email-address)“ und „[Eine E-Mail-Adresse zum {% data variables.product.product_name %}-Konto hinzufügen](/articles/adding-an-email-address-to-your-github-account).“
