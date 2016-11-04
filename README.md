# jailbreakerlestful
ps://getcomposer.org/installer | php
9
 * $ sudo mv composer.phar /usr/local/bin/composer
10
 *
11
 * Install Composer on Windows
12
 * https://getcomposer.org/
13
 *
14
 * Once you have setup composer, just run this in the folder where you will save the source files
15
 * composer require appshed/extension-api=~2.2
16
 *
17
 * Alternatively if you don't want to use, or cannot use, composer, download the api in a phar
18
 * https://raw.githubusercontent.com/AppShed/extension-api/master/build/appshed-api.phar
19
 * In this case just change the first line require to
20
 * require_once 'appshed-api.phar';
21
 */
22
require_once 'vendor/autoload.php';
23
class App882581
24
{
25
    /** @var App882581 $instance */
26
    protected static $instance;
27
    /** @var AppShed\Remote\Element\App $app */
28
    protected $app;
29
    public static function instance()
30
    {
31
        if (!static::$instance) {
32
            static::$instance = new static();
33
        }
34
        return static::$instance;
35
    }
36
    protected function getTab2662351()
37
    {
38
        $tab2662351 = new AppShed\Remote\Element\Tab('iDev ROBLOX ONLY!', new AppShed\Remote\Style\Image('https://d1yeqpqwjn2qg3.cloudfront.net/1f8cMPChthKg8oLgCcf2e_EYi18=/fit-in/60x60/http://appshed-id-images.s3-website-eu-west-1.amazonaws.com/1590418'));
39
        $tab2662351->setScreenLink('12111640', null, true);
40
        return $tab2662351;
41
    }
42
    protected function getTab2662352()
43
    {
44
        $tab2662352 = new AppShed\Remote\Element\Tab('Jailbreaker user!', new AppShed\Remote\Style\Image('https://d1yeqpqwjn2qg3.cloudfront.net/fg3tvhaselseaoRuZUNRZk4PJvo=/fit-in/60x60/http://appshed-id-images.s3-website-eu-west-1.amazonaws.com/5316004'));
45
        $tab2662352->setScreenLink('12111650', null, true);
46
        return $tab2662352;
47
    }
48
    public function get()
49
    {
50
        if (!$this->app) {
51
            $this->app = new AppShed\Remote\Element\App('Jailbreakerlestful');
52
            $this->app->setIcon(new AppShed\Remote\Style\Image('https://d1yeqpqwjn2qg3.cloudfront.net/l2QbovU8g5F3jwca4knT4CoQR8Q=/fit-in/156x156/http://appshed-id-images.s3-website-eu-west-1.amazonaws.com/5315902'));
53
            $this->app->setDescription('This is a Jailbreaker Plz download and rate 5 this is all versions
54
G+:RBLXKhoa Vu
55
ROBLOX:Khoavu679 
56
Facebook:Khoa Vu
57
Show us what you got and post or message');
58
            $this->app->setSplash(new AppShed\Remote\Style\Image('https://d1yeqpqwjn2qg3.cloudfront.net/PcQ2L2sk6-5Ww0xt2wOQKMB_nZA=/640x960/http://appshed-id-images.s3-website-eu-west-1.amazonaws.com/5315918'));
59
            $this->app->setDisableIos7(true);
60
            $this->app->addChild($this->getTab2662351());
61
            $this->app->addChild($this->getTab2662352());
62
        }
63
        return $this->app;
64
    }
65
}
66
if (AppShed\Remote\HTML\Remote::isOptionsRequest()) {
67
    AppShed\Remote\HTML\Remote::getCORSResponseHeaders();
68
}
69
$remote = new AppShed\Remote\HTML\Remote(App882581::instance()->get());
70
$remote->getResponse();
 
