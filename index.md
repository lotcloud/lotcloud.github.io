---
layout: home
title: "Home"
nav_order: 1
description: "Living Off The Cloud - A repository for native cloud techniques that may be abused by a Threat Actor."
permalink: /
---

# Living off the Cloud
A repository that captures native cloud techniques which may be abused by a Threat Actor. This repository is aimed at helping security professionals understand, detect and mitgiate native cloud attack scenarios. 

## What is Living off the Cloud?

Similar to "Living off the Land" techniques, Threat Actors can leverage legitimate cloud services and features to:

- Establish persistence
- Evade detection
- Escalate privileges
- Exfiltrate data
- Maintain access

This repository catalogs these techniques across major cloud platforms.

---

## Platforms
<div class="platform-grid">
  <div class="platform-card">
    <h3>Microsoft 365</h3>
    <p>Entra ID, Exchange Online, SharePoint, Teams and related services</p>
    <a href="/m365/" class="btn">View Techniques →</a>
  </div>
</div>

---

## Contributing

Contributions are welcome for new techniques and improvements to existing documentation.

See our [Contributing Guide](https://github.com/lotcloud/living-off-the-cloud) for details on how to submit improvements.

---

## Disclaimer

This information is provided on an educational basis to secure cloud environments. Use this information responsibly and ethically.
<style>
.platform-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.platform-card {
  padding: 1.5rem;
  border: 1px solid var(--border-color);
  border-radius: 0.5rem;
  background-color: rgba(0, 0, 0, 0.02);
}

.platform-card h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  font-size: 1.25rem;
}

.platform-card p {
  margin-bottom: 1rem;
  color: #666;
  font-size: 0.9rem;
}

.platform-card .btn {
  display: inline-block;
  padding: 0.5rem 1rem;
  background-color: #0d6efd;
  color: white;
  text-decoration: none;
  border-radius: 0.25rem;
  font-size: 0.9rem;
  font-weight: 500;
  transition: background-color 0.2s;
}

.platform-card .btn:hover {
  background-color: #0b5ed7;
  text-decoration: none;
}

@media (max-width: 768px) {
  .platform-grid {
    grid-template-columns: 1fr;
  }
}
</style>