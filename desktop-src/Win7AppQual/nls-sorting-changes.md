---
description: NLS 排序變更
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: NLS 排序變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57cfaf2a9891c2d952637429786729670fc103c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088056"
---
# <a name="nls-sorting-changes"></a><span data-ttu-id="799d3-103">NLS 排序變更</span><span class="sxs-lookup"><span data-stu-id="799d3-103">NLS Sorting Changes</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="799d3-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="799d3-104">Affected Platforms</span></span>

 <span data-ttu-id="799d3-105">**客戶** 端-windows XP、windows Vista、windows 7</span><span class="sxs-lookup"><span data-stu-id="799d3-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="799d3-106">**伺服器** -windows server 2003、windows server 2008、windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="799d3-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="799d3-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="799d3-107">Feature Impact</span></span>

 <span data-ttu-id="799d3-108">**嚴重性** -高</span><span class="sxs-lookup"><span data-stu-id="799d3-108">**Severity** - High</span></span>  
<span data-ttu-id="799d3-109">**頻率** -低 (少數應用程式受到影響，但如果受到影響，一律會中斷) </span><span class="sxs-lookup"><span data-stu-id="799d3-109">**Frequency** - Low (few apps impacted, but if impacted, always broken)</span></span>  


## <a name="description"></a><span data-ttu-id="799d3-110">Description</span><span class="sxs-lookup"><span data-stu-id="799d3-110">Description</span></span>

<span data-ttu-id="799d3-111"> (NLS) 函式的國家語言支援可協助應用程式支援世界各地使用者的不同語言和地區設定特定需求。</span><span class="sxs-lookup"><span data-stu-id="799d3-111">The National Language Support (NLS) functions help applications support the different language- and locale-specific needs of users around the world.</span></span> <span data-ttu-id="799d3-112">新的 Windows 版本幾乎都包含 NLS 變更。</span><span class="sxs-lookup"><span data-stu-id="799d3-112">New Windows versions almost invariably include NLS changes.</span></span> <span data-ttu-id="799d3-113">此變更會影響定序和排序，因此具有持續性索引的應用程式。</span><span class="sxs-lookup"><span data-stu-id="799d3-113">This change affects collation and sorting, and therefore applications that have persistent indexes.</span></span>

<span data-ttu-id="799d3-114">定序資料表有兩個數字，可識別其版本 (修訂) ：已定義的版本和 NLS 版本。</span><span class="sxs-lookup"><span data-stu-id="799d3-114">A collation table has two numbers that identify its version (revision): the defined version and the NLS version.</span></span> <span data-ttu-id="799d3-115">這兩個版本都是 DWORD 值，由主要版本和次要版本所組成。</span><span class="sxs-lookup"><span data-stu-id="799d3-115">Both versions are DWORD values, composed of a major version and a minor version.</span></span> <span data-ttu-id="799d3-116">值的第一個位元組是保留的，接下來的兩個位元組代表主要版本，而最後一個位元組代表次要版本。</span><span class="sxs-lookup"><span data-stu-id="799d3-116">The first byte of a value is reserved, the next two bytes represent the major version, and the last byte represents the minor version.</span></span> <span data-ttu-id="799d3-117">以十六進位詞彙來說，此模式為0xRRMMMMmm，其中 R 等於 Reserved、M 等於主要，而 m 等於次要。</span><span class="sxs-lookup"><span data-stu-id="799d3-117">In hexadecimal terms, the pattern is 0xRRMMMMmm, where R equals Reserved, M equals major, and m equals minor.</span></span> <span data-ttu-id="799d3-118">例如，次要版本為4的主要版本3會以0x304 表示。</span><span class="sxs-lookup"><span data-stu-id="799d3-118">For example, a major version of 3 with a minor version of 4 is represented as 0x304.</span></span>

<span data-ttu-id="799d3-119">針對主要版本，有一或多個程式碼點變更，讓應用程式必須重新為所有資料重新編制索引，以便讓比較有效。</span><span class="sxs-lookup"><span data-stu-id="799d3-119">For a major version, one or more code points change so that the application must re-index all data for comparisons to be valid.</span></span> <span data-ttu-id="799d3-120">針對次要版本，不會移動任何專案，但會新增程式碼點。</span><span class="sxs-lookup"><span data-stu-id="799d3-120">For a minor version, nothing moves, but code points are added.</span></span> <span data-ttu-id="799d3-121">針對此類型的版本，應用程式只需要使用先前不可排序的值來重新編制字串的索引。</span><span class="sxs-lookup"><span data-stu-id="799d3-121">For this type of version, the application only has to re-index strings with previously unsortable values.</span></span> <span data-ttu-id="799d3-122">總而言之，與地區設定特定的例外狀況資料表和預設資料表中的資料變更有關，版本號碼的意義如下：</span><span class="sxs-lookup"><span data-stu-id="799d3-122">In summary, here is what the version numbers mean in relation to the data changes in the locale-specific exception tables and default tables:</span></span>

