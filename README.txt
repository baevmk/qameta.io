
Content organization:



TODO: create archetypes 

All content organized by subfolders. Content that created in content folders are draft.


TODO: organize contents and DATA

.
└── content
    ├── about
	|	├── Contact 
    |	└── ...
    ├── blogs
    |	├── Allure 2.0-BETA6 released 
    |	├── Allure 2.0-BETA5 released
    |	├── ...
    |	└── Allure 2.0-BETA3 released
    ├── people
    |	├── Baev Dmitrii
    |	├── ...
    |	├── Eroshenko Artem
    |	└── Seliverstov Stas
    ├── FAQ
    |   ├── _index.md
    |   ├── wtf1.md
    |   ├── ...
    |   └── wtf2.md

Data organization:
maindata.yaml

TODO: List pages
create and configure list pages (tut12) with _index.md


TODO: HOUTO print content for # pages in folder

--  content /
     -- cn /
         -- post /
         -- teach /
     -- en /
         -- post /
         -- read /


range
Iterates over a map, array, or slice.
Syntax: range COLLECTION

first
Slices an array to only the first N elements.
Syntax: first LIMIT COLLECTION

{{ range where .Pages "File.Dir" "in" "/cn/post/" }}
{{ with .Site.GetPage "page" "blogs" }}

{{ range first 3  }}


-----------------------------------------------------------------
this shit work!!!
{{ with .Site.GetPage "page" "about" "contact.md" }}
	{{ .Title }}
	{{ .Content }}

	<!-- IF/ELSE example -->
	{{ if isset .Params "phone" }}
		{{ printf .Params.phone }}
	{{else}}
		not set params
	{{ end }}

{{ end }}
-----------------------------------------------------------------


Leveraging the - in the following example will remove the extra white space surrounding the .Title variable and remove the newline:
<div>
  {{- .Title -}}
</div>


{{ range where .Data.Pages.ByDate "Section" "events" }}


{{ range where .Data.Pages.ByDate "Section" "blogs" }}
  {{ .Content }}
{{ end }}
-----------------------------------------------------------------
Link bar
					{{ range $.Site.Home.Sections }}
						Section: {{ .Title }}
						{{ range .Pages }}
							Section Page: {{ .Title }}
						{{ end }}
					{{ end }}
-------------------------------------------------------------------
<!-- Take Data  from datasheet (Now take from contact.md)
				<h1 class="secondary-text">{{ .Site.Data.maindata.title_contact_1 }}<span class="primary-text">{{ .Site.Data.maindata.title_contact_2 }}</span></h1>
				<p class="secondary-text">
					Phone number: <span class="primary-text">{{ .Site.Data.maindata.phone_contact }} </span></br>
					E-mail: <span class="primary-text">{{ .Site.Data.maindata.email_contact }} </span></br>
					Address: <span class="primary-text">{{ .Site.Data.maindata.address_contact }} </span></br>
				</p>
			-->

Firefox:
Ctrl + Shift + M - Responsive Design View - You can test FlexBoxGrid
Ctrl + Shift + C - Inspector


--------------------------------------------------------------------
12/13/2017
Old showcase was deleted from main project

	<!-- Can't define variables inside .Range, defined before -->
	{{ $showcase_title_1 := .Site.Data.maindata.title_showcase_1 }}
	{{ $showcase_title_2 := .Site.Data.maindata.title_showcase_2 }}
	{{ $showcase_description := .Site.Data.maindata.description_showcase }}
	{{ $showcase_image := .Site.Data.maindata.image_showcase }}

<!-- Content container -->
	<div class="container">
		<div class="showcase_row row center-xs center-sm center-md center-lg middle-xs middle-sm middle-md middle-lg">

			<div class="showcase_content col-xs-12 col-sm-4 col-md-4 col-lg-4">

				<!-- FA rocket -->
				<div class="primary_h1 fas fa-rocket"></div>
				<!-- Showcase staff -->
				<h1 class="common_h2"> {{ $showcase_title_1 }} </br>
				<span class="primary_h2"> {{ $showcase_title_2 }} </span></h1>
				<div class="common_text"> {{ $showcase_description }} </div>
				<!-- Buttons -->
				<button class="button"> Download</button>
				<button class="button"> Learn More</button>	

			</div>
			<div class="col-xs-12 col-sm-8 col-md-8 col-lg-8">
				<img class="showcase_img" src=" {{ $showcase_image }} ">
			</div>

		</div>
	</div>

---------------------------------------------------------------------------