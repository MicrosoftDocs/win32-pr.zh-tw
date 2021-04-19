---
description: MsiPatchMetadata 資料表包含移除修補程式以及新增/移除程式所使用之 Windows Installer 修補程式的相關資訊。
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: MsiPatchMetadata 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975324"
---
# <a name="msipatchmetadata-table"></a><span data-ttu-id="a4c29-103">MsiPatchMetadata 資料表</span><span class="sxs-lookup"><span data-stu-id="a4c29-103">MsiPatchMetadata Table</span></span>

<span data-ttu-id="a4c29-104">MsiPatchMetadata 資料表包含移除修補程式以及 **新增/移除程式** 所使用之 Windows Installer 修補程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a4c29-104">The MsiPatchMetadata Table contains information about a Windows Installer patch that is required to remove the patch and that is used by **Add/Remove Programs**.</span></span>

<span data-ttu-id="a4c29-105">未在修補資料庫中安裝此資料表的修補程式 ( .msp 檔) 無法移除，而且會遺失 [ **新增/移除程式**] 中的部分資訊。</span><span class="sxs-lookup"><span data-stu-id="a4c29-105">Patches installed without this table present in the patch database (.msp file) cannot be removed, and are missing some information from **Add/Remove Programs**.</span></span> <span data-ttu-id="a4c29-106">資料表必須在 patch 檔案的資料庫中，而不是在修補程式的轉換中。</span><span class="sxs-lookup"><span data-stu-id="a4c29-106">The table must be in the database of the patch file and not in a transform in the patch.</span></span>

