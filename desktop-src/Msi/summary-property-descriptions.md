---
description: 下表說明安裝套件、轉換和修補程式的摘要屬性。
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: 摘要屬性描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980042"
---
# <a name="summary-property-descriptions"></a><span data-ttu-id="a978a-103">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="a978a-103">Summary Property Descriptions</span></span>

<span data-ttu-id="a978a-104">下表說明安裝套件、轉換和修補程式的摘要屬性。</span><span class="sxs-lookup"><span data-stu-id="a978a-104">Summary properties for installation packages, transforms, and patches are described in the following tables.</span></span> <span data-ttu-id="a978a-105">請注意，根據資料庫屬於安裝封裝、轉換或修補封裝，特定摘要屬性的意義可能會不同。</span><span class="sxs-lookup"><span data-stu-id="a978a-105">Note that the meaning of a particular summary property can be different depending on whether the database belongs to an installation package, transform, or patch package.</span></span> <span data-ttu-id="a978a-106">如需屬性識別碼、Pid 和類型的詳細資訊，請參閱 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md)。</span><span class="sxs-lookup"><span data-stu-id="a978a-106">For more information about the property IDs, PIDs, and types, see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

## <a name="installation-packages"></a><span data-ttu-id="a978a-107">安裝套件</span><span class="sxs-lookup"><span data-stu-id="a978a-107">Installation Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a978a-108">摘要屬性</span><span class="sxs-lookup"><span data-stu-id="a978a-108">Summary property</span></span></th>
<th><span data-ttu-id="a978a-109">此屬性在安裝資料庫中的意義</span><span class="sxs-lookup"><span data-stu-id="a978a-109">Meaning of this property in an Installation database</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a978a-110"><a href="title-summary.md"><strong>標題</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-110"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="a978a-111">此檔案的描述做為安裝套件。</span><span class="sxs-lookup"><span data-stu-id="a978a-111">A description of this file as an installation package.</span></span> <span data-ttu-id="a978a-112">描述應該包含片語 &quot; <a href="about-the-installer-database.md">安裝資料庫</a>。&quot;</span><span class="sxs-lookup"><span data-stu-id="a978a-112">The description should include the phrase &quot;<a href="about-the-installer-database.md">Installation Database</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-113"><a href="subject-summary.md"><strong>主體</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-113"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="a978a-114">此封裝所安裝之產品的名稱。</span><span class="sxs-lookup"><span data-stu-id="a978a-114">The name of the product installed by this package.</span></span> <span data-ttu-id="a978a-115">這應該與 <a href="productname.md"><strong>ProductName</strong></a> 屬性中的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="a978a-115">This should be the same name as in the <a href="productname.md"><strong>ProductName</strong></a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-116"><a href="author-summary.md"><strong>作者</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-116"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="a978a-117">此產品的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="a978a-117">The name of the manufacturer of this product.</span></span> <span data-ttu-id="a978a-118">這應該與 [ <a href="manufacturer.md"><strong>製造商</strong></a> ] 屬性中的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="a978a-118">This should be the same name as in the <a href="manufacturer.md"><strong>Manufacturer</strong></a> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-119"><a href="keywords-summary.md"><strong>關鍵字</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-119"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="a978a-120">檔案瀏覽器可以用來對檔案進行關鍵字搜尋的關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="a978a-120">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="a978a-121">關鍵字應該包含 &quot; 安裝程式以及 &quot; 產品特定關鍵字。</span><span class="sxs-lookup"><span data-stu-id="a978a-121">The keywords should include &quot;Installer&quot; as well as product-specific keywords.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-122"><a href="comments-summary.md"><strong>註解</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-122"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="a978a-123">包含片語： &quot; 此安裝程式資料庫包含安裝 <<em>產品名稱</em>所需的邏輯和資料 > 。&quot;</span><span class="sxs-lookup"><span data-stu-id="a978a-123">Contains the phrase: &quot;This installer database contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-124"><a href="template-summary.md"><strong>範本</strong></a> (必要) </span><span class="sxs-lookup"><span data-stu-id="a978a-124"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="a978a-125">與此安裝套件相容的平臺和語言。</span><span class="sxs-lookup"><span data-stu-id="a978a-125">The platform and languages compatible with this installation package.</span></span> <span data-ttu-id="a978a-126">請參閱語法的 <a href="template-summary.md"><strong>範本</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="a978a-126">See <a href="template-summary.md"><strong>Template</strong></a> for syntax.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-127"><a href="last-saved-by-summary.md"><strong>上次儲存者</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-127"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="a978a-128">資料庫編輯工具的開發人員可能會在開發程式中使用這個屬性，來追蹤最後一個修改安裝資料庫的人員。</span><span class="sxs-lookup"><span data-stu-id="a978a-128">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="a978a-129">在最後的出貨資料庫中，這個屬性應該設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="a978a-129">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="a978a-130">安裝程式會在<a href="administrative-installation.md"><strong>系統管理安裝</strong></a>期間將此屬性設為<a href="logonuser.md"><strong>LogonUser</strong></a>屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a978a-130">The installer sets this property to the value of the <a href="logonuser.md"><strong>LogonUser</strong></a> property during an <a href="administrative-installation.md"><strong>administrative installation</strong></a>.</span></span> <span data-ttu-id="a978a-131">安裝程式永遠不會使用這個屬性，而且使用者永遠不需要修改它。</span><span class="sxs-lookup"><span data-stu-id="a978a-131">The installer never uses this property and a user never needs to modify it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-132"> (必要的<a href="revision-number-summary.md"><strong>修訂編號</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="a978a-132"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="a978a-133">包含安裝程式套件的 <a href="package-codes.md">封裝程式碼</a> 。</span><span class="sxs-lookup"><span data-stu-id="a978a-133">Contains the <a href="package-codes.md">package code</a> for the installer package.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-134"><a href="last-printed-summary.md"><strong>前次列印時間</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-134"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="a978a-135">可以設定為 <a href="administrative-installation.md">系統管理安裝</a> 期間的日期和時間，以在建立系統管理映射時錄製。</span><span class="sxs-lookup"><span data-stu-id="a978a-135">May be set to the date and time during an <a href="administrative-installation.md">administrative installation</a> to record when the administrative image was created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-136"><a href="create-time-date-summary.md"><strong>建立時間/日期</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-136"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="a978a-137">此安裝程式資料庫的建立時間和日期。</span><span class="sxs-lookup"><span data-stu-id="a978a-137">The time and date when this installer database was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-138"><a href="last-saved-time-date-summary.md"><strong>上次儲存的時間/日期</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-138"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="a978a-139">上次儲存安裝程式資料庫時的目前系統時間和日期。</span><span class="sxs-lookup"><span data-stu-id="a978a-139">The current system time and date at the time the installer database was last saved.</span></span> <span data-ttu-id="a978a-140">一開始是 null。</span><span class="sxs-lookup"><span data-stu-id="a978a-140">Initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-141">需要 (<a href="page-count-summary.md"><strong>頁面計數</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="a978a-141"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="a978a-142">包含用來識別此安裝套件所需之最小安裝程式版本的值。</span><span class="sxs-lookup"><span data-stu-id="a978a-142">Contains a value used to identify the minimum installer version required by this installation package.</span></span> <span data-ttu-id="a978a-143">例如，如果封裝至少需要2.0 版的安裝程式，則此屬性應該設定為200的整數。</span><span class="sxs-lookup"><span data-stu-id="a978a-143">For example, if the package requires at minimum the 2.0 version of the installer, this property should be set to an integer of 200.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a978a-144">這個屬性的值必須是200或更高的 <a href="64-bit-windows-installer-packages.md">64 位 Windows Installer 套件</a>。</span><span class="sxs-lookup"><span data-stu-id="a978a-144">The value of this property must be 200 or greater with <a href="64-bit-windows-installer-packages.md">64-bit Windows Installer Packages</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-145">需要 (<a href="word-count-summary.md"><strong>字數統計</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="a978a-145"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="a978a-146">來源檔案映射的類型。</span><span class="sxs-lookup"><span data-stu-id="a978a-146">The type of the source file image.</span></span> <span data-ttu-id="a978a-147">儲存以取代標準計數屬性。</span><span class="sxs-lookup"><span data-stu-id="a978a-147">Stored in place of the standard Count property.</span></span> <span data-ttu-id="a978a-148">這個屬性是位欄位。</span><span class="sxs-lookup"><span data-stu-id="a978a-148">This property is a bit field.</span></span> <span data-ttu-id="a978a-149">請參閱 [ <a href="word-count-summary.md"><strong>字數統計</strong></a> ] 主題以取得值。</span><span class="sxs-lookup"><span data-stu-id="a978a-149">See the <a href="word-count-summary.md"><strong>Word Count</strong></a> topic for the values.</span></span><br/> <span data-ttu-id="a978a-150">從 Windows Vista 上的 Windows Installer 4.0 版開始，這個屬性會包含用來指定是否需要提升許可權的位。</span><span class="sxs-lookup"><span data-stu-id="a978a-150">Starting with Windows Installer version 4.0 on Windows Vista, this property includes bits to specify whether elevated privileges are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-151"><a href="character-count-summary.md"><strong>字元計數</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-151"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="a978a-152">Null</span><span class="sxs-lookup"><span data-stu-id="a978a-152">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-153"><a href="creating-application-summary.md"><strong>正在建立應用程式</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-153"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="a978a-154">包含用來撰寫此安裝資料庫之軟體的名稱。</span><span class="sxs-lookup"><span data-stu-id="a978a-154">Contains the name of the software used to author this installation database.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-155"><a href="security-summary.md"><strong>安全性</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-155"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="a978a-156">這個屬性的值應該是2建議的唯讀。</span><span class="sxs-lookup"><span data-stu-id="a978a-156">The value of this property should be 2 - Recommended read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-157"><a href="codepage-summary.md"><strong>字碼頁</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-157"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="a978a-158">用來顯示摘要資訊的 ANSI 字碼頁數值。</span><span class="sxs-lookup"><span data-stu-id="a978a-158">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="a978a-159">在摘要資訊中設定任何字串屬性之前，必須先設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a978a-159">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a><span data-ttu-id="a978a-160">轉換</span><span class="sxs-lookup"><span data-stu-id="a978a-160">Transforms</span></span>



| <span data-ttu-id="a978a-161">摘要屬性</span><span class="sxs-lookup"><span data-stu-id="a978a-161">Summary property</span></span>                                              | <span data-ttu-id="a978a-162">轉換中這個屬性的意義</span><span class="sxs-lookup"><span data-stu-id="a978a-162">Meaning of this property in a Transform</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a978a-163">**標題**</span><span class="sxs-lookup"><span data-stu-id="a978a-163">**Title**</span></span>](title-summary.md)                                | <span data-ttu-id="a978a-164">這個檔案做為轉換的描述。</span><span class="sxs-lookup"><span data-stu-id="a978a-164">A description of this file as a transform.</span></span> <span data-ttu-id="a978a-165">描述應該包含「[轉換](database-transforms.md)」這個片語。</span><span class="sxs-lookup"><span data-stu-id="a978a-165">The description should include the phrase: "[Transform](database-transforms.md)."</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="a978a-166">**主體**</span><span class="sxs-lookup"><span data-stu-id="a978a-166">**Subject**</span></span>](subject-summary.md)                            | <span data-ttu-id="a978a-167">原始安裝套件所安裝的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="a978a-167">The name of the product installed by the original installation package.</span></span> <span data-ttu-id="a978a-168">這應該與原始安裝套件中的 [主旨 [**摘要**](subject-summary.md) ] 屬性值相同。</span><span class="sxs-lookup"><span data-stu-id="a978a-168">This should be the same value as the [**Subject Summary**](subject-summary.md) property in the original installation package.</span></span>                                                                                            |
| [<span data-ttu-id="a978a-169">**作者**</span><span class="sxs-lookup"><span data-stu-id="a978a-169">**Author**</span></span>](author-summary.md)                              | <span data-ttu-id="a978a-170">此轉換的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="a978a-170">The name of the manufacturer of this transform.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="a978a-171">**關鍵字**</span><span class="sxs-lookup"><span data-stu-id="a978a-171">**Keywords**</span></span>](keywords-summary.md)                          | <span data-ttu-id="a978a-172">檔案瀏覽器可以用來對檔案進行關鍵字搜尋的關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="a978a-172">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="a978a-173">關鍵字應該包含「安裝程式」，以及產品特定的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="a978a-173">The keywords should include "Installer" as well as product-specific keywords.</span></span>                                                                                                                             |
| [<span data-ttu-id="a978a-174">**註解**</span><span class="sxs-lookup"><span data-stu-id="a978a-174">**Comments**</span></span>](comments-summary.md)                          | <span data-ttu-id="a978a-175">包含片語：「此轉換包含安裝 <*產品名稱*> 所需的邏輯和資料。」</span><span class="sxs-lookup"><span data-stu-id="a978a-175">Contains the phrase: "This transform contains the logic and data required to install <*product name*>."</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="a978a-176">[**範本**](template-summary.md) (必要) </span><span class="sxs-lookup"><span data-stu-id="a978a-176">[**Template**](template-summary.md) (REQUIRED)</span></span>               | <span data-ttu-id="a978a-177">與此轉換相容的平臺和語言版本。</span><span class="sxs-lookup"><span data-stu-id="a978a-177">The platform and language versions compatible with this transform.</span></span> <span data-ttu-id="a978a-178">如果沒有任何限制，此值可以保留空白。</span><span class="sxs-lookup"><span data-stu-id="a978a-178">This value may be left blank if there are no restrictions.</span></span> <span data-ttu-id="a978a-179">只能為轉換指定一種語言。</span><span class="sxs-lookup"><span data-stu-id="a978a-179">Only one language can be specified for a transform.</span></span> <span data-ttu-id="a978a-180">如需語法的詳細資訊，請參閱 [**範本**](template-summary.md)。</span><span class="sxs-lookup"><span data-stu-id="a978a-180">For more information about the syntax, see [**Template**](template-summary.md).</span></span>                                |
| [<span data-ttu-id="a978a-181">**上次儲存者**</span><span class="sxs-lookup"><span data-stu-id="a978a-181">**Last Saved By**</span></span>](last-saved-by-summary.md)                | <span data-ttu-id="a978a-182">在資料庫轉換之後， (s 的平臺和語言識別項) 。</span><span class="sxs-lookup"><span data-stu-id="a978a-182">The platform and language ID(s) that the database has after it has been transformed.</span></span> <span data-ttu-id="a978a-183">新資料庫中的 [ [**範本摘要**](template-summary.md) ] 屬性應該設定為相同的值。</span><span class="sxs-lookup"><span data-stu-id="a978a-183">The [**Template Summary**](template-summary.md) property in the new database should be set to the same values.</span></span>                                                                                              |
| <span data-ttu-id="a978a-184"> (必要的 [**修訂編號**](revision-number-summary.md)) </span><span class="sxs-lookup"><span data-stu-id="a978a-184">[**Revision Number**](revision-number-summary.md) (REQUIRED)</span></span> | <span data-ttu-id="a978a-185">新的和原始產品的產品代碼 Guid 和版本清單，以及升級程式碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="a978a-185">A list of the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="a978a-186">清單會以分號分隔，如下所示。</span><span class="sxs-lookup"><span data-stu-id="a978a-186">The list is separated by semicolons as follows.</span></span> <span data-ttu-id="a978a-187">*原始產品-程式碼原始-版本*;*新產品程式碼新產品-版本*; *升級-程式碼*</span><span class="sxs-lookup"><span data-stu-id="a978a-187">*Original-Product-Code Original-Product-Version*;*New-Product Code New-Product-Version*; *Upgrade-Code*</span></span><br/>                       |
| [<span data-ttu-id="a978a-188">**前次列印時間**</span><span class="sxs-lookup"><span data-stu-id="a978a-188">**Last Printed**</span></span>](last-printed-summary.md)                  | <span data-ttu-id="a978a-189">Null</span><span class="sxs-lookup"><span data-stu-id="a978a-189">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="a978a-190">**建立時間/日期**</span><span class="sxs-lookup"><span data-stu-id="a978a-190">**Create Time/Date**</span></span>](create-time-date-summary.md)          | <span data-ttu-id="a978a-191">建立轉換的時間和日期。</span><span class="sxs-lookup"><span data-stu-id="a978a-191">The time and date when the transform was created.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a978a-192">**上次儲存的時間/日期**</span><span class="sxs-lookup"><span data-stu-id="a978a-192">**Last Saved Time/Date**</span></span>](last-saved-time-date-summary.md)  | <span data-ttu-id="a978a-193">儲存轉換時目前的系統時間和日期。</span><span class="sxs-lookup"><span data-stu-id="a978a-193">The current system time and date at the time the transform was saved.</span></span> <span data-ttu-id="a978a-194">一開始是 null。</span><span class="sxs-lookup"><span data-stu-id="a978a-194">Initially null.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="a978a-195">需要 ([**頁面計數**](page-count-summary.md)) </span><span class="sxs-lookup"><span data-stu-id="a978a-195">[**Page Count**](page-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="a978a-196">值，用來指出處理轉換所需的最低安裝程式版本。</span><span class="sxs-lookup"><span data-stu-id="a978a-196">A value used to indicate the minimum installer version required to process the transform.</span></span> <span data-ttu-id="a978a-197">此值應該設定為屬於用來產生轉換之資料庫的兩個 [**頁面計數**](page-count-summary.md) 屬性值的最大值。</span><span class="sxs-lookup"><span data-stu-id="a978a-197">The value should be set to the greater of the two [**Page Count**](page-count-summary.md) property values that belong to the databases used to generate the transform.</span></span>                                 |
| <span data-ttu-id="a978a-198">需要 ([**字數統計**](word-count-summary.md)) </span><span class="sxs-lookup"><span data-stu-id="a978a-198">[**Word Count**](word-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="a978a-199">Null</span><span class="sxs-lookup"><span data-stu-id="a978a-199">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="a978a-200">**字元計數**</span><span class="sxs-lookup"><span data-stu-id="a978a-200">**Character Count**</span></span>](character-count-summary.md)            | <span data-ttu-id="a978a-201">摘要資訊資料流程的這個部分分成 2 16 位單字。</span><span class="sxs-lookup"><span data-stu-id="a978a-201">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="a978a-202">上方文字包含 [*轉換驗證旗標*](t-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a978a-202">The upper word contains [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="a978a-203">下方的單字包含 [*轉換錯誤條件旗標*](t-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a978a-203">Lower word contains [*transform error condition flags*](t-gly.md).</span></span> |
| [<span data-ttu-id="a978a-204">**正在建立應用程式**</span><span class="sxs-lookup"><span data-stu-id="a978a-204">**Creating Application**</span></span>](creating-application-summary.md)  | <span data-ttu-id="a978a-205">包含用來建立此轉換之軟體的名稱。</span><span class="sxs-lookup"><span data-stu-id="a978a-205">Contains the name of the software used to create this transform.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="a978a-206">**安全性**</span><span class="sxs-lookup"><span data-stu-id="a978a-206">**Security**</span></span>](security-summary.md)                          | <span data-ttu-id="a978a-207">這個屬性的值應該是4強制的唯讀。</span><span class="sxs-lookup"><span data-stu-id="a978a-207">The value of this property should be 4 - Enforced read-only.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="a978a-208">**字碼頁**</span><span class="sxs-lookup"><span data-stu-id="a978a-208">**Codepage**</span></span>](codepage-summary.md)                          | <span data-ttu-id="a978a-209">用來顯示摘要資訊的 ANSI 字碼頁數值。</span><span class="sxs-lookup"><span data-stu-id="a978a-209">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="a978a-210">必須先設定這個屬性，才能在摘要資訊中設定任何字串屬性。</span><span class="sxs-lookup"><span data-stu-id="a978a-210">This property must be set before any string properties can be set in the summary information.</span></span>                                                                                                                    |



 

