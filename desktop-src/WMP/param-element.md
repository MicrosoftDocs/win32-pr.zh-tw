---
title: " (WMP SDK) 的 PARAM 元素"
description: PARAM 元素會定義與播放清單或播放清單元素相關聯的自訂參數。
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- PARAM 元素 Windows Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979564"
---
# <a name="param-element"></a><span data-ttu-id="e3633-104">PARAM 元素</span><span class="sxs-lookup"><span data-stu-id="e3633-104">PARAM Element</span></span>

<span data-ttu-id="e3633-105">**PARAM** 元素會定義與播放清單或播放清單元素相關聯的自訂參數。</span><span class="sxs-lookup"><span data-stu-id="e3633-105">The **PARAM** element defines a custom parameter associated with a playlist or an element of a playlist.</span></span>

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a><span data-ttu-id="e3633-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3633-106">Parameters</span></span>

<span data-ttu-id="e3633-107">參數也可以與顯示相關聯，而不是個別的剪輯，方法是將這個專案直接放在 **.asx** 標記之後。</span><span class="sxs-lookup"><span data-stu-id="e3633-107">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="e3633-108">這些專案是由其名稱和開頭為零的索引值所參考。</span><span class="sxs-lookup"><span data-stu-id="e3633-108">These items are referenced by their names and an index value beginning with zero.</span></span>

> [!Note]  
> <span data-ttu-id="e3633-109">此 **ASX** 元素僅適用于 Windows Media Player 6.01 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="e3633-109">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="e3633-110">Microsoft Internet Explorer 5 的標準安裝包含相容的 Windows Media Player 版本。</span><span class="sxs-lookup"><span data-stu-id="e3633-110">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

 

## <a name="attributes"></a><span data-ttu-id="e3633-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e3633-111">Attributes</span></span>

<span data-ttu-id="e3633-112">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e3633-112">**NAME**</span></span>

<span data-ttu-id="e3633-113">用來存取參數值的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3633-113">Name used to access the parameter value.</span></span> <span data-ttu-id="e3633-114">名稱可以是任何有效的字串。</span><span class="sxs-lookup"><span data-stu-id="e3633-114">The name can be any valid string.</span></span> <span data-ttu-id="e3633-115">已定義下列字串。</span><span class="sxs-lookup"><span data-stu-id="e3633-115">The following strings have already been defined.</span></span>



