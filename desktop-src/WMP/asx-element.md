---
title: ASX 元素
description: ASX 元素會將檔案定義為中繼檔。
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- ASX 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983155"
---
# <a name="asx-element"></a><span data-ttu-id="6ab43-104">ASX 元素</span><span class="sxs-lookup"><span data-stu-id="6ab43-104">ASX Element</span></span>

<span data-ttu-id="6ab43-105">**ASX** 元素會將檔案定義為中繼檔。</span><span class="sxs-lookup"><span data-stu-id="6ab43-105">The **ASX** element defines a file as a metafile.</span></span>

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a><span data-ttu-id="6ab43-106">屬性</span><span class="sxs-lookup"><span data-stu-id="6ab43-106">Attributes</span></span>

<span data-ttu-id="6ab43-107">`VERSION` (必要)</span><span class="sxs-lookup"><span data-stu-id="6ab43-107">`VERSION` (required)</span></span>

<span data-ttu-id="6ab43-108">十進位數，代表中繼檔的語法版本號碼。</span><span class="sxs-lookup"><span data-stu-id="6ab43-108">Decimal number representing the version number of the syntax for the metafile.</span></span> <span data-ttu-id="6ab43-109">設定為3或3.0。</span><span class="sxs-lookup"><span data-stu-id="6ab43-109">Set to 3 or 3.0.</span></span>

<span data-ttu-id="6ab43-110">**PREVIEWMODE** (選用) </span><span class="sxs-lookup"><span data-stu-id="6ab43-110">**PREVIEWMODE** (optional)</span></span>

<span data-ttu-id="6ab43-111">值，指出在播放第一個剪輯之前 Windows Media Player 是否進入預覽模式。</span><span class="sxs-lookup"><span data-stu-id="6ab43-111">Value indicating whether Windows Media Player enters preview mode before playing the first clip.</span></span>

<span data-ttu-id="6ab43-112">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6ab43-112">Must be one of the following values.</span></span>



| <span data-ttu-id="6ab43-113">值</span><span class="sxs-lookup"><span data-stu-id="6ab43-113">Value</span></span> | <span data-ttu-id="6ab43-114">描述</span><span class="sxs-lookup"><span data-stu-id="6ab43-114">Description</span></span>                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab43-115">YES</span><span class="sxs-lookup"><span data-stu-id="6ab43-115">YES</span></span>   | <span data-ttu-id="6ab43-116">Windows Media Player 在播放第一個剪輯之前進入預覽模式。</span><span class="sxs-lookup"><span data-stu-id="6ab43-116">Windows Media Player enters preview mode before playing the first clip.</span></span>                            |
| <span data-ttu-id="6ab43-117">否</span><span class="sxs-lookup"><span data-stu-id="6ab43-117">NO</span></span>    | <span data-ttu-id="6ab43-118">預設值。</span><span class="sxs-lookup"><span data-stu-id="6ab43-118">The default value.</span></span> <span data-ttu-id="6ab43-119">在播放第一個剪輯之前，Windows Media Player 不會進入預覽模式。</span><span class="sxs-lookup"><span data-stu-id="6ab43-119">Windows Media Player does not enter preview mode before playing the first clip.</span></span> |



 

<span data-ttu-id="6ab43-120">**BANNERBAR** (選用) </span><span class="sxs-lookup"><span data-stu-id="6ab43-120">**BANNERBAR** (optional)</span></span>

<span data-ttu-id="6ab43-121">值，指出 Windows Media Player 是否保留橫幅圖形的空間。</span><span class="sxs-lookup"><span data-stu-id="6ab43-121">Value indicating whether Windows Media Player reserves space for a banner graphic.</span></span>

<span data-ttu-id="6ab43-122">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6ab43-122">Must be one of the following values.</span></span>



| <span data-ttu-id="6ab43-123">值</span><span class="sxs-lookup"><span data-stu-id="6ab43-123">Value</span></span> | <span data-ttu-id="6ab43-124">描述</span><span class="sxs-lookup"><span data-stu-id="6ab43-124">Description</span></span>                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab43-125">AUTO</span><span class="sxs-lookup"><span data-stu-id="6ab43-125">AUTO</span></span>  | <span data-ttu-id="6ab43-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="6ab43-126">The default value.</span></span> <span data-ttu-id="6ab43-127">Windows Media Player 只有在內容包含一段內容時，才會保留橫幅列的空間。</span><span class="sxs-lookup"><span data-stu-id="6ab43-127">Windows Media Player reserves space for the banner bar only when a piece of content includes one.</span></span>                       |
| <span data-ttu-id="6ab43-128">FIXED</span><span class="sxs-lookup"><span data-stu-id="6ab43-128">FIXED</span></span> | <span data-ttu-id="6ab43-129">Windows Media Player 會針對每個播放的內容保留一個固定的空間，而不論是否有相關聯的橫幅。</span><span class="sxs-lookup"><span data-stu-id="6ab43-129">Windows Media Player reserves a fixed space for a banner graphic for every piece of content played, whether there is an associated banner.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="6ab43-130">父/子項目</span><span class="sxs-lookup"><span data-stu-id="6ab43-130">Parent/Child Elements</span></span>



