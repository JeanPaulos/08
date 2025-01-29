<?php
/*
Plugin Name: Wasvoorschriften E-mail Bijlage
Description: Voegt een afbeelding toe aan WooCommerce bestelbevestigingse-mails.
Version: 1.0
Author: Jean Paul van der Meer
*/

if ( ! defined( 'ABSPATH' ) ) {
    exit; // Exit if accessed directly
}

add_action('woocommerce_email_attachments', 'add_custom_attachment_to_wc_emails', 10, 3);

function add_custom_attachment_to_wc_emails($attachments, $email_id, $order) {
    // Controleer of het de bestelling is die naar de klant wordt gestuurd
    if ($email_id === 'customer_processing_order' || $email_id === 'customer_completed_order') {
        // Voeg het pad naar je afbeelding toe
        $upload_dir = wp_upload_dir();
        $attachments[] = $upload_dir['basedir'] . '/wassen/wasvoorschriften.jpg'; // vervang dit met het juiste pad naar je afbeelding
    }

    return $attachments;
}