| <span data-ttu-id="e3633-116">String</span><span class="sxs-lookup"><span data-stu-id="e3633-116">String</span></span>                          | <span data-ttu-id="e3633-117">Description</span><span class="sxs-lookup"><span data-stu-id="e3633-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3633-118">AllowShuffle</span><span class="sxs-lookup"><span data-stu-id="e3633-118">AllowShuffle</span></span>                    | <span data-ttu-id="e3633-119">**VALUE** 屬性會指定中繼檔播放清單是否允許 Windows Media Player 隨機播放的功能，以隨機順序播放專案。</span><span class="sxs-lookup"><span data-stu-id="e3633-119">The **VALUE** attribute specifies whether the metafile playlist allows the Windows Media Player shuffle feature to play the entries in random order.</span></span> <span data-ttu-id="e3633-120">**VALUE** 屬性可以設定為 "Yes" 或 "No"。</span><span class="sxs-lookup"><span data-stu-id="e3633-120">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="e3633-121">預設值為 "No"。</span><span class="sxs-lookup"><span data-stu-id="e3633-121">The default value is "No".</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e3633-122">CanPause</span><span class="sxs-lookup"><span data-stu-id="e3633-122">CanPause</span></span>                        | <span data-ttu-id="e3633-123">**VALUE** 屬性會指定使用者是否可以暫停播放。</span><span class="sxs-lookup"><span data-stu-id="e3633-123">The **VALUE** attribute specifies whether the user can pause playback.</span></span> <span data-ttu-id="e3633-124">**VALUE** 屬性可以設定為 "Yes" 或 "No"。</span><span class="sxs-lookup"><span data-stu-id="e3633-124">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="e3633-125">預設值為 [是]。</span><span class="sxs-lookup"><span data-stu-id="e3633-125">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e3633-126">CanSeek</span><span class="sxs-lookup"><span data-stu-id="e3633-126">CanSeek</span></span>                         | <span data-ttu-id="e3633-127">**VALUE** 屬性會指定使用者是否可以使用搜尋列、向前快轉或快速反轉，來變更目前的播放位置。</span><span class="sxs-lookup"><span data-stu-id="e3633-127">The **VALUE** attribute specifies whether the user can change the current playback position by using the seek bar, fast forward, or fast reverse.</span></span> <span data-ttu-id="e3633-128">**VALUE** 屬性可以設定為 "Yes" 或 "No"。</span><span class="sxs-lookup"><span data-stu-id="e3633-128">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="e3633-129">預設值為 [是]。</span><span class="sxs-lookup"><span data-stu-id="e3633-129">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="e3633-130">CanSkipBack</span><span class="sxs-lookup"><span data-stu-id="e3633-130">CanSkipBack</span></span>                     | <span data-ttu-id="e3633-131">**VALUE** 屬性會指定使用者是否可以按一下 [**上一步**]，跳到上一個播放清單專案。</span><span class="sxs-lookup"><span data-stu-id="e3633-131">The **VALUE** attribute specifies whether the user can skip backward to the previous playlist item by clicking **Previous**.</span></span> <span data-ttu-id="e3633-132">**VALUE** 屬性可以設定為 "Yes" 或 "No"。</span><span class="sxs-lookup"><span data-stu-id="e3633-132">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="e3633-133">預設值為 [是]。</span><span class="sxs-lookup"><span data-stu-id="e3633-133">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e3633-134">CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="e3633-134">CanSkipForward</span></span>                  | <span data-ttu-id="e3633-135">**值** 屬性指定使用者是否可以按一下 **[下一步]**，跳到下一個播放清單專案。</span><span class="sxs-lookup"><span data-stu-id="e3633-135">The **VALUE** attribute specifies whether the user can skip forward to the next playlist item by clicking **Next**.</span></span> <span data-ttu-id="e3633-136">**VALUE** 屬性可以設定為 "Yes" 或 "No"。</span><span class="sxs-lookup"><span data-stu-id="e3633-136">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="e3633-137">預設值為 [是]。</span><span class="sxs-lookup"><span data-stu-id="e3633-137">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="e3633-138">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="e3633-138">CPRadioID</span></span>                       | <span data-ttu-id="e3633-139">**VALUE** 屬性會指定由類型1線上商店提供的收音機摘要識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3633-139">The **VALUE** attribute specifies the ID of a radio feed provided by a type 1 online store.</span></span> <span data-ttu-id="e3633-140">也就是說， **VALUE** 屬性必須等於線上商店目錄中其中一個收音機摘要的 RadioID 欄位。</span><span class="sxs-lookup"><span data-stu-id="e3633-140">That is, the **VALUE** attribute must be equal to the RadioID field of one of the radio feeds in the online store's catalog.</span></span> <span data-ttu-id="e3633-141">父元素是 **ASX** 元素。</span><span class="sxs-lookup"><span data-stu-id="e3633-141">The parent element is the **ASX** element.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="e3633-142">編碼</span><span class="sxs-lookup"><span data-stu-id="e3633-142">Encoding</span></span>                        | <span data-ttu-id="e3633-143">**VALUE** 屬性會設定為 "utf-8"，表示中繼檔是 UNICODE (utf-8) 編碼的檔案。</span><span class="sxs-lookup"><span data-stu-id="e3633-143">The **VALUE** attribute is set to "utf-8" to indicate that the metafile is a Unicode (UTF-8) encoded file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e3633-144">HtmlFlink</span><span class="sxs-lookup"><span data-stu-id="e3633-144">HtmlFlink</span></span>                       | <span data-ttu-id="e3633-145">**值** 屬性是類型1線上商店所提供的字串。</span><span class="sxs-lookup"><span data-stu-id="e3633-145">The **VALUE** attribute is a string provided by a type 1 online store.</span></span> <span data-ttu-id="e3633-146">Windows Media Player 將字串傳遞至 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) 方法，該方法是由線上商店的外掛程式所執行。</span><span class="sxs-lookup"><span data-stu-id="e3633-146">Windows Media Player passes the string to the [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="e3633-147">**GetItemInfo** 方法會傳回要在播放程式的 [**現正播放**] 窗格中顯示的網頁 URL。</span><span class="sxs-lookup"><span data-stu-id="e3633-147">The **GetItemInfo** method returns the URL of the webpage to display in the **Now Playing** pane of the Player.</span></span> <span data-ttu-id="e3633-148">網頁可以存取 **外部** 物件所公開的所有方法，以鍵入1個存放區。</span><span class="sxs-lookup"><span data-stu-id="e3633-148">The webpage has access to all of the methods that the **External** object exposes to type 1 stores.</span></span> <span data-ttu-id="e3633-149">如需這些方法的清單，請參閱 [類型1線上商店的外部物件](external-object-for-type-1-online-stores.md)。</span><span class="sxs-lookup"><span data-stu-id="e3633-149">For a list of those methods, see [External Object for Type 1 Online Stores](external-object-for-type-1-online-stores.md).</span></span> |
| <span data-ttu-id="e3633-150">HTMLView</span><span class="sxs-lookup"><span data-stu-id="e3633-150">HTMLView</span></span>                        | <span data-ttu-id="e3633-151">**值** 屬性指定 URL，此 URL 會根據父項目為 **ASX** 元素或 **entry 專案**，在播放清單或目前專案的完整模式播放程式的 [**立即播放**] 窗格中顯示。</span><span class="sxs-lookup"><span data-stu-id="e3633-151">The **VALUE** attribute specifies a URL that displays in the **Now Playing** pane of the full mode Player for the duration of the playlist or the current entry depending on whether the parent element is the **ASX** element or an **ENTRY** element.</span></span> <span data-ttu-id="e3633-152">Windows Media Player 控制項不支援 HTMLView。</span><span class="sxs-lookup"><span data-stu-id="e3633-152">HTMLView is not supported for the Windows Media Player control.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e3633-153">記錄：*FieldName* \[ ：*NameSpace*\]</span><span class="sxs-lookup"><span data-stu-id="e3633-153">Log:*FieldName*\[:*NameSpace*\]</span></span> | <span data-ttu-id="e3633-154">**Value** 屬性會指定指定的記錄欄位將設定為的值。</span><span class="sxs-lookup"><span data-stu-id="e3633-154">The **VALUE** attribute specifies the value that the indicated log field will be set to.</span></span> <span data-ttu-id="e3633-155">**NAME** 屬性的：*命名空間* 部分是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e3633-155">The :*NameSpace* portion of the **NAME** attribute is optional.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e3633-156">Prebuffer</span><span class="sxs-lookup"><span data-stu-id="e3633-156">Prebuffer</span></span>                       | <span data-ttu-id="e3633-157">**VALUE** 屬性會指定下一個播放清單專案是否會在目前專案的結尾之前開始緩衝處理，這樣可讓您順暢地轉換。</span><span class="sxs-lookup"><span data-stu-id="e3633-157">The **VALUE** attribute specifies whether the next playlist entry begins buffering before the end of the current entry, which enables a seamless transition.</span></span> <span data-ttu-id="e3633-158">**VALUE** 屬性可以設定為 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="e3633-158">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e3633-159">ShowWhileBuffering</span><span class="sxs-lookup"><span data-stu-id="e3633-159">ShowWhileBuffering</span></span>              | <span data-ttu-id="e3633-160">**VALUE** 屬性會指定目前 **專案專案** 所參考的影像檔，是否會在下次播放播放清單專案時，繼續顯示超過指定的時間長度。</span><span class="sxs-lookup"><span data-stu-id="e3633-160">The **VALUE** attribute specifies whether an image file referenced by the current **ENTRY** element continues to display past its specified duration time while the next playlist entry is buffered.</span></span> <span data-ttu-id="e3633-161">**VALUE** 屬性可以設定為 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="e3633-161">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="e3633-162">**VALUE**</span><span class="sxs-lookup"><span data-stu-id="e3633-162">**VALUE**</span></span>

