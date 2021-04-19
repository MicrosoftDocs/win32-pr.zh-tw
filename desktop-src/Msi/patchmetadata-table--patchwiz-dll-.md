---
description: PatchMetadata 資料表包含移除修補程式所需之 Windows Installer 修補程式的相關資訊，以及新增/移除程式所使用的資訊。
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: 'PatchMetadata 資料表 (PATCHWIZ.DLL) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990471"
---
# <a name="patchmetadata-table-patchwizdll"></a><span data-ttu-id="3cc7e-103">PatchMetadata 資料表 (PATCHWIZ.DLL) </span><span class="sxs-lookup"><span data-stu-id="3cc7e-103">PatchMetadata Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="3cc7e-104">PatchMetadata 資料表包含移除修補程式所需之 Windows Installer 修補程式的相關資訊，以及新增/移除程式所使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-104">The PatchMetadata Table contains information about a Windows Installer patch that is required to remove a patch and that is used by Add/Remove Programs.</span></span> <span data-ttu-id="3cc7e-105">PatchMetadata 資料表中的所有屬性都會加入至 .msp 檔案的 [MsiPatchMetadata 資料表](msipatchmetadata-table.md) 中，以取得修補程式。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-105">All the properties in the PatchMetadata Table are added to the [MsiPatchMetadata Table](msipatchmetadata-table.md) of the .msp file for a patch.</span></span>

<span data-ttu-id="3cc7e-106">PatchMetadata 資料表在 patch 建立屬性檔中是必要的， (. pcp 檔案中的 MinimumRequiredMsiVersion 等於300的) [檔案。](properties-table-patchwiz-dll-.md)</span><span class="sxs-lookup"><span data-stu-id="3cc7e-106">The PatchMetadata Table is required in patch creation properties files (.pcp files) that have a MinimumRequiredMsiVersion equal to 300 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="3cc7e-107">如果 MinimumRequiredMsiVersion 不等於300，則資料表是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-107">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

<span data-ttu-id="3cc7e-108">PatchMetadata 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-108">The PatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="3cc7e-109">Column</span><span class="sxs-lookup"><span data-stu-id="3cc7e-109">Column</span></span>   | <span data-ttu-id="3cc7e-110">類型</span><span class="sxs-lookup"><span data-stu-id="3cc7e-110">Type</span></span> | <span data-ttu-id="3cc7e-111">答案</span><span class="sxs-lookup"><span data-stu-id="3cc7e-111">Key</span></span> | <span data-ttu-id="3cc7e-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="3cc7e-112">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="3cc7e-113">公司</span><span class="sxs-lookup"><span data-stu-id="3cc7e-113">Company</span></span>  | <span data-ttu-id="3cc7e-114">text</span><span class="sxs-lookup"><span data-stu-id="3cc7e-114">text</span></span> | <span data-ttu-id="3cc7e-115">Y</span><span class="sxs-lookup"><span data-stu-id="3cc7e-115">Y</span></span>   | <span data-ttu-id="3cc7e-116">Y</span><span class="sxs-lookup"><span data-stu-id="3cc7e-116">Y</span></span>        |
| <span data-ttu-id="3cc7e-117">屬性</span><span class="sxs-lookup"><span data-stu-id="3cc7e-117">Property</span></span> | <span data-ttu-id="3cc7e-118">text</span><span class="sxs-lookup"><span data-stu-id="3cc7e-118">text</span></span> | <span data-ttu-id="3cc7e-119">Y</span><span class="sxs-lookup"><span data-stu-id="3cc7e-119">Y</span></span>   | <span data-ttu-id="3cc7e-120">N</span><span class="sxs-lookup"><span data-stu-id="3cc7e-120">N</span></span>        |
| <span data-ttu-id="3cc7e-121">值</span><span class="sxs-lookup"><span data-stu-id="3cc7e-121">Value</span></span>    | <span data-ttu-id="3cc7e-122">text</span><span class="sxs-lookup"><span data-stu-id="3cc7e-122">text</span></span> |     | <span data-ttu-id="3cc7e-123">Y</span><span class="sxs-lookup"><span data-stu-id="3cc7e-123">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="3cc7e-124">資料行</span><span class="sxs-lookup"><span data-stu-id="3cc7e-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3cc7e-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>公司</span><span class="sxs-lookup"><span data-stu-id="3cc7e-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="3cc7e-126">公司名稱。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-126">The name of the company.</span></span> <span data-ttu-id="3cc7e-127">空白欄位 (Null 值) 表示此資料列包含其中一個標準中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-127">An empty field (a Null value) indicates that this row contains one of the standard metadata properties.</span></span> <span data-ttu-id="3cc7e-128">公司可以將資料列加入至資料表，並在此欄位中輸入公司名稱，以擴充屬性集。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-128">A company can extend the property set by adding a row to the table, and entering a company name in this field.</span></span>

