---
layout: default
title: Frontier-CS
permalink: /
---

<section class="fc-hero fc-hero-bench">
  <div class="fc-hero-copy">
    <h1><span>Frontier-CS</span><span>Benchmark</span></h1>
    <div class="fc-hero-points">
      <p><em>Unsolved:</em> no solution has achieved perfect scores</p>
      <p><em>Open-ended:</em> research &amp; optimization challenges</p>
      <p><em>Verifiable:</em> continuous scoring, always room to improve</p>
      <p><em>Diverse:</em> systems, ML, algorithms, security, and more</p>
    </div>
    <p class="fc-release-link">→ Read our release blog <a href="{{ '/blog/feb-release/' | relative_url }}">here</a>.</p>
  </div>

  <div class="fc-terminal-card" aria-label="Frontier-CS command line benchmark preview">
    <div class="fc-terminal-top">
      <span></span>
      <span></span>
      <span></span>
      <p>frontier-cs · codebase_adaptation · evaluation</p>
    </div>
    <div class="fc-terminal-body">
      <p class="fc-terminal-line fc-terminal-comment" style="--line-delay: 0.2s;"># Run with any standard agent CLI</p>
      <p class="fc-terminal-line" style="--line-delay: 0.9s;"><span class="fc-prompt">$</span> uv run harbor run -d frontier-cs-algorithm \</p>
      <p class="fc-terminal-line fc-terminal-indent" style="--line-delay: 1.6s;">-a claude-code -m "anthropic/claude-opus-4-6"</p>
    </div>
  </div>
</section>

<section class="fc-section fc-latest">
  <div class="fc-section-heading fc-section-heading-row">
    <div>
      <p class="fc-kicker">Latest</p>
      <h2>Recent posts</h2>
    </div>
    <a href="{{ '/blog/' | relative_url }}">View all</a>
  </div>
  <div class="fc-post-grid">
    {% assign latest_posts = site.posts | sort: "date" | reverse %}
    {% assign latest_count = 0 %}
    {% for post in latest_posts %}
      {% include blog_card.html post=post variant="compact" %}
      {% assign latest_count = latest_count | plus: 1 %}
      {% if latest_count >= 3 %}
        {% break %}
      {% endif %}
    {% endfor %}
  </div>
  <div class="fc-post-list-strip">
    <h3>At Frontier-CS, we build benchmarks for open-ended, verifiable AI evaluation.</h3>
    <div class="fc-post-list">
      {% for post in latest_posts offset:3 limit:5 %}
      {% assign post_label = post.tags | first %}
      {% if post_label == blank %}
        {% assign post_label = post.date | date: "%b %-d, %Y" %}
      {% endif %}
      <a class="fc-post-list-item" href="{{ post.url | relative_url }}">
        <span>{{ post.title }}</span>
        <em>{{ post_label }}</em>
      </a>
      {% endfor %}
    </div>
  </div>
</section>

