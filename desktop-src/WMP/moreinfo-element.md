---
title: MOREINFO 元素
description: MOREINFO 元素會指定與顯示、剪輯或橫幅相關聯之網站、電子郵件地址或指令碼命令的 URL。
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- MOREINFO 元素 Windows Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983980"
---
# <a name="moreinfo-element"></a><span data-ttu-id="9e06c-104">MOREINFO 元素</span><span class="sxs-lookup"><span data-stu-id="9e06c-104">MOREINFO Element</span></span>

<span data-ttu-id="9e06c-105">**MOREINFO** 元素會指定與顯示、剪輯或橫幅相關聯之網站、電子郵件地址或指令碼命令的 URL。</span><span class="sxs-lookup"><span data-stu-id="9e06c-105">The **MOREINFO** element specifies a URL to a website, email address, or script command associated with a show, clip, or banner.</span></span>

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a><span data-ttu-id="9e06c-106">屬性</span><span class="sxs-lookup"><span data-stu-id="9e06c-106">Attributes</span></span>

<span data-ttu-id="9e06c-107">需要) **HREF** (</span><span class="sxs-lookup"><span data-stu-id="9e06c-107">**HREF** (required)</span></span>

<span data-ttu-id="9e06c-108">網站、電子郵件地址或指令碼命令的 URL。</span><span class="sxs-lookup"><span data-stu-id="9e06c-108">URL to a website, email address, or script command.</span></span>

<span data-ttu-id="9e06c-109">**目標**</span><span class="sxs-lookup"><span data-stu-id="9e06c-109">**TARGET**</span></span>

<span data-ttu-id="9e06c-110">值，定義瀏覽器將在其中開啟 **HREF** 屬性所定義之頁面的框架或視窗。</span><span class="sxs-lookup"><span data-stu-id="9e06c-110">Value defining the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span>

<span data-ttu-id="9e06c-111">這可以是包含視窗名稱的字串，或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9e06c-111">This can be a string containing a window name, or one of the following values.</span></span>



| <span data-ttu-id="9e06c-112">值</span><span class="sxs-lookup"><span data-stu-id="9e06c-112">Value</span></span>    | <span data-ttu-id="9e06c-113">描述</span><span class="sxs-lookup"><span data-stu-id="9e06c-113">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e06c-114">\_空白</span><span class="sxs-lookup"><span data-stu-id="9e06c-114">\_blank</span></span>  | <span data-ttu-id="9e06c-115">檔會在新的瀏覽器視窗中載入。</span><span class="sxs-lookup"><span data-stu-id="9e06c-115">The document loads in a new browser window.</span></span>                                                                              |
| <span data-ttu-id="9e06c-116">\_自我</span><span class="sxs-lookup"><span data-stu-id="9e06c-116">\_self</span></span>   | <span data-ttu-id="9e06c-117">檔載入的框架與包含 Windows Media Player 控制項的目前檔相同。</span><span class="sxs-lookup"><span data-stu-id="9e06c-117">The document loads in the same frame as the current document containing the Windows Media Player control.</span></span>                |
| <span data-ttu-id="9e06c-118">\_父母</span><span class="sxs-lookup"><span data-stu-id="9e06c-118">\_parent</span></span> | <span data-ttu-id="9e06c-119">檔會在目前框架的直屬父框架中載入，如果沒有父框架，則會載入目前的畫面格。</span><span class="sxs-lookup"><span data-stu-id="9e06c-119">The document loads in the immediate parent frame of the current frame, or the current frame if there is no parent frame.</span></span> |
| <span data-ttu-id="9e06c-120">\_top</span><span class="sxs-lookup"><span data-stu-id="9e06c-120">\_top</span></span>    | <span data-ttu-id="9e06c-121">檔會在完整的瀏覽器視窗中載入，取代所有其他的畫面格或檔。</span><span class="sxs-lookup"><span data-stu-id="9e06c-121">The document loads in the full browser window, replacing all other frames or documents.</span></span>                                  |



 

## <a name="parentchild-elements"></a><span data-ttu-id="9e06c-122">父/子項目</span><span class="sxs-lookup"><span data-stu-id="9e06c-122">Parent/Child Elements</span></span>



| <span data-ttu-id="9e06c-123">階層</span><span class="sxs-lookup"><span data-stu-id="9e06c-123">Hierarchy</span></span>       | <span data-ttu-id="9e06c-124">元素</span><span class="sxs-lookup"><span data-stu-id="9e06c-124">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="9e06c-125">父元素</span><span class="sxs-lookup"><span data-stu-id="9e06c-125">Parent elements</span></span> | <span data-ttu-id="9e06c-126">**ASX**、 **ENTRY**、 **橫幅**</span><span class="sxs-lookup"><span data-stu-id="9e06c-126">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="9e06c-127">子元素</span><span class="sxs-lookup"><span data-stu-id="9e06c-127">Child elements</span></span>  | <span data-ttu-id="9e06c-128">無</span><span class="sxs-lookup"><span data-stu-id="9e06c-128">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="9e06c-129">備註</span><span class="sxs-lookup"><span data-stu-id="9e06c-129">Remarks</span></span>

<span data-ttu-id="9e06c-130">這個元素會指定網站、電子郵件地址 **或指令碼命令的 URL。使用者可以按一下與 MOREINFO 元素相關聯的圖形或文字，以存取 URL 的目標** 。</span><span class="sxs-lookup"><span data-stu-id="9e06c-130">This element specifies a URL to a website, email address, **or script command. The user can access the target of the URL by clicking on the graphic or text associated with the MOREINFO** element.</span></span> <span data-ttu-id="9e06c-131">詳細資料取決於 **MOREINFO** 元素的父元素：</span><span class="sxs-lookup"><span data-stu-id="9e06c-131">The details depend on the parent element of the **MOREINFO** element:</span></span>

-   <span data-ttu-id="9e06c-132">如果 **MOREINFO** 專案是 **ASX** 元素的子系，則使用者可以按一下 [顯示標題] 來存取 URL。</span><span class="sxs-lookup"><span data-stu-id="9e06c-132">If the **MOREINFO** element is the child of an **ASX** element, the user can access the URL by clicking the show title.</span></span>
-   <span data-ttu-id="9e06c-133">如果 **MOREINFO** **專案是專案專案** 的子系，則使用者可以按一下剪輯標題來存取 URL。</span><span class="sxs-lookup"><span data-stu-id="9e06c-133">If the **MOREINFO** element is the child of an **ENTRY** element, the user can access the URL by clicking the clip title.</span></span>
-   <span data-ttu-id="9e06c-134">如果 **MOREINFO** 專案是 **橫幅** 元素的子系，則使用者可以按一下橫幅圖形來存取 URL。</span><span class="sxs-lookup"><span data-stu-id="9e06c-134">If the **MOREINFO** element is the child of a **BANNER** element, the user can access the URL by clicking the banner graphic.</span></span>

<span data-ttu-id="9e06c-135">如果 **HREF** 屬性指定網站的 url，瀏覽器會開啟並流覽至 url。</span><span class="sxs-lookup"><span data-stu-id="9e06c-135">If the **HREF** attribute specifies a URL to a website, the browser opens and navigates to the URL.</span></span> <span data-ttu-id="9e06c-136">如果 **HREF** 屬性指定了電子郵件地址，則會啟動使用者的電子郵件應用程式。</span><span class="sxs-lookup"><span data-stu-id="9e06c-136">If the **HREF** attribute specifies an email address, the user's email application starts.</span></span> <span data-ttu-id="9e06c-137">如果 **HREF** 屬性指定了指令碼命令，則指令碼命令會在瀏覽器中執行。</span><span class="sxs-lookup"><span data-stu-id="9e06c-137">If the **HREF** attribute specifies a script command, the script command executes in the browser.</span></span>

<span data-ttu-id="9e06c-138">**注意**</span><span class="sxs-lookup"><span data-stu-id="9e06c-138">**Note**</span></span>

<span data-ttu-id="9e06c-139">如果 **MOREINFO** 專案出現在 **Asx** 或 **ENTRY 專案** 中，則將滑鼠游標停留在 [ **asx** ] 元素的 [顯示 (的標題) 或針對 **專案**) 的 [剪輯 (]，就可以選取並使用 Windows Media Player 來存取 **HREF** 屬性中定義的 URL。</span><span class="sxs-lookup"><span data-stu-id="9e06c-139">If the **MOREINFO** element appears within an **ASX** or **ENTRY** element, when the mouse cursor is held over the title of the show (for an **ASX** element) or clip (for an **ENTRY** element), the URL defined in the **HREF** attribute can be selected and accessed by Windows Media Player.</span></span>

<span data-ttu-id="9e06c-140">**目標** 屬性會定義瀏覽器將在其中開啟 **HREF** 屬性所定義之頁面的框架或視窗。</span><span class="sxs-lookup"><span data-stu-id="9e06c-140">The **TARGET** attribute defines the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span> <span data-ttu-id="9e06c-141">這個屬性的值會遵循標準 HTML 語法和定義。</span><span class="sxs-lookup"><span data-stu-id="9e06c-141">The values for this attribute follow standard HTML syntax and definitions.</span></span> <span data-ttu-id="9e06c-142">在內嵌于網頁的控制項的案例中，如果未定義 **目標** 屬性，URL 會載入目前的瀏覽器視窗，並取代現有的頁面，這表示內容會停止播放。</span><span class="sxs-lookup"><span data-stu-id="9e06c-142">In the case of a control embedded in a webpage, if no **TARGET** attribute is defined, the URL loads the current browser window and replaces the existing page, which means the content stops playing.</span></span> <span data-ttu-id="9e06c-143">因此，建議您在網頁中內嵌 Windows Media Player 控制項時，一律指定 **目標** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9e06c-143">Therefore, it is recommended that you always specify a **TARGET** attribute when embedding the Windows Media Player control in a webpage.</span></span>

<span data-ttu-id="9e06c-144">如果中繼檔是在獨立 Windows Media Player 中開啟，則會忽略 **目標** 屬性，並在現有的瀏覽器視窗中載入 URL。</span><span class="sxs-lookup"><span data-stu-id="9e06c-144">If the metafile is opened in the stand-alone Windows Media Player, the **TARGET** attribute is ignored, and the URL loads in an existing browser window.</span></span> <span data-ttu-id="9e06c-145">如果目前沒有開啟瀏覽器視窗，則會在新的瀏覽器視窗中載入 URL。</span><span class="sxs-lookup"><span data-stu-id="9e06c-145">If there is no browser window currently open, the URL loads in a new browser window.</span></span>

## <a name="examples"></a><span data-ttu-id="9e06c-146">範例</span><span class="sxs-lookup"><span data-stu-id="9e06c-146">Examples</span></span>


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="9e06c-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e06c-147">Requirements</span></span>



| <span data-ttu-id="9e06c-148">需求</span><span class="sxs-lookup"><span data-stu-id="9e06c-148">Requirement</span></span> | <span data-ttu-id="9e06c-149">值</span><span class="sxs-lookup"><span data-stu-id="9e06c-149">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="9e06c-150">版本</span><span class="sxs-lookup"><span data-stu-id="9e06c-150">Version</span></span><br/> | <span data-ttu-id="9e06c-151">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="9e06c-151">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e06c-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e06c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e06c-153">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="9e06c-153">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="9e06c-154">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="9e06c-154">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





