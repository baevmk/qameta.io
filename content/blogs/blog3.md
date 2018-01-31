+++
title = "Allure 2.0-BETA4 released"
date = "2017-02-06T12:00:00+03:00"
# Taxonomies
tags = ["allure","release"]
categories = ["blog"]
author = "baev"
+++


[download]: https://bintray.com/qameta/generic/allure2/2.0-BETA4
[milestone]: https://github.com/allure-framework/allure2/milestone/2?closed=1
[commits]: https://github.com/allure-framework/allure2/compare/2.0-BETA3...2.0-BETA4

It is my pleasure to announce that the Allure 2 beta release 4 is [available now][download].

Release contains several bug fixes (including command line for Darwin), 
some major changes (statuses), and visual improvements.

First of all, we got rid of `pending` status. A reason for that was that we 
realized it's usually hard to determine what is the difference between `cancelled` 
and `pending` statuses, so we decided to use `skipped` instead of both. 
Also Allure now has support of `unknown` status - this status means that something 
went wrong, and Allure can't determine real test's status. Though to be honest, 
you should never expect to see it in your report (at least in a perfect world).

Furthermore, this release introduces `flaky` tests. As for now, adapters don't 
support this feature yet, the only way to use it, marking a test case as `flaky`, 
is to add to test case a label `status_details` with a value `flaky`. 

![Flaky tests](/img/blog/allure-2.0-beta4/group-flaky.png)



Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam vel ante luctus, placerat leo sed, congue leo. Aliquam vel odio vulputate, ornare metus vel, tempor orci. Nam euismod turpis eget rhoncus ultrices. Vivamus tortor risus, eleifend in mollis in, tincidunt ut sapien. Cras cursus orci et nulla dignissim pulvinar. Pellentesque elementum nunc eros, vel lobortis arcu finibus sit amet. Pellentesque scelerisque, turpis eget finibus aliquet, neque neque suscipit diam, pretium semper turpis arcu non nibh. Ut risus mauris, lacinia ac elit non, posuere hendrerit urna. Duis ac condimentum lorem. Suspendisse feugiat cursus lorem, eu efficitur justo. Vestibulum augue magna, tempus eget tellus vitae, tincidunt mollis ex. Nullam suscipit auctor velit sed lacinia. Integer scelerisque lorem non mauris vestibulum elementum. Duis in hendrerit felis.

Nulla sit amet lorem quis ligula sodales sollicitudin at non eros. Nam imperdiet felis a metus condimentum, eget aliquam eros commodo. Phasellus posuere vel massa at tristique. Maecenas augue massa, blandit vitae bibendum quis, consequat eu felis. Praesent congue mollis odio vel fringilla. Nunc cursus ut magna sit amet pharetra. Proin pharetra, dui eget rutrum suscipit, odio augue iaculis enim, id tristique sapien odio at augue. Duis fringilla mi a nisi egestas, quis elementum lorem mollis. Nam venenatis felis ex, vitae mattis nisi sodales id. Nulla elit justo, accumsan non velit sit amet, commodo consectetur lacus. Nam in enim vulputate, congue lectus eget, malesuada turpis. Nam ut erat neque. Praesent maximus neque et metus vehicula, sed blandit eros maximus. Pellentesque vitae condimentum mi. Praesent et porta justo, sit amet semper urna.

Suspendisse quis enim quis leo viverra tristique quis a quam. In dapibus cursus luctus. Quisque laoreet ut lectus et posuere. Duis vitae sagittis nunc. Ut blandit, nulla eu euismod suscipit, leo mauris tempor est, in sodales massa diam vitae libero. Nulla ornare vel tortor non blandit. Sed bibendum posuere hendrerit.

Pellentesque suscipit varius nulla, non bibendum dolor lacinia et. Duis nec nisl sit amet libero malesuada lobortis. Morbi ac venenatis sapien, sed vestibulum mauris. Vestibulum vulputate eros a nisi finibus auctor. Vivamus id fermentum dolor, in bibendum augue. Curabitur eget placerat eros, vitae blandit augue. Proin laoreet odio eget placerat faucibus. Suspendisse potenti. Mauris elementum, dui eu rutrum hendrerit, nisl dolor bibendum ante, a ultrices velit orci vel velit. Curabitur tincidunt metus id ornare ullamcorper. Ut quis accumsan erat. Cras ullamcorper nulla lectus. Fusce congue porta ex, vel volutpat orci tristique ac. Aliquam at nibh nisl. Suspendisse tempus lorem non rutrum iaculis.

Nullam feugiat et nisi sit amet tristique. Mauris eu sem lacinia, semper risus nec, tincidunt sapien. Nullam scelerisque, mi mollis vestibulum tincidunt, velit augue finibus massa, eget convallis arcu neque nec libero. Vestibulum vel augue quis dolor euismod varius. Nunc sit amet cursus libero, ac aliquam erat. Nam quis enim elit. Aenean non porta felis. Sed malesuada, ante ut vehicula sagittis, tortor ex tempor quam, in placerat quam leo at ligula. Integer vestibulum volutpat augue in sagittis. Duis ut urna finibus, fringilla nibh in, cursus eros. Mauris sollicitudin neque et suscipit suscipit. Vestibulum ultrices finibus nunc, ut mattis erat pulvinar ut. Etiam laoreet finibus ornare. Integer maximus enim id arcu semper suscipit. 

Also time information is now shown for test groups (you can switch this off by clicking on the information icon)

![Test groups info](/img/blog/allure-2.0-beta4/group-info.png)

And finally, the ability to copy full name of test case to clipboard is back (flash free!)

![Copy to clipboard](/img/blog/allure-2.0-beta4/copy-to-clipboard.png)
<img width="90%" alt="Copy to clipboard" src="/img/blog/allure-2.0-beta4/copy-to-clipboard.png">

That is pretty much it. The full list of changes you can find in related [milestone][milestone] or [commits list][commits].

Regards,
Allure Team
