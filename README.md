# How-detect-robots-and-spiders-with-PHP
How-detect-robots-and-spiders-with-PHP

Here is the simple function for detecting spiders and robots. It will return true or false.


function is_bot(){
    $bots = array(
        'Googlebot',
        'Baiduspider',
        'ia_archiver',
        'R6_FeedFetcher',
        'NetcraftSurveyAgent',
        'Sogou web spider',
        'bingbot',
        'Yahoo! Slurp',
        'facebookexternalhit',
        'PrintfulBot',
        'msnbot',
        'Twitterbot',
        'UnwindFetchor',
        'urlresolver',
        'Butterfly',
        'TweetmemeBot');
 
   foreach($bots as $b){
      if( stripos( $_SERVER['HTTP_USER_AGENT'], $b ) !== false ) return true;
   }
   return false;
}




