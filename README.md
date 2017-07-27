# nav-menu-walker-microformat
A code for initializing nav menu in Wordpress to support Google's microformat.

To use, simply modify your Wordpress menu code. For example: 
if( has_nav_menu( 'primary' ) ) : ?>
				<nav id="site-links" class="flat">
				<?php wp_nav_menu( array(
						'container'  => '',
						'items_wrap' => '<ul id="site-link-navigation" class="clearfix" itemscope itemtype="https://schema.org/SiteNavigationElement" role="navigation" aria-label="' . __( 'Primary Menu', 'freshstart') . '">%3$s</ul>',
						'menu_class'     => 'primary-menu',
						'theme_location' => 'primary',
						'walker'         => new Primary_Menu_Walker
					) ); ?>
				</nav><!-- end of site-header-menu-->
<?php endif; ?>