<span data-ttu-id="e3633-163">與此參數相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="e3633-163">Value associated with this parameter.</span></span> <span data-ttu-id="e3633-164">可以是數值或字串值。</span><span class="sxs-lookup"><span data-stu-id="e3633-164">It can be either a numeric or string value.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="e3633-165">父/子項目</span><span class="sxs-lookup"><span data-stu-id="e3633-165">Parent/Child Elements</span></span>



| <span data-ttu-id="e3633-166">階層</span><span class="sxs-lookup"><span data-stu-id="e3633-166">Hierarchy</span></span>       | <span data-ttu-id="e3633-167">元素</span><span class="sxs-lookup"><span data-stu-id="e3633-167">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="e3633-168">父元素</span><span class="sxs-lookup"><span data-stu-id="e3633-168">Parent elements</span></span> | <span data-ttu-id="e3633-169">**ASX**， **進入**</span><span class="sxs-lookup"><span data-stu-id="e3633-169">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="e3633-170">子元素</span><span class="sxs-lookup"><span data-stu-id="e3633-170">Child elements</span></span>  | <span data-ttu-id="e3633-171">無</span><span class="sxs-lookup"><span data-stu-id="e3633-171">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="e3633-172">備註</span><span class="sxs-lookup"><span data-stu-id="e3633-172">Remarks</span></span>

