---
description: 下表列出 DirectShow 篩選準則分類的 Clsid。
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: 篩選準則分類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385569"
---
# <a name="filter-categories"></a><span data-ttu-id="4d044-103">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="4d044-103">Filter Categories</span></span>

<span data-ttu-id="4d044-104">下表列出 DirectShow 篩選準則分類的 Clsid。</span><span class="sxs-lookup"><span data-stu-id="4d044-104">The following tables list the CLSIDs for the DirectShow filter categories.</span></span>

-   [<span data-ttu-id="4d044-105">DirectShow 篩選準則類別</span><span class="sxs-lookup"><span data-stu-id="4d044-105">DirectShow Filter Categories</span></span>](#directshow-filter-categories)
-   [<span data-ttu-id="4d044-106">其他篩選準則類別</span><span class="sxs-lookup"><span data-stu-id="4d044-106">Other Filter Categories</span></span>](#other-filter-categories)
-   [<span data-ttu-id="4d044-107">DirectShow 濾波器中繼類別</span><span class="sxs-lookup"><span data-stu-id="4d044-107">DirectShow Filter Meta-Category</span></span>](#directshow-filter-meta-category)
-   [<span data-ttu-id="4d044-108">SQL-DMO 類別</span><span class="sxs-lookup"><span data-stu-id="4d044-108">DMO Categories</span></span>](#dmo-categories)
-   [<span data-ttu-id="4d044-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d044-109">Related topics</span></span>](#related-topics)

## <a name="directshow-filter-categories"></a><span data-ttu-id="4d044-110">DirectShow 篩選準則類別</span><span class="sxs-lookup"><span data-stu-id="4d044-110">DirectShow Filter Categories</span></span>

<span data-ttu-id="4d044-111">此處所列的類別是由 [篩選器](filter-mapper.md)對應程式所列舉。</span><span class="sxs-lookup"><span data-stu-id="4d044-111">The categories listed here are enumerated by the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="4d044-112">不過，根據預設，篩選器對應程式會忽略具有最大值的類別 \_ \_ 不 \_ 使用或較少。</span><span class="sxs-lookup"><span data-stu-id="4d044-112">By default, however, the Filter Mapper ignores categories with merits of MERIT\_DO\_NOT\_USE or less.</span></span> <span data-ttu-id="4d044-113">如需詳細資訊，請參閱 [**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters)。</span><span class="sxs-lookup"><span data-stu-id="4d044-113">For more information, see [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span></span> <span data-ttu-id="4d044-114">此處所列的所有類別也可以使用 [系統裝置](system-device-enumerator.md)列舉值來列舉。</span><span class="sxs-lookup"><span data-stu-id="4d044-114">All of the categories listed here can also be enumerated with the [System Device Enumerator](system-device-enumerator.md).</span></span>

<span data-ttu-id="4d044-115">下列類別宣告于 Uuid. h 中。</span><span class="sxs-lookup"><span data-stu-id="4d044-115">The following categories are declared in Uuids.h.</span></span> <span data-ttu-id="4d044-116">包含標頭檔 Dshow .h。</span><span class="sxs-lookup"><span data-stu-id="4d044-116">Include the header file Dshow.h.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d044-117">易記名稱</span><span class="sxs-lookup"><span data-stu-id="4d044-117">Friendly Name</span></span></th>
<th><span data-ttu-id="4d044-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="4d044-118">CLSID</span></span></th>
<th><span data-ttu-id="4d044-119">優點</span><span class="sxs-lookup"><span data-stu-id="4d044-119">Merit</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d044-120">音訊捕獲來源</span><span class="sxs-lookup"><span data-stu-id="4d044-120">Audio Capture Sources</span></span></td>
<td><span data-ttu-id="4d044-121"><strong>CLSID_AudioInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-121"><strong>CLSID_AudioInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="4d044-122"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-122"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d044-123">音訊壓縮機</span><span class="sxs-lookup"><span data-stu-id="4d044-123">Audio Compressors</span></span></td>
<td><span data-ttu-id="4d044-124"><strong>CLSID_AudioCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-124"><strong>CLSID_AudioCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="4d044-125"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-125"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d044-126">音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="4d044-126">Audio Renderers</span></span></td>
<td><span data-ttu-id="4d044-127"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-127"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
<td><span data-ttu-id="4d044-128"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-128"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d044-129">裝置控制篩選</span><span class="sxs-lookup"><span data-stu-id="4d044-129">Device Control Filters</span></span></td>
<td><span data-ttu-id="4d044-130"><strong>CLSID_DeviceControlCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-130"><strong>CLSID_DeviceControlCategory</strong></span></span></td>
<td><span data-ttu-id="4d044-131"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-131"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d044-132">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="4d044-132">DirectShow Filters</span></span></td>
<td><span data-ttu-id="4d044-133"><strong>CLSID_LegacyAmFilterCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-133"><strong>CLSID_LegacyAmFilterCategory</strong></span></span></td>
<td><span data-ttu-id="4d044-134"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-134"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d044-135">外部轉譯器</span><span class="sxs-lookup"><span data-stu-id="4d044-135">External Renderers</span></span></td>
<td><span data-ttu-id="4d044-136"><strong>CLSID_TransmitCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-136"><strong>CLSID_TransmitCategory</strong></span></span></td>
<td><span data-ttu-id="4d044-137"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-137"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d044-138">Midi 轉譯器</span><span class="sxs-lookup"><span data-stu-id="4d044-138">Midi Renderers</span></span></td>
<td><span data-ttu-id="4d044-139"><strong>CLSID_MidiRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-139"><strong>CLSID_MidiRendererCategory</strong></span></span></td>
<td><span data-ttu-id="4d044-140"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-140"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d044-141">影片捕獲來源</span><span class="sxs-lookup"><span data-stu-id="4d044-141">Video Capture Sources</span></span></td>
<td><span data-ttu-id="4d044-142"><strong>CLSID_VideoInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-142"><strong>CLSID_VideoInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="4d044-143"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-143"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d044-144">影片壓縮機</span><span class="sxs-lookup"><span data-stu-id="4d044-144">Video Compressors</span></span></td>
<td><span data-ttu-id="4d044-145"><strong>CLSID_VideoCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-145"><strong>CLSID_VideoCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="4d044-146"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-146"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d044-147">WDM 串流解壓縮裝置</span><span class="sxs-lookup"><span data-stu-id="4d044-147">WDM Stream Decompression Devices</span></span></td>
<td><span data-ttu-id="4d044-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span><span class="sxs-lookup"><span data-stu-id="4d044-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="4d044-149">此類別包含硬體 DVD 解碼器。</span><span class="sxs-lookup"><span data-stu-id="4d044-149">This category contains hardware DVD decoders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="4d044-150"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-150"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d044-151">WDM 串流捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="4d044-151">WDM Streaming Capture Devices</span></span></td>
<td><span data-ttu-id="4d044-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span></span></td>
<td><span data-ttu-id="4d044-153"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-153"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d044-154">WDM 串流處理的縱橫條裝置</span><span class="sxs-lookup"><span data-stu-id="4d044-154">WDM Streaming Crossbar Devices</span></span></td>
<td><span data-ttu-id="4d044-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span></span></td>
<td><span data-ttu-id="4d044-156"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-156"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d044-157">WDM 串流轉譯裝置</span><span class="sxs-lookup"><span data-stu-id="4d044-157">WDM Streaming Rendering Devices</span></span></td>
<td><span data-ttu-id="4d044-158"><strong>AM_KSCATEGORY_RENDER</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-158"><strong>AM_KSCATEGORY_RENDER</strong></span></span></td>
<td><span data-ttu-id="4d044-159"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-159"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d044-160">WDM 串流的 t/分隔裝置</span><span class="sxs-lookup"><span data-stu-id="4d044-160">WDM Streaming Tee/Splitter Devices</span></span></td>
<td><span data-ttu-id="4d044-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span></span></td>
<td><span data-ttu-id="4d044-162"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-162"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d044-163">WDM 串流電視音訊裝置</span><span class="sxs-lookup"><span data-stu-id="4d044-163">WDM Streaming TV Audio Devices</span></span></td>
<td><span data-ttu-id="4d044-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span></span></td>
<td><span data-ttu-id="4d044-165"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-165"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d044-166">WDM 串流電視調諧器裝置</span><span class="sxs-lookup"><span data-stu-id="4d044-166">WDM Streaming TV Tuner Devices</span></span></td>
<td><span data-ttu-id="4d044-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span></span></td>
<td><span data-ttu-id="4d044-168"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-168"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d044-169">WDM 串流 VBI 編解碼器</span><span class="sxs-lookup"><span data-stu-id="4d044-169">WDM Streaming VBI Codecs</span></span></td>
<td><span data-ttu-id="4d044-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span></span></td>
<td><span data-ttu-id="4d044-171"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="4d044-171"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4d044-172">下列類別宣告于標頭檔 Ks 中。</span><span class="sxs-lookup"><span data-stu-id="4d044-172">The following categories are declared in the header file Ks.h.</span></span>



| <span data-ttu-id="4d044-173">易記名稱</span><span class="sxs-lookup"><span data-stu-id="4d044-173">Friendly Name</span></span>                          | <span data-ttu-id="4d044-174">CLSID</span><span class="sxs-lookup"><span data-stu-id="4d044-174">CLSID</span></span>                                   | <span data-ttu-id="4d044-175">優點</span><span class="sxs-lookup"><span data-stu-id="4d044-175">Merit</span></span>                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="4d044-176">WDM 串流通訊轉換</span><span class="sxs-lookup"><span data-stu-id="4d044-176">WDM Streaming Communication Transforms</span></span> | <span data-ttu-id="4d044-177">**KSCATEGORY \_ COMMUNICATIONSTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="4d044-177">**KSCATEGORY\_COMMUNICATIONSTRANSFORM**</span></span> | <span data-ttu-id="4d044-178">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-178">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="4d044-179">WDM 串流資料轉換</span><span class="sxs-lookup"><span data-stu-id="4d044-179">WDM Streaming Data Transforms</span></span>          | <span data-ttu-id="4d044-180">**KSCATEGORY \_ DATATRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="4d044-180">**KSCATEGORY\_DATATRANSFORM**</span></span>           | <span data-ttu-id="4d044-181">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-181">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="4d044-182">WDM 串流介面轉換</span><span class="sxs-lookup"><span data-stu-id="4d044-182">WDM Streaming Interface Transforms</span></span>     | <span data-ttu-id="4d044-183">**KSCATEGORY \_ INTERFACETRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="4d044-183">**KSCATEGORY\_INTERFACETRANSFORM**</span></span>      | <span data-ttu-id="4d044-184">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-184">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="4d044-185">WDM 串流混音器裝置</span><span class="sxs-lookup"><span data-stu-id="4d044-185">WDM Streaming Mixer Devices</span></span>            | <span data-ttu-id="4d044-186">**KSCATEGORY \_ 混音器**</span><span class="sxs-lookup"><span data-stu-id="4d044-186">**KSCATEGORY\_MIXER**</span></span>                   | <span data-ttu-id="4d044-187">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-187">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="4d044-188">下列類別宣告于標頭檔 Bdamedia 中。</span><span class="sxs-lookup"><span data-stu-id="4d044-188">The following categories are declared in the header file Bdamedia.h.</span></span> <span data-ttu-id="4d044-189">包含下列標頭檔： ks. h、ksmedia .h 和 bdamedia。</span><span class="sxs-lookup"><span data-stu-id="4d044-189">Include the following header files: ks.h, ksmedia.h, and bdamedia.h.</span></span>



| <span data-ttu-id="4d044-190">易記名稱</span><span class="sxs-lookup"><span data-stu-id="4d044-190">Friendly Name</span></span>                       | <span data-ttu-id="4d044-191">CLSID</span><span class="sxs-lookup"><span data-stu-id="4d044-191">CLSID</span></span>                                       | <span data-ttu-id="4d044-192">優點</span><span class="sxs-lookup"><span data-stu-id="4d044-192">Merit</span></span>                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| <span data-ttu-id="4d044-193">BDA 網路提供者</span><span class="sxs-lookup"><span data-stu-id="4d044-193">BDA Network Providers</span></span>               | <span data-ttu-id="4d044-194">**KSCATEGORY \_ BDA \_ 網路 \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="4d044-194">**KSCATEGORY\_BDA\_NETWORK\_PROVIDER**</span></span>      | <span data-ttu-id="4d044-195">**一般的業績 \_**</span><span class="sxs-lookup"><span data-stu-id="4d044-195">**MERIT\_NORMAL**</span></span>       |
| <span data-ttu-id="4d044-196">BDA 接收器元件</span><span class="sxs-lookup"><span data-stu-id="4d044-196">BDA Receiver Components</span></span>             | <span data-ttu-id="4d044-197">**KSCATEGORY \_ BDA \_ 接收器 \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="4d044-197">**KSCATEGORY\_BDA\_RECEIVER\_COMPONENT**</span></span>    | <span data-ttu-id="4d044-198">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-198">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="4d044-199">BDA 轉譯篩選</span><span class="sxs-lookup"><span data-stu-id="4d044-199">BDA Rendering Filters</span></span>               | <span data-ttu-id="4d044-200">**KSCATEGORY \_ IP \_ 接收**</span><span class="sxs-lookup"><span data-stu-id="4d044-200">**KSCATEGORY\_IP\_SINK**</span></span>                    | <span data-ttu-id="4d044-201">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-201">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="4d044-202">BDA 來源篩選</span><span class="sxs-lookup"><span data-stu-id="4d044-202">BDA Source Filters</span></span>                  | <span data-ttu-id="4d044-203">**KSCATEGORY \_ BDA \_ 網路 \_ 調諧器**</span><span class="sxs-lookup"><span data-stu-id="4d044-203">**KSCATEGORY\_BDA\_NETWORK\_TUNER**</span></span>         | <span data-ttu-id="4d044-204">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-204">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="4d044-205">BDA 傳輸資訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="4d044-205">BDA Transport Information Renderers</span></span> | <span data-ttu-id="4d044-206">**KSCATEGORY \_ BDA \_ 傳輸 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="4d044-206">**KSCATEGORY\_BDA\_TRANSPORT\_INFORMATION**</span></span> | <span data-ttu-id="4d044-207">**一般的業績 \_**</span><span class="sxs-lookup"><span data-stu-id="4d044-207">**MERIT\_NORMAL**</span></span>       |



 

> [!Note]  
> <span data-ttu-id="4d044-208">在「DirectShow 篩選」類別下註冊的解碼器 (CLSID \_ LegacyAmFilterCategory) 。</span><span class="sxs-lookup"><span data-stu-id="4d044-208">Decoders are registered under the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory).</span></span>

 

## <a name="other-filter-categories"></a><span data-ttu-id="4d044-209">其他篩選準則類別</span><span class="sxs-lookup"><span data-stu-id="4d044-209">Other Filter Categories</span></span>

<span data-ttu-id="4d044-210">您可以使用系統裝置列舉值來列舉此處所列的類別，但不會對篩選器對應程式顯示這些類別，而且 [智慧連接](intelligent-connect.md)不會使用這些類別。</span><span class="sxs-lookup"><span data-stu-id="4d044-210">The categories listed here can be enumerated with the System Device Enumerator, but are not visible to the Filter Mapper and are not used by [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="4d044-211">下列類別宣告于標頭檔 Qedit 中。</span><span class="sxs-lookup"><span data-stu-id="4d044-211">The following categories are declared in the header file Qedit.h.</span></span>



| <span data-ttu-id="4d044-212">易記名稱</span><span class="sxs-lookup"><span data-stu-id="4d044-212">Friendly Name</span></span>            | <span data-ttu-id="4d044-213">CLID</span><span class="sxs-lookup"><span data-stu-id="4d044-213">CLID</span></span>                             | <span data-ttu-id="4d044-214">優點</span><span class="sxs-lookup"><span data-stu-id="4d044-214">Merit</span></span>                   |
|--------------------------|----------------------------------|-------------------------|
| <span data-ttu-id="4d044-215"> (1 輸入) 的影片效果</span><span class="sxs-lookup"><span data-stu-id="4d044-215">Video Effects (1 input)</span></span>  | <span data-ttu-id="4d044-216">**CLSID \_ VideoEffects1Category**</span><span class="sxs-lookup"><span data-stu-id="4d044-216">**CLSID\_VideoEffects1Category**</span></span> | <span data-ttu-id="4d044-217">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-217">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="4d044-218"> (2 輸入的影片效果) </span><span class="sxs-lookup"><span data-stu-id="4d044-218">Video Effects (2 inputs)</span></span> | <span data-ttu-id="4d044-219">**CLSID \_ VideoEffects2Category**</span><span class="sxs-lookup"><span data-stu-id="4d044-219">**CLSID\_VideoEffects2Category**</span></span> | <span data-ttu-id="4d044-220">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-220">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="4d044-221">這些類別包含適用于 [DirectShow 編輯服務](directshow-editing-services.md)的影片效果和轉換：</span><span class="sxs-lookup"><span data-stu-id="4d044-221">These categories contain video effects and transitions for [DirectShow Editing Services](directshow-editing-services.md):</span></span>

-   <span data-ttu-id="4d044-222">「影片效果 (1 輸入) 」包含影片效果。</span><span class="sxs-lookup"><span data-stu-id="4d044-222">"Video Effects (1 input)" contains video effects.</span></span>
-   <span data-ttu-id="4d044-223">「影片效果 (2 輸入) 」包含影片轉換。</span><span class="sxs-lookup"><span data-stu-id="4d044-223">"Video Effects (2 input)" contains video transitions.</span></span>

<span data-ttu-id="4d044-224">如需詳細資訊，請參閱 [列舉效果和轉換](enumerating-effects-and-transitions.md)。</span><span class="sxs-lookup"><span data-stu-id="4d044-224">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="4d044-225">下列類別宣告于標頭檔 Uuid. h 中。</span><span class="sxs-lookup"><span data-stu-id="4d044-225">The following categories are declared in the header file Uuids.h.</span></span> <span data-ttu-id="4d044-226">包含標頭檔 Dshow .h。</span><span class="sxs-lookup"><span data-stu-id="4d044-226">Include the header file Dshow.h.</span></span>



| <span data-ttu-id="4d044-227">易記名稱</span><span class="sxs-lookup"><span data-stu-id="4d044-227">Friendly Name</span></span>       | <span data-ttu-id="4d044-228">CLID</span><span class="sxs-lookup"><span data-stu-id="4d044-228">CLID</span></span>                                | <span data-ttu-id="4d044-229">優點</span><span class="sxs-lookup"><span data-stu-id="4d044-229">Merit</span></span>                   |
|---------------------|-------------------------------------|-------------------------|
| <span data-ttu-id="4d044-230">EncAPI 編碼器</span><span class="sxs-lookup"><span data-stu-id="4d044-230">EncAPI Encoders</span></span>     | <span data-ttu-id="4d044-231">**CLSID \_ MediaEncoderCategory**</span><span class="sxs-lookup"><span data-stu-id="4d044-231">**CLSID\_MediaEncoderCategory**</span></span>     | <span data-ttu-id="4d044-232">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-232">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="4d044-233">EncAPI Multiplexers</span><span class="sxs-lookup"><span data-stu-id="4d044-233">EncAPI Multiplexers</span></span> | <span data-ttu-id="4d044-234">**CLSID \_ MediaMultiplexerCategory**</span><span class="sxs-lookup"><span data-stu-id="4d044-234">**CLSID\_MediaMultiplexerCategory**</span></span> | <span data-ttu-id="4d044-235">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="4d044-235">**MERIT\_DO\_NOT\_USE**</span></span> |



 

## <a name="directshow-filter-meta-category"></a><span data-ttu-id="4d044-236">DirectShow 篩選 Meta-Category</span><span class="sxs-lookup"><span data-stu-id="4d044-236">DirectShow Filter Meta-Category</span></span>



| <span data-ttu-id="4d044-237">易記名稱</span><span class="sxs-lookup"><span data-stu-id="4d044-237">Friendly Name</span></span>                 | <span data-ttu-id="4d044-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="4d044-238">CLSID</span></span>                            | <span data-ttu-id="4d044-239">優點</span><span class="sxs-lookup"><span data-stu-id="4d044-239">Merit</span></span>          |
|-------------------------------|----------------------------------|----------------|
| <span data-ttu-id="4d044-240">ActiveMovie 篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="4d044-240">ActiveMovie Filter Categories</span></span> | <span data-ttu-id="4d044-241">**CLSID \_ ActiveMovieCategories**</span><span class="sxs-lookup"><span data-stu-id="4d044-241">**CLSID\_ActiveMovieCategories**</span></span> | <span data-ttu-id="4d044-242">不適用</span><span class="sxs-lookup"><span data-stu-id="4d044-242">Not applicable</span></span> |



 

<span data-ttu-id="4d044-243">此中繼類別包含篩選分類的清單。</span><span class="sxs-lookup"><span data-stu-id="4d044-243">This meta-category contains a list of filter categories.</span></span> <span data-ttu-id="4d044-244">如果篩選準則類別未出現在此清單中，則 [篩選器](filter-mapper.md) 對應程式會忽略類別，這表示篩選準則無法用於 [智慧型連接](intelligent-connect.md)。</span><span class="sxs-lookup"><span data-stu-id="4d044-244">If a filter category does not appear within this list, the [Filter Mapper](filter-mapper.md) ignores the category, which means the filter is not available for [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="4d044-245">若要列舉篩選類別目錄的清單，請使用值 CLSID ActiveMovieCategories 來呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) \_ 。</span><span class="sxs-lookup"><span data-stu-id="4d044-245">To enumerate the list of filter categories, call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the value CLSID\_ActiveMovieCategories.</span></span> <span data-ttu-id="4d044-246">這個方法所傳回的名字標記支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="4d044-246">The monikers returned by this method support the following properties.</span></span>



| <span data-ttu-id="4d044-247">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="4d044-247">Property Name</span></span>  | <span data-ttu-id="4d044-248">描述</span><span class="sxs-lookup"><span data-stu-id="4d044-248">Description</span></span>                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d044-249">友好</span><span class="sxs-lookup"><span data-stu-id="4d044-249">"FriendlyName"</span></span> | <span data-ttu-id="4d044-250">類別名稱 (VT \_ BSTR) 。</span><span class="sxs-lookup"><span data-stu-id="4d044-250">Category name (VT\_BSTR).</span></span>                                                              |
| <span data-ttu-id="4d044-251">調</span><span class="sxs-lookup"><span data-stu-id="4d044-251">"Merit"</span></span>        | <span data-ttu-id="4d044-252">類別 (VT \_ I4) 。</span><span class="sxs-lookup"><span data-stu-id="4d044-252">Category merit (VT\_I4).</span></span> <span data-ttu-id="4d044-253">如果這個屬性不存在，請視為 **「 \_ \_ 未 \_ 使用**」。</span><span class="sxs-lookup"><span data-stu-id="4d044-253">If this property is absent, treat as **MERIT\_DO\_NOT\_USE**.</span></span> |
| <span data-ttu-id="4d044-254">CLSID</span><span class="sxs-lookup"><span data-stu-id="4d044-254">"CLSID"</span></span>        | <span data-ttu-id="4d044-255">類別 CLSID (VT \_ BSTR) 。</span><span class="sxs-lookup"><span data-stu-id="4d044-255">Category CLSID (VT\_BSTR).</span></span>                                                             |



 

<span data-ttu-id="4d044-256">若要在此清單中加入新的篩選準則類別，請呼叫 [**IFilterMapper2：： CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory)。</span><span class="sxs-lookup"><span data-stu-id="4d044-256">To add a new filter category to this list, call [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span></span>

## <a name="dmo-categories"></a><span data-ttu-id="4d044-257">SQL-DMO 類別</span><span class="sxs-lookup"><span data-stu-id="4d044-257">DMO Categories</span></span>

<span data-ttu-id="4d044-258">DirectX 媒體物件 (DMOs) 使用與 DirectShow 篩選器不同的列舉機制。</span><span class="sxs-lookup"><span data-stu-id="4d044-258">DirectX Media Objects (DMOs) use a different enumeration mechanism from DirectShow filters.</span></span> <span data-ttu-id="4d044-259">如需詳細資訊，請參閱 [註冊 sql-dmo](registering-a-dmo.md)。</span><span class="sxs-lookup"><span data-stu-id="4d044-259">For more information, see [Registering a DMO](registering-a-dmo.md).</span></span> <span data-ttu-id="4d044-260">不過，您可以使用系統裝置列舉值來列舉 SQL-DMO 類別。</span><span class="sxs-lookup"><span data-stu-id="4d044-260">However, you can use the System Device Enumerator to enumerate DMO categories.</span></span> <span data-ttu-id="4d044-261">此名字會系結至 [Sql-dmo 包裝函式篩選器](dmo-wrapper-filter.md) ，並使用 sql-dmo 自動初始化篩選。</span><span class="sxs-lookup"><span data-stu-id="4d044-261">The monikers bind to the [DMO Wrapper Filter](dmo-wrapper-filter.md) and automatically initialize the filter with the DMO.</span></span>

<span data-ttu-id="4d044-262">此外，某些 SQL-DMO 類別會對應至 DirectShow 篩選準則類別，以供智慧型 connect 之用：</span><span class="sxs-lookup"><span data-stu-id="4d044-262">In addition, some of the DMO categories are mapped to DirectShow filter categories for the purposes of intelligent connect:</span></span>



| <span data-ttu-id="4d044-263">SQL-DMO 類別</span><span class="sxs-lookup"><span data-stu-id="4d044-263">DMO Category</span></span>                    | <span data-ttu-id="4d044-264">DirectShow 對等</span><span class="sxs-lookup"><span data-stu-id="4d044-264">DirectShow Equivalent</span></span>              |
|---------------------------------|------------------------------------|
| <span data-ttu-id="4d044-265">**DMOCATEGORY \_ 音訊 \_ 編碼器**</span><span class="sxs-lookup"><span data-stu-id="4d044-265">**DMOCATEGORY\_AUDIO\_ENCODER**</span></span> | <span data-ttu-id="4d044-266">**CLSID \_ AudioCompressorCategory**</span><span class="sxs-lookup"><span data-stu-id="4d044-266">**CLSID\_AudioCompressorCategory**</span></span> |
| <span data-ttu-id="4d044-267">**DMOCATEGORY \_ 音訊 \_ 解碼器**</span><span class="sxs-lookup"><span data-stu-id="4d044-267">**DMOCATEGORY\_AUDIO\_DECODER**</span></span> | <span data-ttu-id="4d044-268">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="4d044-268">**CLSID\_LegacyAmFilterCategory**</span></span>  |
| <span data-ttu-id="4d044-269">**DMOCATEGORY \_ 影片 \_ 編碼器**</span><span class="sxs-lookup"><span data-stu-id="4d044-269">**DMOCATEGORY\_VIDEO\_ENCODER**</span></span> | <span data-ttu-id="4d044-270">**CLSID \_ VideoCompressorCategory**</span><span class="sxs-lookup"><span data-stu-id="4d044-270">**CLSID\_VideoCompressorCategory**</span></span> |
| <span data-ttu-id="4d044-271">**DMOCATEGORY \_ 影片 \_ 解碼器**</span><span class="sxs-lookup"><span data-stu-id="4d044-271">**DMOCATEGORY\_VIDEO\_DECODER**</span></span> | <span data-ttu-id="4d044-272">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="4d044-272">**CLSID\_LegacyAmFilterCategory**</span></span>  |



 

<span data-ttu-id="4d044-273">請注意，影片效果和音訊效果類別未對應到任何 DirectShow 類別。</span><span class="sxs-lookup"><span data-stu-id="4d044-273">Note that the video effect and audio effect categories are not mapped to any DirectShow categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d044-274">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d044-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d044-275">常數和 Guid</span><span class="sxs-lookup"><span data-stu-id="4d044-275">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="4d044-276">列舉裝置和篩選器</span><span class="sxs-lookup"><span data-stu-id="4d044-276">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="4d044-277">智慧型連接</span><span class="sxs-lookup"><span data-stu-id="4d044-277">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="4d044-278">登錄機碼的版面配置</span><span class="sxs-lookup"><span data-stu-id="4d044-278">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="4d044-279">使用篩選器對應程式</span><span class="sxs-lookup"><span data-stu-id="4d044-279">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)
</dt> <dt>

[<span data-ttu-id="4d044-280">使用系統裝置列舉值</span><span class="sxs-lookup"><span data-stu-id="4d044-280">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




