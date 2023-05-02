# title-menu


{% assign submenu = l.title | handleize %}

{% capture l_title %},{{ l.title | split: ' ' }},{% endcapture %}

{% if settings.mega1_title == l.title %}
<li class="{% if l.active %}active {% endif %}dropdown mega-menu">
  <a href="{{ l.url }}" class="dropdown-toggle dropdown-link" data-toggle="dropdown">
    <p class="{% if menu_label_1 contains l_title %}menu-sale-layout{% endif %} {% if menu_label_2 contains l_title %}menu-hot-layout{% endif %}">
      {{ l.title }}
      {% if menu_label_1 contains l_title %}
      <span class="menu-label label-sale">{{ settings.new_text }}</span>
      {% endif %}
      {% if menu_label_2 contains l_title %}
      <span class="menu-label label-hot">{{ settings.hot_text }}</span>
      {% endif %}
    </p>
    <i class="fa fa-angle-down"></i>
    <i class="sub-dropdown1"></i>
    <i class="sub-dropdown"></i>
  </a>
  <div class="megamenu-container megamenu-container-1 dropdown-menu" {% if settings.mega1_background %}style="background-image:  url({{ settings.mega1_background | img_url: '', crop: '' }})"{% endif %}>
    <ul class="sub-mega-menu">
      {% if settings.mega1_col1_linklist != "" %}
      <li class="mega-links mega1-collumn1">
        <ul>
          <li class="list-title">{{ linklists[settings.mega1_col1_linklist].title }}</li>
          {% for link in linklists[settings.mega1_col1_linklist].links %}
          <li class="list-unstyled li-sub-mega">
            <a href="{{ link.url }}">{{ link.title | escape }}</a>           
          </li>
          {% endfor %}
        </ul>
      </li>
      {% endif %}
      {% if settings.mega1_col2_linklist1 != "" or settings.mega1_col2_linklist2 != "" %}
      <li class="mega-links mega1-collumn2">
        <ul>
          <li class="list-title">{{ linklists[settings.mega1_col2_linklist1].title }}</li>
          {% for link in linklists[settings.mega1_col2_linklist1].links %}
          <li class="list-unstyled li-sub-mega">
            <a href="{{ link.url }}">{{ link.title | escape }}</a>           
          </li>
          {% endfor %}
        </ul>
        <ul>
          <li class="list-title">{{ linklists[settings.mega1_col2_linklist2].title }}</li>
          {% for link in linklists[settings.mega1_col2_linklist2].links %}
          <li class="list-unstyled li-sub-mega">
            <a href="{{ link.url }}">{{ link.title | escape }}</a>           
          </li>
          {% endfor %}
        </ul>
      </li>
      {% endif %}
      {% if settings.mega1_col3_linklist1 != "" or settings.mega1_col3_linklist2 != "" %}
      <li class="mega-links mega1-collumn3">
        <ul>
          <li class="list-title">{{ linklists[settings.mega1_col3_linklist1].title }}</li>
          {% for link in linklists[settings.mega1_col3_linklist1].links %}
          <li class="list-unstyled li-sub-mega">
            <a href="{{ link.url }}">{{ link.title | escape }}</a>           
          </li>
          {% endfor %}
        </ul>
        <ul>
          <li class="list-title">{{ linklists[settings.mega1_col3_linklist2].title }}</li>
          {% for link in linklists[settings.mega1_col3_linklist2].links %}
          <li class="list-unstyled li-sub-mega">
            <a href="{{ link.url }}">{{ link.title | escape }}</a>           
          </li>
          {% endfor %}
        </ul>
      </li>
      {% endif %}
    </ul>
  </div>  
