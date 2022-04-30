## Welcome to GitHub Page

<div class="button-group filter-button-group justify-content-center">
    <a class="btn btn-sm btn-primary" data-filter="web3">Web3</a>
    <a class="btn btn-sm btn-primary" data-filter="defi">DeFi</a>
    <a class="btn btn-sm btn-primary active" data-filter="*">All</a>
</div>



<div class="grid">
  {% for line in site.data.basetest1 %}
     <div class="col-md-4 col-sm-6 portfolio-item {{ line.title }}">
        <a class="portfolio-link" data-toggle="modal" href="#p{{ forloop.index }}">
          {{ line.tldr }}
        </a>
     </div>
  {% endfor %}
</div>


<ul>
{% for line in site.data.basetest1 %}
  <li>
    {{line.title}} -- {{line.tldr}}
  </li>
 {% endfor %} 
</ul>
