# wordpress code



##Site URL 
---------------------***------------------
```php
<?php echo site_url(); ?>  
```
---------------------***------------------
```php
<?php echo do_shortcode('[image-carousel]'); ?>
```
---------------------***------------------
```php
if ( is_front_page() ) {	
	echo'<h2>Only Displays On The Front Page</h2>';
}
```
---------------------***------------------
```php
<?php if( have_rows('careers', 59) ): ?>
    <ul>
    <?php while( have_rows('careers', 59) ): the_row(); ?>
        <li><?php the_sub_field('careersimage'); ?></li>
    <?php endwhile; ?>
    </ul>
<?php endif; ?>
```
---------------------***------------------
```php
<?php
if( have_rows('careers') ):
    while ( have_rows('careers') ) : the_row();
    the_sub_field('careersimage');
    endwhile;
else :
  echo "No data";
endif;
?>
```
---------------------***------------------
```php
  <?php if( have_rows('transactions') ): ?>
    <?php while( have_rows('transactions') ): the_row(); ?>
         <div><img src="<?php  the_sub_field('transactionsimage'); ?>" alt="" /> </div>                      
    <?php endwhile; ?>
<?php endif; ?>
```
---------------------***------------------
