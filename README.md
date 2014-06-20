flat-hackernews
===============

Hides threaded conversations in Hacker News and gives a flat view.

How-to-use
----------

- Add this link to your bookmarks. 

javascript:{if(location.hostname%3D%3D%22news.ycombinator.com%22)%7Bvar%20spacerImages%3Ddocument.getElementsByTagName(%22img%22)%3Bvar%20comments%3DArray.prototype.slice.call(spacerImages).filter(function(e)%7Breturn%20e.src%3D%3D%22https%3A%2F%2Fnews.ycombinator.com%2Fs.gif%22%26%26e.width%2540%3D%3D0%26%26(e.height%3D%3D1%7C%7Ce.height%3D%3D2)%7D)%3Bcomments%3Dcomments.map(function(e)%7Breturn%7Bdepth%3Ae.width%2F40%2Crowele%3Ae.parentElement.parentElement.parentElement.parentElement.parentElement.parentElement%2Ctxt%3Ae.parentElement.parentElement.lastChild.children%5B2%5D%7D%7D)%3Bif(typeof%20__flathn__%3D%3D%22undefined%22)%7B__flathn__%3Dtrue%3Bfor(var%20i%3D0%3Bi%3Ccomments.length%3Bi%2B%2B)%7Bif(comments%5Bi%5D.depth%3E1)%7Bcomments%5Bi%5D.rowele.style.display%3D%22none%22%7Dif(comments%5Bi%5D.depth%3D%3D1)%7Bcomments%5Bi%5D.txt.style.fontSize%3D%220.7em%22%3Bcomments%5Bi%5D.txt.parentElement.children%5B0%5D.children%5B0%5D.style.fontSize%3D%220.75em%22%3Bif(comments%5Bi%5D.txt.lastChild.textContent%3D%3D%22reply%22)comments%5Bi%5D.txt.lastChild.style.display%3D%22none%22%3Bif(comments%5Bi%5D.txt.parentElement.lastChild.textContent%3D%3D%22reply%22)comments%5Bi%5D.txt.parentElement.lastChild.style.display%3D%22none%22%7D%7D%7Delse%7Bdelete%20__flathn__%3Bfor(var%20i%3D0%3Bi%3Ccomments.length%3Bi%2B%2B)%7Bcomments%5Bi%5D.rowele.style.display%3D%22%22%3Bcomments%5Bi%5D.txt.style.fontSize%3D%22%22%3Bcomments%5Bi%5D.txt.parentElement.children%5B0%5D.children%5B0%5D.style.fontSize%3D%22%22%3Bcomments%5Bi%5D.txt.lastChild.style.display%3D%22%22%3Bcomments%5Bi%5D.txt.parentElement.lastChild.style.display%3D%22%22%7D%7D%7Delse%7Balert(%22This%20works%20with%20only%20Hacker%20News.%20Open%20a%20discussion%20at%20news.ycombinator.com%20and%20try%20again.%22)%7D}void(0);

- Open a discussion at Hacker News and click on this bookmark. The injected JS will hide comments at depth > 1.