<span data-ttu-id="799d3-123">**NLSVersion 主要** –變更「例外狀況」中的程式碼點或地區設定特定的資料表</span><span class="sxs-lookup"><span data-stu-id="799d3-123">**NLSVersion Major** – Changed code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="799d3-124">**NLSVersion 次要** -在「例外狀況」或地區設定特有的資料表中加入新的程式碼點</span><span class="sxs-lookup"><span data-stu-id="799d3-124">**NLSVersion Minor** – Added new code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="799d3-125">**DefinedVersion 主要** -變更預設表格中的程式碼點</span><span class="sxs-lookup"><span data-stu-id="799d3-125">**DefinedVersion Major** – Changed code points in the default table</span></span>  
<span data-ttu-id="799d3-126">**DefinedVersion 次要** -在預設資料表中加入新的程式碼點</span><span class="sxs-lookup"><span data-stu-id="799d3-126">**DefinedVersion Minor** – Added new code points in the default table</span></span>  


<span data-ttu-id="799d3-127">**排序發行版本的版本號碼：**</span><span class="sxs-lookup"><span data-stu-id="799d3-127">**Sorting version numbers for released versions:**</span></span>



| <span data-ttu-id="799d3-128">作業系統</span><span class="sxs-lookup"><span data-stu-id="799d3-128">Operating System</span></span>    | <span data-ttu-id="799d3-129">版本</span><span class="sxs-lookup"><span data-stu-id="799d3-129">Release</span></span>           | <span data-ttu-id="799d3-130">版本 (0xRRMMMMmm) </span><span class="sxs-lookup"><span data-stu-id="799d3-130">Version (0xRRMMMMmm)</span></span>         |
|---------------------|-------------------|------------------------------|
| <span data-ttu-id="799d3-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="799d3-131">Windows XP</span></span>          | <span data-ttu-id="799d3-132">RTM/SP1/SP2/SP3/.。。</span><span class="sxs-lookup"><span data-stu-id="799d3-132">RTM/SP1/SP2/SP3/…</span></span> | <span data-ttu-id="799d3-133">N/A-無 GetNLSVersion () API</span><span class="sxs-lookup"><span data-stu-id="799d3-133">N/A - no GetNLSVersion() API</span></span> |
| <span data-ttu-id="799d3-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="799d3-134">Windows Server 2003</span></span> | <span data-ttu-id="799d3-135">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="799d3-135">RTM/SP1</span></span>           | <span data-ttu-id="799d3-136">0x00 0000 01</span><span class="sxs-lookup"><span data-stu-id="799d3-136">0x00 0000 01</span></span>                 |
| <span data-ttu-id="799d3-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="799d3-137">Windows Vista</span></span>       | <span data-ttu-id="799d3-138">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="799d3-138">RTM/SP1</span></span>           | <span data-ttu-id="799d3-139">0x00 0405 00</span><span class="sxs-lookup"><span data-stu-id="799d3-139">0x00 0405 00</span></span>                 |
| <span data-ttu-id="799d3-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="799d3-140">Windows Server 2008</span></span> | <span data-ttu-id="799d3-141">RTM</span><span class="sxs-lookup"><span data-stu-id="799d3-141">RTM</span></span>               | <span data-ttu-id="799d3-142">0x00 0501 00/0x00 5001 00</span><span class="sxs-lookup"><span data-stu-id="799d3-142">0x00 0501 00 / 0x00 5001 00</span></span>  |
| <span data-ttu-id="799d3-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="799d3-143">Windows 7</span></span>           | <span data-ttu-id="799d3-144">RTM</span><span class="sxs-lookup"><span data-stu-id="799d3-144">RTM</span></span>               | <span data-ttu-id="799d3-145">0x00060100</span><span class="sxs-lookup"><span data-stu-id="799d3-145">0x00060100</span></span>                   |



 

## <a name="manifestation"></a><span data-ttu-id="799d3-146">表現</span><span class="sxs-lookup"><span data-stu-id="799d3-146">Manifestation</span></span>

<span data-ttu-id="799d3-147">應用程式 (例如資料庫) 具有不檢查 NLS 版本的持續性索引，並在版本變更時重新建立索引，將無法正確排序，或可能無法提供要求的結果。</span><span class="sxs-lookup"><span data-stu-id="799d3-147">Applications (such as databases) with persistent indexes that do not check the NLS version and re-index upon version change will fail to sort correctly or may fail to provide requested results.</span></span>

