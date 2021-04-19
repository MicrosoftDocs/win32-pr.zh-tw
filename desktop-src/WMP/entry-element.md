---
title: ENTRY 元素
description: ENTRY 元素會指定要轉譯為剪輯的 Windows Media 檔案。
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- ENTRY 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984880"
---
# <a name="entry-element"></a><span data-ttu-id="08dd5-104">ENTRY 元素</span><span class="sxs-lookup"><span data-stu-id="08dd5-104">ENTRY Element</span></span>

<span data-ttu-id="08dd5-105">**ENTRY** 元素會指定要轉譯為剪輯的 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="08dd5-105">The **ENTRY** element specifies a Windows Media file to render as a clip.</span></span>

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a><span data-ttu-id="08dd5-106">屬性</span><span class="sxs-lookup"><span data-stu-id="08dd5-106">Attributes</span></span>

<span data-ttu-id="08dd5-107">**CLIENTSKIP**</span><span class="sxs-lookup"><span data-stu-id="08dd5-107">**CLIENTSKIP**</span></span>

<span data-ttu-id="08dd5-108">值，指出使用者是否可以向前跳過剪輯。</span><span class="sxs-lookup"><span data-stu-id="08dd5-108">Value indicating whether the user can skip forward past the clip.</span></span>

<span data-ttu-id="08dd5-109">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="08dd5-109">Possible values include the following.</span></span>



| <span data-ttu-id="08dd5-110">值</span><span class="sxs-lookup"><span data-stu-id="08dd5-110">Value</span></span> | <span data-ttu-id="08dd5-111">描述</span><span class="sxs-lookup"><span data-stu-id="08dd5-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="08dd5-112">YES</span><span class="sxs-lookup"><span data-stu-id="08dd5-112">YES</span></span>   | <span data-ttu-id="08dd5-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="08dd5-113">Default.</span></span> <span data-ttu-id="08dd5-114">使用者可以跳過剪輯之後的向前跳過。</span><span class="sxs-lookup"><span data-stu-id="08dd5-114">User can skip forward past the clip.</span></span> |
| <span data-ttu-id="08dd5-115">否</span><span class="sxs-lookup"><span data-stu-id="08dd5-115">NO</span></span>    | <span data-ttu-id="08dd5-116">使用者無法向前跳過剪輯。</span><span class="sxs-lookup"><span data-stu-id="08dd5-116">User cannot skip forward past the clip.</span></span>       |



 

<span data-ttu-id="08dd5-117">**SKIPIFREF**</span><span class="sxs-lookup"><span data-stu-id="08dd5-117">**SKIPIFREF**</span></span>

<span data-ttu-id="08dd5-118">值，指出當 **ENTRY 專案** 透過使用 **ENTRYREF** 元素包含在第二個中繼檔中時，Windows Media Player 是否應略過此剪輯。</span><span class="sxs-lookup"><span data-stu-id="08dd5-118">Value indicating whether Windows Media Player should skip this clip when the **ENTRY** element is included in a second metafile through the use of an **ENTRYREF** element.</span></span>

<span data-ttu-id="08dd5-119">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="08dd5-119">Possible values include the following.</span></span>



| <span data-ttu-id="08dd5-120">值</span><span class="sxs-lookup"><span data-stu-id="08dd5-120">Value</span></span> | <span data-ttu-id="08dd5-121">描述</span><span class="sxs-lookup"><span data-stu-id="08dd5-121">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="08dd5-122">YES</span><span class="sxs-lookup"><span data-stu-id="08dd5-122">YES</span></span>   | <span data-ttu-id="08dd5-123">如果透過 **ENTRYREF** 元素參考，Windows Media Player 將會忽略此專案。</span><span class="sxs-lookup"><span data-stu-id="08dd5-123">Windows Media Player will ignore this entry, if referenced through an **ENTRYREF** element.</span></span> |
| <span data-ttu-id="08dd5-124">否</span><span class="sxs-lookup"><span data-stu-id="08dd5-124">NO</span></span>    | <span data-ttu-id="08dd5-125">預設值。</span><span class="sxs-lookup"><span data-stu-id="08dd5-125">Default.</span></span> <span data-ttu-id="08dd5-126">Windows Media Player 不會忽略此專案。</span><span class="sxs-lookup"><span data-stu-id="08dd5-126">Windows Media Player will not ignore this entry.</span></span>                                   |



 

## <a name="parentchild-elements"></a><span data-ttu-id="08dd5-127">父/子項目</span><span class="sxs-lookup"><span data-stu-id="08dd5-127">Parent/Child Elements</span></span>



| <span data-ttu-id="08dd5-128">階層</span><span class="sxs-lookup"><span data-stu-id="08dd5-128">Hierarchy</span></span>       | <span data-ttu-id="08dd5-129">元素</span><span class="sxs-lookup"><span data-stu-id="08dd5-129">Elements</span></span>                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08dd5-130">父元素</span><span class="sxs-lookup"><span data-stu-id="08dd5-130">Parent elements</span></span> | <span data-ttu-id="08dd5-131">**ASX**、 **事件**、 **重複**</span><span class="sxs-lookup"><span data-stu-id="08dd5-131">**ASX**, **EVENT**, **REPEAT**</span></span>                                                                                                                                                               |
| <span data-ttu-id="08dd5-132">子元素</span><span class="sxs-lookup"><span data-stu-id="08dd5-132">Child elements</span></span>  | <span data-ttu-id="08dd5-133">**ABSTRACT**、 **AUTHOR**、 **橫幅**、 **BASE**、 **著作權**、 **DURATION**、 **ENDMARKER**、 **MOREINFO**、 **PARAM**、 **PREVIEWDURATION**、 **REF**、 **STARTMARKER**、 **STARTTIME**、 **TITLE**</span><span class="sxs-lookup"><span data-stu-id="08dd5-133">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **DURATION**, **ENDMARKER**, **MOREINFO**, **PARAM**, **PREVIEWDURATION**, **REF**, **STARTMARKER**, **STARTTIME**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="08dd5-134">備註</span><span class="sxs-lookup"><span data-stu-id="08dd5-134">Remarks</span></span>