<span data-ttu-id="e3633-173">此元素可讓使用者在包含它的 **ENTRY 專案** 內，放置每個剪輯的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e3633-173">This element allows users to place additional information about each clip inside the **ENTRY** element that contains it.</span></span> <span data-ttu-id="e3633-174">若要取出播放清單 **專案** 中指定的中繼資料資訊，請使用 *媒體*。**getItemInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="e3633-174">To retrieve metadata information specified in the playlist **ENTRY**, use the *Media*.**getItemInfo** method.</span></span> <span data-ttu-id="e3633-175">*媒體*。**getItemInfo** 方法會在指定參數名稱的情況下，取得 **value** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e3633-175">The *Media*.**getItemInfo** method retrieves the value of the **VALUE** attribute, given the name of the parameter.</span></span> <span data-ttu-id="e3633-176">舊版 Windows Media Player 會使用 **GetMediaParameter** 方法來取得播放清單 **專案** 中指定的中繼資料資訊，並使用指定的參數名稱和專案的索引編號。</span><span class="sxs-lookup"><span data-stu-id="e3633-176">Previous versions of Windows Media Player retrieve metadata information specified in the playlist **ENTRY**, using the **GetMediaParameter** method given the name of the parameter and an index number for the entry.</span></span>

<span data-ttu-id="e3633-177">參數也可以與顯示相關聯，而不是個別的剪輯，方法是將這個專案直接放在 **.asx** 標記之後。</span><span class="sxs-lookup"><span data-stu-id="e3633-177">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="e3633-178">這些專案是由其名稱和開頭為零的索引值所參考。</span><span class="sxs-lookup"><span data-stu-id="e3633-178">These items are referenced by their names and an index value beginning with zero.</span></span>

<span data-ttu-id="e3633-179">**注意**</span><span class="sxs-lookup"><span data-stu-id="e3633-179">**Note**</span></span>

<span data-ttu-id="e3633-180">此 **ASX** 元素僅適用于 Windows Media Player 6.01 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="e3633-180">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="e3633-181">Microsoft Internet Explorer 5 的標準安裝包含相容的 Windows Media Player 版本。</span><span class="sxs-lookup"><span data-stu-id="e3633-181">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="e3633-182">範例</span><span class="sxs-lookup"><span data-stu-id="e3633-182">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="e3633-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3633-183">Requirements</span></span>



| <span data-ttu-id="e3633-184">需求</span><span class="sxs-lookup"><span data-stu-id="e3633-184">Requirement</span></span> | <span data-ttu-id="e3633-185">值</span><span class="sxs-lookup"><span data-stu-id="e3633-185">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3633-186">版本</span><span class="sxs-lookup"><span data-stu-id="e3633-186">Version</span></span><br/> | <span data-ttu-id="e3633-187">Windows Media Player 7.0 版或更新版本，預先定義的名稱屬性需要 Windows Media Player 9 系列或更新版本，預先定義的名稱屬性需要 Windows Media Player 10 或更新版本 CanPause、CanSeek、CanSkipBack 和 CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="e3633-187">Windows Media Player version 7.0 or later, Windows Media Player 9 Series or later is required for the predefined NAME attributes, Windows Media Player 10 or later is required for the predefined names CanPause, CanSeek, CanSkipBack, and CanSkipForward</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3633-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3633-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3633-189">**顯示 Windows Media Player 中的網頁**</span><span class="sxs-lookup"><span data-stu-id="e3633-189">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="e3633-190">**記錄資料流程資料**</span><span class="sxs-lookup"><span data-stu-id="e3633-190">**Logging Stream Data**</span></span>](logging-stream-data.md)
</dt> <dt>

[<span data-ttu-id="e3633-191">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="e3633-191">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="e3633-192">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="e3633-192">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





