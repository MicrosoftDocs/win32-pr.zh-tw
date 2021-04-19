---
title: REF 元素
description: REF 元素會指定數位媒體內容的 URL。
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- REF 元素 Windows Media Player
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995280"
---
# <a name="ref-element"></a><span data-ttu-id="d1c30-104">REF 元素</span><span class="sxs-lookup"><span data-stu-id="d1c30-104">REF Element</span></span>

<span data-ttu-id="d1c30-105">**REF** 元素會指定數位媒體內容的 URL。</span><span class="sxs-lookup"><span data-stu-id="d1c30-105">The **REF** element specifies a URL for digital media content.</span></span>

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a><span data-ttu-id="d1c30-106">屬性</span><span class="sxs-lookup"><span data-stu-id="d1c30-106">Attributes</span></span>

<span data-ttu-id="d1c30-107">需要) **HREF** (</span><span class="sxs-lookup"><span data-stu-id="d1c30-107">**HREF** (required)</span></span>

<span data-ttu-id="d1c30-108">Windows Media Player 所支援的任何媒體內容的 URL。</span><span class="sxs-lookup"><span data-stu-id="d1c30-108">URL to any piece of media content supported by Windows Media Player.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d1c30-109">父/子項目</span><span class="sxs-lookup"><span data-stu-id="d1c30-109">Parent/Child Elements</span></span>



| <span data-ttu-id="d1c30-110">階層</span><span class="sxs-lookup"><span data-stu-id="d1c30-110">Hierarchy</span></span>       | <span data-ttu-id="d1c30-111">元素</span><span class="sxs-lookup"><span data-stu-id="d1c30-111">Elements</span></span>                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d1c30-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d1c30-112">Parent elements</span></span> | <span data-ttu-id="d1c30-113">**進入**</span><span class="sxs-lookup"><span data-stu-id="d1c30-113">**ENTRY**</span></span>                                                                        |
| <span data-ttu-id="d1c30-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d1c30-114">Child elements</span></span>  | <span data-ttu-id="d1c30-115">**DURATION**、 **ENDMARKER**、 **PREVIEWDURATION**、 **STARTMARKER**、 **STARTTIME**</span><span class="sxs-lookup"><span data-stu-id="d1c30-115">**DURATION**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d1c30-116">備註</span><span class="sxs-lookup"><span data-stu-id="d1c30-116">Remarks</span></span>

<span data-ttu-id="d1c30-117">這個元素會指定一段媒體內容的 URL。</span><span class="sxs-lookup"><span data-stu-id="d1c30-117">This element specifies a URL for a piece of media content.</span></span> <span data-ttu-id="d1c30-118">URL 可以使用 Windows Media Player 所支援的任何通訊協定，指向任何支援的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d1c30-118">The URL can point to any media type supported, using any protocol supported by Windows Media Player.</span></span>

<span data-ttu-id="d1c30-119">支援的媒體類型包括仍為 .gif 和 .jpg 影像的影像，以及副檔名為 .gif 的 Flash 檔案。</span><span class="sxs-lookup"><span data-stu-id="d1c30-119">The media types supported include still images such as .gif and .jpg images and Flash files with an .swf file name extension.</span></span> <span data-ttu-id="d1c30-120">這些媒體類型適用于將廣告內容包含在播放清單中。</span><span class="sxs-lookup"><span data-stu-id="d1c30-120">These media types are useful for including advertising content within a playlist.</span></span> <span data-ttu-id="d1c30-121">使用迴圈中播放的影像檔案和 Flash 檔案，您也必須在 **REF** 元素中包含 **DURATION** 元素，以指定顯示媒體專案的時間量。</span><span class="sxs-lookup"><span data-stu-id="d1c30-121">With image files and Flash files that play in a loop, you must also specify the amount of time to display the media item by including a **DURATION** element within the **REF** element.</span></span> <span data-ttu-id="d1c30-122">如果您想要在播放播放清單中的下一個專案時，繼續顯示影像，請在 **Entry 專案** 中包含 **PARAM** 元素、將其 **name** 屬性設定為 ShowWhileBuffering，然後將其 **value** 屬性設為 true。</span><span class="sxs-lookup"><span data-stu-id="d1c30-122">If you want an image to continue displaying while the next entry in the playlist is buffered, include a **PARAM** element within the **ENTRY** element, set its **name** attribute to ShowWhileBuffering, and set its **value** attribute to true.</span></span>

<span data-ttu-id="d1c30-123">若要參考 CD 或 DVD 上允許的內容，請提供 wmpcd 和 wmpdvd 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d1c30-123">To reference content on a CD or a DVD that allows it, the wmpcd and wmpdvd protocols are provided.</span></span> <span data-ttu-id="d1c30-124">例如，將 **HREF** 屬性設定為 "wmpdvd://f/5/3" 將會播放 dvd 上的第3章，但只有在已撰寫 dvd 才能允許時。</span><span class="sxs-lookup"><span data-stu-id="d1c30-124">For example, setting the **HREF** attribute to "wmpdvd://f/5/3" will play chapter 3 of title 5 on a DVD, but only if the DVD has been authored to allow it.</span></span>

<span data-ttu-id="d1c30-125">如果使用功能變數名稱伺服器 (DNS) 名稱（而非 IP 位址）指定位址，則開啟媒體專案時，從防火牆後方開啟數位媒體的應用程式將會有較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="d1c30-125">Applications that open digital media from behind a firewall will have better performance when opening the media items if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="d1c30-126">此元素最常見的用法是用於 URL 變換。</span><span class="sxs-lookup"><span data-stu-id="d1c30-126">The most common use of this element is for URL rollover.</span></span> <span data-ttu-id="d1c30-127">如果 Windows Media Player 無法開啟 **REF** 元素中定義的媒體片段，它會嘗試下一個 **REF** 元素中的 URL。</span><span class="sxs-lookup"><span data-stu-id="d1c30-127">If Windows Media Player is unable to open a piece of media defined in a **REF** element, it tries the URL in the next **REF** element.</span></span> <span data-ttu-id="d1c30-128">一旦 Windows Media Player 從一個 **專案專案** 範圍內定義的 URL 開啟媒體內容，它就會忽略該 **entry 專案** 內的後續 **REF** 標記。</span><span class="sxs-lookup"><span data-stu-id="d1c30-128">Once Windows Media Player opens media content from a URL defined within the scope of one **ENTRY** element, it ignores subsequent **REF** tags within that **ENTRY** element.</span></span> <span data-ttu-id="d1c30-129">內容完成播放之後，Windows Media Player 移至下一個 **專案專案** （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d1c30-129">After the piece of content is done playing, Windows Media Player moves on to the next **ENTRY** element, if any.</span></span>

-   <span data-ttu-id="d1c30-130">**重要** 一旦 Windows Media Player 建立與所參考內容片段的連接，它就會忽略該 **專案** 中的所有其他 **REF** 元素，不論連接是正常或異常地終止。</span><span class="sxs-lookup"><span data-stu-id="d1c30-130">**Important** Once Windows Media Player establishes a connection to a referenced piece of content, it ignores all other **REF** elements in that **ENTRY**, whether the connection terminates normally or abnormally.</span></span>

<span data-ttu-id="d1c30-131">如果參考的媒體專案是影像檔案，則必須使用 **DURATION** 元素來指定影像的顯示時間。</span><span class="sxs-lookup"><span data-stu-id="d1c30-131">If the media item referenced is an image file, the **DURATION** element must be used to specify the display time for the image.</span></span>

<span data-ttu-id="d1c30-132">**注意**</span><span class="sxs-lookup"><span data-stu-id="d1c30-132">**Note**</span></span>

<span data-ttu-id="d1c30-133">嘗試播放包含第一個框架音效的 Flash 媒體可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="d1c30-133">Attempting to play Flash media that includes sound with the first frame may yield unexpected results.</span></span> <span data-ttu-id="d1c30-134">您應該撰寫 Flash 內容，以在第二個畫面格開始時播放音效。</span><span class="sxs-lookup"><span data-stu-id="d1c30-134">You should author Flash content to play sound starting no earlier than the second frame.</span></span>

## <a name="examples"></a><span data-ttu-id="d1c30-135">範例</span><span class="sxs-lookup"><span data-stu-id="d1c30-135">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="d1c30-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1c30-136">Requirements</span></span>



| <span data-ttu-id="d1c30-137">需求</span><span class="sxs-lookup"><span data-stu-id="d1c30-137">Requirement</span></span> | <span data-ttu-id="d1c30-138">值</span><span class="sxs-lookup"><span data-stu-id="d1c30-138">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d1c30-139">版本</span><span class="sxs-lookup"><span data-stu-id="d1c30-139">Version</span></span><br/> | <span data-ttu-id="d1c30-140">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="d1c30-140">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1c30-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1c30-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c30-142">**支援的通訊協定和檔案類型**</span><span class="sxs-lookup"><span data-stu-id="d1c30-142">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> <dt>

[<span data-ttu-id="d1c30-143">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="d1c30-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d1c30-144">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="d1c30-144">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





