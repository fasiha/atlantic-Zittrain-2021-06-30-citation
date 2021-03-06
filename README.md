This is a personal mirror, for citation and archival research purposes, of Jonathan Zittrain's "The Internet Is Rotting" published in [The Atlantic](https://www.theatlantic.com/technology/archive/2021/06/the-internet-is-a-collective-hallucination/619320/) on 2021-06-30.

Below are the steps I took to create this archive.

After copying the `article` tag from the Atlantic,
- `div.ArticleLeadArt_root__gi0oh`: I don't need article lead art but maybe I do?
- `div.ArticleUtilityBar_root__fMTYg`: I don't need this utility bar of share links
- don't need any `gpt-ad` alas: I have a subscription
- don't need any `p.ArticleRelatedContentLink_root__1Ukm-`: related content is an interesting meta-descriptor of the article but let's try not to be avant garde
- also deleting `div.ArticleRelatedContentModule_root__1MN9q`, for the same reason
- replace images' `src` with a local download (I used `curl -LO <URL>`)
  - for files hosted by Google, keep the same hash-like filename, but add an extension, so we have 2CUDyR8ziF3a3zgAsLJvs9wbNM6MTGJWaAiY3vNF4YtpGHqo_2Lf05OMF52afJi9fedLMRx7yEnWqPMHMJbj8FIAo5mvaLe4Z35YKyG3awoNM5DfPLKG83sZQN_u8NcDieE7cr8.png
  - for files hosted by the Atlantic CDN, which interestingly have URLs like `IMG_1324_200x300/original.png`, keep the `IMG_1324` snippet (that's that very common naming convention of cameras and phones)
  - the article lead art (mentioned above) has a different URL format. It does have a random-seeming alphanumeric string (`x0rTnEzjYCF0gUwecYjEfjv8OMY=`), but it doesn't base64-decode into anything so I'll just keep the "Untitled_10_1" in the URL 😅
- I love that a lot of URLs here are perma.cc URLs (though many others aren't)
- I deleted some empty `div`s
- Added `<meta charset="utf-8">` at the top (mainly for Safari's sake)