| <span data-ttu-id="6ab43-131">階層</span><span class="sxs-lookup"><span data-stu-id="6ab43-131">Hierarchy</span></span>       | <span data-ttu-id="6ab43-132">元素</span><span class="sxs-lookup"><span data-stu-id="6ab43-132">Elements</span></span>                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab43-133">父元素</span><span class="sxs-lookup"><span data-stu-id="6ab43-133">Parent elements</span></span> | <span data-ttu-id="6ab43-134">無。</span><span class="sxs-lookup"><span data-stu-id="6ab43-134">None.</span></span> <span data-ttu-id="6ab43-135">**ASX** 元素必須是每個中繼檔中的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="6ab43-135">The **ASX** element must be the first element in every metafile.</span></span>                                                                                                 |
| <span data-ttu-id="6ab43-136">子元素</span><span class="sxs-lookup"><span data-stu-id="6ab43-136">Child elements</span></span>  | <span data-ttu-id="6ab43-137">**ABSTRACT**、 **AUTHOR**、 **橫幅**、 **BASE**、 **著作權**、 **ENTRY**、 **ENTRYREF**、 **EVENT**、 **MOREINFO**、 **PREVIEWDURATION**、 **PARAM**、 **REPEAT**、 **TITLE**</span><span class="sxs-lookup"><span data-stu-id="6ab43-137">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **ENTRY**, **ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6ab43-138">備註</span><span class="sxs-lookup"><span data-stu-id="6ab43-138">Remarks</span></span>

<span data-ttu-id="6ab43-139">中繼檔播放清單的前四個字元必須是 "<ASX"。</span><span class="sxs-lookup"><span data-stu-id="6ab43-139">The first four characters of a metafile playlist must be "<ASX".</span></span> <span data-ttu-id="6ab43-140">在 **ASX** 元素範圍內定義的其他元素（例如 **標題** 和 **作者**）會與 Windows Media Player 所顯示的顯示資訊相關聯。</span><span class="sxs-lookup"><span data-stu-id="6ab43-140">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the show information displayed by Windows Media Player.</span></span>

<span data-ttu-id="6ab43-141">針對 Windows Media Player，語法版本號碼為3.0。</span><span class="sxs-lookup"><span data-stu-id="6ab43-141">For Windows Media Player, the syntax version number is 3.0.</span></span> <span data-ttu-id="6ab43-142">Windows Media Player 支援所有舊版的中繼檔語法。</span><span class="sxs-lookup"><span data-stu-id="6ab43-142">Windows Media Player supports all previous versions of metafile syntax.</span></span> <span data-ttu-id="6ab43-143">**VERSION** 屬性可接受的值包括3.0 和 3 (，但) 不含小數點。</span><span class="sxs-lookup"><span data-stu-id="6ab43-143">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="6ab43-144">如果 **PREVIEWMODE** 屬性的值為 YES，Windows Media Player 在播放第一個剪輯之前立即進入預覽模式。</span><span class="sxs-lookup"><span data-stu-id="6ab43-144">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player immediately enters preview mode before playing the first clip.</span></span> <span data-ttu-id="6ab43-145">當 Windows Media Player 進入預覽模式時，它會預覽中繼檔中所參考的每個剪輯。</span><span class="sxs-lookup"><span data-stu-id="6ab43-145">When Windows Media Player enters preview mode, it previews each clip referenced in the metafile.</span></span> <span data-ttu-id="6ab43-146">**PREVIEWDURATION** 元素決定每個預覽的持續時間。</span><span class="sxs-lookup"><span data-stu-id="6ab43-146">The **PREVIEWDURATION** element determines the duration of each preview.</span></span>

