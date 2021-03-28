---
description: 搜尋：應用程式通訊協定是一種可延伸的慣例，可在 Windows Vista Service Pack 1 (SP1) 和更新版本上呼叫桌面搜尋應用程式。
title: 使用搜尋通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991738"
---
# <a name="using-the-search-protocol"></a><span data-ttu-id="23c71-103">使用搜尋通訊協定</span><span class="sxs-lookup"><span data-stu-id="23c71-103">Using the search Protocol</span></span>

<span data-ttu-id="23c71-104">**搜尋：** [應用程式通訊協定](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85))是一種可延伸的慣例，可在 Windows Vista SERVICE Pack 1 (SP1) 和更新版本上呼叫桌面搜尋應用程式。</span><span class="sxs-lookup"><span data-stu-id="23c71-104">The **search:** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is an extensible convention for calling the desktop search application on Windows Vista with Service Pack 1 (SP1) and later versions.</span></span> <span data-ttu-id="23c71-105">此通訊協定是在 Windows Vista SP1 (中建立的，如需詳細資訊，請參閱知識庫檔中 windows vista [desktop search 的 windows Vista Service Pack 1 變更（Windows Vista Service Pack 1 中的 Windows vista desktop Search 變更](https://support.microsoft.com/kb/941946) ）) ，讓 Windows 能夠判斷和呼叫預設桌面搜尋應用程式。</span><span class="sxs-lookup"><span data-stu-id="23c71-105">The protocol was created in Windows Vista with SP1 (for information see the Knowledge Base article [Overview of Windows Vista desktop search Changes in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) to give Windows a way to determine and call the default desktop search application.</span></span>

<span data-ttu-id="23c71-106">通訊協定語法提供許多參數，可用於執行常見的桌面搜尋，例如使用者輸入的搜尋字詞或搜尋開始的位置。</span><span class="sxs-lookup"><span data-stu-id="23c71-106">The protocol syntax provides a number of parameters useful for performing common desktop searches, such as user-entered search terms or the location on which the search was begun.</span></span> <span data-ttu-id="23c71-107">當使用者從兩個可用的搜尋專案點之一搜尋 ([ **開始** ] 功能表或 Windows 檔案總管) 時，作業系統會使用搜尋通訊協定來啟動預設的桌面搜尋應用程式。</span><span class="sxs-lookup"><span data-stu-id="23c71-107">When users search from one of the two available search entry points (either the **Start** menu or Windows Explorer), the operating system uses the search protocol to launch the default desktop search application.</span></span> <span data-ttu-id="23c71-108">其執行方式是將使用者輸入的搜尋詞彙新增至標準搜尋通訊協定語法，並將該資訊傳遞給註冊為預設搜尋應用程式的應用程式。</span><span class="sxs-lookup"><span data-stu-id="23c71-108">It does this by adding the user-entered search terms to the standard search protocol syntax and passing that information to the application registered as the default search application.</span></span>

<span data-ttu-id="23c71-109">如果未安裝其他桌面搜尋應用程式，則在這些進入點中輸入的搜尋會啟動 Windows Search Explorer。</span><span class="sxs-lookup"><span data-stu-id="23c71-109">If no other desktop search applications are installed, a search entered into these entry points launches the Windows Search Explorer.</span></span> <span data-ttu-id="23c71-110">但是，協力廠商開發人員可以建立、安裝及註冊其應用程式，以處理搜尋通訊協定，並作為預設搜尋應用程式。</span><span class="sxs-lookup"><span data-stu-id="23c71-110">However, third-party developers can create, install, and register their applications to handle the search protocol and to be the default search application.</span></span> <span data-ttu-id="23c71-111">這類應用程式必須支援搜尋通訊協定語法，並使用 [ [預設程式](default-programs.md) ] 功能註冊，以確保 Windows 的順暢體驗。</span><span class="sxs-lookup"><span data-stu-id="23c71-111">Such applications need to support the search protocol syntax and register with the [Default Programs](default-programs.md) feature to ensure a seamless experience with Windows.</span></span>

<span data-ttu-id="23c71-112">如果您開發的應用程式要在特定的桌面搜尋應用程式上使用或建立，您不應該依賴 **search：** protocol。</span><span class="sxs-lookup"><span data-stu-id="23c71-112">If you develop an application that is intended to use or build upon a specific desktop search application, you should not depend exclusively on the **search:** protocol.</span></span> <span data-ttu-id="23c71-113">因為許多應用程式可能擁有 **搜尋：** 通訊協定，所以不保證您的目標桌面搜尋應用程式在任何指定的時間都有該應用程式。</span><span class="sxs-lookup"><span data-stu-id="23c71-113">Because many applications could own the **search:** protocol, there is no guarantee that your targeted desktop search application will own it at any given time.</span></span> <span data-ttu-id="23c71-114">相反地，您應該使用該目標桌面搜尋應用程式所定義的私人搜尋通訊協定。</span><span class="sxs-lookup"><span data-stu-id="23c71-114">Instead, you should use a private search protocol defined by that targeted desktop search application.</span></span> <span data-ttu-id="23c71-115">這表示，要作為協力廠商應用程式平臺的桌面搜尋應用程式應該同時支援 **search：** protocol 和其專屬的搜尋通訊協定。</span><span class="sxs-lookup"><span data-stu-id="23c71-115">This means that desktop search applications intended to be a platform for third-party applications should support both the **search:** protocol and their own proprietary search protocol.</span></span>

> [!Note]  
> <span data-ttu-id="23c71-116">**Search：** 通訊協定不會取代專屬的 [搜尋-ms：](../search/-search-3x-wds-qryidx-searchms.md) protocol。</span><span class="sxs-lookup"><span data-stu-id="23c71-116">The **search:** protocol does not replace the proprietary [search-ms:](../search/-search-3x-wds-qryidx-searchms.md) protocol.</span></span> <span data-ttu-id="23c71-117">應用程式仍然可以使用 **search-ms：** protocol 來啟動 Window search Explorer，或以無訊息方式查詢 Windows Search 索引子。</span><span class="sxs-lookup"><span data-stu-id="23c71-117">Applications can still use the **search-ms:** protocol to launch Window Search Explorer or to silently query the Windows Search indexer.</span></span>

 

<span data-ttu-id="23c71-118">本主題包含下列項目：</span><span class="sxs-lookup"><span data-stu-id="23c71-118">This topic covers the following:</span></span>

-   [<span data-ttu-id="23c71-119">語法</span><span class="sxs-lookup"><span data-stu-id="23c71-119">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="23c71-120">Windows Vista SP1 使用搜尋：通訊協定</span><span class="sxs-lookup"><span data-stu-id="23c71-120">Windows Vista with SP1 use of the search: protocol</span></span>](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [<span data-ttu-id="23c71-121">範例</span><span class="sxs-lookup"><span data-stu-id="23c71-121">Examples</span></span>](#examples)
-   [<span data-ttu-id="23c71-122">註冊處理通訊協定的應用程式</span><span class="sxs-lookup"><span data-stu-id="23c71-122">Registering the Application that Handles the Protocol</span></span>](#registering-the-application-that-handles-the-protocol)
    -   [<span data-ttu-id="23c71-123">登錄專案</span><span class="sxs-lookup"><span data-stu-id="23c71-123">Registry Entries</span></span>](#registry-entries)
-   [<span data-ttu-id="23c71-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="23c71-124">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="23c71-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="23c71-125">Syntax</span></span>

<span data-ttu-id="23c71-126">搜尋通訊協定會使用下列標準的 URL 編碼語法：</span><span class="sxs-lookup"><span data-stu-id="23c71-126">The search protocol uses the following standard URL-encoded syntax:</span></span>


```C++
search:parameter=value[&parameter=value]&
```



<span data-ttu-id="23c71-127">語法一開始會識別通訊協定本身 (**搜尋：**) 。</span><span class="sxs-lookup"><span data-stu-id="23c71-127">The syntax begins by identifying the protocol itself (**search:**).</span></span> <span data-ttu-id="23c71-128">參數/值組是傳遞給搜尋引擎的引數，如下表所述，其中顯示搜尋通訊協定語法的所有可能參數。</span><span class="sxs-lookup"><span data-stu-id="23c71-128">The parameter/value pairs are arguments passed to the Search engine, as described in the following table, which shows all of the possible parameters for the search protocol syntax.</span></span>



| <span data-ttu-id="23c71-129">參數</span><span class="sxs-lookup"><span data-stu-id="23c71-129">Parameter</span></span>                                              | <span data-ttu-id="23c71-130">值</span><span class="sxs-lookup"><span data-stu-id="23c71-130">Value</span></span>                                                         | <span data-ttu-id="23c71-131">描述</span><span class="sxs-lookup"><span data-stu-id="23c71-131">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c71-132">查詢</span><span class="sxs-lookup"><span data-stu-id="23c71-132">query</span></span>                                                  | <span data-ttu-id="23c71-133">URL 編碼的文字</span><span class="sxs-lookup"><span data-stu-id="23c71-133">URL-encoded text</span></span>                                              | <span data-ttu-id="23c71-134">使用者輸入的查詢文字。</span><span class="sxs-lookup"><span data-stu-id="23c71-134">The query text entered by the user.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="23c71-135">inputlocale</span><span class="sxs-lookup"><span data-stu-id="23c71-135">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="23c71-136">任何有效的語言代碼識別碼 (LCID) </span><span class="sxs-lookup"><span data-stu-id="23c71-136">Any valid language code identifier (LCID)</span></span>                     | <span data-ttu-id="23c71-137">識別查詢之輸入語言的 LCID。</span><span class="sxs-lookup"><span data-stu-id="23c71-137">The LCID that identifies the input language for the query.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="23c71-138">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="23c71-138">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="23c71-139">任何有效的 LCID</span><span class="sxs-lookup"><span data-stu-id="23c71-139">Any valid LCID</span></span>                                                | <span data-ttu-id="23c71-140">識別索引子之國際版本語言的 LCID。</span><span class="sxs-lookup"><span data-stu-id="23c71-140">The LCID that identifies the language of the international version of the Indexer.</span></span> <span data-ttu-id="23c71-141">預設值為 1033 (en-us) 。</span><span class="sxs-lookup"><span data-stu-id="23c71-141">The default is 1033 (en-us).</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="23c71-142">粉</span><span class="sxs-lookup"><span data-stu-id="23c71-142">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="23c71-143">AQS 語句</span><span class="sxs-lookup"><span data-stu-id="23c71-143">AQS statement</span></span>                                                 | <span data-ttu-id="23c71-144">此引數會限制要搜尋的範圍。</span><span class="sxs-lookup"><span data-stu-id="23c71-144">This argument restricts the scope being searched.</span></span> <span data-ttu-id="23c71-145">在 Windows Vista 中，搜尋通訊協定支援完整 AQS 以及引數的特殊實作為 `location` 。</span><span class="sxs-lookup"><span data-stu-id="23c71-145">In Windows Vista, the search protocol supports full AQS as well as a special implementation for a `location` argument.</span></span> <span data-ttu-id="23c71-146">在 Windows XP 中，除了與的特殊執行之外，搜尋通訊協定也支援完整 `kind` AQS `store` 。</span><span class="sxs-lookup"><span data-stu-id="23c71-146">In Windows XP, the search protocol also supports full AQS, except for a special implementation of `kind` and `store`.</span></span> |
| [<span data-ttu-id="23c71-147">語法</span><span class="sxs-lookup"><span data-stu-id="23c71-147">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="23c71-148">NQS，AQS (不區分大小寫) </span><span class="sxs-lookup"><span data-stu-id="23c71-148">NQS, AQS (not case sensitive)</span></span>                                 | <span data-ttu-id="23c71-149">用來搜尋索引的查詢語法：自然查詢語法或 Advanced Query 語法 (AQS) 。</span><span class="sxs-lookup"><span data-stu-id="23c71-149">The query syntax to use to search the index: either Natural Query Syntax or Advanced Query Syntax (AQS).</span></span> <span data-ttu-id="23c71-150">AQS 是預設值，而且一律會假設為已剖析且受支援。</span><span class="sxs-lookup"><span data-stu-id="23c71-150">AQS is the default and is always assumed parsed and supported.</span></span>                                                                                                                        |
| [<span data-ttu-id="23c71-151">stackedby</span><span class="sxs-lookup"><span data-stu-id="23c71-151">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="23c71-152">屬性系統中的任何有效屬性</span><span class="sxs-lookup"><span data-stu-id="23c71-152">Any valid property from the property system</span></span>                   | <span data-ttu-id="23c71-153">屬性，指定要用來堆疊結果的資料行。</span><span class="sxs-lookup"><span data-stu-id="23c71-153">A property that specifies the column to stack results by.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="23c71-154">subquery</span><span class="sxs-lookup"><span data-stu-id="23c71-154">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="23c71-155">已儲存的搜尋檔案 (的完整指定路徑 \* 。搜尋-ms) </span><span class="sxs-lookup"><span data-stu-id="23c71-155">A fully specified path for a Saved Search file (\*.search-ms)</span></span> | <span data-ttu-id="23c71-156">子查詢的結果會當做查詢的來源使用。</span><span class="sxs-lookup"><span data-stu-id="23c71-156">The results of the subquery are used as the source for the query.</span></span> <span data-ttu-id="23c71-157">也就是說，會針對子查詢的結果搜尋查詢詞彙。</span><span class="sxs-lookup"><span data-stu-id="23c71-157">That is, the query terms are searched for against the results of the subquery.</span></span>                                                                                                                                               |
| <span data-ttu-id="23c71-158">displayname</span><span class="sxs-lookup"><span data-stu-id="23c71-158">displayname</span></span>                                            | <span data-ttu-id="23c71-159">URL 編碼的字串</span><span class="sxs-lookup"><span data-stu-id="23c71-159">URL-encoded string</span></span>                                            | <span data-ttu-id="23c71-160">目前搜尋的名稱。</span><span class="sxs-lookup"><span data-stu-id="23c71-160">The name of the current search.</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a><span data-ttu-id="23c71-161">Windows Vista SP1 使用搜尋：通訊協定</span><span class="sxs-lookup"><span data-stu-id="23c71-161">Windows Vista with SP1 use of the search: protocol</span></span>

<span data-ttu-id="23c71-162">Windows Vista （含 SP1）有數個進入點，可從中呼叫 **search：** protocol。</span><span class="sxs-lookup"><span data-stu-id="23c71-162">Windows Vista with SP1 has several entry points from which it calls the **search:** protocol.</span></span> <span data-ttu-id="23c71-163">這些進入點概述如下，以及與每個專案相關聯的一般語法。</span><span class="sxs-lookup"><span data-stu-id="23c71-163">These entry points are outlined below as well as the common syntax associated with each.</span></span>



| <span data-ttu-id="23c71-164">搜尋通訊協定進入點</span><span class="sxs-lookup"><span data-stu-id="23c71-164">Search protocol entry point</span></span> | <span data-ttu-id="23c71-165">Location</span><span class="sxs-lookup"><span data-stu-id="23c71-165">Location</span></span>         | <span data-ttu-id="23c71-166">查詢呼叫</span><span class="sxs-lookup"><span data-stu-id="23c71-166">Query called</span></span>                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="23c71-167">**隨處搜尋**</span><span class="sxs-lookup"><span data-stu-id="23c71-167">**Search Everywhere**</span></span>       | <span data-ttu-id="23c71-168">**開始** 功能表</span><span class="sxs-lookup"><span data-stu-id="23c71-168">**Start** menu</span></span>   | <span data-ttu-id="23c71-169">搜尋： query =<*搜尋字詞*></span><span class="sxs-lookup"><span data-stu-id="23c71-169">search:query=<*Search Term*></span></span>                                   |
| <span data-ttu-id="23c71-170">**隨處搜尋**</span><span class="sxs-lookup"><span data-stu-id="23c71-170">**Search Everywhere**</span></span>       | <span data-ttu-id="23c71-171">Windows 檔案總管</span><span class="sxs-lookup"><span data-stu-id="23c71-171">Windows Explorer</span></span> | <span data-ttu-id="23c71-172">搜尋：查詢 =<*搜尋詞彙*>&連結 = 位置： <*位置*></span><span class="sxs-lookup"><span data-stu-id="23c71-172">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="23c71-173">Windows 標誌鍵+F</span><span class="sxs-lookup"><span data-stu-id="23c71-173">Windows logo key+F</span></span>          | <span data-ttu-id="23c71-174">任何位置</span><span class="sxs-lookup"><span data-stu-id="23c71-174">Anywhere</span></span>         | <span data-ttu-id="23c71-175">搜索：</span><span class="sxs-lookup"><span data-stu-id="23c71-175">search:</span></span>                                                              |
| <span data-ttu-id="23c71-176">CTRL+F</span><span class="sxs-lookup"><span data-stu-id="23c71-176">CTRL+F</span></span>                      | <span data-ttu-id="23c71-177">Windows 檔案總管</span><span class="sxs-lookup"><span data-stu-id="23c71-177">Windows Explorer</span></span> | <span data-ttu-id="23c71-178">搜尋：查詢 =<*搜尋詞彙*>&連結 = 位置： <*位置*></span><span class="sxs-lookup"><span data-stu-id="23c71-178">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="23c71-179">F3</span><span class="sxs-lookup"><span data-stu-id="23c71-179">F3</span></span>                          | <span data-ttu-id="23c71-180">**開始** 功能表</span><span class="sxs-lookup"><span data-stu-id="23c71-180">**Start** menu</span></span>   | <span data-ttu-id="23c71-181">搜索：</span><span class="sxs-lookup"><span data-stu-id="23c71-181">search:</span></span>                                                              |
| <span data-ttu-id="23c71-182">F3</span><span class="sxs-lookup"><span data-stu-id="23c71-182">F3</span></span>                          | <span data-ttu-id="23c71-183">Windows 檔案總管</span><span class="sxs-lookup"><span data-stu-id="23c71-183">Windows Explorer</span></span> | <span data-ttu-id="23c71-184">搜尋：查詢 =<*搜尋詞彙*>&連結 = 位置： <*位置*></span><span class="sxs-lookup"><span data-stu-id="23c71-184">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |



 

<span data-ttu-id="23c71-185">Windows Vista SP1 搜尋通訊協定進入點不會利用搜尋通訊協定中的所有可能參數。</span><span class="sxs-lookup"><span data-stu-id="23c71-185">The Windows Vista with SP1 search protocol entry points do not take advantage of all the possible parameters in the search protocol.</span></span> <span data-ttu-id="23c71-186">只有處理來自 Windows Vista SP1 呼叫的應用程式，才能使用下表作為其所需的最小值指南。</span><span class="sxs-lookup"><span data-stu-id="23c71-186">Applications that are only concerned with handling search protocol calls from Windows Vista with SP1 can use the following table as a guide to the minimum they need to implement.</span></span>



| <span data-ttu-id="23c71-187">參數</span><span class="sxs-lookup"><span data-stu-id="23c71-187">Parameter</span></span>                                              | <span data-ttu-id="23c71-188">由 Windows 使用？</span><span class="sxs-lookup"><span data-stu-id="23c71-188">Used by Windows?</span></span> | <span data-ttu-id="23c71-189">Windows Vista SP1 在呼叫搜尋時如何使用它：</span><span class="sxs-lookup"><span data-stu-id="23c71-189">How Windows Vista with SP1 uses it when calling search:</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c71-190">查詢</span><span class="sxs-lookup"><span data-stu-id="23c71-190">query</span></span>                                                  | <span data-ttu-id="23c71-191">Yes</span><span class="sxs-lookup"><span data-stu-id="23c71-191">Yes</span></span>              | <span data-ttu-id="23c71-192">使用者輸入的查詢文字。</span><span class="sxs-lookup"><span data-stu-id="23c71-192">The query text entered by the user.</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="23c71-193">粉</span><span class="sxs-lookup"><span data-stu-id="23c71-193">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="23c71-194">Yes</span><span class="sxs-lookup"><span data-stu-id="23c71-194">Yes</span></span>              | <span data-ttu-id="23c71-195">[連結](search-protocol-crumb.md) 會使用 `location` 引數來指定查詢的來源。</span><span class="sxs-lookup"><span data-stu-id="23c71-195">[crumb](search-protocol-crumb.md) uses the `location` argument to specify where the query came from.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="23c71-196">subquery</span><span class="sxs-lookup"><span data-stu-id="23c71-196">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="23c71-197">Yes</span><span class="sxs-lookup"><span data-stu-id="23c71-197">Yes</span></span>              | <span data-ttu-id="23c71-198">[子查詢](search-protocol-subquery.md)引數的結果會用來做為要搜尋之專案的範圍。</span><span class="sxs-lookup"><span data-stu-id="23c71-198">The results of the [Subquery](search-protocol-subquery.md) argument are used as the scope of items to search.</span></span> <span data-ttu-id="23c71-199">這通常會在使用者使用. 搜尋-ms 檔案來搜尋，然後從該搜尋內呼叫預設桌面搜尋應用程式時使用。</span><span class="sxs-lookup"><span data-stu-id="23c71-199">This would typically be used if a user was using a .search-ms file to search and then called the default desktop search application from within that search.</span></span> |
| [<span data-ttu-id="23c71-200">inputlocale</span><span class="sxs-lookup"><span data-stu-id="23c71-200">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="23c71-201">No</span><span class="sxs-lookup"><span data-stu-id="23c71-201">No</span></span>               | <span data-ttu-id="23c71-202">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="23c71-202">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="23c71-203">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="23c71-203">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="23c71-204">No</span><span class="sxs-lookup"><span data-stu-id="23c71-204">No</span></span>               | <span data-ttu-id="23c71-205">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="23c71-205">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="23c71-206">語法</span><span class="sxs-lookup"><span data-stu-id="23c71-206">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="23c71-207">No</span><span class="sxs-lookup"><span data-stu-id="23c71-207">No</span></span>               | <span data-ttu-id="23c71-208">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="23c71-208">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="23c71-209">stackedby</span><span class="sxs-lookup"><span data-stu-id="23c71-209">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="23c71-210">No</span><span class="sxs-lookup"><span data-stu-id="23c71-210">No</span></span>               | <span data-ttu-id="23c71-211">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="23c71-211">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="23c71-212">displayname</span><span class="sxs-lookup"><span data-stu-id="23c71-212">displayname</span></span>                                            | <span data-ttu-id="23c71-213">No</span><span class="sxs-lookup"><span data-stu-id="23c71-213">No</span></span>               | <span data-ttu-id="23c71-214">目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="23c71-214">Not currently used.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a><span data-ttu-id="23c71-215">範例</span><span class="sxs-lookup"><span data-stu-id="23c71-215">Examples</span></span>

<span data-ttu-id="23c71-216">如果使用者在 [開始] 功能表中輸入 **「Microsoft」** 並按一下 [ **隨處搜尋**]，則會進行結果搜尋通訊協定呼叫：</span><span class="sxs-lookup"><span data-stu-id="23c71-216">If a user enters "Microsoft" in the **Start** menu and clicks **Search Everywhere**, the resulting search protocol call is made:</span></span>


```C++
search:query=microsoft&
```



<span data-ttu-id="23c71-217">如果使用者在 C： MyFolder 內的 Windows 檔案總管中輸入「西雅圖」， \\ 然後按一下 [ **隨處搜尋**]，則會使用 '： ' 和 ' ' 的 escape 字元進行下列呼叫 \\ ：</span><span class="sxs-lookup"><span data-stu-id="23c71-217">If a user enters "Seattle" in Windows Explorer within C:\\MyFolder and then clicks **Search Everywhere**, the following call is made, using escape characters for ':' and '\\':</span></span>


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a><span data-ttu-id="23c71-218">註冊處理通訊協定的應用程式</span><span class="sxs-lookup"><span data-stu-id="23c71-218">Registering the Application that Handles the Protocol</span></span>

<span data-ttu-id="23c71-219">由於有多個應用程式可以爭用搜尋通訊協定，因此您應該在安裝期間使用 [ [預設程式](default-programs.md) ] 功能來註冊您的應用程式，讓使用者能夠更輕鬆地設定預設值。</span><span class="sxs-lookup"><span data-stu-id="23c71-219">Because multiple applications can contend for the search protocol, you should register your application with the [Default Programs](default-programs.md) feature during installation to enable the user to configure the default more easily.</span></span> <span data-ttu-id="23c71-220">除了通常會在 Windows XP 下進行的安裝程式之外，Windows Vista 應用程式必須向 [預設程式] 功能註冊，讓應用程式和使用者可以順暢地設定預設值。</span><span class="sxs-lookup"><span data-stu-id="23c71-220">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista-based application must register with the Default Programs feature so that the application and users can seamlessly configure defaults.</span></span>

<span data-ttu-id="23c71-221">在使用者的電腦上安裝必要的二進位檔案之後，您的安裝常式應完成這些一般工作：</span><span class="sxs-lookup"><span data-stu-id="23c71-221">After installing the necessary binary files on the user's computer, your installation routine should complete these general tasks:</span></span>

1.  <span data-ttu-id="23c71-222">將 Progid 寫入 **HKEY \_ 本機 \_ 電腦**，如下所述。</span><span class="sxs-lookup"><span data-stu-id="23c71-222">Write ProgIDs to **HKEY\_LOCAL\_MACHINE**, as described below.</span></span> <span data-ttu-id="23c71-223">請注意，應用程式必須建立搜尋通訊協定的應用程式特定 Progid。</span><span class="sxs-lookup"><span data-stu-id="23c71-223">Note that applications must create application-specific ProgIDs for the search protocol.</span></span>
2.  <span data-ttu-id="23c71-224">索取電腦層級搜尋通訊協定關聯。</span><span class="sxs-lookup"><span data-stu-id="23c71-224">Claim machine-level search protocol association.</span></span>
3.  <span data-ttu-id="23c71-225">使用 [預設程式](default-programs.md)來註冊應用程式，如 [註冊應用程式以搭配預設程式使用](default-programs.md)，以做為搜尋通訊協定的競爭者。</span><span class="sxs-lookup"><span data-stu-id="23c71-225">Register the application with [Default Programs](default-programs.md), as explained in [Registering an Application for Use with Default Programs](default-programs.md), as a contender for the search protocol.</span></span>

### <a name="registry-entries"></a><span data-ttu-id="23c71-226">登錄項目</span><span class="sxs-lookup"><span data-stu-id="23c71-226">Registry Entries</span></span>

<span data-ttu-id="23c71-227">以下是虛構桌面搜尋應用程式（Contoso 搜尋）所需的登錄專案範例。</span><span class="sxs-lookup"><span data-stu-id="23c71-227">The following are examples of the required registry entries for a fictional desktop search application, Contoso Search.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a><span data-ttu-id="23c71-228">相關主題</span><span class="sxs-lookup"><span data-stu-id="23c71-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23c71-229">進階查詢語法</span><span class="sxs-lookup"><span data-stu-id="23c71-229">Advanced Query Syntax</span></span>](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[<span data-ttu-id="23c71-230">預設程式</span><span class="sxs-lookup"><span data-stu-id="23c71-230">Default Programs</span></span>](default-programs.md)
</dt> </dl>

 

 
