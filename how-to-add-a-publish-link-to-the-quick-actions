add_filter('post_row_actions', function ( $actions )
{
    global $post;

    // If the post hasn't been published yet
    if ( get_post_status($post) != 'publish' )
    {
        $nonce = wp_create_nonce('quick-publish-action');

        $link = get_admin_url('path to where') . "?id={$post->id}&amp;_wpnonce=$nonce";

        $actions['publish'] = "<a href=\"$link\">Publish</a>";
    }

    return $actions;
});
