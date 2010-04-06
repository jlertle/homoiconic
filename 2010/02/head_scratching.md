Scratching my Head
===

    AdvancedOpenWater:~ raganwald$ irb
    irb(main):001:0> 1 <=> 2
    => -1
    irb(main):002:0> [1,2] <=> [1,2]
    => 0
    irb(main):003:0> [1,2] <=> [1,1]
    => 1
    irb(main):004:0> [1,2] <=> [2,1]
    => -1
    
So far so good, I think I understand how Ruby's Array class implements the "boat" operator. Which implies something about ordering arrays. Let's confirm my understanding:

    irb(main):005:0> [1,2] < [2,1]
    NoMethodError: undefined method `<' for [1, 2]:Array
            from (irb):5
            from :0
    
Ha! As [Pete Forde][peteforde] puts it, "Nothing about Ruby surprises me any more."

----
	
Follow [me](http://reginald.braythwayt.com) on [Twitter](http://twitter.com/raganwald) or [RSS](http://feeds.feedburner.com/raganwald "raganwald's rss feed"): <a href="http://feeds.feedburner.com/raganwald">.

[peteforde]: http://twitter.com/peteforde "Pete Fode on Twitter"