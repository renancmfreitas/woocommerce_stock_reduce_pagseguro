
/**
* Auto reduce WooCommerce order stock at checkout.
* Add to theme functions.php file
*/
 
add_action( 'woocommerce_thankyou', 'woocommerce_reduce_order_stock' );
function woocommerce_reduce_order_stock( $order_id ) {
    global $woocommerce;
 
    if ( !$order_id )
        return;
    $order = new WC_Order( $order_id );
    $order->reduce_order_stock();
}

add_filter( 'woocommerce_payment_complete_reduce_order_stock', '__return_false' );
