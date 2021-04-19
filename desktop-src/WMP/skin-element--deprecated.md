---
title: " (已淘汰的面板元素) "
description: 本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- 面板元素 (已淘汰的) Windows Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995363"
---
# <a name="skin-element-deprecated"></a><span data-ttu-id="83c27-104"> (已淘汰的面板元素) </span><span class="sxs-lookup"><span data-stu-id="83c27-104">SKIN Element (deprecated)</span></span>

<span data-ttu-id="83c27-105">本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="83c27-105">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="83c27-106">面板 **元素會** 指定框線的 URL。</span><span class="sxs-lookup"><span data-stu-id="83c27-106">The **SKIN** element specifies a URL to a border.</span></span>

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="83c27-107">屬性</span><span class="sxs-lookup"><span data-stu-id="83c27-107">Attributes</span></span>

<span data-ttu-id="83c27-108">需要) **HREF** (</span><span class="sxs-lookup"><span data-stu-id="83c27-108">**HREF** (required)</span></span>

<span data-ttu-id="83c27-109">副檔名為 wmz 之壓縮框線檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="83c27-109">URL for a compressed border file with a file name extension .wmz.</span></span> <span data-ttu-id="83c27-110">針對 Windows Media Player 9 系列或更新版本，此值只能參考使用者硬碟上與中繼檔播放清單相同的框線檔。</span><span class="sxs-lookup"><span data-stu-id="83c27-110">For Windows Media Player 9 Series or later, this value can reference only border files on the user's hard disk located in the same directory as the metafile playlist.</span></span> <span data-ttu-id="83c27-111">請參閱範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="83c27-111">See the example code.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="83c27-112">父/子項目</span><span class="sxs-lookup"><span data-stu-id="83c27-112">Parent/Child Elements</span></span>



| <span data-ttu-id="83c27-113">階層</span><span class="sxs-lookup"><span data-stu-id="83c27-113">Hierarchy</span></span>       | <span data-ttu-id="83c27-114">元素</span><span class="sxs-lookup"><span data-stu-id="83c27-114">Elements</span></span> |
|-----------------|----------|
| <span data-ttu-id="83c27-115">父元素</span><span class="sxs-lookup"><span data-stu-id="83c27-115">Parent elements</span></span> | <span data-ttu-id="83c27-116">**.ASX**</span><span class="sxs-lookup"><span data-stu-id="83c27-116">**ASX**</span></span>  |
| <span data-ttu-id="83c27-117">子元素</span><span class="sxs-lookup"><span data-stu-id="83c27-117">Child elements</span></span>  | <span data-ttu-id="83c27-118">無</span><span class="sxs-lookup"><span data-stu-id="83c27-118">None</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="83c27-119">備註</span><span class="sxs-lookup"><span data-stu-id="83c27-119">Remarks</span></span>

<span data-ttu-id="83c27-120">面板 **元素用** 來建立框線，類似于面板，但會顯示在完整模式 Windows Media Player 的 [ **立即播放** ] 區域中。</span><span class="sxs-lookup"><span data-stu-id="83c27-120">The **SKIN** element is used to create a border, which is similar to a skin but is displayed in the **Now Playing** area of the full mode Windows Media Player.</span></span> <span data-ttu-id="83c27-121">面板 **元素只** 適用于框線，這會出現在完整模式 Windows Media Player 中，而不適用於一般的面板，這會完全取代 Windows Media Player 的 compact 模式。</span><span class="sxs-lookup"><span data-stu-id="83c27-121">The **SKIN** element is used only for borders, which appear inside the full mode Windows Media Player, and not for regular skins, which entirely replace the compact mode Windows Media Player.</span></span>

<span data-ttu-id="83c27-122">在 Windows Media 下載套件 (副檔名為 wmd 的) 中， **面板元素可** 讓框線具有內容，並連結至其他網站。</span><span class="sxs-lookup"><span data-stu-id="83c27-122">In a Windows Media Download Package (with a .wmd file name extension), the **SKIN** element enables a border to have content and link to other sites.</span></span> <span data-ttu-id="83c27-123">Windows Media 下載套件是壓縮檔案，其中包含 border 檔案和 Windows Media 中繼檔。</span><span class="sxs-lookup"><span data-stu-id="83c27-123">The Windows Media Download Package is a compressed file that contains a border file and a Windows Media metafile.</span></span> <span data-ttu-id="83c27-124">副檔名為 wmz 的框線檔 () 會壓縮，並且包含具有 wms 副檔名) 的外觀 (定義檔。</span><span class="sxs-lookup"><span data-stu-id="83c27-124">The border file (with a .wmz file name extension) is compressed, and includes a skin definition file (with a .wms file name extension).</span></span>

<span data-ttu-id="83c27-125">**外觀** 元素有三個元件：</span><span class="sxs-lookup"><span data-stu-id="83c27-125">A **SKIN** element has three components:</span></span>

-   <span data-ttu-id="83c27-126">外觀</span><span class="sxs-lookup"><span data-stu-id="83c27-126">A skin</span></span>
-   <span data-ttu-id="83c27-127">部分內容</span><span class="sxs-lookup"><span data-stu-id="83c27-127">Some content</span></span>
-   <span data-ttu-id="83c27-128">中繼檔</span><span class="sxs-lookup"><span data-stu-id="83c27-128">A metafile</span></span>

<span data-ttu-id="83c27-129">Windows Media 下載套件中包含的面板必須是圖形中的矩形。</span><span class="sxs-lookup"><span data-stu-id="83c27-129">Skins included with Windows Media Download Packages must be rectangular in shape.</span></span> <span data-ttu-id="83c27-130">使用非矩形的外觀建立框線可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="83c27-130">Creating borders with skins that are not rectangular may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="83c27-131">範例</span><span class="sxs-lookup"><span data-stu-id="83c27-131">Examples</span></span>


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a><span data-ttu-id="83c27-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="83c27-132">Requirements</span></span>



| <span data-ttu-id="83c27-133">需求</span><span class="sxs-lookup"><span data-stu-id="83c27-133">Requirement</span></span> | <span data-ttu-id="83c27-134">值</span><span class="sxs-lookup"><span data-stu-id="83c27-134">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="83c27-135">版本</span><span class="sxs-lookup"><span data-stu-id="83c27-135">Version</span></span><br/> | <span data-ttu-id="83c27-136">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="83c27-136">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83c27-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83c27-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c27-138">**Windows Media Player (已淘汰) 的框線**</span><span class="sxs-lookup"><span data-stu-id="83c27-138">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="83c27-139">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="83c27-139">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="83c27-140">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="83c27-140">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





