---
title: 橫幅元素
description: 橫幅元素會定義要出現在顯示面板中之圖形檔案的 URL。
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- 橫幅元素 Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978440"
---
# <a name="banner-element"></a><span data-ttu-id="db3ad-104">橫幅元素</span><span class="sxs-lookup"><span data-stu-id="db3ad-104">BANNER Element</span></span>

<span data-ttu-id="db3ad-105">**橫幅** 元素會定義要出現在顯示面板中之圖形檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="db3ad-105">The **BANNER** element defines a URL to a graphic file that will appear in the display panel.</span></span>

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a><span data-ttu-id="db3ad-106">屬性</span><span class="sxs-lookup"><span data-stu-id="db3ad-106">Attributes</span></span>

<span data-ttu-id="db3ad-107">需要) **HREF** (</span><span class="sxs-lookup"><span data-stu-id="db3ad-107">**HREF** (required)</span></span>

<span data-ttu-id="db3ad-108">顯示面板中顯示之圖形檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="db3ad-108">URL to a graphic file that is displayed in the display panel.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="db3ad-109">父/子項目</span><span class="sxs-lookup"><span data-stu-id="db3ad-109">Parent/Child Elements</span></span>



| <span data-ttu-id="db3ad-110">階層</span><span class="sxs-lookup"><span data-stu-id="db3ad-110">Hierarchy</span></span>       | <span data-ttu-id="db3ad-111">元素</span><span class="sxs-lookup"><span data-stu-id="db3ad-111">Elements</span></span>                   |
|-----------------|----------------------------|
| <span data-ttu-id="db3ad-112">父元素</span><span class="sxs-lookup"><span data-stu-id="db3ad-112">Parent elements</span></span> | <span data-ttu-id="db3ad-113">**ASX**， **進入**</span><span class="sxs-lookup"><span data-stu-id="db3ad-113">**ASX**, **ENTRY**</span></span>         |
| <span data-ttu-id="db3ad-114">子元素</span><span class="sxs-lookup"><span data-stu-id="db3ad-114">Child elements</span></span>  | <span data-ttu-id="db3ad-115">**ABSTRACT**、 **MOREINFO**</span><span class="sxs-lookup"><span data-stu-id="db3ad-115">**ABSTRACT**, **MOREINFO**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="db3ad-116">備註</span><span class="sxs-lookup"><span data-stu-id="db3ad-116">Remarks</span></span>

<span data-ttu-id="db3ad-117">此元素會定義顯示在影片內容下方 Windows Media Player 顯示面板中的圖形檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="db3ad-117">This element defines a URL to a graphic file that appears in the Windows Media Player display panel, beneath the video content.</span></span> <span data-ttu-id="db3ad-118">如果媒體只是音訊，則會顯示橫幅圖形。</span><span class="sxs-lookup"><span data-stu-id="db3ad-118">If the media is audio only, the banner graphic is displayed by itself.</span></span> <span data-ttu-id="db3ad-119">Windows Media Player 會在圖形的橫幅橫條圖) 中保留空間32圖元高、194圖元寬 (。</span><span class="sxs-lookup"><span data-stu-id="db3ad-119">Windows Media Player reserves a space 32 pixels high by 194 pixels wide (the banner bar) for the graphic.</span></span> <span data-ttu-id="db3ad-120">如果在 URL 中定義的圖形小於該圖形，則會顯示其原始大小。</span><span class="sxs-lookup"><span data-stu-id="db3ad-120">If the graphic defined in the URL is smaller than that, it displays at its original size.</span></span> <span data-ttu-id="db3ad-121">如果圖形大於保留空間，Windows Media Player 將會裁剪影像以符合空間。</span><span class="sxs-lookup"><span data-stu-id="db3ad-121">If the graphic is larger than the reserved space, Windows Media Player will crop the image to fit the space.</span></span>

<span data-ttu-id="db3ad-122">您可以使用 **橫幅** 元素範圍內的 **抽象** 專案，在使用者將滑鼠指標暫停在橫幅圖形上時，將文字顯示為工具提示。</span><span class="sxs-lookup"><span data-stu-id="db3ad-122">You can use an **ABSTRACT** element within the scope of the **BANNER** element to display text as a ToolTip when the user pauses the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="db3ad-123">**橫幅** 元素內的 **MOREINFO** 專案會定義使用者按一下橫幅圖形時，使用者所使用的 URL。</span><span class="sxs-lookup"><span data-stu-id="db3ad-123">A **MOREINFO** element within a **BANNER** element defines a URL to which the user is taken when the user clicks the banner graphic.</span></span> <span data-ttu-id="db3ad-124"> (URL 可以是任何路徑或通訊協定，例如電子郵件連結、超文字傳輸通訊協定 (網站的 HTTP) URL，甚至是 Microsoft JScript 命令 ) 。當指標移到圖形上時，圖形會變成浮凸效果，並看起來像按鈕。</span><span class="sxs-lookup"><span data-stu-id="db3ad-124">(The URL can be any path or protocol, such as an email link, a Hypertext Transfer Protocol (HTTP) URL to a website, or even a Microsoft JScript command.) When the pointer is moved over the graphic, the graphic becomes embossed and looks like a button.</span></span>

<span data-ttu-id="db3ad-125">當播放清單中的所有剪輯都在播放時，會顯示為 **ASX** 元素定義的 **橫幅** 元素。</span><span class="sxs-lookup"><span data-stu-id="db3ad-125">A **BANNER** element defined for an **ASX** element displays while all clips in the playlist are playing.</span></span> <span data-ttu-id="db3ad-126">在 **專案專案** 中定義的 **橫幅** 元素只會在播放剪輯時顯示，而在這段期間，會覆寫父 **ASX** 元素內定義的任何橫幅。</span><span class="sxs-lookup"><span data-stu-id="db3ad-126">A **BANNER** element defined in an **ENTRY** element displays only while that clip is playing, and during that time overrides any banner defined within the parent **ASX** element.</span></span> <span data-ttu-id="db3ad-127">您可以藉由設定 **ASX** 專案的 **BANNERBAR** 屬性，來指定 Windows Media Player 如何保留橫幅的空間。</span><span class="sxs-lookup"><span data-stu-id="db3ad-127">You can specify how Windows Media Player reserves space for the banner by setting the **BANNERBAR** attribute of the **ASX** element.</span></span>

<span data-ttu-id="db3ad-128">使用 DRM 檔案時，或在網頁中內嵌 Windows Media Player 時，不支援橫幅影像。</span><span class="sxs-lookup"><span data-stu-id="db3ad-128">Banner images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

## <a name="examples"></a><span data-ttu-id="db3ad-129">範例</span><span class="sxs-lookup"><span data-stu-id="db3ad-129">Examples</span></span>

<span data-ttu-id="db3ad-130">以下是沒有子項目的 **橫幅** 元素範例：</span><span class="sxs-lookup"><span data-stu-id="db3ad-130">The following is an example of a **BANNER** element without child elements:</span></span>


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



<span data-ttu-id="db3ad-131">以下是包含 **抽象** 和 **MOREINFO** 專案的 **橫幅** 元素範例。</span><span class="sxs-lookup"><span data-stu-id="db3ad-131">The following is an example of a **BANNER** element containing **ABSTRACT** and **MOREINFO** elements.</span></span>


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a><span data-ttu-id="db3ad-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="db3ad-132">Requirements</span></span>



| <span data-ttu-id="db3ad-133">需求</span><span class="sxs-lookup"><span data-stu-id="db3ad-133">Requirement</span></span> | <span data-ttu-id="db3ad-134">值</span><span class="sxs-lookup"><span data-stu-id="db3ad-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="db3ad-135">版本</span><span class="sxs-lookup"><span data-stu-id="db3ad-135">Version</span></span><br/> | <span data-ttu-id="db3ad-136">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="db3ad-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db3ad-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db3ad-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3ad-138">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="db3ad-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="db3ad-139">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="db3ad-139">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