<span data-ttu-id="a4c29-107">MsiPatchMetadata 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="a4c29-107">The MsiPatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="a4c29-108">Column</span><span class="sxs-lookup"><span data-stu-id="a4c29-108">Column</span></span>   | <span data-ttu-id="a4c29-109">類型</span><span class="sxs-lookup"><span data-stu-id="a4c29-109">Type</span></span>                         | <span data-ttu-id="a4c29-110">答案</span><span class="sxs-lookup"><span data-stu-id="a4c29-110">Key</span></span> | <span data-ttu-id="a4c29-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="a4c29-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="a4c29-112">公司</span><span class="sxs-lookup"><span data-stu-id="a4c29-112">Company</span></span>  | [<span data-ttu-id="a4c29-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="a4c29-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="a4c29-114">Y</span><span class="sxs-lookup"><span data-stu-id="a4c29-114">Y</span></span>   | <span data-ttu-id="a4c29-115">Y</span><span class="sxs-lookup"><span data-stu-id="a4c29-115">Y</span></span>        |
| <span data-ttu-id="a4c29-116">屬性</span><span class="sxs-lookup"><span data-stu-id="a4c29-116">Property</span></span> | [<span data-ttu-id="a4c29-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="a4c29-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="a4c29-118">Y</span><span class="sxs-lookup"><span data-stu-id="a4c29-118">Y</span></span>   | <span data-ttu-id="a4c29-119">N</span><span class="sxs-lookup"><span data-stu-id="a4c29-119">N</span></span>        |
| <span data-ttu-id="a4c29-120">值</span><span class="sxs-lookup"><span data-stu-id="a4c29-120">Value</span></span>    | [<span data-ttu-id="a4c29-121">Text</span><span class="sxs-lookup"><span data-stu-id="a4c29-121">Text</span></span>](text.md)             | <span data-ttu-id="a4c29-122">N</span><span class="sxs-lookup"><span data-stu-id="a4c29-122">N</span></span>   | <span data-ttu-id="a4c29-123">N</span><span class="sxs-lookup"><span data-stu-id="a4c29-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a4c29-124">資料行</span><span class="sxs-lookup"><span data-stu-id="a4c29-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a4c29-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>公司</span><span class="sxs-lookup"><span data-stu-id="a4c29-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="a4c29-126">公司名稱。</span><span class="sxs-lookup"><span data-stu-id="a4c29-126">The name of the company.</span></span> <span data-ttu-id="a4c29-127">空白欄位 (Null 值) 表示資料列包含 Windows Installer 的其中一個標準中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="a4c29-127">An empty field (a Null value) indicates that the row contains one of the standard metadata properties of the Windows Installer.</span></span> <span data-ttu-id="a4c29-128">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="a4c29-128">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="a4c29-129">藉由將資料列加入至資料表，並在此欄位中輸入公司名稱，您可以新增任何公司來擴充屬性集。</span><span class="sxs-lookup"><span data-stu-id="a4c29-129">By adding a row to the table and entering a company name in this field, you can add any company to extend the property set.</span></span>

</dd> <dt>

<span data-ttu-id="a4c29-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產</span><span class="sxs-lookup"><span data-stu-id="a4c29-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="a4c29-131">中繼資料屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4c29-131">The name of a metadata property.</span></span>

</dd> <dt>

<span data-ttu-id="a4c29-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="a4c29-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="a4c29-133">中繼資料屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a4c29-133">The value of the metadata property.</span></span> <span data-ttu-id="a4c29-134">這絕對不能是 Null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="a4c29-134">This can never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4c29-135">備註</span><span class="sxs-lookup"><span data-stu-id="a4c29-135">Remarks</span></span>

<span data-ttu-id="a4c29-136">可在 Windows Installer 3.0 和更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="a4c29-136">Available in Windows Installer 3.0 and later.</span></span>

<span data-ttu-id="a4c29-137">在 [公司名稱] 欄位中包含 Null 值的 MsiPatchMetadata 資料表中，資料列會參考下列其中一個標準 Windows Installer 中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="a4c29-137">Rows in the MsiPatchMetadata Table that contain a Null value in the CompanyName field refer to one of the following standard Windows Installer metadata properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4c29-138">屬性</span><span class="sxs-lookup"><span data-stu-id="a4c29-138">Property</span></span></th>
<th><span data-ttu-id="a4c29-139">描述</span><span class="sxs-lookup"><span data-stu-id="a4c29-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4c29-140">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="a4c29-140">AllowRemoval</span></span></td>
<td><span data-ttu-id="a4c29-141">指出修補程式是否為 <a href="uninstallable-patches.md">可卸載修補程式</a>。</span><span class="sxs-lookup"><span data-stu-id="a4c29-141">Indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="a4c29-142">如果 [值] 欄位包含 0 (零) ，就無法移除修補程式。</span><span class="sxs-lookup"><span data-stu-id="a4c29-142">If the value field contains 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="a4c29-143">如果 [值] 欄位包含一個 (1) ，則修補程式是可卸載修補程式。會註冊此屬性，並使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。</span><span class="sxs-lookup"><span data-stu-id="a4c29-143">If the value field contains one (1), the patch is an Uninstallable Patch.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4c29-144">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="a4c29-144">ManufacturerName</span></span></td>
<td><span data-ttu-id="a4c29-145">應用程式的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="a4c29-145">Name of the manufacturer of the application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4c29-146">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="a4c29-146">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="a4c29-147">表示修補程式以產品的 RTM 版本或最新的主要升級修補程式為目標。</span><span class="sxs-lookup"><span data-stu-id="a4c29-147">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="a4c29-148">在包含順序資訊的次要升級修補程式中撰寫此選用屬性，以指出修補程式會移除產品 RTM 版本的所有修補程式，或最新的主要升級修補程式。</span><span class="sxs-lookup"><span data-stu-id="a4c29-148">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="a4c29-149">這個屬性可在 Windows Installer 3.1 和更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="a4c29-149">This property is available in Windows Installer 3.1 and later.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4c29-150">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="a4c29-150">TargetProductName</span></span></td>
<td><span data-ttu-id="a4c29-151">應用程式或目標應用程式套件的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4c29-151">Name of the application or target application suite.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4c29-152">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="a4c29-152">MoreInfoURL</span></span></td>
<td><span data-ttu-id="a4c29-153">提供此修補程式特定資訊的 URL。</span><span class="sxs-lookup"><span data-stu-id="a4c29-153">A URL that provides information specific to this patch.</span></span> <span data-ttu-id="a4c29-154">這個屬性已註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。</span><span class="sxs-lookup"><span data-stu-id="a4c29-154">This property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="a4c29-155">從 Windows XP Service Pack 2 開始 (SP2) ，此值可以是 [ <strong>新增/移除程式</strong>] 中顯示之修補程式的支援連結。</span><span class="sxs-lookup"><span data-stu-id="a4c29-155">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4c29-156">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="a4c29-156">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="a4c29-157">.Msp 檔的建立時間，格式為 mm-yy HH： MM (month-day-year hour：分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="a4c29-157">Creation time of the .msp file in the form of mm-dd-yy HH:MM (month-day-year hour:minute).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4c29-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="a4c29-158">DisplayName</span></span></td>
<td><span data-ttu-id="a4c29-159">適用于公開顯示的修補程式標題。</span><span class="sxs-lookup"><span data-stu-id="a4c29-159">A title for the patch that is okay for public display.</span></span> <span data-ttu-id="a4c29-160">這個屬性會註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。</span><span class="sxs-lookup"><span data-stu-id="a4c29-160">This property is registered, and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="a4c29-161">從 Windows XP SP2 開始，此值是在 [ <strong>新增/移除程式</strong>] 中顯示之修補程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4c29-161">Beginning with Windows XP with SP2, this value is the name of the patch that is displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4c29-162">Description</span><span class="sxs-lookup"><span data-stu-id="a4c29-162">Description</span></span></td>
<td><span data-ttu-id="a4c29-163">修補程式的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="a4c29-163">Brief description of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4c29-164">分類</span><span class="sxs-lookup"><span data-stu-id="a4c29-164">Classification</span></span></td>
<td><span data-ttu-id="a4c29-165">字串值，包含由 patch 作者定義的任意更新分類。</span><span class="sxs-lookup"><span data-stu-id="a4c29-165">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="a4c29-166">例如，修補程式作者可以指定將每個修補程式分類為一個修正程式、安全性匯總、重大更新、更新、Service Pack 或更新彙總套件。</span><span class="sxs-lookup"><span data-stu-id="a4c29-166">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="a4c29-167">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="a4c29-167">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4c29-168">OptimizeCA</span><span class="sxs-lookup"><span data-stu-id="a4c29-168">OptimizeCA</span></span></td>
<td><span data-ttu-id="a4c29-169">指出 Windows Installer 是否應該在套用修補程式時略過自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a4c29-169">Indicates whether the Windows Installer should skip custom actions when applying the patch.</span></span> <span data-ttu-id="a4c29-170">這可以減少套用修補程式所需的時間。</span><span class="sxs-lookup"><span data-stu-id="a4c29-170">This can reduce the time required to apply the patch.</span></span> <span data-ttu-id="a4c29-171">OptimizeCA 屬性可以有下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="a4c29-171">The OptimizeCA property can have one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="a4c29-172">0-不要略過任何自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a4c29-172">0 - Do not skip any custom actions.</span></span></li>
<li><span data-ttu-id="a4c29-173">1-略過屬性和目錄指派自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a4c29-173">1 - Skip property and directory assignment custom actions.</span></span> <span data-ttu-id="a4c29-174"><a href="custom-action-type-35.md">自訂動作類型 35</a> 和 <a href="custom-action-type-51.md">自訂動作類型 51</a> 可以是屬性和目錄指派自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a4c29-174"><a href="custom-action-type-35.md">Custom Action Type 35</a> and <a href="custom-action-type-51.md">Custom Action Type 51</a> can be property and directory assignment custom actions.</span></span></li>
<li><span data-ttu-id="a4c29-175">2-略過不屬於屬性或目錄指派的立即自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a4c29-175">2 - Skip immediate custom actions that do not fall into the property or directory assignments.</span></span> <span data-ttu-id="a4c29-176">立即自訂動作不會在 <a href="customaction-table.md">CustomAction 資料表</a>的 Type 資料行中包含 msidbCustomActionTypeInScript 選項。</span><span class="sxs-lookup"><span data-stu-id="a4c29-176">The immediate custom actions do not include msidbCustomActionTypeInScript option in the Type column of the <a href="customaction-table.md">CustomAction Table</a>.</span></span></li>
<li><span data-ttu-id="a4c29-177">4-略過腳本內執行的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a4c29-177">4 - Skip custom actions that run within the script.</span></span></li>
</ul>
<span data-ttu-id="a4c29-178">所有要安裝的修補程式或未略過自訂動作的 OptimizeCA 值都必須相同。</span><span class="sxs-lookup"><span data-stu-id="a4c29-178">The value of OptimizeCA must be the same for all patches that are being installed or no custom actions are skipped.</span></span> <span data-ttu-id="a4c29-179">例如，如果安裝了兩個修補程式，且 OptimizeCA 分別設定為值1和2，則不會略過任何自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a4c29-179">For example, if two patches are being installed, and OptimizeCA is set to the values 1 and 2 respectively, no custom actions are skipped.</span></span> <br/> <span data-ttu-id="a4c29-180">處理多個新的修補程式時，可以結合 OptimizeCA 的值。</span><span class="sxs-lookup"><span data-stu-id="a4c29-180">The values of OptimizeCA can be combined when processing multiple new patches.</span></span> <span data-ttu-id="a4c29-181">如果所有修補程式都有 1 (值中包含一個) ，則會略過所有屬性和目錄指派自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a4c29-181">If all patches have a 1 (one) included in the values, then all property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="a4c29-182">如果某個修補程式的屬性值為 3 (三個) ，其中一個修補程式的值為 1 (一個屬性) ，則會略過屬性和目錄指派自訂動作。</span><span class="sxs-lookup"><span data-stu-id="a4c29-182">If one patch has the value 3 (three)for the property, and one patch has the value 1 (one) for the property, the property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="a4c29-183">不過，其他立即的自訂動作會執行，因為並非所有要求的修補程式都會略過。</span><span class="sxs-lookup"><span data-stu-id="a4c29-183">However, the other immediate custom actions run, because not all of the patches requested are skipped.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4c29-184">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="a4c29-184">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="a4c29-185">如果這個屬性設定為 1 (要在交易中套用的所有修補程式中的一個) ，則會盡可能將修補程式的應用程式優化。</span><span class="sxs-lookup"><span data-stu-id="a4c29-185">If this property is set to 1 (one) in all the patches to be applied in a transaction, an application of the patch is optimized if possible.</span></span> <span data-ttu-id="a4c29-186">如需詳細資訊，請參閱 <a href="patch-optimization.md">修補程式優化</a>。</span><span class="sxs-lookup"><span data-stu-id="a4c29-186">For more information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="a4c29-187">從 Windows Installer 3.1 開始提供。</span><span class="sxs-lookup"><span data-stu-id="a4c29-187">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a><span data-ttu-id="a4c29-188">驗證</span><span class="sxs-lookup"><span data-stu-id="a4c29-188">Validation</span></span>

<dl>

[<span data-ttu-id="a4c29-189">ICE03</span><span class="sxs-lookup"><span data-stu-id="a4c29-189">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a4c29-190">ICE06</span><span class="sxs-lookup"><span data-stu-id="a4c29-190">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="a4c29-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4c29-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4c29-192">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="a4c29-192">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