</dd> <dt>

<span data-ttu-id="3cc7e-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產</span><span class="sxs-lookup"><span data-stu-id="3cc7e-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="3cc7e-130">中繼資料屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-130">The name of a metadata property.</span></span> <span data-ttu-id="3cc7e-131">PatchMetadata 資料表中需要 AllowRemoval、ManufacturerName、TargetProductName、MoreInfoURL、DisplayName、Description 和分類屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-131">The AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description, and Classification properties are required in the PatchMetadata Table .</span></span> <span data-ttu-id="3cc7e-132">如果 [公司] 欄位是空的，則這個欄位必須包含下列其中一個標準中繼資料屬性 (Null 值) 。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-132">This field must contain one of the following standard metadata properties if the Company field is empty (a Null value).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3cc7e-133">屬性</span><span class="sxs-lookup"><span data-stu-id="3cc7e-133">Property</span></span></th>
<th><span data-ttu-id="3cc7e-134">描述</span><span class="sxs-lookup"><span data-stu-id="3cc7e-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3cc7e-135">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="3cc7e-135">AllowRemoval</span></span></td>
<td><span data-ttu-id="3cc7e-136">整數值，指出修補程式是否為 <a href="uninstallable-patches.md">可卸載修補程式</a>。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-136">An integer value that indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="3cc7e-137">如果 [值] 欄位包含 0 (零) ，就無法移除修補程式。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-137">If the Value field contains a 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="3cc7e-138">如果 [值] 欄位包含1個 (一個) ，則修補程式是可卸載修補程式。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-138">If the Value field contains 1 (one), the patch is an Uninstallable Patch.</span></span> <span data-ttu-id="3cc7e-139">此為必要屬性。這個屬性已註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-139">This property is required.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc7e-140">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="3cc7e-140">ManufacturerName</span></span></td>
<td><span data-ttu-id="3cc7e-141">字串值，其中包含應用程式的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-141">A string value that contains the name of the manufacturer of the application.</span></span> <span data-ttu-id="3cc7e-142">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-142">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc7e-143">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="3cc7e-143">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="3cc7e-144">表示修補程式以產品的 RTM 版本或最新的主要升級修補程式為目標。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-144">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="3cc7e-145">在包含順序資訊的次要升級修補程式中撰寫此選用屬性，以指出修補程式會移除產品 RTM 版本的所有修補程式，或最新的主要升級修補程式。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-145">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="3cc7e-146">從 Windows Installer 3.1 開始，可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-146">This property is available beginning with Windows Installer 3.1.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3cc7e-147">若要要求安裝 Windows Installer 3.1 以套用修補程式，請在 pcp 檔案的 <a href="properties-table-patchwiz-dll-.md">Properties 資料表</a> 中，將 MinimumRequiredMsiVersion 屬性設定為310。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-147">To require that Windows Installer 3.1 be installed to apply the patch, set the MinimumRequiredMsiVersion property to 310 in the <a href="properties-table-patchwiz-dll-.md">Properties Table</a> of the .pcp file.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc7e-148">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="3cc7e-148">TargetProductName</span></span></td>
<td><span data-ttu-id="3cc7e-149">包含應用程式或目標應用程式套件名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-149">A string value that contains the name of the application or target application suite.</span></span> <span data-ttu-id="3cc7e-150">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-150">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc7e-151">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="3cc7e-151">MoreInfoURL</span></span></td>
<td><span data-ttu-id="3cc7e-152">字串值，包含指向此修補程式資訊的 URL。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-152">A string value that contains a URL pointing to information for this patch.</span></span> <span data-ttu-id="3cc7e-153">這個必要屬性已註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-153">This required property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="3cc7e-154">從 Windows XP Service Pack 2 開始 (SP2) ，此值可以是 [新增/移除程式] 中顯示之修補程式的支援連結。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-154">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in Add/Remove Programs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc7e-155">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="3cc7e-155">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="3cc7e-156">字串值，包含 .msp 檔的建立時間，格式為 mm-dd-yy HH： MM (月-日-年小時：分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-156">A string value that contains the creation time of the .msp file in the form mm-dd-yy HH:MM (month-day-year hour:minute).</span></span> <span data-ttu-id="3cc7e-157">這是選用屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-157">This property is optional.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc7e-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="3cc7e-158">DisplayName</span></span></td>
<td><span data-ttu-id="3cc7e-159">字串值，包含適用于公開顯示之修補程式的標題。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-159">A string value that contains the title for the patch that is suitable for public display.</span></span> <span data-ttu-id="3cc7e-160">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-160">This property is required.</span></span> <span data-ttu-id="3cc7e-161">這個屬性已註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-161">This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="3cc7e-162">從 Windows XP SP2 開始，此值是在 Windows XP 加裝 SP2 開頭的 [新增/移除程式] 中顯示的修補程式名稱。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-162">Beginning with Windows XP with SP2, this value is the name of the patch displayed in Add/Remove Programs beginning with Windows XP with SP2.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc7e-163">Description</span><span class="sxs-lookup"><span data-stu-id="3cc7e-163">Description</span></span></td>
<td><span data-ttu-id="3cc7e-164">包含修補程式簡短描述的字串值。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-164">A string value that contains a brief description of the patch.</span></span> <span data-ttu-id="3cc7e-165">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-165">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3cc7e-166">分類</span><span class="sxs-lookup"><span data-stu-id="3cc7e-166">Classification</span></span></td>
<td><span data-ttu-id="3cc7e-167">字串值，包含由 patch 作者定義的任意更新分類。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-167">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="3cc7e-168">例如，修補程式作者可以指定將每個修補程式分類為一個修正程式、安全性匯總、重大更新、更新、Service Pack 或更新彙總套件。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-168">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="3cc7e-169">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-169">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3cc7e-170">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="3cc7e-170">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="3cc7e-171">如果這個屬性設定為 1 (要在交易中套用的所有修補程式中的一個) ，則會盡可能將修補程式的應用程式優化。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-171">If this property is set to 1 (one) in all the patches to be applied in a transaction, the application of the patch is optimized if possible.</span></span> <span data-ttu-id="3cc7e-172">如需詳細資訊，請參閱 <a href="patch-optimization.md">修補程式優化</a>。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-172">For information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="3cc7e-173">從 Windows Installer 3.1 開始提供。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-173">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="3cc7e-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="3cc7e-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="3cc7e-175">中繼資料屬性的值。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-175">Value of the metadata property.</span></span> <span data-ttu-id="3cc7e-176">這絕對不能是 Null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-176">This can never be Null or an empty string.</span></span> <span data-ttu-id="3cc7e-177">這個值可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-177">This value can be localized.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3cc7e-178">備註</span><span class="sxs-lookup"><span data-stu-id="3cc7e-178">Remarks</span></span>

<span data-ttu-id="3cc7e-179">從 Windows Installer 3.0 開始提供。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-179">Available beginning in Windows Installer 3.0.</span></span>

<span data-ttu-id="3cc7e-180">所有撰寫至 PatchMetadata 資料表的屬性都會新增至 msp 檔案的 MsiPatchMetadata 資料表中。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-180">All properties authored into the PatchMetadata Table are added to the MsiPatchMetadata table of the msp file.</span></span> <span data-ttu-id="3cc7e-181">AllowRemoval、MoreInfoURL 和 DisplayName 屬性都會註冊，而且可透過 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)存取。</span><span class="sxs-lookup"><span data-stu-id="3cc7e-181">AllowRemoval, MoreInfoURL and DisplayName properties are registered and are accessible through the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

 

 