<span data-ttu-id="6ab43-147">**BANNERBAR** 屬性會定義 Windows Media Player 是否保留橫幅圖形的空間。</span><span class="sxs-lookup"><span data-stu-id="6ab43-147">The **BANNERBAR** attribute defines whether Windows Media Player reserves space for a banner graphic.</span></span> <span data-ttu-id="6ab43-148">橫幅是媒體內容播放時，顯示在影片顯示區域中的圖形。</span><span class="sxs-lookup"><span data-stu-id="6ab43-148">A banner is a graphic that is displayed in the video display area while media content is playing.</span></span> <span data-ttu-id="6ab43-149"> (使用 **橫幅** 專案將橫幅新增至內容。 ) 如果 **BANNERBAR** 的值是固定的，Windows Media Player 會針對媒體內容的每個部分保留橫幅空間，不論媒體內容是否有橫幅。</span><span class="sxs-lookup"><span data-stu-id="6ab43-149">(Use the **BANNER** element to add a banner to the content.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for every piece of media content, whether the media content has a banner.</span></span> <span data-ttu-id="6ab43-150">如果媒體內容沒有相關聯的橫幅，保留給一個的空間會是黑色。</span><span class="sxs-lookup"><span data-stu-id="6ab43-150">If a piece of media content does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="6ab43-151">如果 [ **BANNERBAR** ] 屬性的值為 [自動]，Windows Media Player 只有當媒體內容包含時，才會保留橫幅的空間。</span><span class="sxs-lookup"><span data-stu-id="6ab43-151">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the media content includes one.</span></span>

<span data-ttu-id="6ab43-152">如果您建立具有多個剪輯的中繼檔 (專案或 **ENTRYREF** **專案**) ，並將 [ **BANNERBAR** ] 屬性的值設定為 [自動]，Windows Media Player 可能會調整大小以允許一個剪輯的橫幅圖形出現空間，然後在下一個剪輯未包含橫幅圖形時再調整大小。</span><span class="sxs-lookup"><span data-stu-id="6ab43-152">If you create a metafile with multiple clips (**ENTRY** or **ENTRYREF** elements) and set the value of the **BANNERBAR** attribute to AUTO, Windows Media Player might resize to allow space for a banner graphic for one clip, and then resize again if the next clip does not contain a banner graphic.</span></span> <span data-ttu-id="6ab43-153">如果您想要讓視窗的大小維持相同的 (但) 的影片大小變更時，請使用 **BANNERBAR** 屬性的固定值。</span><span class="sxs-lookup"><span data-stu-id="6ab43-153">If you want the size of the window to stay the same (except when the video size changes), use the FIXED value for the **BANNERBAR** attribute.</span></span>

<span data-ttu-id="6ab43-154">針對橫幅圖形所保留的空間為32圖元高、194圖元寬。</span><span class="sxs-lookup"><span data-stu-id="6ab43-154">The space reserved for a banner graphic is 32 pixels high by 194 pixels wide.</span></span> <span data-ttu-id="6ab43-155">保留的空間會出現在影片區域下方任何轉譯的影片內容和6圖元上方，讓6圖元的視頻區域框線具有空格。</span><span class="sxs-lookup"><span data-stu-id="6ab43-155">The reserved space appears below any rendered video content and 6 pixels above the lower edge of the video area, allowing space for the 6-pixel video area border.</span></span> <span data-ttu-id="6ab43-156">保留的橫幅空間會以水準方式置中。</span><span class="sxs-lookup"><span data-stu-id="6ab43-156">The reserved banner space is centered horizontally.</span></span>

<span data-ttu-id="6ab43-157">Windows Media Player 會以橫幅空間最左邊的圖元開始呈現圖形。</span><span class="sxs-lookup"><span data-stu-id="6ab43-157">Windows Media Player renders the graphic beginning in the leftmost pixel of the banner space.</span></span> <span data-ttu-id="6ab43-158">如果圖形填滿整個空間，則會以水準方式顯示。</span><span class="sxs-lookup"><span data-stu-id="6ab43-158">If the graphic fills the entire space, it will appear centered horizontally.</span></span> <span data-ttu-id="6ab43-159">否則將會有尾端的空格。</span><span class="sxs-lookup"><span data-stu-id="6ab43-159">Otherwise there will be trailing space.</span></span> <span data-ttu-id="6ab43-160">請注意，不論 **BANNERBAR** 屬性的值為何，Windows Media Player 的最小寬度一律會比影片剪輯的大小更寬。</span><span class="sxs-lookup"><span data-stu-id="6ab43-160">Note that the minimum width of Windows Media Player is always wider than the size of the video clip, regardless of the value of the **BANNERBAR** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="6ab43-161">範例</span><span class="sxs-lookup"><span data-stu-id="6ab43-161">Examples</span></span>


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="6ab43-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ab43-162">Requirements</span></span>



| <span data-ttu-id="6ab43-163">需求</span><span class="sxs-lookup"><span data-stu-id="6ab43-163">Requirement</span></span> | <span data-ttu-id="6ab43-164">值</span><span class="sxs-lookup"><span data-stu-id="6ab43-164">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="6ab43-165">版本</span><span class="sxs-lookup"><span data-stu-id="6ab43-165">Version</span></span><br/> | <span data-ttu-id="6ab43-166">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="6ab43-166">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ab43-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ab43-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab43-168">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="6ab43-168">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6ab43-169">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="6ab43-169">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