<span data-ttu-id="08dd5-135">此元素是 Windows Media 中繼檔中的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="08dd5-135">This element is the fundamental construct in a Windows Media metafile.</span></span> <span data-ttu-id="08dd5-136">**ENTRY 專案** 和其相關聯的屬性會定義單一邏輯內容片段的中繼資訊，稱為「剪輯」。</span><span class="sxs-lookup"><span data-stu-id="08dd5-136">The **ENTRY** element and its associated attributes define meta-information for a single, logical piece of content, called a clip.</span></span> <span data-ttu-id="08dd5-137">**專案專案** 範圍內的子專案會定義 Windows Media Player 的媒體內容以開啟 (**REF**) 、Windows Media Player 會顯示為文字的剪輯相關資訊 (**作者**、**著作權**、**標題**) ，以及其他與剪輯相關的設定。</span><span class="sxs-lookup"><span data-stu-id="08dd5-137">Child elements within the scope of an **ENTRY** element define media content for Windows Media Player to open (**REF**), information about the clip that Windows Media Player will display as text (**AUTHOR**, **COPYRIGHT**, **TITLE**), and other settings related to the clip.</span></span> <span data-ttu-id="08dd5-138">**REF** 子項目會連結要針對父項目 **專案** 進行資料流程處理的內容。</span><span class="sxs-lookup"><span data-stu-id="08dd5-138">The **REF** child element links the content to be streamed for the parent **ENTRY** element.</span></span> <span data-ttu-id="08dd5-139">雖然腳本不會中斷，但在沒有 **REF** 子系的情況下，**專案** 沒有意義。</span><span class="sxs-lookup"><span data-stu-id="08dd5-139">Though the script will not break, the **ENTRY** is meaningless without a **REF** child.</span></span>

<span data-ttu-id="08dd5-140">如果 [ **CLIENTSKIP** ] 屬性的值為 [否]，使用者就無法向前跳過 **專案專案** 所定義的內容片段。</span><span class="sxs-lookup"><span data-stu-id="08dd5-140">If the value of the **CLIENTSKIP** attribute is NO, the user cannot skip forward past the piece of content defined by the **ENTRY** element.</span></span> <span data-ttu-id="08dd5-141">如果子系 **REF** 元素參考另一個中繼檔，則無法使用。</span><span class="sxs-lookup"><span data-stu-id="08dd5-141">This does not work if the child **REF** element references another metafile.</span></span> <span data-ttu-id="08dd5-142">應該使用 **ENTRYREF** 元素參考嵌套的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="08dd5-142">Nested metafiles should be referenced using the **ENTRYREF** element.</span></span>

<span data-ttu-id="08dd5-143">**SKIPIFREF** 屬性僅適用于透過使用 **ENTRYREF** 專案所包含在第二個中繼檔中的 **專案專案**。</span><span class="sxs-lookup"><span data-stu-id="08dd5-143">The **SKIPIFREF** attribute pertains only to **ENTRY** elements that are included in a second metafile through the use of an **ENTRYREF** element.</span></span> <span data-ttu-id="08dd5-144">**ENTRYREF** 元素會參考另一個中繼檔，以便在目前的檔案中包含邏輯。</span><span class="sxs-lookup"><span data-stu-id="08dd5-144">The **ENTRYREF** element references another metafile for logical inclusion in the current file.</span></span> <span data-ttu-id="08dd5-145">如果所參考之中繼檔中 **專案專案** 的 **SKIPIFREF** 屬性值為 YES，Windows Media Player 會忽略此提取專案，並移至下一個 **專案** 專案（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="08dd5-145">If the value of the **SKIPIFREF** attribute for an **ENTRY** element from the referenced metafile file is YES, Windows Media Player ignores this pulled-in entry, and moves on to the next **ENTRY** element, if any.</span></span> <span data-ttu-id="08dd5-146">下一個 **專案** 專案可以是原始檔案中的下一個專案，或是 **ENTRYREF** 元素所參考之中繼檔中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="08dd5-146">The next **ENTRY** element can be the next entry in the original file, or the next entry in the metafile referenced in the **ENTRYREF** element.</span></span>

## <a name="examples"></a><span data-ttu-id="08dd5-147">範例</span><span class="sxs-lookup"><span data-stu-id="08dd5-147">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="08dd5-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="08dd5-148">Requirements</span></span>



| <span data-ttu-id="08dd5-149">需求</span><span class="sxs-lookup"><span data-stu-id="08dd5-149">Requirement</span></span> | <span data-ttu-id="08dd5-150">值</span><span class="sxs-lookup"><span data-stu-id="08dd5-150">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="08dd5-151">版本</span><span class="sxs-lookup"><span data-stu-id="08dd5-151">Version</span></span><br/> | <span data-ttu-id="08dd5-152">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="08dd5-152">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08dd5-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08dd5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08dd5-154">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="08dd5-154">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="08dd5-155">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="08dd5-155">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