## <a name="patch-packages"></a><span data-ttu-id="a978a-211">修補套件</span><span class="sxs-lookup"><span data-stu-id="a978a-211">Patch Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a978a-212">摘要屬性</span><span class="sxs-lookup"><span data-stu-id="a978a-212">Summary property</span></span></th>
<th><span data-ttu-id="a978a-213">修補程式套件中這個屬性的意義</span><span class="sxs-lookup"><span data-stu-id="a978a-213">Meaning of this property in a Patch package</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a978a-214"><a href="title-summary.md"><strong>標題</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-214"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="a978a-215">此檔案作為修補封裝的描述。</span><span class="sxs-lookup"><span data-stu-id="a978a-215">A description of this file as a patch package.</span></span> <span data-ttu-id="a978a-216">描述應該包含片語： &quot; <a href="patch-packages.md">Patch</a>。&quot;</span><span class="sxs-lookup"><span data-stu-id="a978a-216">The description should include the phrase: &quot;<a href="patch-packages.md">Patch</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-217"><a href="subject-summary.md"><strong>主體</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-217"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="a978a-218">包含產品名稱之修補程式的描述。</span><span class="sxs-lookup"><span data-stu-id="a978a-218">A description of the patch that includes the name of the product.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-219"><a href="author-summary.md"><strong>作者</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-219"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="a978a-220">Patch 封裝的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="a978a-220">The name of the manufacturer of the patch package.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-221"><a href="keywords-summary.md"><strong>關鍵字</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-221"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="a978a-222">以分號分隔的修補程式來源清單。</span><span class="sxs-lookup"><span data-stu-id="a978a-222">A semicolon delimited list of sources of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-223"><a href="comments-summary.md"><strong>註解</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-223"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="a978a-224">包含片語： &quot; 此修補套裝程式含安裝 <<em>產品名稱</em>所需的邏輯和資料 > 。&quot;</span><span class="sxs-lookup"><span data-stu-id="a978a-224">Contains the phrase: &quot;This patch contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-225"><a href="template-summary.md"><strong>範本</strong></a> (必要) </span><span class="sxs-lookup"><span data-stu-id="a978a-225"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="a978a-226">以分號分隔的產品代碼清單，可接受此修補程式。</span><span class="sxs-lookup"><span data-stu-id="a978a-226">A semicolon delimited list of the product codes that can accept this patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-227"><a href="last-saved-by-summary.md"><strong>上次儲存者</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-227"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="a978a-228">以分號分隔的轉換 substorage 名稱清單（以這個修補程式套用的順序排列）。</span><span class="sxs-lookup"><span data-stu-id="a978a-228">A semicolon delimited list of transform substorage names in the order they are applied by this patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-229"> (必要的<a href="revision-number-summary.md"><strong>修訂編號</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="a978a-229"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="a978a-230">包含修補程式的 GUID 修補程式碼。</span><span class="sxs-lookup"><span data-stu-id="a978a-230">Contains the GUID patch code for the patch.</span></span> <span data-ttu-id="a978a-231">之後可能會有修補程式的程式碼 Guid 清單，這些修補程式會在套用此修補程式時移除。</span><span class="sxs-lookup"><span data-stu-id="a978a-231">This may be followed by a list of patch code GUIDs for patches that are removed when this patch is applied.</span></span> <span data-ttu-id="a978a-232">系統會串連修補程式碼，而不使用分隔符號分隔清單中的 Guid。</span><span class="sxs-lookup"><span data-stu-id="a978a-232">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a978a-233">如果 patch 套件包含 <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> 資料表，修補程式不會移除目前修補程式的 GUID 之後所列的修補程式。</span><span class="sxs-lookup"><span data-stu-id="a978a-233">If the patch package contains a <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> table, the patch does not remove patches listed after the current patch's GUID.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-234"><a href="last-printed-summary.md"><strong>前次列印時間</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-234"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="a978a-235">Null</span><span class="sxs-lookup"><span data-stu-id="a978a-235">Null</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-236"><a href="create-time-date-summary.md"><strong>建立時間/日期</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-236"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="a978a-237">建立修補檔案的時間和日期。</span><span class="sxs-lookup"><span data-stu-id="a978a-237">The time and date when patch file was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-238"><a href="last-saved-time-date-summary.md"><strong>上次儲存的時間/日期</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-238"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="a978a-239">儲存修補程式套件時的目前系統時間和日期。</span><span class="sxs-lookup"><span data-stu-id="a978a-239">The current system time and date at the time the patch package was saved.</span></span> <span data-ttu-id="a978a-240">此值一開始是 null。</span><span class="sxs-lookup"><span data-stu-id="a978a-240">This value is initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-241">需要 (<a href="page-count-summary.md"><strong>頁面計數</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="a978a-241"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="a978a-242">Null</span><span class="sxs-lookup"><span data-stu-id="a978a-242">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-243">需要 (<a href="word-count-summary.md"><strong>字數統計</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="a978a-243"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="a978a-244">包含值，指出安裝修補程式所需的最小 Windows Installer 版本。</span><span class="sxs-lookup"><span data-stu-id="a978a-244">Contains a value that indicates the minimum Windows Installer version that is required to install the patch.</span></span> <span data-ttu-id="a978a-245">文字計數值為4的 patch 需要 Windows Installer 3.0 版或更高版本，才能套用修補程式。</span><span class="sxs-lookup"><span data-stu-id="a978a-245">A patch with a word count value of 4 requires Windows Installer version 3.0 or higher for the patch to be applied.</span></span> <span data-ttu-id="a978a-246">值為3表示需要 Windows Installer 版本2.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a978a-246">A value of 3 indicates that Windows Installer version 2.0 or higher is required.</span></span> <span data-ttu-id="a978a-247">值為2表示需要 Windows Installer 版本1.2 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a978a-247">A value of 2 indicates that Windows Installer version 1.2 or higher is required.</span></span> <span data-ttu-id="a978a-248">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="a978a-248">The default value is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-249"><a href="character-count-summary.md"><strong>字元計數</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-249"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="a978a-250">Null</span><span class="sxs-lookup"><span data-stu-id="a978a-250">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-251"><a href="creating-application-summary.md"><strong>正在建立應用程式</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-251"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="a978a-252">用來建立修補程式的軟體名稱。</span><span class="sxs-lookup"><span data-stu-id="a978a-252">The name of the software used to create the patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a978a-253"><a href="security-summary.md"><strong>安全性</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-253"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="a978a-254">這個屬性的值應該是4強制的唯讀。</span><span class="sxs-lookup"><span data-stu-id="a978a-254">The value of this property should be 4 - Enforced read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a978a-255"><a href="codepage-summary.md"><strong>字碼頁</strong></a></span><span class="sxs-lookup"><span data-stu-id="a978a-255"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="a978a-256">用來顯示摘要資訊的 ANSI 字碼頁數值。</span><span class="sxs-lookup"><span data-stu-id="a978a-256">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="a978a-257">在摘要資訊中設定任何字串屬性之前，必須先設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a978a-257">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