<span data-ttu-id="799d3-148">在使用者介面的案例中，會列出 (例如，字母、數位、英數位元、符號等等) 可能會不正確地排序。</span><span class="sxs-lookup"><span data-stu-id="799d3-148">In the case of user interfaces, lists (for example, alphabetical, numeric, alphanumeric, symbols, and so on) may sort incorrectly.</span></span>

## <a name="solution"></a><span data-ttu-id="799d3-149">解決方法</span><span class="sxs-lookup"><span data-stu-id="799d3-149">Solution</span></span>

<span data-ttu-id="799d3-150">在 Windows Vista) 之前，您的應用程式可以呼叫 **GetNLSVersionEx** (windows vista 或更新版本) 或 **GetNLSVersion** (，以取得定序資料表的已定義版本和 NLS 版本。</span><span class="sxs-lookup"><span data-stu-id="799d3-150">Your application can call either **GetNLSVersionEx** (Windows Vista or later) or **GetNLSVersion** (prior to Windows Vista) to retrieve both the defined version and the NLS version for a collation table.</span></span>

-   <span data-ttu-id="799d3-151">GetNLSVersionEx:</span><span class="sxs-lookup"><span data-stu-id="799d3-151">GetNLSVersionEx:</span></span>

<span data-ttu-id="799d3-152">*針對名稱所指定的地區設定，取得指定 NLS 功能目前版本的相關資訊*</span><span class="sxs-lookup"><span data-stu-id="799d3-152">*Retrieves information about the current version of a specified NLS capability for a locale specified by name*</span></span>  
<span data-ttu-id="799d3-153">此函數可讓 Active Directory 之類的應用程式判斷 NLS 變更是否會影響特定索引資料表所使用的地區設定。</span><span class="sxs-lookup"><span data-stu-id="799d3-153">This function allows an application such as Active Directory to determine whether an NLS change affects the locale used for a particular index table.</span></span> <span data-ttu-id="799d3-154">如果沒有，就不需要重新建立資料表的索引。</span><span class="sxs-lookup"><span data-stu-id="799d3-154">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="799d3-155">如需詳細資訊，請參閱處理地區設定和語言資訊。</span><span class="sxs-lookup"><span data-stu-id="799d3-155">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="799d3-156">此函數支援自訂地區設定。</span><span class="sxs-lookup"><span data-stu-id="799d3-156">This function supports custom locales.</span></span> <span data-ttu-id="799d3-157">如果 *lpLocaleName* 指定補充地區設定，則抓取的資料是與該補充地區設定相關聯之定序順序的正確資料。</span><span class="sxs-lookup"><span data-stu-id="799d3-157">If *lpLocaleName* specifies a supplemental locale, the data retrieved is the correct data for the collation order associated with that supplemental locale.</span></span>  

<span data-ttu-id="799d3-158">**注意：** Windows Vista 之前的 Windows 版本不支援 **GetNLSVersionEx**。</span><span class="sxs-lookup"><span data-stu-id="799d3-158">**Note:** Versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  


-   <span data-ttu-id="799d3-159">GetNLSVersion (用於 Windows Vista) 之前的 Windows 版本上執行的應用程式：</span><span class="sxs-lookup"><span data-stu-id="799d3-159">GetNLSVersion (use for applications running on versions of Windows prior to Windows Vista):</span></span>

<span data-ttu-id="799d3-160">*針對識別碼指定的地區設定，取得所指定 NLS 功能目前版本的相關資訊*</span><span class="sxs-lookup"><span data-stu-id="799d3-160">*Retrieves information about the current version of a specified NLS capability for a locale specified by identifier*</span></span>  
<span data-ttu-id="799d3-161">此函數可讓 Active Directory 之類的應用程式判斷 NLS 變更是否會影響用於特定索引資料表的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="799d3-161">This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table.</span></span> <span data-ttu-id="799d3-162">如果沒有，就不需要重新建立資料表的索引。</span><span class="sxs-lookup"><span data-stu-id="799d3-162">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="799d3-163">如需詳細資訊，請參閱處理地區設定和語言資訊。</span><span class="sxs-lookup"><span data-stu-id="799d3-163">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="799d3-164">**注意：** 此函式只會捕獲識別碼所指定之地區設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="799d3-164">**Note:** This function retrieves information only about a locale specified by identifier.</span></span> <span data-ttu-id="799d3-165">**GetNLSVersionEx** 函數支援其他地區設定、功能和 RFC 4646 名稱。</span><span class="sxs-lookup"><span data-stu-id="799d3-165">The **GetNLSVersionEx** function supports additional locales, features, and RFC 4646 names.</span></span> <span data-ttu-id="799d3-166">不過，Windows Vista 之前的 Windows 版本不支援 **GetNLSVersionEx**。</span><span class="sxs-lookup"><span data-stu-id="799d3-166">However, versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  
<span data-ttu-id="799d3-167">只在 Windows Vista 和更新版本上執行的應用程式應該在此函式的喜好設定中使用 **GetNLSVersionEx** 。</span><span class="sxs-lookup"><span data-stu-id="799d3-167">Applications meant to run only on Windows Vista and later should use **GetNLSVersionEx** in preference to this function.</span></span> <span data-ttu-id="799d3-168">**GetNLSVersionEx** 可為補充地區設定提供良好的支援。</span><span class="sxs-lookup"><span data-stu-id="799d3-168">**GetNLSVersionEx** provides good support for supplemental locales.</span></span>  


## <a name="compatibility-test"></a><span data-ttu-id="799d3-169">相容性測試</span><span class="sxs-lookup"><span data-stu-id="799d3-169">Compatibility Test</span></span>

<span data-ttu-id="799d3-170">**指示定序版本是否已變更 (也就是您需要重新建立) 索引的步驟：**</span><span class="sxs-lookup"><span data-stu-id="799d3-170">**Steps to tell if a collation version changed (that is, you need to re-index):**</span></span>

-   <span data-ttu-id="799d3-171">當您對資料進行原始索引編制時，**請使用 GetNLSVersionEx ()** 取出 **NLSVERSIONINFOEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="799d3-171">**Use GetNLSVersionEx()** to retrieve an **NLSVERSIONINFOEX** structure when doing the original indexing of your data.</span></span>
-   <span data-ttu-id="799d3-172">使用您的索引儲存下列屬性來識別版本：  **NLSVERSIONINFOEX. dwNLSVersion** 和 **NLSVERSIONINFOEX. dwDefinedVersion** –這兩個屬性一起指定您要使用的排序表版本。</span><span class="sxs-lookup"><span data-stu-id="799d3-172">Store the following properties with your index to identify the version:  **NLSVERSIONINFOEX.dwNLSVersion** and **NLSVERSIONINFOEX.dwDefinedVersion** – These two properties together specify the version of the sorting table you are using.</span></span>  
    <span data-ttu-id="799d3-173">**NLSVERSIONINFOEX. dwEffectiveId** -這會指定排序的有效地區設定。</span><span class="sxs-lookup"><span data-stu-id="799d3-173">**NLSVERSIONINFOEX.dwEffectiveId** - This specifies the effective locale of your sort.</span></span> <span data-ttu-id="799d3-174">自訂地區設定會指向內建地區設定的排序。</span><span class="sxs-lookup"><span data-stu-id="799d3-174">A custom locale will point to an in-box locale's sort.</span></span>  
    
-   <span data-ttu-id="799d3-175">使用索引時， **GetNlsVersionEx ()** 探索您的資料版本。</span><span class="sxs-lookup"><span data-stu-id="799d3-175">When using the index use **GetNlsVersionEx()** to discover the version of your data.</span></span>
-   <span data-ttu-id="799d3-176">如果三個屬性中的任一個已變更，則您使用的排序資料可能會傳回不同的結果，而且您可能會無法找到記錄的任何索引。</span><span class="sxs-lookup"><span data-stu-id="799d3-176">If any of the three properties has changed, the sorting data you are using could return different results and any indexing you have may fail to find records.</span></span>
-   <span data-ttu-id="799d3-177">如果您知道您的資料不包含不正確 Unicode 程式碼點 (也就是，您的所有字串從對 **IsNLSDefinedString ()**) 的呼叫傳回 **TRUE** ，如果只有 **dwNLSVersion** 和 **dwDefinedVersion** 的低位元組變更 () 以上所述的次要版本，則您可以將它們視為相同。</span><span class="sxs-lookup"><span data-stu-id="799d3-177">If you KNOW that your data does not contain invalid Unicode code points (that is, all of your strings returned **TRUE** from a call to **IsNLSDefinedString()**), then you may consider them the same if ONLY the low byte of **dwNLSVersion** and **dwDefinedVersion** changed (the minor versions described above).</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="799d3-178">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="799d3-178">Links to Other Resources</span></span>

-   [<span data-ttu-id="799d3-179">Windows 應用程式的國際化</span><span class="sxs-lookup"><span data-stu-id="799d3-179">Internationalization for Windows Applications</span></span>](../intl/international-support.md)
-   [<span data-ttu-id="799d3-180">GetNLSVersionEx 函式</span><span class="sxs-lookup"><span data-stu-id="799d3-180">GetNLSVersionEx Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [<span data-ttu-id="799d3-181">GetNLSVersion 函式</span><span class="sxs-lookup"><span data-stu-id="799d3-181">GetNLSVersion Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [<span data-ttu-id="799d3-182">如何判斷定序版本是否已變更</span><span class="sxs-lookup"><span data-stu-id="799d3-182">How to tell if the collation version changed</span></span>](/archive/blogs/shawnste/)

 

 
