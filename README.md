#Des Moines Workers' Alliance Bolt CMS Theme

This is a theme for BoltCMS, built for the Des Moines Workers' Alliance.

##Overview of files
`/css`: compiled sass (theme.css)
`/css/sass`: sass files
`entry.twig`: A single entry, for the newspaper/blogging aspect
`index.twig`: Static index file, takes a block for aims, and grabs some info on the projects
`listing.twig`: General list of entries, used for search (through actual search and by taxonomy)
`newspaper.twig`: Formatted listing of entries. The large post at top needs a 'featured' tag, the three underneath it are just the three most recent, others are similar to `listing.twig`. You need a block for the advert at the bottom.
`page.twig`: General purpose page
`partials/_foot.twig`: Footer. The menu comes from the menu partial.
`partials/_head.twig`: HTML head and menubar. Menu items come from the menu partial.
`partials/_menu.twig`: Gets the items in menu as a ul with lis. Only is the one level.
`partials/_share_buttons.twig`: HTML and some inline CSS for sharing pages to Facebook or Twitter
`partials/_sub_pager.twig`: Custom buttons for pagination
`project_single.twig`: A single project
`projects.twig`: A listing of projects with their teaser

##Installing
If you would like to use this theme as a base here is the general config I have now.

###Content types

* Pages (Page)
	* Fields
		* title (text)
		* slug (slug)
		* image (image)
		* body (html)
	* Template: any (specific things, or page.twig)
* Projects (Project)
	* Fields
		* title (text)
		* slug (slug)
		* image (image)
		* teaser (html)
		* body (html)
	* Template: project_single.twig
* Entries (Entry)
	* Fields
		* title (text)
		* slug (slug)
		* teaser (html)
		* body (html)
		* image (image)
		* video (video)
	* Taxonomy: tags
	* Record template: entry.twig
	* Listing template: newspaper.twig
	* Listing records: 10
	* Note: The first large post is a featured post and needs the 'featured' tag to show
* Blocks (Block)
	* Fields
		* title (text)
		* slug (slug)
		* content (html)
		* contentlink (text)
		* image (image)
	* Viewless: true
	* Searchable: false

###Config Notes
* You can use `sitename` and `payoff`
* Set `homepage_template` to `index.twig`
* All of the default htmlcleaner tags (sans code and tt) look consistent

#License
GPL-v3
