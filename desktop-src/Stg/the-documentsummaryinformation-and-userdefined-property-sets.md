---
title: DocumentSummaryInformation 和使用者設定的屬性集
description: DocumentSummaryInformation 和使用者設定的屬性集是摘要資訊屬性集的延伸。 這兩個屬性集可以同時存在。
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- 使用者設定的屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507204"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a><span data-ttu-id="4d4b2-106">DocumentSummaryInformation 和使用者設定的屬性集</span><span class="sxs-lookup"><span data-stu-id="4d4b2-106">The DocumentSummaryInformation and UserDefined Property Sets</span></span>

<span data-ttu-id="4d4b2-107">**DocumentSummaryInformation** 和 **使用者** 設定的屬性集是 [摘要資訊屬性集](the-summary-information-property-set.md)的延伸。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-107">A **DocumentSummaryInformation** and **UserDefined** property set is an extension to [the Summary Information property set](the-summary-information-property-set.md).</span></span> <span data-ttu-id="4d4b2-108">這兩個屬性集可以同時存在。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-108">Both property sets can exist simultaneously.</span></span>

<span data-ttu-id="4d4b2-109">包含 **DocumentSummaryInformation** 屬性集之資料流程的名稱為 **" \\ 005DocumentSummaryInformation"**。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-109">The name of the stream that contains the **DocumentSummaryInformation** property set is **"\\005DocumentSummaryInformation"**.</span></span> <span data-ttu-id="4d4b2-110">**DocumentSummaryInformation** 屬性集的格式識別碼 (FMTID) 為 **D5CDD502-2E9C-101B-9397-08002B2CF9AE**。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-110">The format identifier (FMTID) for the **DocumentSummaryInformation** property set is **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="4d4b2-111">提供的標頭檔中提供此值的宣告作為 **FMTID \_ DocSummaryInformation**。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-111">The declaration for this value is available in the provided header files as **FMTID\_DocSummaryInformation**.</span></span> <span data-ttu-id="4d4b2-112">如需詳細資訊，請參閱 [IStorage](names-in-istorage.md)中 [的名稱、摘要資訊屬性集](the-summary-information-property-set.md)、 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 和 [Format 識別碼](format-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-112">For more information, see [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [Format Identifiers](format-identifiers.md).</span></span>

<span data-ttu-id="4d4b2-113">針對自訂使用者定義的屬性，此資料流程也有個別的區段，如同在 **DocumentSummaryInformation** 和 **使用者** 定義的屬性集中。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-113">This stream also has a separate section for the custom-user-defined properties as in the **DocumentSummaryInformation** and **UserDefined** property sets.</span></span> <span data-ttu-id="4d4b2-114">此區段會以個別屬性集的形式出現在 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面中，並以 **FMTID \_ UserDefinedProperties**) ： **D5CDD505-2E9C-101B-9397-08002B2CF9AE** 的形式 (提供下列 FMTID。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-114">This section appears in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface as a separate property set, with the following FMTID (available as **FMTID\_UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="4d4b2-115">這兩個屬性集是單一資料流程可以包含多個屬性集的唯一一個屬性集。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-115">These two property sets are the only ones for which a single stream can hold multiple property sets.</span></span> <span data-ttu-id="4d4b2-116">這兩個屬性集在單一資料流程中的事實，會影響 **IPropertySetStorage** 介面的行為。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-116">The fact that these two property sets are in a single stream affects the behavior of the **IPropertySetStorage** interface.</span></span> <span data-ttu-id="4d4b2-117">如需詳細資訊，請參閱 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-117">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span></span>

<span data-ttu-id="4d4b2-118">下表列出新增的屬性至 **DocumentSummaryInformation** 和 **使用者** 設定的屬性集。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-118">The following table lists the added properties to the **DocumentSummaryInformation** and **UserDefined** property set.</span></span> <span data-ttu-id="4d4b2-119">如同 **SummaryInformation** 屬性集，名稱通常不會儲存在屬性集中，而是從屬性識別碼推斷而來。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-119">As in the **SummaryInformation** property set, the names are not typically stored in the property set, but are inferred from the property identifier.</span></span>



| <span data-ttu-id="4d4b2-120">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="4d4b2-120">Property name</span></span>      | <span data-ttu-id="4d4b2-121">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="4d4b2-121">Property identifier</span></span>     | <span data-ttu-id="4d4b2-122">屬性識別碼值</span><span class="sxs-lookup"><span data-stu-id="4d4b2-122">Property identifier value</span></span> | <span data-ttu-id="4d4b2-123">VARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="4d4b2-123">VARIANT type</span></span>                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| <span data-ttu-id="4d4b2-124">類別</span><span class="sxs-lookup"><span data-stu-id="4d4b2-124">Category</span></span>           | <span data-ttu-id="4d4b2-125">**PIDDSI \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-125">**PIDDSI\_CATEGORY**</span></span>    | <span data-ttu-id="4d4b2-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4d4b2-126">0x00000002</span></span>                | <span data-ttu-id="4d4b2-127">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-127">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="4d4b2-128">PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="4d4b2-128">PresentationTarget</span></span> | <span data-ttu-id="4d4b2-129">**PIDDSI \_ PRESFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-129">**PIDDSI\_PRESFORMAT**</span></span>  | <span data-ttu-id="4d4b2-130">0x00000003</span><span class="sxs-lookup"><span data-stu-id="4d4b2-130">0x00000003</span></span>                | <span data-ttu-id="4d4b2-131">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-131">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="4d4b2-132">位元組</span><span class="sxs-lookup"><span data-stu-id="4d4b2-132">Bytes</span></span>              | <span data-ttu-id="4d4b2-133">**PIDDSI \_ BYTECOUNT**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-133">**PIDDSI\_BYTECOUNT**</span></span>   | <span data-ttu-id="4d4b2-134">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4d4b2-134">0x00000004</span></span>                | <span data-ttu-id="4d4b2-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-135">**VT\_I4**</span></span>                        |
| <span data-ttu-id="4d4b2-136">線條</span><span class="sxs-lookup"><span data-stu-id="4d4b2-136">Lines</span></span>              | <span data-ttu-id="4d4b2-137">**PIDDSI \_ LINECOUNT**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-137">**PIDDSI\_LINECOUNT**</span></span>   | <span data-ttu-id="4d4b2-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4d4b2-138">0x00000005</span></span>                | <span data-ttu-id="4d4b2-139">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-139">**VT\_I4**</span></span>                        |
| <span data-ttu-id="4d4b2-140">段落</span><span class="sxs-lookup"><span data-stu-id="4d4b2-140">Paragraphs</span></span>         | <span data-ttu-id="4d4b2-141">**PIDDSI \_ PARCOUNT**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-141">**PIDDSI\_PARCOUNT**</span></span>    | <span data-ttu-id="4d4b2-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="4d4b2-142">0x00000006</span></span>                | <span data-ttu-id="4d4b2-143">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-143">**VT\_I4**</span></span>                        |
| <span data-ttu-id="4d4b2-144">投影片</span><span class="sxs-lookup"><span data-stu-id="4d4b2-144">Slides</span></span>             | <span data-ttu-id="4d4b2-145">**PIDDSI \_ SLIDECOUNT**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-145">**PIDDSI\_SLIDECOUNT**</span></span>  | <span data-ttu-id="4d4b2-146">0x00000007</span><span class="sxs-lookup"><span data-stu-id="4d4b2-146">0x00000007</span></span>                | <span data-ttu-id="4d4b2-147">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-147">**VT\_I4**</span></span>                        |
| <span data-ttu-id="4d4b2-148">備註</span><span class="sxs-lookup"><span data-stu-id="4d4b2-148">Notes</span></span>              | <span data-ttu-id="4d4b2-149">**PIDDSI \_ NOTECOUNT**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-149">**PIDDSI\_NOTECOUNT**</span></span>   | <span data-ttu-id="4d4b2-150">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4d4b2-150">0x00000008</span></span>                | <span data-ttu-id="4d4b2-151">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-151">**VT\_I4**</span></span>                        |
| <span data-ttu-id="4d4b2-152">HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="4d4b2-152">HiddenSlides</span></span>       | <span data-ttu-id="4d4b2-153">**PIDDSI \_ HIDDENCOUNT**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-153">**PIDDSI\_HIDDENCOUNT**</span></span> | <span data-ttu-id="4d4b2-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4d4b2-154">0x00000009</span></span>                | <span data-ttu-id="4d4b2-155">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-155">**VT\_I4**</span></span>                        |
| <span data-ttu-id="4d4b2-156">MMClips</span><span class="sxs-lookup"><span data-stu-id="4d4b2-156">MMClips</span></span>            | <span data-ttu-id="4d4b2-157">**PIDDSI \_ MMCLIPCOUNT**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-157">**PIDDSI\_MMCLIPCOUNT**</span></span> | <span data-ttu-id="4d4b2-158">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="4d4b2-158">0x0000000A</span></span>                | <span data-ttu-id="4d4b2-159">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-159">**VT\_I4**</span></span>                        |
| <span data-ttu-id="4d4b2-160">ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="4d4b2-160">ScaleCrop</span></span>          | <span data-ttu-id="4d4b2-161">**PIDDSI \_ SCALE**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-161">**PIDDSI\_SCALE**</span></span>       | <span data-ttu-id="4d4b2-162">0x0000000B</span><span class="sxs-lookup"><span data-stu-id="4d4b2-162">0x0000000B</span></span>                | <span data-ttu-id="4d4b2-163">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-163">**VT\_BOOL**</span></span>                      |
| <span data-ttu-id="4d4b2-164">HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="4d4b2-164">HeadingPairs</span></span>       | <span data-ttu-id="4d4b2-165">**PIDDSI \_ HEADINGPAIR**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-165">**PIDDSI\_HEADINGPAIR**</span></span> | <span data-ttu-id="4d4b2-166">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="4d4b2-166">0x0000000C</span></span>                | <span data-ttu-id="4d4b2-167">**VT \_VARIANT** \| **VT \_ 向量**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-167">**VT\_VARIANT** \| **VT\_VECTOR**</span></span> |
| <span data-ttu-id="4d4b2-168">TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="4d4b2-168">TitlesofParts</span></span>      | <span data-ttu-id="4d4b2-169">**PIDDSI \_ DOCPARTS**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-169">**PIDDSI\_DOCPARTS**</span></span>    | <span data-ttu-id="4d4b2-170">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="4d4b2-170">0x0000000D</span></span>                | <span data-ttu-id="4d4b2-171">**VT \_向量** \| **VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-171">**VT\_VECTOR** \| **VT\_LPSTR**</span></span>   |
| <span data-ttu-id="4d4b2-172">Manager</span><span class="sxs-lookup"><span data-stu-id="4d4b2-172">Manager</span></span>            | <span data-ttu-id="4d4b2-173">**PIDDSI \_ 管理員**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-173">**PIDDSI\_MANAGER**</span></span>     | <span data-ttu-id="4d4b2-174">0x0000000E</span><span class="sxs-lookup"><span data-stu-id="4d4b2-174">0x0000000E</span></span>                | <span data-ttu-id="4d4b2-175">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-175">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="4d4b2-176">公司</span><span class="sxs-lookup"><span data-stu-id="4d4b2-176">Company</span></span>            | <span data-ttu-id="4d4b2-177">**PIDDSI \_ 公司**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-177">**PIDDSI\_COMPANY**</span></span>     | <span data-ttu-id="4d4b2-178">0x0000000F</span><span class="sxs-lookup"><span data-stu-id="4d4b2-178">0x0000000F</span></span>                | <span data-ttu-id="4d4b2-179">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-179">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="4d4b2-180">LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="4d4b2-180">LinksUpToDate</span></span>      | <span data-ttu-id="4d4b2-181">**PIDDSI \_ LINKSDIRTY**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-181">**PIDDSI\_LINKSDIRTY**</span></span>  | <span data-ttu-id="4d4b2-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d4b2-182">0x00000010</span></span>                | <span data-ttu-id="4d4b2-183">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-183">**VT\_BOOL**</span></span>                      |



 

<span data-ttu-id="4d4b2-184">這些屬性具有下列用途：</span><span class="sxs-lookup"><span data-stu-id="4d4b2-184">These properties have the following uses:</span></span>

<dl> <dt>

<span data-ttu-id="4d4b2-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別</span><span class="sxs-lookup"><span data-stu-id="4d4b2-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-186">使用者輸入的文字字串，指出檔案所屬的類別 (備忘錄、提案等) 。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-186">A text string typed by the user that indicates what category the file belongs to (memo, proposal, and so on).</span></span> <span data-ttu-id="4d4b2-187">它很適合用來尋找相同類型的檔案。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-187">It is useful for finding files of same type.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span><span class="sxs-lookup"><span data-stu-id="4d4b2-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-189">簡報 (35mm、印表機、影片等) 的目標格式。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-189">Target format for presentation (35mm, printer, video, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>位元組</span><span class="sxs-lookup"><span data-stu-id="4d4b2-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-191">位元組數。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-191">Number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>線</span><span class="sxs-lookup"><span data-stu-id="4d4b2-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Lines</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-193">行數。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-193">Number of lines.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>段落</span><span class="sxs-lookup"><span data-stu-id="4d4b2-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Paragraphs</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-195">段落數目。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-195">Number of paragraphs.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>幻燈片</span><span class="sxs-lookup"><span data-stu-id="4d4b2-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Slides</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-197">幻燈片數目。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-197">Number of slides.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>筆記</span><span class="sxs-lookup"><span data-stu-id="4d4b2-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notes</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-199">包含附注的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-199">Number of pages that contain notes.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="4d4b2-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-201">隱藏的幻燈片數。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-201">Number of slides that are hidden.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span><span class="sxs-lookup"><span data-stu-id="4d4b2-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-203">音效或影片剪輯的數目。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-203">Number of sound or video clips.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="4d4b2-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-205">當需要調整縮圖時，設定為 True (-1) 。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-205">Set to True (-1) when scaling of the thumbnail is desired.</span></span> <span data-ttu-id="4d4b2-206">如果未設定，則需要裁剪。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-206">If not set, cropping is desired.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="4d4b2-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-208">內部使用的屬性，指出不同檔部分的群組以及每個群組中的專案數。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-208">Internally used property indicating the grouping of different document parts and the number of items in each group.</span></span> <span data-ttu-id="4d4b2-209">檔部分的標題會儲存在 **TitlesofParts** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-209">The titles of the document parts are stored in the **TitlesofParts** property.</span></span> <span data-ttu-id="4d4b2-210">**HeadingPairs** 屬性會以一組重複的 **vt \_ LPSTR** (或 **vt \_ LPWSTR**) 和 **vt \_ I4** 值，儲存為 variant 的向量。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-210">The **HeadingPairs** property is stored as a vector of variants, in repeating pairs of **VT\_LPSTR** (or **VT\_LPWSTR**) and **VT\_I4** values.</span></span> <span data-ttu-id="4d4b2-211">**Vt \_ LPSTR** 值代表標題名稱，而 **vt \_ I4** 值則表示該標題底下的檔部分計數。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-211">The **VT\_LPSTR** value represents a heading name, and the **VT\_I4** value indicates the count of document parts under that heading.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="4d4b2-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-213">檔元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-213">Names of document parts.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>經理</span><span class="sxs-lookup"><span data-stu-id="4d4b2-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-215">專案的管理員。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-215">Manager of the project.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>公司</span><span class="sxs-lookup"><span data-stu-id="4d4b2-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-217">公司名稱。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-217">Company name.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b2-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="4d4b2-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span></span>
</dt> <dd>

<span data-ttu-id="4d4b2-219">布林值，指出針對所有應用程式，自訂連結是否受到過度雜訊的阻礙。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-219">Boolean value to indicate whether the custom links are hampered by excessive noise, for all applications.</span></span>

> [!Note]  
> <span data-ttu-id="4d4b2-220">如12.3 中所述。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-220">As described in 12.3.</span></span> <span data-ttu-id="4d4b2-221">OLE 2.0 設計規格之屬性集的序列化格式， **HeadingPairs** 和 **TitlesofParts** 屬性中的 vector 元素應該在屬性集內的32位界限上對齊。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-221">Serialized Format for Property Sets of the OLE 2.0 Design Specification, vector elements in the **HeadingPairs** and **TitlesofParts** properties should be aligned on 32 bit boundaries within the property set.</span></span> <span data-ttu-id="4d4b2-222">不過，在 **DocumentSummaryInformation** 和 **使用者** 配置的屬性集中，當屬性集的字碼頁不是 Unicode 時，必須封裝這些元素。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-222">However, in the **DocumentSummaryInformation** and **UserDefined** property sets, when the code page of the property set is not Unicode, these elements must be packed.</span></span>

 

</dd> </dl>

<span data-ttu-id="4d4b2-223">您可以使用可設定的屬性集來保存 **任何屬性。**</span><span class="sxs-lookup"><span data-stu-id="4d4b2-223">The **UserDefined** property set can be used to hold any properties.</span></span> <span data-ttu-id="4d4b2-224">通常，它是用來儲存使用者所建立的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="4d4b2-224">Typically, it is used to store named properties created by a user.</span></span>

 

 




