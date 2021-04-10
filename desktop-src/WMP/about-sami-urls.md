---
title: 關於薩米文的 Url
description: 關於薩米文的 Url
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- 'Windows Media Player，可同步的可存取媒體交換 (薩米文) '
- 'Windows Media Player 物件模型、已同步處理的可存取媒體交換 (薩米文) '
- '物件模型、同步的可存取媒體交換 (薩米) '
- 'Windows Media Player 行動裝置、已同步處理的可存取媒體交換 (薩米文) '
- 'Windows Media Player ActiveX 控制項、同步存取媒體交換 (薩米文) '
- 'Windows Media Player 的行動 ActiveX 控制項、已同步處理的可存取媒體交換 (薩米文) '
- 'ActiveX 控制項、同步的可存取媒體交換 (薩米) '
- 已同步處理的可存取媒體交換 (薩米) ，檔案
- 薩米文 (同步處理的可存取媒體交換) 、檔案
- 已同步的可存取媒體交換 (薩米) 、Url
- 薩米文 (同步處理的可存取媒體交換) 、Url
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183321"
---
# <a name="about-sami-urls"></a><span data-ttu-id="ac357-114">關於薩米文的 Url</span><span class="sxs-lookup"><span data-stu-id="ac357-114">About SAMI URLs</span></span>

<span data-ttu-id="ac357-115">您可以使用單一 URL，將薩米文的檔案與數位媒體檔案相關聯。</span><span class="sxs-lookup"><span data-stu-id="ac357-115">SAMI files can be associated with digital media files by using a single URL.</span></span> <span data-ttu-id="ac357-116">這是使用 *薩米* 文 URL 參數來完成的。</span><span class="sxs-lookup"><span data-stu-id="ac357-116">This is accomplished by using *the sami* URL parameter.</span></span> <span data-ttu-id="ac357-117">URL 參數的前面會有基底 URL 和？</span><span class="sxs-lookup"><span data-stu-id="ac357-117">The URL parameter is preceded by the base URL and a ?</span></span> <span data-ttu-id="ac357-118">字元之後。</span><span class="sxs-lookup"><span data-stu-id="ac357-118">character.</span></span> <span data-ttu-id="ac357-119">具有 *薩米* 參數的 URL 會遵循此語法：</span><span class="sxs-lookup"><span data-stu-id="ac357-119">A URL with a *sami* parameter follows this syntax:</span></span>

<span data-ttu-id="ac357-120">*URL*？*薩米* = 文 *captionsURL*。</span><span class="sxs-lookup"><span data-stu-id="ac357-120">*URL*?*sami*=*captionsURL*.</span></span>

<span data-ttu-id="ac357-121">URL 參數的值會在參數名稱和等號後面，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="ac357-121">The value of the URL parameter follows the parameter name and an equals sign, as in the following example:</span></span>


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



<span data-ttu-id="ac357-122">此 URL 語法常用於超連結或 Windows Media 中繼檔，以直接連結至數位媒體檔案和薩米文檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="ac357-122">This URL syntax is commonly used in a hyperlink or a Windows Media metafile to link directly to the locations of both the digital media file and the SAMI file.</span></span> <span data-ttu-id="ac357-123">當使用者按一下超連結時，Windows Media Player 會以完整模式啟動，並播放數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="ac357-123">When the user clicks on the hyperlink, Windows Media Player launches in full mode and plays the digital media content.</span></span>

<span data-ttu-id="ac357-124">如果未指定 *薩米* URL 參數，Windows Media Player 將會尋找與數位媒體檔案位於相同位置的薩米文檔案，而且檔案名除外（副檔名必須是 smi-s）也會有相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac357-124">If the *sami* URL parameter is not specified, Windows Media Player will look for a SAMI file that is in the same location as the digital media file and that has the same file name except for the file name extension, which must be .smi.</span></span> <span data-ttu-id="ac357-125">如果有這類檔案存在，則會在播放程式中啟用標題顯示時自動開啟。</span><span class="sxs-lookup"><span data-stu-id="ac357-125">If such a file is present, it will be opened automatically if caption display has been enabled in the Player.</span></span>

<span data-ttu-id="ac357-126">按一下 [ **播放** ] 功能表，然後按一下 [ **標題] 和 [副標題**]，再按一下 [ **開啟**]，即可在 Windows Media Player 中啟用隱藏式輔助字幕。</span><span class="sxs-lookup"><span data-stu-id="ac357-126">Closed captions are enabled in Windows Media Player by clicking the **Play** menu, then clicking **Captions and Subtitles**, and then clicking **On**.</span></span> <span data-ttu-id="ac357-127">如果啟用了隱藏式輔助字幕，當媒體專案播放時，會顯示包含在薩米文檔案中的標題。</span><span class="sxs-lookup"><span data-stu-id="ac357-127">If closed captions are enabled, the captions contained in the SAMI file will display while the media item plays.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac357-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac357-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac357-129">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="ac357-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




