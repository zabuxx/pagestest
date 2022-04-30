## Welcome to GitHub Page

<div class="button-group filter-button-group justify-content-center">
    <a class="btn btn-sm btn-primary" data-filter="web3">Web3</a>
    <a class="btn btn-sm btn-primary" data-filter="defi">DeFi</a>
    <a class="btn btn-sm btn-primary active" data-filter="*">All</a>
</div>


<script src="https://code.jquery.com/jquery-3.1.0.min.js" integrity="sha256-cCueBR6CsyA4/9szpPfrX3s49M9vUU5BgtiJj06wt/s=" crossorigin="anonymous"></script>
<script src="https://unpkg.com/isotope-layout@3.0/dist/isotope.pkgd.js"></script>
<script src="https://unpkg.com/imagesloaded@4/imagesloaded.pkgd.min.js"></script>

<script>
  var $grid = $('.grid').imagesLoaded( function() {
      $grid.isotope({});
  });
  $('.filter-button-group').on( 'click', 'a', function() {
      var filterValue = $(this).attr('data-filter');
      $grid.isotope({ filter: filterValue });
   });
   $('.button-group a.btn').on('click', function(){
      $('.button-group a.btn').removeClass('active');
      $(this).addClass('active');
   });
</script>


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