</li>
{% elsif settings.mega2_title == l.title %}
<li class="{% if l.active %}active {% endif %}dropdown-1 mega-menu">
  <a href="{{ l.url }}" class="dropdown-toggle dropdown-link" data-toggle="dropdown">
    <p class="{% if menu_label_1 contains l_title %}menu-sale-layout{% endif %} {% if menu_label_2 contains l_title %}menu-hot-layout{% endif %}">
      {{ l.title }}
      {% if menu_label_1 contains l_title %}
      <span class="menu-label label-sale">{{ settings.new_text }}</span>
      {% endif %}
      {% if menu_label_2 contains l_title %}
      <span class="menu-label label-hot">{{ settings.hot_text }}</span>
      {% endif %}
    </p>
    <i class="fa fa-angle-down"></i>
    <i class="sub-dropdown1"></i>
    <i class="sub-dropdown"></i>
  </a>
  <div class="megamenu-container megamenu-container-2 dropdown-menu" {% if settings.mega2_background %}style="background-image:  url({{ settings.mega2_background | img_url: '', crop: '' }})"{% endif %}>
    <ul class="sub-mega-menu">
      {% if settings.mega2_col1_linklist != "" %}
      <li class="mega-links mega2-collumn1">
        <ul>
          <li class="list-title">{{ linklists[settings.mega2_col1_linklist].title }}</li>
          {% for link in linklists[settings.mega2_col1_linklist].links %}
          <li class="list-unstyled li-sub-mega">
            <a href="{{ link.url }}">{{ link.title | escape }}</a>           
          </li>
          {% endfor %}
        </ul>
      </li>
      {% endif %}
      {% if settings.mega2_col2_linklist != "" %}
      <li class="mega-links mega2-collumn2">
        <ul>
          <li class="list-title">{{ linklists[settings.mega2_col2_linklist].title }}</li>
          {% for link in linklists[settings.mega2_col2_linklist].links %}
          <li class="list-unstyled li-sub-mega">
            <a href="{{ link.url }}">{{ link.title | escape }}</a>           
          </li>
          {% endfor %}
        </ul>
      </li>
      {% endif %}
      {% if settings.mega2_col3_linklist != "" %}
      <li class="mega-links mega2-collumn3">
        <ul>
          <li class="list-title">{{ linklists[settings.mega2_col3_linklist].title }}</li>
          {% for link in linklists[settings.mega2_col3_linklist].links %}
          <li class="list-unstyled li-sub-mega">
            <a href="{{ link.url }}">{{ link.title | escape }}</a>           
          </li>
          {% endfor %}
        </ul>
      </li>
      {% endif %}
    </ul>
  </div>  
</li>	
{% elsif settings.mega3_title == l.title %}
<li class="{% if l.active %}active {% endif %}dropdown mega-menu">
  <a href="{{ l.url }}" class="dropdown-toggle dropdown-link" data-toggle="dropdown">
    <p class="{% if menu_label_1 contains l_title %}menu-sale-layout{% endif %} {% if menu_label_2 contains l_title %}menu-hot-layout{% endif %}">
      {{ l.title }}
      {% if menu_label_1 contains l_title %}
      <span class="menu-label label-sale">{{ settings.new_text }}</span>
      {% endif %}
      {% if menu_label_2 contains l_title %}
      <span class="menu-label label-hot">{{ settings.hot_text }}</span>
      {% endif %}
    </p>
    <i class="fa fa-angle-down"></i>
    <i class="sub-dropdown1"></i>
    <i class="sub-dropdown"></i>
  </a>
  <div class="megamenu-container megamenu-container-3 dropdown-menu">
    <div class="sub-mega-menu-group">
      <ul class="sub-mega-menu">
        {% if settings.mega3_col1_linklist != "" %}
        <li class="mega-links mega3-collumn1">
          <ul>
            <li class="list-title">{{ linklists[settings.mega3_col1_linklist].title }}</li>
            {% for link in linklists[settings.mega3_col1_linklist].links %}
            <li class="list-unstyled li-sub-mega">
              <a href="{{ link.url }}">{{ link.title | escape }}</a>           
            </li>
            {% endfor %}
          </ul>
        </li>
        {% endif %}
        {% if settings.mega3_col2_linklist != "" %}
        <li class="mega-links mega3-collumn2">
          <ul>
            <li class="list-title">{{ linklists[settings.mega3_col2_linklist].title }}</li>
            {% for link in linklists[settings.mega3_col2_linklist].links %}
            <li class="list-unstyled li-sub-mega">
              <a href="{{ link.url }}">{{ link.title | escape }}</a>           
            </li>
            {% endfor %}
          </ul>
        </li>
        {% endif %}
        {% if settings.mega3_col3_linklist != "" %}
        <li class="mega-links mega3-collumn3">
          <ul>
            <li class="list-title">{{ linklists[settings.mega3_col3_linklist].title }}</li>
            {% for link in linklists[settings.mega3_col3_linklist].links %}
            <li class="list-unstyled li-sub-mega">
              <a href="{{ link.url }}">{{ link.title | escape }}</a>           
            </li>
            {% endfor %}
          </ul>
        </li>
        {% endif %}
        {% if settings.mega3_col4_linklist != "" %}
        <li class="mega-links mega3-collumn4">
          <ul>
            <li class="list-title">{{ linklists[settings.mega3_col4_linklist].title }}</li>
            {% for link in linklists[settings.mega3_col4_linklist].links %}
            <li class="list-unstyled li-sub-mega">
              <a href="{{ link.url }}">{{ link.title | escape }}</a>           
            </li>
            {% endfor %}
          </ul>
        </li>
        {% endif %}
      </ul>
    </div>    
  </div>  