<section id="leaderboard" class="fc-section fc-leaderboard">
  <div class="fc-section-heading fc-section-heading-row">
    <div>
      <p class="fc-kicker">Leaderboard</p>
      <h2>Frontier-CS model rankings</h2>
    </div>
    <span>Updated 2026-05-04</span>
  </div>

  <div class="fc-leaderboard-grid">
    <article class="fc-leaderboard-card">
      <div class="fc-leaderboard-card-header">
        <h3>Algorithmic Track</h3>
        <p>172 problems</p>
      </div>
      <div class="fc-table-wrap">
        <table>
          <thead>
            <tr>
              <th>Rank</th>
              <th>Model</th>
              <th>Score@1</th>
              <th>Avg@5</th>
              <th>Score@5</th>
              <th>Elo</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><span class="fc-medal">🥇</span></td>
              <td><span class="fc-model-name">gemini-3.0-pro</span></td>
              <td>33.12</td>
              <td>34.58</td>
              <td>56.09</td>
              <td>1265</td>
            </tr>
            <tr>
              <td><span class="fc-medal">🥈</span></td>
              <td><span class="fc-model-name">gpt-5.2-thinking</span></td>
              <td>32.40</td>
              <td>33.11</td>
              <td>47.19</td>
              <td>1242</td>
            </tr>
            <tr>
              <td><span class="fc-medal">🥉</span></td>
              <td><span class="fc-model-name">gpt-5-thinking</span></td>
              <td>23.10</td>
              <td>22.58</td>
              <td>39.73</td>
              <td>1196</td>
            </tr>
            <tr>
              <td>4</td>
              <td><span class="fc-model-name">deepseek-3.2</span></td>
              <td>24.83</td>
              <td>23.89</td>
              <td>41.44</td>
              <td>1193</td>
            </tr>
            <tr>
              <td>5</td>
              <td><span class="fc-model-name">grok-4</span></td>
              <td>24.04</td>
              <td>22.98</td>
              <td>36.81</td>
              <td>1174</td>
            </tr>
            <tr>
              <td>6</td>
              <td><span class="fc-model-name">gemini-2.5-pro</span></td>
              <td>20.34</td>
              <td>19.32</td>
              <td>36.65</td>
              <td>1167</td>
            </tr>
            <tr>
              <td>7</td>
              <td><span class="fc-model-name">gpt-5.1-thinking</span></td>
              <td>20.64</td>
              <td>21.49</td>
              <td>34.76</td>
              <td>1164</td>
            </tr>
          </tbody>
        </table>
      </div>
      <p class="fc-human-reference">Human reference: 86.99 (Score@1)</p>
    </article>

    <article class="fc-leaderboard-card">
      <div class="fc-leaderboard-card-header">
        <h3>Research Track</h3>
        <p>68 problems</p>
      </div>
      <div class="fc-table-wrap">
        <table>
          <thead>
            <tr>
              <th>Rank</th>
              <th>Model</th>
              <th>Score@1</th>
              <th>Avg@5</th>
              <th>Score@5</th>
              <th>Elo</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><span class="fc-medal">🥇</span></td>
              <td><span class="fc-model-name">gemini-3.0-pro</span></td>
              <td>46.55</td>
              <td>43.14</td>
              <td>59.22</td>
              <td>1283</td>
            </tr>
            <tr>
              <td><span class="fc-medal">🥈</span></td>
              <td><span class="fc-model-name">gpt-5-thinking</span></td>
              <td>30.91</td>
              <td>34.94</td>
              <td>55.25</td>
              <td>1218</td>
            </tr>
            <tr>
              <td><span class="fc-medal">🥉</span></td>
              <td><span class="fc-model-name">gpt-5.1-thinking</span></td>
              <td>32.12</td>
              <td>33.70</td>
              <td>56.79</td>
              <td>1214</td>
            </tr>
            <tr>
              <td>4</td>
              <td><span class="fc-model-name">gpt-5.2-thinking</span></td>
              <td>30.29</td>
              <td>34.09</td>
              <td>58.90</td>
              <td>1210</td>
            </tr>
            <tr>
              <td>5</td>
              <td><span class="fc-model-name">gemini-2.5-pro</span></td>
              <td>21.66</td>
              <td>25.74</td>
              <td>51.57</td>
              <td>1180</td>
            </tr>
            <tr>
              <td>6</td>
              <td><span class="fc-model-name">grok-4</span></td>
              <td>26.75</td>
              <td>24.01</td>
              <td>48.15</td>
              <td>1149</td>
            </tr>
            <tr>
              <td>7</td>
              <td><span class="fc-model-name">deepseek-3.2</span></td>
              <td>21.51</td>
              <td>21.76</td>
              <td>44.41</td>
              <td>1146</td>
            </tr>
          </tbody>
        </table>
      </div>
    </article>
  </div>
</section>

<section class="fc-section fc-contributors">
  <h2>100+ Contributors from</h2>
  <p class="fc-contributors-label">Academic institutions</p>
  <div class="fc-logo-marquee" aria-label="Contributing academic institutions">
    <div class="fc-logo-track">
      <div class="fc-school-card">
        <img src="{{ 'assets/img/institutions/stanford.svg' | relative_url }}" alt="Stanford logo">
        <p>Stanford</p>
      </div>
      <div class="fc-school-card">
        <img src="{{ 'assets/img/institutions/berkeley.svg' | relative_url }}" alt="UC Berkeley logo">
        <p>UC Berkeley</p>
      </div>
      <div class="fc-school-card">
        <img src="{{ 'assets/img/institutions/princeton.svg' | relative_url }}" alt="Princeton logo">
        <p>Princeton</p>
      </div>
      <div class="fc-school-card">
        <img src="{{ 'assets/img/institutions/stanford.svg' | relative_url }}" alt="Stanford logo">
        <p>Stanford</p>
      </div>
      <div class="fc-school-card">
        <img src="{{ 'assets/img/institutions/berkeley.svg' | relative_url }}" alt="UC Berkeley logo">
        <p>UC Berkeley</p>
      </div>
      <div class="fc-school-card">
        <img src="{{ 'assets/img/institutions/princeton.svg' | relative_url }}" alt="Princeton logo">
        <p>Princeton</p>
      </div>
    </div>
  </div>
</section>

<footer class="fc-bottom-nav" aria-label="Footer navigation">
  <a class="fc-bottom-brand" href="{{ '/' | relative_url }}">
    <span>Frontier-CS</span>
    <em>2026 · MIT License</em>
  </a>
  <nav>
    <a href="{{ '/blog/' | relative_url }}">Blog</a>
    <a href="{{ '/#leaderboard' | relative_url }}">Leaderboard</a>
    <a href="{{ '/get-involved/' | relative_url }}">Join</a>
    <a href="https://discord.com/invite/k4hd2nU4UE" target="_blank" rel="noopener noreferrer">Discord</a>
    <a href="https://github.com/FrontierCS/Frontier-CS" target="_blank" rel="noopener noreferrer">Repository ↗</a>
  </nav>
</footer>