</li>	
{% elsif linklists[submenu].links.size > 0 %}
<li class="nav-item{% if l.active %} active{% endif %} dropdown navigation">
  <a href="{{ l.url }}" class="dropdown-toggle dropdown-link" data-toggle="dropdown">
    <p class="{% if menu_label_1 contains l_title %}menu-sale-layout{% endif %} {% if menu_label_2 contains l_title %}menu-hot-layout{% endif %}">
      {{ l.title }}
      {% if menu_label_1 contains l_title %}
      <span class="menu-label label-sale">{{ settings.new_text }}</span>
      {% endif %}
      {% if menu_label_2 contains l_title %}
      <span class="menu-label label-hot">{{ settings.hot_text }}</span>
      {% endif %}
    </p>
    <i class="fa fa-angle-down"></i>
    <i class="sub-dropdown1"></i>
    <i class="sub-dropdown"></i>
  </a>
  <ul class="dropdown-menu">    
    {% for l in linklists[submenu].links %}
    {% include 'navigation-sub-links' with forloop.index %}
    {% endfor %}
  </ul>
</li>
{% else %}
<li class="nav-item{% if l.active %} active{% endif %}">
  <a href="{{ l.url }}">
    <p class="{% if menu_label_1 contains l_title %}menu-sale-layout{% endif %} {% if menu_label_2 contains l_title %}menu-hot-layout{% endif %}">
      {{ l.title }}
      {% if menu_label_1 contains l_title %}
      <span class="menu-label label-sale">{{ settings.new_text }}</span>
      {% endif %}
      {% if menu_label_2 contains l_title %}
      <span class="menu-label label-hot">{{ settings.hot_text }}</span>
      {% endif %}
    </p>
  </a>
</li>
{% endif %}




 {
    "name": "Mega Menu",
    "settings": [
      {
        "type": "header",
        "content": "Main Menu Setting"
      },
      {
        "type": "link_list",
        "id": "nav_linklist",
        "label": "Main Menu Link"
      },
      {
        "type": "checkbox",
        "id": "nav_sticky",
        "label": "Active Sticky (float) Navigation?",
        "default": true
      },
      {
        "type": "header",
        "content": "Menu Label"
      },
      {
        "type": "text",
        "id": "menu_label_1",
        "label": "New:",
        "info": "Separate tags with comma"
      },
      {
        "type": "text",
        "id": "menu_label_2",
        "label": "Hot:",
        "info": "Separate tags with comma"
      },
      {
        "type": "header",
        "content": "Mega Menu 01"
      },
      {
        "type": "text",
        "id": "mega1_title",
        "label": "Mega Menu 01 Title",
        "info": "(blank if you don't want to use)"
      },
      {
        "type": "link_list",
        "id": "mega1_col1_linklist",
        "label": "1st Column: Link List"
      },
      {
        "type": "link_list",
        "id": "mega1_col2_linklist1",
        "label": "2nd Column: Link List 1"
      },
      {
        "type": "link_list",
        "id": "mega1_col2_linklist2",
        "label": "2nd Column: Link List 2"
      },
      {
        "type": "link_list",
        "id": "mega1_col3_linklist1",
        "label": "3rd Column: Link List 1"
      },
      {
        "type": "link_list",
        "id": "mega1_col3_linklist2",
        "label": "3rd Column: Link List 2"
      },
      {
        "type": "image_picker",
        "id": "mega1_background",
        "label": "Upload Background"
      },
      {
        "type": "header",
        "content": "Mega Menu 02"
      },
      {
        "type": "text",
        "id": "mega2_title",
        "label": "Mega Menu 02 Title",
        "info": "(blank if you don't want to use)"
      },
      {
        "type": "link_list",
        "id": "mega2_col1_linklist",
        "label": "1st Column: Link List"
      },
      {
        "type": "link_list",
        "id": "mega2_col2_linklist",
        "label": "2nd Column: Link List"
      },
      {
        "type": "link_list",
        "id": "mega2_col3_linklist",
        "label": "3rd Column: Link List"
      },
      {
        "type": "image_picker",
        "id": "mega2_background",
        "label": "Upload Background"
      },
      {
        "type": "header",
        "content": "Mega Menu 03"
      },
      {
        "type": "text",
        "id": "mega3_title",
        "label": "Mega Menu 03 Title",
        "info": "(blank if you don't want to use)"
      },
      {
        "type": "link_list",
        "id": "mega3_col1_linklist",
        "label": "1st Column: Link List"
      },
      {
        "type": "link_list",
        "id": "mega3_col2_linklist",
        "label": "2nd Column: Link List"
      },
      {
        "type": "link_list",
        "id": "mega3_col3_linklist",
        "label": "3rd Column: Link List"
      },
      {
        "type": "link_list",
        "id": "mega3_col4_linklist",
        "label": "4th Column: Link List"
      }
    ]
  },
