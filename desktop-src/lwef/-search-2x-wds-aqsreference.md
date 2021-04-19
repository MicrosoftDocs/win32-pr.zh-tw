---
title: 進階查詢語法
description: " (AQS) 的 Advanced Query 語法，可供 Microsoft Windows 桌面搜尋 (WDS) 協助使用者和程式設計師更妥善地定義和縮小搜尋的範圍。"
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: bd00821e60c8d950a7ec384b62d7ff062066f224
ms.sourcegitcommit: 8bba855bfee06d018edb16c1af70fa4d4344445b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "106965417"
---
# <a name="advanced-query-syntax"></a><span data-ttu-id="52248-103">進階查詢語法</span><span class="sxs-lookup"><span data-stu-id="52248-103">Advanced Query Syntax</span></span>

> [!NOTE]
> <span data-ttu-id="52248-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="52248-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="52248-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="52248-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="52248-106"> (AQS) 的 Advanced Query 語法，可供 Microsoft Windows 桌面搜尋 (WDS) 協助使用者和程式設計師更妥善地定義和縮小搜尋的範圍。</span><span class="sxs-lookup"><span data-stu-id="52248-106">The Advanced Query Syntax (AQS) is used by Microsoft Windows Desktop Search (WDS) to help users and programmers better define and narrow their searches.</span></span> <span data-ttu-id="52248-107">使用 AQS 可讓您輕鬆地縮小搜尋範圍，並提供更好的結果集。</span><span class="sxs-lookup"><span data-stu-id="52248-107">Using AQS is an easy way to narrow searches and deliver better result sets.</span></span> <span data-ttu-id="52248-108">下列參數可縮小搜尋範圍：</span><span class="sxs-lookup"><span data-stu-id="52248-108">Searches can be narrowed by the following parameters:</span></span>

-   <span data-ttu-id="52248-109">檔種類：資料夾、檔、簡報、圖片等等。</span><span class="sxs-lookup"><span data-stu-id="52248-109">File kinds: folders, documents, presentations, pictures and so on.</span></span>
-   <span data-ttu-id="52248-110">檔案存放區：特定的資料庫和位置。</span><span class="sxs-lookup"><span data-stu-id="52248-110">File stores: specific databases and locations.</span></span>
-   <span data-ttu-id="52248-111">檔案屬性：大小、日期、標題等等。</span><span class="sxs-lookup"><span data-stu-id="52248-111">File properties: size, date, title and so on.</span></span>
-   <span data-ttu-id="52248-112">檔案內容：關鍵字，例如「專案交付專案」、「AQS」、「藍色 suede 鞋」等等。</span><span class="sxs-lookup"><span data-stu-id="52248-112">File contents: keywords like "project deliverables," "AQS," "blue suede shoes," and so on.</span></span>

<span data-ttu-id="52248-113">此外，搜尋參數可以使用搜尋運算子來合併。</span><span class="sxs-lookup"><span data-stu-id="52248-113">Furthermore, search parameters can be combined using search operators.</span></span> <span data-ttu-id="52248-114">本節的其餘部分將說明查詢語法、參數和運算子，以及如何結合以提供目標搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="52248-114">The remainder of this section explains the query syntax, the parameters and operators, and how they can be combined to offer targeted search results.</span></span> <span data-ttu-id="52248-115">這些表格描述與 WDS 搭配使用的語法，以及可針對 **Windows 桌面搜尋** 結果視窗中顯示的每個檔案種類查詢的屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-115">The tables describe the syntax to use with WDS, as well as the properties that can be queried for each file kind displayed in the **Windows Desktop Search** results window.</span></span>

## <a name="desktop-search-syntax"></a><span data-ttu-id="52248-116">桌面搜尋語法</span><span class="sxs-lookup"><span data-stu-id="52248-116">Desktop Search Syntax</span></span>

<span data-ttu-id="52248-117">搜尋查詢可以包含一或多個關鍵字，以及布林運算子和選擇性準則。</span><span class="sxs-lookup"><span data-stu-id="52248-117">A search query can include one or more keywords, with Boolean operators and optional criteria.</span></span> <span data-ttu-id="52248-118">這些選擇性準則可以根據下列內容縮小搜尋範圍：</span><span class="sxs-lookup"><span data-stu-id="52248-118">These optional criteria can narrow a search based on the following:</span></span>

-   <span data-ttu-id="52248-119">檔案所在的範圍或資料存放區</span><span class="sxs-lookup"><span data-stu-id="52248-119">Scope or data store in which files reside</span></span>
-   <span data-ttu-id="52248-120">檔案的種類</span><span class="sxs-lookup"><span data-stu-id="52248-120">Kinds of files</span></span>
-   <span data-ttu-id="52248-121">檔案的受控屬性</span><span class="sxs-lookup"><span data-stu-id="52248-121">Managed properties of files</span></span>

<span data-ttu-id="52248-122">以下是更詳細說明的選擇性準則，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="52248-122">The optional criteria, described in greater detail following, use the following syntax:</span></span>

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

<span data-ttu-id="52248-123">假設使用者想要搜尋的檔中包含「上一季」、John 或 Joanne 所建立的片語，以及使用者儲存到 >mydocuments 資料夾。</span><span class="sxs-lookup"><span data-stu-id="52248-123">Suppose a user wants to search for a document containing the phrase "last quarter," created by John or Joanne, and that the user saved to the folder mydocuments.</span></span> <span data-ttu-id="52248-124">查詢可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="52248-124">The query may look like this:</span></span>

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a><span data-ttu-id="52248-125">範圍：位置和資料存放區</span><span class="sxs-lookup"><span data-stu-id="52248-125">Scope: Locations and Data Stores</span></span>

<span data-ttu-id="52248-126">使用者可以將搜尋範圍限制在特定資料夾位置或資料存放區。</span><span class="sxs-lookup"><span data-stu-id="52248-126">Users can limit the scope of their searches to specific folder locations or data stores.</span></span> <span data-ttu-id="52248-127">例如，如果您使用數個電子郵件帳戶，而您想要將查詢限制為 Microsoft Outlook 或 Microsoft Outlook Express，則可以使用 `store:outlook` 或分別使用或 `store:oe` 。</span><span class="sxs-lookup"><span data-stu-id="52248-127">For example, if you use several email accounts and you want to limit a query to either Microsoft Outlook or Microsoft Outlook Express, you can use `store:outlook` or `store:oe` respectively.</span></span>



| <span data-ttu-id="52248-128">依資料存放區限制搜尋</span><span class="sxs-lookup"><span data-stu-id="52248-128">Restrict Search by Data Store</span></span> | <span data-ttu-id="52248-129">用法</span><span class="sxs-lookup"><span data-stu-id="52248-129">Use</span></span>              | <span data-ttu-id="52248-130">範例</span><span class="sxs-lookup"><span data-stu-id="52248-130">Example</span></span>                                  |
|-------------------------------|------------------|------------------------------------------|
| <span data-ttu-id="52248-131">桌面</span><span class="sxs-lookup"><span data-stu-id="52248-131">Desktop</span></span>                       | <span data-ttu-id="52248-132">桌面</span><span class="sxs-lookup"><span data-stu-id="52248-132">desktop</span></span>          | <span data-ttu-id="52248-133">存放區： desktop</span><span class="sxs-lookup"><span data-stu-id="52248-133">store:desktop</span></span>                            |
| <span data-ttu-id="52248-134">檔案</span><span class="sxs-lookup"><span data-stu-id="52248-134">Files</span></span>                         | <span data-ttu-id="52248-135">files</span><span class="sxs-lookup"><span data-stu-id="52248-135">files</span></span>            | <span data-ttu-id="52248-136">store： files</span><span class="sxs-lookup"><span data-stu-id="52248-136">store:files</span></span>                              |
| <span data-ttu-id="52248-137">Outlook</span><span class="sxs-lookup"><span data-stu-id="52248-137">Outlook</span></span>                       | <span data-ttu-id="52248-138">Outlook</span><span class="sxs-lookup"><span data-stu-id="52248-138">outlook</span></span>          | <span data-ttu-id="52248-139">store： outlook</span><span class="sxs-lookup"><span data-stu-id="52248-139">store:outlook</span></span>                            |
| <span data-ttu-id="52248-140">Outlook Express</span><span class="sxs-lookup"><span data-stu-id="52248-140">Outlook Express</span></span>               | <span data-ttu-id="52248-141">Oe</span><span class="sxs-lookup"><span data-stu-id="52248-141">oe</span></span>               | <span data-ttu-id="52248-142">store： oe</span><span class="sxs-lookup"><span data-stu-id="52248-142">store:oe</span></span>                                 |
| <span data-ttu-id="52248-143">特定資料夾</span><span class="sxs-lookup"><span data-stu-id="52248-143">Specific Folder</span></span>               | <span data-ttu-id="52248-144">資料夾資料夾或</span><span class="sxs-lookup"><span data-stu-id="52248-144">foldername or in</span></span> | <span data-ttu-id="52248-145">資料夾資料夾： >mydocuments 或 in： >mydocuments</span><span class="sxs-lookup"><span data-stu-id="52248-145">foldername:MyDocuments or in:MyDocuments</span></span> |



 

<span data-ttu-id="52248-146">如果您有可用來編目自訂存放區的通訊協定處理常式（例如 Lotus Notes），您可以使用存放區的存放區或通訊協定處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="52248-146">If you have a protocol handler in place to crawl custom stores, like Lotus Notes, you can use the name of the store or protocol handler for the store.</span></span> <span data-ttu-id="52248-147">例如，如果您實作為「附注」的「Lotus Notes」資料存放區來執行通訊協定處理常式，則查詢語法會是 `store:notes` 。</span><span class="sxs-lookup"><span data-stu-id="52248-147">For example, if you implemented a protocol handler to include a Lotus Notes data store as "notes," the query syntax would be `store:notes`.</span></span>

### <a name="common-file-kinds"></a><span data-ttu-id="52248-148">一般檔案類型</span><span class="sxs-lookup"><span data-stu-id="52248-148">Common File Kinds</span></span>

<span data-ttu-id="52248-149">使用者也可以將搜尋限制為特定類型的檔案，稱為「檔種類」。</span><span class="sxs-lookup"><span data-stu-id="52248-149">Users can also limit their searches to specific types of files, called file kinds.</span></span> <span data-ttu-id="52248-150">下表列出檔案種類，並提供用來搜尋這類檔案的語法範例。</span><span class="sxs-lookup"><span data-stu-id="52248-150">The following table lists the file kinds and offers examples of the syntax used to search for these kinds of files.</span></span>



| <span data-ttu-id="52248-151">依檔案類型限制：</span><span class="sxs-lookup"><span data-stu-id="52248-151">To Restrict by File Type:</span></span>       | <span data-ttu-id="52248-152">用法</span><span class="sxs-lookup"><span data-stu-id="52248-152">Use</span></span>              | <span data-ttu-id="52248-153">範例</span><span class="sxs-lookup"><span data-stu-id="52248-153">Example</span></span>                        |
|---------------------------------|------------------|--------------------------------|
| <span data-ttu-id="52248-154">所有檔案類型</span><span class="sxs-lookup"><span data-stu-id="52248-154">All file types</span></span>                  | <span data-ttu-id="52248-155">一切</span><span class="sxs-lookup"><span data-stu-id="52248-155">everything</span></span>       | <span data-ttu-id="52248-156">種類：所有專案</span><span class="sxs-lookup"><span data-stu-id="52248-156">kind:everything</span></span>                |
| <span data-ttu-id="52248-157">通訊</span><span class="sxs-lookup"><span data-stu-id="52248-157">Communications</span></span>                  | <span data-ttu-id="52248-158">通訊</span><span class="sxs-lookup"><span data-stu-id="52248-158">communications</span></span>   | <span data-ttu-id="52248-159">種類：通訊</span><span class="sxs-lookup"><span data-stu-id="52248-159">kind:communications</span></span>            |
| <span data-ttu-id="52248-160">連絡人</span><span class="sxs-lookup"><span data-stu-id="52248-160">Contacts</span></span>                        | <span data-ttu-id="52248-161">連絡人</span><span class="sxs-lookup"><span data-stu-id="52248-161">contacts</span></span>         | <span data-ttu-id="52248-162">種類：連絡人</span><span class="sxs-lookup"><span data-stu-id="52248-162">kind:contacts</span></span>                  |
| <span data-ttu-id="52248-163">電子郵件</span><span class="sxs-lookup"><span data-stu-id="52248-163">E-mail</span></span>                          | <span data-ttu-id="52248-164">電子郵件</span><span class="sxs-lookup"><span data-stu-id="52248-164">email</span></span>            | <span data-ttu-id="52248-165">種類： email</span><span class="sxs-lookup"><span data-stu-id="52248-165">kind:email</span></span>                     |
| <span data-ttu-id="52248-166">立即 Messenger 對話</span><span class="sxs-lookup"><span data-stu-id="52248-166">Instant Messenger conversations</span></span> | <span data-ttu-id="52248-167">我</span><span class="sxs-lookup"><span data-stu-id="52248-167">im</span></span>               | <span data-ttu-id="52248-168">種類： im</span><span class="sxs-lookup"><span data-stu-id="52248-168">kind:im</span></span>                        |
| <span data-ttu-id="52248-169">會議</span><span class="sxs-lookup"><span data-stu-id="52248-169">Meetings</span></span>                        | <span data-ttu-id="52248-170">會議</span><span class="sxs-lookup"><span data-stu-id="52248-170">meetings</span></span>         | <span data-ttu-id="52248-171">種類：會議</span><span class="sxs-lookup"><span data-stu-id="52248-171">kind:meetings</span></span>                  |
| <span data-ttu-id="52248-172">工作</span><span class="sxs-lookup"><span data-stu-id="52248-172">Tasks</span></span>                           | <span data-ttu-id="52248-173">工作</span><span class="sxs-lookup"><span data-stu-id="52248-173">tasks</span></span>            | <span data-ttu-id="52248-174">種類： tasks</span><span class="sxs-lookup"><span data-stu-id="52248-174">kind:tasks</span></span>                     |
| <span data-ttu-id="52248-175">備註</span><span class="sxs-lookup"><span data-stu-id="52248-175">Notes</span></span>                           | <span data-ttu-id="52248-176">版本</span><span class="sxs-lookup"><span data-stu-id="52248-176">notes</span></span>            | <span data-ttu-id="52248-177">kind： notes</span><span class="sxs-lookup"><span data-stu-id="52248-177">kind:notes</span></span>                     |
| <span data-ttu-id="52248-178">文件</span><span class="sxs-lookup"><span data-stu-id="52248-178">Documents</span></span>                       | <span data-ttu-id="52248-179">docs</span><span class="sxs-lookup"><span data-stu-id="52248-179">docs</span></span>             | <span data-ttu-id="52248-180">種類：檔</span><span class="sxs-lookup"><span data-stu-id="52248-180">kind:docs</span></span>                      |
| <span data-ttu-id="52248-181">文字檔</span><span class="sxs-lookup"><span data-stu-id="52248-181">Text documents</span></span>                  | <span data-ttu-id="52248-182">text</span><span class="sxs-lookup"><span data-stu-id="52248-182">text</span></span>             | <span data-ttu-id="52248-183">kind： text</span><span class="sxs-lookup"><span data-stu-id="52248-183">kind:text</span></span>                      |
| <span data-ttu-id="52248-184">試算表</span><span class="sxs-lookup"><span data-stu-id="52248-184">Spreadsheets</span></span>                    | <span data-ttu-id="52248-185">電子 表格</span><span class="sxs-lookup"><span data-stu-id="52248-185">spreadsheets</span></span>     | <span data-ttu-id="52248-186">種類：試算表</span><span class="sxs-lookup"><span data-stu-id="52248-186">kind:spreadsheets</span></span>              |
| <span data-ttu-id="52248-187">簡報</span><span class="sxs-lookup"><span data-stu-id="52248-187">Presentations</span></span>                   | <span data-ttu-id="52248-188">簡報</span><span class="sxs-lookup"><span data-stu-id="52248-188">presentations</span></span>    | <span data-ttu-id="52248-189">種類：簡報</span><span class="sxs-lookup"><span data-stu-id="52248-189">kind:presentations</span></span>             |
| <span data-ttu-id="52248-190">音樂</span><span class="sxs-lookup"><span data-stu-id="52248-190">Music</span></span>                           | <span data-ttu-id="52248-191">music</span><span class="sxs-lookup"><span data-stu-id="52248-191">music</span></span>            | <span data-ttu-id="52248-192">種類：音樂</span><span class="sxs-lookup"><span data-stu-id="52248-192">kind:music</span></span>                     |
| <span data-ttu-id="52248-193">圖片</span><span class="sxs-lookup"><span data-stu-id="52248-193">Pictures</span></span>                        | <span data-ttu-id="52248-194">圖片</span><span class="sxs-lookup"><span data-stu-id="52248-194">pics</span></span>             | <span data-ttu-id="52248-195">種類：圖片</span><span class="sxs-lookup"><span data-stu-id="52248-195">kind:pics</span></span>                      |
| <span data-ttu-id="52248-196">影片</span><span class="sxs-lookup"><span data-stu-id="52248-196">Videos</span></span>                          | <span data-ttu-id="52248-197">videos</span><span class="sxs-lookup"><span data-stu-id="52248-197">videos</span></span>           | <span data-ttu-id="52248-198">種類：影片</span><span class="sxs-lookup"><span data-stu-id="52248-198">kind:videos</span></span>                    |
| <span data-ttu-id="52248-199">資料夾</span><span class="sxs-lookup"><span data-stu-id="52248-199">Folders</span></span>                         | <span data-ttu-id="52248-200">資料夾</span><span class="sxs-lookup"><span data-stu-id="52248-200">folders</span></span>          | <span data-ttu-id="52248-201">種類：資料夾</span><span class="sxs-lookup"><span data-stu-id="52248-201">kind:folders</span></span>                   |
| <span data-ttu-id="52248-202">資料夾名稱</span><span class="sxs-lookup"><span data-stu-id="52248-202">Folder name</span></span>                     | <span data-ttu-id="52248-203">資料夾資料夾或</span><span class="sxs-lookup"><span data-stu-id="52248-203">foldername or in</span></span> | <span data-ttu-id="52248-204">資料夾資料夾： mydocs 或 in： mydocs</span><span class="sxs-lookup"><span data-stu-id="52248-204">foldername:mydocs or in:mydocs</span></span> |
| <span data-ttu-id="52248-205">我的最愛</span><span class="sxs-lookup"><span data-stu-id="52248-205">Favorites</span></span>                       | <span data-ttu-id="52248-206">我的最愛</span><span class="sxs-lookup"><span data-stu-id="52248-206">favorites</span></span>        | <span data-ttu-id="52248-207">種類：我的最愛</span><span class="sxs-lookup"><span data-stu-id="52248-207">kind:favorites</span></span>                 |
| <span data-ttu-id="52248-208">程式</span><span class="sxs-lookup"><span data-stu-id="52248-208">Programs</span></span>                        | <span data-ttu-id="52248-209">程式集</span><span class="sxs-lookup"><span data-stu-id="52248-209">programs</span></span>         | <span data-ttu-id="52248-210">種類：程式</span><span class="sxs-lookup"><span data-stu-id="52248-210">kind:programs</span></span>                  |



 

### <a name="boolean-operators"></a><span data-ttu-id="52248-211">布林運算子</span><span class="sxs-lookup"><span data-stu-id="52248-211">Boolean Operators</span></span>

<span data-ttu-id="52248-212">搜尋關鍵字和檔案屬性可以合併，以使用運算子擴大或縮小搜尋的範圍。</span><span class="sxs-lookup"><span data-stu-id="52248-212">Search keywords and file properties can be combined to broaden or narrow a search with operators.</span></span> <span data-ttu-id="52248-213">下表說明搜尋查詢中使用的常見運算子。</span><span class="sxs-lookup"><span data-stu-id="52248-213">The following table explains common operators used in a search query.</span></span>



| <span data-ttu-id="52248-214">關鍵字/符號</span><span class="sxs-lookup"><span data-stu-id="52248-214">Keyword/Symbol</span></span>  | <span data-ttu-id="52248-215">範例</span><span class="sxs-lookup"><span data-stu-id="52248-215">Examples</span></span>                                              | <span data-ttu-id="52248-216">函式</span><span class="sxs-lookup"><span data-stu-id="52248-216">Function</span></span>                                                                                                       |
|-----------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52248-217">NOT</span><span class="sxs-lookup"><span data-stu-id="52248-217">NOT</span></span>             | <span data-ttu-id="52248-218">社交非安全性</span><span class="sxs-lookup"><span data-stu-id="52248-218">social NOT security</span></span><br/>                        | <span data-ttu-id="52248-219">尋找包含 *社交*（但不是 *安全性*）的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-219">Finds items that contain *social*, but not *security*.</span></span><br/>                                              |
|                 | <span data-ttu-id="52248-220">社會保障</span><span class="sxs-lookup"><span data-stu-id="52248-220">social  security</span></span><br/>                           | <span data-ttu-id="52248-221">尋找包含 *社交* 和 *安全性* 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-221">Finds items that contain *social* and *security*.</span></span><br/>                                              |
| <span data-ttu-id="52248-222">OR</span><span class="sxs-lookup"><span data-stu-id="52248-222">OR</span></span>              | <span data-ttu-id="52248-223">社交或安全性</span><span class="sxs-lookup"><span data-stu-id="52248-223">social OR security</span></span><br/>                         | <span data-ttu-id="52248-224">尋找包含 *社交* 或 *安全性* 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-224">Finds items that contain *social* or *security*.</span></span><br/>                                                    |
| <span data-ttu-id="52248-225">引號</span><span class="sxs-lookup"><span data-stu-id="52248-225">Quotation marks</span></span> | <span data-ttu-id="52248-226">「社會安全」</span><span class="sxs-lookup"><span data-stu-id="52248-226">"social security"</span></span><br/>                          | <span data-ttu-id="52248-227">尋找包含確切片語 *社會安全* 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-227">Finds items that contain the exact phrase *social security*.</span></span><br/>                                        |
| <span data-ttu-id="52248-228">括號</span><span class="sxs-lookup"><span data-stu-id="52248-228">Parentheses</span></span>     | <span data-ttu-id="52248-229"> (社會安全) </span><span class="sxs-lookup"><span data-stu-id="52248-229">(social security)</span></span><br/>                          | <span data-ttu-id="52248-230">依任何順序尋找包含 *社交* 和 *安全性* 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-230">Finds items that contain *social* and *security* in any order.</span></span><br/>                                      |
| >            | <span data-ttu-id="52248-231">日期： >11/05/04</span><span class="sxs-lookup"><span data-stu-id="52248-231">date:>11/05/04</span></span><br/> <span data-ttu-id="52248-232">大小： >500</span><span class="sxs-lookup"><span data-stu-id="52248-232">size:>500</span></span><br/>  | <span data-ttu-id="52248-233">尋找日期為11/05/04 之後的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-233">Finds items with a date after 11/05/04.</span></span> <br/> <span data-ttu-id="52248-234">尋找大小超過500個位元組的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-234">Finds items with a size greater than 500 bytes.</span></span><br/> |
| <            | <span data-ttu-id="52248-235">日期： <11/05/04</span><span class="sxs-lookup"><span data-stu-id="52248-235">date:<11/05/04</span></span> <br/> <span data-ttu-id="52248-236">大小： <500</span><span class="sxs-lookup"><span data-stu-id="52248-236">size:<500</span></span><br/> | <span data-ttu-id="52248-237">尋找日期早于11/05/04 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-237">Finds items with a date before 11/05/04.</span></span> <br/> <span data-ttu-id="52248-238">尋找大小小於500個位元組的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-238">Finds items with a size less than 500 bytes.</span></span><br/>   |
| <span data-ttu-id="52248-239">..</span><span class="sxs-lookup"><span data-stu-id="52248-239">..</span></span>              | <span data-ttu-id="52248-240">日期： 11/05/04. 11/10/04</span><span class="sxs-lookup"><span data-stu-id="52248-240">date:11/05/04..11/10/04</span></span><br/>                    | <span data-ttu-id="52248-241">尋找日期開頭為11/05/04 且結束于11/10/04 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-241">Finds items with a date beginning on 11/05/04 and ending on 11/10/04.</span></span><br/>                               |



 

> [!Note]
>
> <span data-ttu-id="52248-242">運算子 **不** 是 and **或** 必須是大寫，而且無法在一個查詢中結合 (例如 `social OR security NOT retirement`) 。</span><span class="sxs-lookup"><span data-stu-id="52248-242">The operators **NOT** and **OR** must be in uppercase and cannot be combined in one query (e.g., `social OR security NOT retirement`).</span></span>

 

### <a name="boolean-properties"></a><span data-ttu-id="52248-243">布林值屬性</span><span class="sxs-lookup"><span data-stu-id="52248-243">Boolean Properties</span></span>

<span data-ttu-id="52248-244">某些檔案類型可讓使用者使用布林值屬性來搜尋檔案，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="52248-244">Some file types let users search for files using Boolean properties, as described in the following table.</span></span>



| <span data-ttu-id="52248-245">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-245">Property</span></span>       | <span data-ttu-id="52248-246">範例</span><span class="sxs-lookup"><span data-stu-id="52248-246">Example</span></span>                   | <span data-ttu-id="52248-247">函式</span><span class="sxs-lookup"><span data-stu-id="52248-247">Function</span></span>                                                                                                        |
|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52248-248">是：附件</span><span class="sxs-lookup"><span data-stu-id="52248-248">is:attachment</span></span>  | <span data-ttu-id="52248-249">報表為：附件</span><span class="sxs-lookup"><span data-stu-id="52248-249">report is:attachment</span></span>      | <span data-ttu-id="52248-250">尋找包含 *報表* 之附件的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-250">Finds items that have attachments that contain *report*.</span></span> <span data-ttu-id="52248-251">與 `isattachment:true` 相同。</span><span class="sxs-lookup"><span data-stu-id="52248-251">Same as `isattachment:true`.</span></span>                           |
| <span data-ttu-id="52248-252">isonline:</span><span class="sxs-lookup"><span data-stu-id="52248-252">isonline:</span></span>      | <span data-ttu-id="52248-253">報表 isonline： true</span><span class="sxs-lookup"><span data-stu-id="52248-253">report isonline:true</span></span>      | <span data-ttu-id="52248-254">尋找線上且包含 *報表* 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-254">Finds items that are online and which contain *report*.</span></span>                                                         |
| <span data-ttu-id="52248-255">isrecurring</span><span class="sxs-lookup"><span data-stu-id="52248-255">isrecurring:</span></span>   | <span data-ttu-id="52248-256">報表 isrecurring： true</span><span class="sxs-lookup"><span data-stu-id="52248-256">report isrecurring:true</span></span>   | <span data-ttu-id="52248-257">尋找週期性且包含 *報表* 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-257">Finds items that are recurring and which contain *report*.</span></span>                                                       |
| <span data-ttu-id="52248-258">isflagged:</span><span class="sxs-lookup"><span data-stu-id="52248-258">isflagged:</span></span>     | <span data-ttu-id="52248-259">報表 isflagged： true</span><span class="sxs-lookup"><span data-stu-id="52248-259">report isflagged:true</span></span>     | <span data-ttu-id="52248-260">尋找已標示 (評論的專案、後續操作，例如) 和包含 *報表* 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-260">Finds items that are flagged (Review, Follow up, for example) and which contain *report*.</span></span>                       |
| <span data-ttu-id="52248-261">isdeleted</span><span class="sxs-lookup"><span data-stu-id="52248-261">isdeleted:</span></span>     | <span data-ttu-id="52248-262">報表 isdeleted： true</span><span class="sxs-lookup"><span data-stu-id="52248-262">report isdeleted:true</span></span>     | <span data-ttu-id="52248-263">尋找標示為已刪除 (資源回收筒或刪除專案的專案，例如) 和包含 *報表* 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-263">Finds items that are flagged as deleted (Recycle Bin or Deleted Items, for example) and which contain *report*.</span></span> |
| <span data-ttu-id="52248-264">iscompleted</span><span class="sxs-lookup"><span data-stu-id="52248-264">iscompleted:</span></span>   | <span data-ttu-id="52248-265">報表 iscompleted： false</span><span class="sxs-lookup"><span data-stu-id="52248-265">report iscompleted:false</span></span>  | <span data-ttu-id="52248-266">尋找未標示為完成且包含 *報表* 的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-266">Finds items that are not flagged as complete and which contain *report*.</span></span>                                        |
| <span data-ttu-id="52248-267">hasattachment:</span><span class="sxs-lookup"><span data-stu-id="52248-267">hasattachment:</span></span> | <span data-ttu-id="52248-268">報表 hasattachment： true</span><span class="sxs-lookup"><span data-stu-id="52248-268">report hasattachment:true</span></span> | <span data-ttu-id="52248-269">尋找包含 *報表* 和附件的專案</span><span class="sxs-lookup"><span data-stu-id="52248-269">Finds items containing *report* and having attachments</span></span>                                                          |
| <span data-ttu-id="52248-270">hasflag:</span><span class="sxs-lookup"><span data-stu-id="52248-270">hasflag:</span></span>       | <span data-ttu-id="52248-271">報表 hasflag： true</span><span class="sxs-lookup"><span data-stu-id="52248-271">report hasflag:true</span></span>       | <span data-ttu-id="52248-272">尋找包含 *報表* 並具有旗標的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-272">Finds items containing *report* and having flags.</span></span>                                                                |



 

### <a name="dates"></a><span data-ttu-id="52248-273">日期</span><span class="sxs-lookup"><span data-stu-id="52248-273">Dates</span></span>

<span data-ttu-id="52248-274">除了使用稍早所述的運算子來搜尋特定日期和日期範圍之外，AQS 還可讓您 (如 `today` 、或 `tomorrow` `next week`) 和 day (例如 `Tuesday` 或 `Monday..Wednesday`) 和 month (`February` 值) 。</span><span class="sxs-lookup"><span data-stu-id="52248-274">In addition to searching on specific dates and date ranges using the operators described earlier, AQS allows relative date values (like `today`, `tomorrow`, or `next week`) and day (like `Tuesday` or `Monday..Wednesday`) and month (`February`) values.</span></span>



| <span data-ttu-id="52248-275">相對於：</span><span class="sxs-lookup"><span data-stu-id="52248-275">Relative to:</span></span>    | <span data-ttu-id="52248-276">語法範例</span><span class="sxs-lookup"><span data-stu-id="52248-276">Syntax Example</span></span>                                                                                                                         | <span data-ttu-id="52248-277">結果</span><span class="sxs-lookup"><span data-stu-id="52248-277">Result</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52248-278">天</span><span class="sxs-lookup"><span data-stu-id="52248-278">Day</span></span>             | <span data-ttu-id="52248-279">日期：今天</span><span class="sxs-lookup"><span data-stu-id="52248-279">date:today</span></span><br/> <span data-ttu-id="52248-280">日期：明天</span><span class="sxs-lookup"><span data-stu-id="52248-280">date:tomorrow</span></span><br/> <span data-ttu-id="52248-281">日期：昨天</span><span class="sxs-lookup"><span data-stu-id="52248-281">date:yesterday</span></span><br/>                                                               | <span data-ttu-id="52248-282">尋找今天日期的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-282">Finds items with today's date.</span></span><br/> <span data-ttu-id="52248-283">尋找具有明天日期的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-283">Finds items with tomorrow's date.</span></span><br/> <span data-ttu-id="52248-284">尋找昨天日期的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-284">Finds items with yesterday's date.</span></span> <br/>                                                                                                                                                                                                                     |
| <span data-ttu-id="52248-285">周/月/年</span><span class="sxs-lookup"><span data-stu-id="52248-285">Week/Month/year</span></span> | <span data-ttu-id="52248-286">日期：本周</span><span class="sxs-lookup"><span data-stu-id="52248-286">date:this week</span></span><br/> <span data-ttu-id="52248-287">日期：上周</span><span class="sxs-lookup"><span data-stu-id="52248-287">date:last week</span></span><br/> <span data-ttu-id="52248-288">日期：下個月</span><span class="sxs-lookup"><span data-stu-id="52248-288">date:next month</span></span><br/> <span data-ttu-id="52248-289">日期：上月</span><span class="sxs-lookup"><span data-stu-id="52248-289">date:past month</span></span><br/> <span data-ttu-id="52248-290">日期：明年</span><span class="sxs-lookup"><span data-stu-id="52248-290">date:coming year</span></span> <br/> | <span data-ttu-id="52248-291">尋找日期落在目前周內的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-291">Finds items with a date falling within the current week.</span></span><br/> <span data-ttu-id="52248-292">尋找過去一周內有日期的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-292">Finds items with a date falling within the previous week.</span></span><br/> <span data-ttu-id="52248-293">尋找日期落在下一周的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-293">Finds items with a date falling within the upcoming week.</span></span><br/> <span data-ttu-id="52248-294">尋找日期在上個月內發生的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-294">Finds items with a date falling within the previous month.</span></span><br/> <span data-ttu-id="52248-295">尋找日期落在下一年的專案。</span><span class="sxs-lookup"><span data-stu-id="52248-295">Finds items with a date falling within the upcoming year.</span></span> <br/> |



 

## <a name="properties-by-file-kind"></a><span data-ttu-id="52248-296">依檔案類型的屬性</span><span class="sxs-lookup"><span data-stu-id="52248-296">Properties by File Kind</span></span>

<span data-ttu-id="52248-297">使用者可以搜尋不同檔案類型的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-297">Users can search on specific properties of different file kinds.</span></span> <span data-ttu-id="52248-298">某些屬性 (例如檔案大小) 通用於所有檔案，而其他屬性則僅限於特定種類。</span><span class="sxs-lookup"><span data-stu-id="52248-298">Some properties (like file size) are common to all files, while others are limited to a specific kind.</span></span> <span data-ttu-id="52248-299">例如，投影片計數是針對簡報所特有。</span><span class="sxs-lookup"><span data-stu-id="52248-299">Slide count, for example, is specific to presentations.</span></span> <span data-ttu-id="52248-300">下表依檔案種類列出這些屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-300">The following tables list these properties by file kind.</span></span>

### <a name="file-kind-everything"></a><span data-ttu-id="52248-301">檔種類：所有專案</span><span class="sxs-lookup"><span data-stu-id="52248-301">File Kind: Everything</span></span>

<span data-ttu-id="52248-302">這些都是所有檔案類型通用的屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-302">These are properties common to all file kinds.</span></span> <span data-ttu-id="52248-303">若要在查詢中包含所有類型的檔案，語法如下：</span><span class="sxs-lookup"><span data-stu-id="52248-303">To include all types of files in a query, the syntax is:</span></span>

`kind:everything <property>:<value>`

<span data-ttu-id="52248-304">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-304">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-305">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-305">Property</span></span>       | <span data-ttu-id="52248-306">用法</span><span class="sxs-lookup"><span data-stu-id="52248-306">Use</span></span>                      | <span data-ttu-id="52248-307">範例</span><span class="sxs-lookup"><span data-stu-id="52248-307">Example</span></span>                        |
|----------------|--------------------------|--------------------------------|
| <span data-ttu-id="52248-308">標題</span><span class="sxs-lookup"><span data-stu-id="52248-308">Title</span></span>          | <span data-ttu-id="52248-309">標題、主旨或相關</span><span class="sxs-lookup"><span data-stu-id="52248-309">title, subject or about</span></span>  | <span data-ttu-id="52248-310">標題：「每季財務」</span><span class="sxs-lookup"><span data-stu-id="52248-310">title:"Quarterly Financial"</span></span>    |
| <span data-ttu-id="52248-311">狀態</span><span class="sxs-lookup"><span data-stu-id="52248-311">Status</span></span>         | <span data-ttu-id="52248-312">status</span><span class="sxs-lookup"><span data-stu-id="52248-312">status</span></span>                   | <span data-ttu-id="52248-313">狀態：完成</span><span class="sxs-lookup"><span data-stu-id="52248-313">status:complete</span></span>                |
| <span data-ttu-id="52248-314">日期</span><span class="sxs-lookup"><span data-stu-id="52248-314">Date</span></span>           | <span data-ttu-id="52248-315">date</span><span class="sxs-lookup"><span data-stu-id="52248-315">date</span></span>                     | <span data-ttu-id="52248-316">日期：上周</span><span class="sxs-lookup"><span data-stu-id="52248-316">date:last week</span></span>                 |
| <span data-ttu-id="52248-317">修改日期</span><span class="sxs-lookup"><span data-stu-id="52248-317">Date modified</span></span>  | <span data-ttu-id="52248-318">datemodified 或修改</span><span class="sxs-lookup"><span data-stu-id="52248-318">datemodified or modified</span></span> | <span data-ttu-id="52248-319">修改日期：上周</span><span class="sxs-lookup"><span data-stu-id="52248-319">modified:last week</span></span>             |
| <span data-ttu-id="52248-320">重要性</span><span class="sxs-lookup"><span data-stu-id="52248-320">Importance</span></span>     | <span data-ttu-id="52248-321">重要性或優先順序</span><span class="sxs-lookup"><span data-stu-id="52248-321">importance or priority</span></span>   | <span data-ttu-id="52248-322">重要性：高</span><span class="sxs-lookup"><span data-stu-id="52248-322">importance:high</span></span>                |
| <span data-ttu-id="52248-323">大小</span><span class="sxs-lookup"><span data-stu-id="52248-323">Size</span></span>           | <span data-ttu-id="52248-324">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="52248-324">size</span></span>                     | <span data-ttu-id="52248-325">大小： > 50</span><span class="sxs-lookup"><span data-stu-id="52248-325">size:> 50</span></span>                   |
| <span data-ttu-id="52248-326">已刪除</span><span class="sxs-lookup"><span data-stu-id="52248-326">Deleted</span></span>        | <span data-ttu-id="52248-327">已刪除或 isdeleted</span><span class="sxs-lookup"><span data-stu-id="52248-327">deleted or isdeleted</span></span>     | <span data-ttu-id="52248-328">isdeleted： true</span><span class="sxs-lookup"><span data-stu-id="52248-328">isdeleted:true</span></span>                 |
| <span data-ttu-id="52248-329">為附件</span><span class="sxs-lookup"><span data-stu-id="52248-329">Is attachment</span></span>  | <span data-ttu-id="52248-330">isattachment</span><span class="sxs-lookup"><span data-stu-id="52248-330">isattachment</span></span>             | <span data-ttu-id="52248-331">isattachment： true</span><span class="sxs-lookup"><span data-stu-id="52248-331">isattachment:true</span></span>              |
| <span data-ttu-id="52248-332">收件者</span><span class="sxs-lookup"><span data-stu-id="52248-332">To</span></span>             | <span data-ttu-id="52248-333">至或 toname</span><span class="sxs-lookup"><span data-stu-id="52248-333">to or toname</span></span>             | <span data-ttu-id="52248-334">至： bob</span><span class="sxs-lookup"><span data-stu-id="52248-334">to:bob</span></span>                         |
| <span data-ttu-id="52248-335">副本</span><span class="sxs-lookup"><span data-stu-id="52248-335">Cc</span></span>             | <span data-ttu-id="52248-336">cc 或 ccname</span><span class="sxs-lookup"><span data-stu-id="52248-336">cc or ccname</span></span>             | <span data-ttu-id="52248-337">cc： john</span><span class="sxs-lookup"><span data-stu-id="52248-337">cc:john</span></span>                        |
| <span data-ttu-id="52248-338">公司</span><span class="sxs-lookup"><span data-stu-id="52248-338">Company</span></span>        | <span data-ttu-id="52248-339">company</span><span class="sxs-lookup"><span data-stu-id="52248-339">company</span></span>                  | <span data-ttu-id="52248-340">公司： Microsoft</span><span class="sxs-lookup"><span data-stu-id="52248-340">company:Microsoft</span></span>              |
| <span data-ttu-id="52248-341">Location</span><span class="sxs-lookup"><span data-stu-id="52248-341">Location</span></span>       | <span data-ttu-id="52248-342">location</span><span class="sxs-lookup"><span data-stu-id="52248-342">location</span></span>                 | <span data-ttu-id="52248-343">位置：「會議室102」</span><span class="sxs-lookup"><span data-stu-id="52248-343">location:"Conference Room 102"</span></span> |
| <span data-ttu-id="52248-344">類別</span><span class="sxs-lookup"><span data-stu-id="52248-344">Category</span></span>       | <span data-ttu-id="52248-345">category</span><span class="sxs-lookup"><span data-stu-id="52248-345">category</span></span>                 | <span data-ttu-id="52248-346">類別：商務</span><span class="sxs-lookup"><span data-stu-id="52248-346">category:Business</span></span>              |
| <span data-ttu-id="52248-347">關鍵字</span><span class="sxs-lookup"><span data-stu-id="52248-347">Keywords</span></span>       | <span data-ttu-id="52248-348">關鍵字</span><span class="sxs-lookup"><span data-stu-id="52248-348">keywords</span></span>                 | <span data-ttu-id="52248-349">關鍵字：「銷售預測」</span><span class="sxs-lookup"><span data-stu-id="52248-349">keywords:"sales projections"</span></span>   |
| <span data-ttu-id="52248-350">專輯</span><span class="sxs-lookup"><span data-stu-id="52248-350">Album</span></span>          | <span data-ttu-id="52248-351">專輯</span><span class="sxs-lookup"><span data-stu-id="52248-351">album</span></span>                    | <span data-ttu-id="52248-352">專輯：「每晚飛出」</span><span class="sxs-lookup"><span data-stu-id="52248-352">album:"Fly by Night"</span></span>           |
| <span data-ttu-id="52248-353">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="52248-353">File name</span></span>      | <span data-ttu-id="52248-354">filename 或 file</span><span class="sxs-lookup"><span data-stu-id="52248-354">filename or file</span></span>         | <span data-ttu-id="52248-355">檔案名： MyResume</span><span class="sxs-lookup"><span data-stu-id="52248-355">filename:MyResume</span></span>              |
| <span data-ttu-id="52248-356">Genre</span><span class="sxs-lookup"><span data-stu-id="52248-356">Genre</span></span>          | <span data-ttu-id="52248-357">genre</span><span class="sxs-lookup"><span data-stu-id="52248-357">genre</span></span>                    | <span data-ttu-id="52248-358">genre:rock</span><span class="sxs-lookup"><span data-stu-id="52248-358">genre:rock</span></span>                     |
| <span data-ttu-id="52248-359">作者</span><span class="sxs-lookup"><span data-stu-id="52248-359">Author</span></span>         | <span data-ttu-id="52248-360">作者或</span><span class="sxs-lookup"><span data-stu-id="52248-360">author or by</span></span>             | <span data-ttu-id="52248-361">作者： "Stephen 王"</span><span class="sxs-lookup"><span data-stu-id="52248-361">author:"Stephen King"</span></span>          |
| <span data-ttu-id="52248-362">人員</span><span class="sxs-lookup"><span data-stu-id="52248-362">People</span></span>         | <span data-ttu-id="52248-363">人或</span><span class="sxs-lookup"><span data-stu-id="52248-363">people or with</span></span>           | <span data-ttu-id="52248-364">使用： (sonja 或 david) </span><span class="sxs-lookup"><span data-stu-id="52248-364">with:(sonja or david)</span></span>          |
| <span data-ttu-id="52248-365">資料夾</span><span class="sxs-lookup"><span data-stu-id="52248-365">Folder</span></span>         | <span data-ttu-id="52248-366">資料夾、或路徑</span><span class="sxs-lookup"><span data-stu-id="52248-366">folder, under or path</span></span>    | <span data-ttu-id="52248-367">資料夾：下載</span><span class="sxs-lookup"><span data-stu-id="52248-367">folder:downloads</span></span>               |
| <span data-ttu-id="52248-368">副檔名</span><span class="sxs-lookup"><span data-stu-id="52248-368">File extension</span></span> | <span data-ttu-id="52248-369">ext 或 fileext</span><span class="sxs-lookup"><span data-stu-id="52248-369">ext or fileext</span></span>           | <span data-ttu-id="52248-370">ext:.txt</span><span class="sxs-lookup"><span data-stu-id="52248-370">ext:.txt</span></span>                       |



 

### <a name="attachment"></a><span data-ttu-id="52248-371">附件</span><span class="sxs-lookup"><span data-stu-id="52248-371">Attachment</span></span>

<span data-ttu-id="52248-372">這些是附件的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-372">These are properties common to attachments.</span></span> <span data-ttu-id="52248-373">若要將搜尋限制為僅限附件，語法為：</span><span class="sxs-lookup"><span data-stu-id="52248-373">To limit the search to attachments only, the syntax is:</span></span>

`kind:attachment <property>:<value>`

<span data-ttu-id="52248-374">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-374">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-375">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-375">Property</span></span> | <span data-ttu-id="52248-376">用法</span><span class="sxs-lookup"><span data-stu-id="52248-376">Use</span></span>            | <span data-ttu-id="52248-377">範例</span><span class="sxs-lookup"><span data-stu-id="52248-377">Example</span></span>                  |
|----------|----------------|--------------------------|
| <span data-ttu-id="52248-378">人員</span><span class="sxs-lookup"><span data-stu-id="52248-378">People</span></span>   | <span data-ttu-id="52248-379">人或</span><span class="sxs-lookup"><span data-stu-id="52248-379">people or with</span></span> | <span data-ttu-id="52248-380">人員： john 或 with： john</span><span class="sxs-lookup"><span data-stu-id="52248-380">people:john or with:john</span></span> |



 

### <a name="contacts"></a><span data-ttu-id="52248-381">連絡人</span><span class="sxs-lookup"><span data-stu-id="52248-381">Contacts</span></span>

<span data-ttu-id="52248-382">這些是連絡人的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-382">These are properties common to contacts.</span></span> <span data-ttu-id="52248-383">若要將搜尋限制為僅限連絡人，語法為：</span><span class="sxs-lookup"><span data-stu-id="52248-383">To limit the search to contacts only, the syntax is:</span></span>

`kind:contacts <property>:<value>`

<span data-ttu-id="52248-384">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-384">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-385">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-385">Property</span></span>              | <span data-ttu-id="52248-386">用法</span><span class="sxs-lookup"><span data-stu-id="52248-386">Use</span></span>                 | <span data-ttu-id="52248-387">範例</span><span class="sxs-lookup"><span data-stu-id="52248-387">Example</span></span>                            |
|-----------------------|---------------------|------------------------------------|
| <span data-ttu-id="52248-388">職稱</span><span class="sxs-lookup"><span data-stu-id="52248-388">Job title</span></span>             | <span data-ttu-id="52248-389">jobtitle</span><span class="sxs-lookup"><span data-stu-id="52248-389">jobtitle</span></span>            | <span data-ttu-id="52248-390">jobtitle： CFO</span><span class="sxs-lookup"><span data-stu-id="52248-390">jobtitle:CFO</span></span>                       |
| <span data-ttu-id="52248-391">IM 位址</span><span class="sxs-lookup"><span data-stu-id="52248-391">IM address</span></span>            | <span data-ttu-id="52248-392">imaddress</span><span class="sxs-lookup"><span data-stu-id="52248-392">imaddress</span></span>           | <span data-ttu-id="52248-393">imaddress： john\_doe@msn.com</span><span class="sxs-lookup"><span data-stu-id="52248-393">imaddress:john\_doe@msn.com</span></span>        |
| <span data-ttu-id="52248-394">助理的電話</span><span class="sxs-lookup"><span data-stu-id="52248-394">Assistant's phone</span></span>     | <span data-ttu-id="52248-395">assistantsphone</span><span class="sxs-lookup"><span data-stu-id="52248-395">assistantsphone</span></span>     | <span data-ttu-id="52248-396">assistantsphone： 555-3323</span><span class="sxs-lookup"><span data-stu-id="52248-396">assistantsphone:555-3323</span></span>           |
| <span data-ttu-id="52248-397">助理名稱</span><span class="sxs-lookup"><span data-stu-id="52248-397">Assistant name</span></span>        | <span data-ttu-id="52248-398">assistantname</span><span class="sxs-lookup"><span data-stu-id="52248-398">assistantname</span></span>       | <span data-ttu-id="52248-399">assistantname： Paul</span><span class="sxs-lookup"><span data-stu-id="52248-399">assistantname:Paul</span></span>                 |
| <span data-ttu-id="52248-400">Profession</span><span class="sxs-lookup"><span data-stu-id="52248-400">Profession</span></span>            | <span data-ttu-id="52248-401">職業</span><span class="sxs-lookup"><span data-stu-id="52248-401">profession</span></span>          | <span data-ttu-id="52248-402">專業： plumber</span><span class="sxs-lookup"><span data-stu-id="52248-402">profession:plumber</span></span>                 |
| <span data-ttu-id="52248-403">暱稱</span><span class="sxs-lookup"><span data-stu-id="52248-403">Nickname</span></span>              | <span data-ttu-id="52248-404">暱稱</span><span class="sxs-lookup"><span data-stu-id="52248-404">nickname</span></span>            | <span data-ttu-id="52248-405">昵稱： Tex</span><span class="sxs-lookup"><span data-stu-id="52248-405">nickname:Tex</span></span>                       |
| <span data-ttu-id="52248-406">配偶</span><span class="sxs-lookup"><span data-stu-id="52248-406">Spouse</span></span>                | <span data-ttu-id="52248-407">配偶</span><span class="sxs-lookup"><span data-stu-id="52248-407">spouse</span></span>              | <span data-ttu-id="52248-408">配偶： Debbie</span><span class="sxs-lookup"><span data-stu-id="52248-408">spouse:Debbie</span></span>                      |
| <span data-ttu-id="52248-409">商業城市</span><span class="sxs-lookup"><span data-stu-id="52248-409">Business city</span></span>         | <span data-ttu-id="52248-410">businesscity</span><span class="sxs-lookup"><span data-stu-id="52248-410">businesscity</span></span>        | <span data-ttu-id="52248-411">businesscity：西雅圖</span><span class="sxs-lookup"><span data-stu-id="52248-411">businesscity:Seattle</span></span>               |
| <span data-ttu-id="52248-412">商務郵遞區號</span><span class="sxs-lookup"><span data-stu-id="52248-412">Business postal code</span></span>  | <span data-ttu-id="52248-413">businesspostalcode</span><span class="sxs-lookup"><span data-stu-id="52248-413">businesspostalcode</span></span>  | <span data-ttu-id="52248-414">businesspostalcode：98006</span><span class="sxs-lookup"><span data-stu-id="52248-414">businesspostalcode:98006</span></span>           |
| <span data-ttu-id="52248-415">商務首頁</span><span class="sxs-lookup"><span data-stu-id="52248-415">Business home page</span></span>    | <span data-ttu-id="52248-416">businesshomepage</span><span class="sxs-lookup"><span data-stu-id="52248-416">businesshomepage</span></span>    | <span data-ttu-id="52248-417">businesshomepage:www</span><span class="sxs-lookup"><span data-stu-id="52248-417">businesshomepage:www.microsoft.com</span></span> |
| <span data-ttu-id="52248-418">回呼電話號碼</span><span class="sxs-lookup"><span data-stu-id="52248-418">Callback phone number</span></span> | <span data-ttu-id="52248-419">callbackphonenumber</span><span class="sxs-lookup"><span data-stu-id="52248-419">callbackphonenumber</span></span> | <span data-ttu-id="52248-420">callbackphonenumber： 555-555-2121</span><span class="sxs-lookup"><span data-stu-id="52248-420">callbackphonenumber:555-555-2121</span></span>   |
| <span data-ttu-id="52248-421">車輛電話</span><span class="sxs-lookup"><span data-stu-id="52248-421">Car phone</span></span>             | <span data-ttu-id="52248-422">carphone</span><span class="sxs-lookup"><span data-stu-id="52248-422">carphone</span></span>            | <span data-ttu-id="52248-423">carphone： 555-555-2121</span><span class="sxs-lookup"><span data-stu-id="52248-423">carphone:555-555-2121</span></span>              |
| <span data-ttu-id="52248-424">Children</span><span class="sxs-lookup"><span data-stu-id="52248-424">Children</span></span>              | <span data-ttu-id="52248-425">兒童</span><span class="sxs-lookup"><span data-stu-id="52248-425">children</span></span>            | <span data-ttu-id="52248-426">子系： Timmy</span><span class="sxs-lookup"><span data-stu-id="52248-426">children:Timmy</span></span>                     |
| <span data-ttu-id="52248-427">名字</span><span class="sxs-lookup"><span data-stu-id="52248-427">First name</span></span>            | <span data-ttu-id="52248-428">firstname</span><span class="sxs-lookup"><span data-stu-id="52248-428">firstname</span></span>           | <span data-ttu-id="52248-429">firstname： John</span><span class="sxs-lookup"><span data-stu-id="52248-429">firstname:John</span></span>                     |
| <span data-ttu-id="52248-430">姓氏</span><span class="sxs-lookup"><span data-stu-id="52248-430">Last name</span></span>             | <span data-ttu-id="52248-431">lastname</span><span class="sxs-lookup"><span data-stu-id="52248-431">lastname</span></span>            | <span data-ttu-id="52248-432">lastname： Doe</span><span class="sxs-lookup"><span data-stu-id="52248-432">lastname:Doe</span></span>                       |
| <span data-ttu-id="52248-433">首頁傳真</span><span class="sxs-lookup"><span data-stu-id="52248-433">Home fax</span></span>              | <span data-ttu-id="52248-434">homefax</span><span class="sxs-lookup"><span data-stu-id="52248-434">homefax</span></span>             | <span data-ttu-id="52248-435">homefax： 555-555-2121</span><span class="sxs-lookup"><span data-stu-id="52248-435">homefax:555-555-2121</span></span>               |
| <span data-ttu-id="52248-436">管理員的名稱</span><span class="sxs-lookup"><span data-stu-id="52248-436">Manager's name</span></span>        | <span data-ttu-id="52248-437">managersname</span><span class="sxs-lookup"><span data-stu-id="52248-437">managersname</span></span>        | <span data-ttu-id="52248-438">managersname： John</span><span class="sxs-lookup"><span data-stu-id="52248-438">managersname:John</span></span>                  |
| <span data-ttu-id="52248-439">呼叫器</span><span class="sxs-lookup"><span data-stu-id="52248-439">Pager</span></span>                 | <span data-ttu-id="52248-440">pager</span><span class="sxs-lookup"><span data-stu-id="52248-440">pager</span></span>               | <span data-ttu-id="52248-441">呼機： 555-555-2121</span><span class="sxs-lookup"><span data-stu-id="52248-441">pager:555-555-2121</span></span>                 |
| <span data-ttu-id="52248-442">商務電話</span><span class="sxs-lookup"><span data-stu-id="52248-442">Business phone</span></span>        | <span data-ttu-id="52248-443">>businessphone</span><span class="sxs-lookup"><span data-stu-id="52248-443">businessphone</span></span>       | <span data-ttu-id="52248-444">>businessphone： 555-555-2121</span><span class="sxs-lookup"><span data-stu-id="52248-444">businessphone:555-555-2121</span></span>         |
| <span data-ttu-id="52248-445">住家電話</span><span class="sxs-lookup"><span data-stu-id="52248-445">Home phone</span></span>            | <span data-ttu-id="52248-446">homePhone</span><span class="sxs-lookup"><span data-stu-id="52248-446">homephone</span></span>           | <span data-ttu-id="52248-447">homephone： 555-555-2121</span><span class="sxs-lookup"><span data-stu-id="52248-447">homephone:555-555-2121</span></span>             |
| <span data-ttu-id="52248-448">行動電話</span><span class="sxs-lookup"><span data-stu-id="52248-448">Mobile phone</span></span>          | <span data-ttu-id="52248-449">手機</span><span class="sxs-lookup"><span data-stu-id="52248-449">mobilephone</span></span>         | <span data-ttu-id="52248-450">mobilephone： 555-555-2121</span><span class="sxs-lookup"><span data-stu-id="52248-450">mobilephone:555-555-2121</span></span>           |
| <span data-ttu-id="52248-451">Office</span><span class="sxs-lookup"><span data-stu-id="52248-451">Office</span></span>                | <span data-ttu-id="52248-452">Office</span><span class="sxs-lookup"><span data-stu-id="52248-452">office</span></span>              | <span data-ttu-id="52248-453">office：範例</span><span class="sxs-lookup"><span data-stu-id="52248-453">office:sample</span></span>                      |
| <span data-ttu-id="52248-454">周年</span><span class="sxs-lookup"><span data-stu-id="52248-454">Anniversary</span></span>           | <span data-ttu-id="52248-455">周年</span><span class="sxs-lookup"><span data-stu-id="52248-455">anniversary</span></span>         | <span data-ttu-id="52248-456">周年紀念日： 1/1/06</span><span class="sxs-lookup"><span data-stu-id="52248-456">anniversary:1/1/06</span></span>                 |
| <span data-ttu-id="52248-457">Birthday</span><span class="sxs-lookup"><span data-stu-id="52248-457">Birthday</span></span>              | <span data-ttu-id="52248-458">生日</span><span class="sxs-lookup"><span data-stu-id="52248-458">birthday</span></span>            | <span data-ttu-id="52248-459">生日： 1/1/06</span><span class="sxs-lookup"><span data-stu-id="52248-459">birthday:1/1/06</span></span>                    |
| <span data-ttu-id="52248-460">網頁</span><span class="sxs-lookup"><span data-stu-id="52248-460">Web page</span></span>              | <span data-ttu-id="52248-461">網頁</span><span class="sxs-lookup"><span data-stu-id="52248-461">webpage</span></span>             | <span data-ttu-id="52248-462">網頁:www</span><span class="sxs-lookup"><span data-stu-id="52248-462">webpage:www.microsoft.com</span></span>          |



 

> [!Note]
>
> <span data-ttu-id="52248-463">電話號碼會依照輸入進行編制索引。</span><span class="sxs-lookup"><span data-stu-id="52248-463">Phone numbers are indexed as entered.</span></span> <span data-ttu-id="52248-464">例如，如果使用者在輸入電話號碼時未包含國家或區功能變數代碼，則如果在電話號碼中使用國家或區功能變數代碼進行搜尋，則使用者將無法找到連絡人。</span><span class="sxs-lookup"><span data-stu-id="52248-464">For example, if a user did not include a country or area code when entering the phone number, users will not be able to locate a contact if searching with country or area code in the phone number.</span></span>

 

### <a name="communications"></a><span data-ttu-id="52248-465">通訊</span><span class="sxs-lookup"><span data-stu-id="52248-465">Communications</span></span>

<span data-ttu-id="52248-466">這些是通訊的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-466">These are properties common to communications.</span></span> <span data-ttu-id="52248-467">若要將搜尋限制為僅限通訊，語法為：</span><span class="sxs-lookup"><span data-stu-id="52248-467">To limit the search to communications only, the syntax is:</span></span>

`kind:communications <property>:<value>`

<span data-ttu-id="52248-468">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-468">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-469">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-469">Property</span></span>       | <span data-ttu-id="52248-470">用法</span><span class="sxs-lookup"><span data-stu-id="52248-470">Use</span></span>                           | <span data-ttu-id="52248-471">範例</span><span class="sxs-lookup"><span data-stu-id="52248-471">Example</span></span>                         |
|----------------|-------------------------------|---------------------------------|
| <span data-ttu-id="52248-472">寄件者</span><span class="sxs-lookup"><span data-stu-id="52248-472">From</span></span>           | <span data-ttu-id="52248-473">from 或召集人</span><span class="sxs-lookup"><span data-stu-id="52248-473">from or organizer</span></span>             | <span data-ttu-id="52248-474">從： john</span><span class="sxs-lookup"><span data-stu-id="52248-474">from:john</span></span>                       |
| <span data-ttu-id="52248-475">已收到</span><span class="sxs-lookup"><span data-stu-id="52248-475">Received</span></span>       | <span data-ttu-id="52248-476">已接收或已傳送</span><span class="sxs-lookup"><span data-stu-id="52248-476">received or sent</span></span>              | <span data-ttu-id="52248-477">已傳送：昨天</span><span class="sxs-lookup"><span data-stu-id="52248-477">sent:yesterday</span></span>                  |
| <span data-ttu-id="52248-478">主體</span><span class="sxs-lookup"><span data-stu-id="52248-478">Subject</span></span>        | <span data-ttu-id="52248-479">主旨或標題</span><span class="sxs-lookup"><span data-stu-id="52248-479">subject or title</span></span>              | <span data-ttu-id="52248-480">主旨：「每季財務」</span><span class="sxs-lookup"><span data-stu-id="52248-480">subject:"Quarterly Financial"</span></span>   |
| <span data-ttu-id="52248-481">具有附件</span><span class="sxs-lookup"><span data-stu-id="52248-481">Has attachment</span></span> | <span data-ttu-id="52248-482">hasattachments, hasattachment</span><span class="sxs-lookup"><span data-stu-id="52248-482">hasattachments, hasattachment</span></span> | <span data-ttu-id="52248-483">hasattachment： true</span><span class="sxs-lookup"><span data-stu-id="52248-483">hasattachment:true</span></span>              |
| <span data-ttu-id="52248-484">附件</span><span class="sxs-lookup"><span data-stu-id="52248-484">Attachments</span></span>    | <span data-ttu-id="52248-485">附件或附件</span><span class="sxs-lookup"><span data-stu-id="52248-485">attachments or attachment</span></span>     | <span data-ttu-id="52248-486">attachment:presentation.ppt</span><span class="sxs-lookup"><span data-stu-id="52248-486">attachment:presentation.ppt</span></span>     |
| <span data-ttu-id="52248-487">密件副本</span><span class="sxs-lookup"><span data-stu-id="52248-487">Bcc</span></span>            | <span data-ttu-id="52248-488">密件副本、bccname 或 bccaddress</span><span class="sxs-lookup"><span data-stu-id="52248-488">bcc, bccname or bccaddress</span></span>    | <span data-ttu-id="52248-489">密件副本： dave</span><span class="sxs-lookup"><span data-stu-id="52248-489">bcc:dave</span></span>                        |
| <span data-ttu-id="52248-490">Cc 位址</span><span class="sxs-lookup"><span data-stu-id="52248-490">Cc address</span></span>     | <span data-ttu-id="52248-491">ccaddress 或 cc</span><span class="sxs-lookup"><span data-stu-id="52248-491">ccaddress or cc</span></span>               | <span data-ttu-id="52248-492">ccaddress： john\_doe@outlook.com</span><span class="sxs-lookup"><span data-stu-id="52248-492">ccaddress:john\_doe@outlook.com</span></span> |
| <span data-ttu-id="52248-493">後續追蹤旗標</span><span class="sxs-lookup"><span data-stu-id="52248-493">Follow-up flag</span></span> | <span data-ttu-id="52248-494">followupflag</span><span class="sxs-lookup"><span data-stu-id="52248-494">followupflag</span></span>                  | <span data-ttu-id="52248-495">followupflag：2</span><span class="sxs-lookup"><span data-stu-id="52248-495">followupflag:2</span></span>                  |
| <span data-ttu-id="52248-496">到期日</span><span class="sxs-lookup"><span data-stu-id="52248-496">Due date</span></span>       | <span data-ttu-id="52248-497">duedate 或逾期</span><span class="sxs-lookup"><span data-stu-id="52248-497">duedate or due</span></span>                | <span data-ttu-id="52248-498">逾期：上周</span><span class="sxs-lookup"><span data-stu-id="52248-498">due:last week</span></span>                   |
| <span data-ttu-id="52248-499">讀取</span><span class="sxs-lookup"><span data-stu-id="52248-499">Read</span></span>           | <span data-ttu-id="52248-500">read 或 isread</span><span class="sxs-lookup"><span data-stu-id="52248-500">read or isread</span></span>                | <span data-ttu-id="52248-501">是： read</span><span class="sxs-lookup"><span data-stu-id="52248-501">is:read</span></span>                         |
| <span data-ttu-id="52248-502">已完成</span><span class="sxs-lookup"><span data-stu-id="52248-502">Is completed</span></span>   | <span data-ttu-id="52248-503">iscompleted</span><span class="sxs-lookup"><span data-stu-id="52248-503">iscompleted</span></span>                   | <span data-ttu-id="52248-504">是：已完成</span><span class="sxs-lookup"><span data-stu-id="52248-504">is:completed</span></span>                    |
| <span data-ttu-id="52248-505">不完整</span><span class="sxs-lookup"><span data-stu-id="52248-505">Incomplete</span></span>     | <span data-ttu-id="52248-506">未完成或 isincomplete</span><span class="sxs-lookup"><span data-stu-id="52248-506">incomplete or isincomplete</span></span>    | <span data-ttu-id="52248-507">為：不完整</span><span class="sxs-lookup"><span data-stu-id="52248-507">is:incomplete</span></span>                   |
| <span data-ttu-id="52248-508">有旗標</span><span class="sxs-lookup"><span data-stu-id="52248-508">Has flag</span></span>       | <span data-ttu-id="52248-509">hasflag 或 isflagged</span><span class="sxs-lookup"><span data-stu-id="52248-509">hasflag or isflagged</span></span>          | <span data-ttu-id="52248-510">具有：旗標</span><span class="sxs-lookup"><span data-stu-id="52248-510">has:flag</span></span>                        |
| <span data-ttu-id="52248-511">持續時間</span><span class="sxs-lookup"><span data-stu-id="52248-511">Duration</span></span>       | <span data-ttu-id="52248-512">duration</span><span class="sxs-lookup"><span data-stu-id="52248-512">duration</span></span>                      | <span data-ttu-id="52248-513">持續時間： > 50</span><span class="sxs-lookup"><span data-stu-id="52248-513">duration:> 50</span></span>                |



 

### <a name="calendar"></a><span data-ttu-id="52248-514">Calendar</span><span class="sxs-lookup"><span data-stu-id="52248-514">Calendar</span></span>

<span data-ttu-id="52248-515">這些是行事曆的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-515">These are properties common to calendars.</span></span> <span data-ttu-id="52248-516">若要將搜尋限制為僅限行事曆，語法為：</span><span class="sxs-lookup"><span data-stu-id="52248-516">To limit the search to calendars only, the syntax is:</span></span>

`kind:calendar <property>:<value>`

<span data-ttu-id="52248-517">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-517">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-518">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-518">Property</span></span>  | <span data-ttu-id="52248-519">用法</span><span class="sxs-lookup"><span data-stu-id="52248-519">Use</span></span>                      | <span data-ttu-id="52248-520">範例</span><span class="sxs-lookup"><span data-stu-id="52248-520">Example</span></span>          |
|-----------|--------------------------|------------------|
| <span data-ttu-id="52248-521">重複執行</span><span class="sxs-lookup"><span data-stu-id="52248-521">Recurring</span></span> | <span data-ttu-id="52248-522">週期性或 isrecurring</span><span class="sxs-lookup"><span data-stu-id="52248-522">recurring or isrecurring</span></span> | <span data-ttu-id="52248-523">是：週期性</span><span class="sxs-lookup"><span data-stu-id="52248-523">is:recurring</span></span>     |
| <span data-ttu-id="52248-524">組織者</span><span class="sxs-lookup"><span data-stu-id="52248-524">Organizer</span></span> | <span data-ttu-id="52248-525">召集人、依據或</span><span class="sxs-lookup"><span data-stu-id="52248-525">organizer, by or from</span></span>    | <span data-ttu-id="52248-526">召集人： debbie</span><span class="sxs-lookup"><span data-stu-id="52248-526">organizer:debbie</span></span> |



 

### <a name="documents"></a><span data-ttu-id="52248-527">文件</span><span class="sxs-lookup"><span data-stu-id="52248-527">Documents</span></span>

<span data-ttu-id="52248-528">這些是檔的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-528">These are properties common to documents.</span></span> <span data-ttu-id="52248-529">若要將搜尋限制為僅限檔，語法為：</span><span class="sxs-lookup"><span data-stu-id="52248-529">To limit the search to documents only, the syntax is:</span></span>

`kind:documents <property>:<value>`

<span data-ttu-id="52248-530">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-530">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-531">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-531">Property</span></span>          | <span data-ttu-id="52248-532">用法</span><span class="sxs-lookup"><span data-stu-id="52248-532">Use</span></span>             | <span data-ttu-id="52248-533">範例</span><span class="sxs-lookup"><span data-stu-id="52248-533">Example</span></span>                       |
|-------------------|-----------------|-------------------------------|
| <span data-ttu-id="52248-534">註解</span><span class="sxs-lookup"><span data-stu-id="52248-534">Comments</span></span>          | <span data-ttu-id="52248-535">comments</span><span class="sxs-lookup"><span data-stu-id="52248-535">comments</span></span>        | <span data-ttu-id="52248-536">批註：「需要最終評論」</span><span class="sxs-lookup"><span data-stu-id="52248-536">comments:"needs final review"</span></span> |
| <span data-ttu-id="52248-537">上次儲存者</span><span class="sxs-lookup"><span data-stu-id="52248-537">Last saved by</span></span>     | <span data-ttu-id="52248-538">lastsavedby</span><span class="sxs-lookup"><span data-stu-id="52248-538">lastsavedby</span></span>     | <span data-ttu-id="52248-539">lastsavedby： john</span><span class="sxs-lookup"><span data-stu-id="52248-539">lastsavedby:john</span></span>              |
| <span data-ttu-id="52248-540">檔管理員</span><span class="sxs-lookup"><span data-stu-id="52248-540">Document manager</span></span>  | <span data-ttu-id="52248-541">documentmanager</span><span class="sxs-lookup"><span data-stu-id="52248-541">documentmanager</span></span> | <span data-ttu-id="52248-542">documentmanager： john</span><span class="sxs-lookup"><span data-stu-id="52248-542">documentmanager:john</span></span>          |
| <span data-ttu-id="52248-543">修訂編號</span><span class="sxs-lookup"><span data-stu-id="52248-543">Revision number</span></span>   | <span data-ttu-id="52248-544">revisionnumber</span><span class="sxs-lookup"><span data-stu-id="52248-544">revisionnumber</span></span>  | <span data-ttu-id="52248-545">revisionnumber：1.0。3</span><span class="sxs-lookup"><span data-stu-id="52248-545">revisionnumber:1.0.3</span></span>          |
| <span data-ttu-id="52248-546">檔案格式</span><span class="sxs-lookup"><span data-stu-id="52248-546">Document format</span></span>   | <span data-ttu-id="52248-547">documentformat</span><span class="sxs-lookup"><span data-stu-id="52248-547">documentformat</span></span>  | <span data-ttu-id="52248-548">documentformat： MIMETYPE</span><span class="sxs-lookup"><span data-stu-id="52248-548">documentformat:MIMETYPE</span></span>       |
| <span data-ttu-id="52248-549">上次列印日期</span><span class="sxs-lookup"><span data-stu-id="52248-549">Date last printed</span></span> | <span data-ttu-id="52248-550">datelastprinted</span><span class="sxs-lookup"><span data-stu-id="52248-550">datelastprinted</span></span> | <span data-ttu-id="52248-551">datelastprinted：上周</span><span class="sxs-lookup"><span data-stu-id="52248-551">datelastprinted:last week</span></span>     |



 

### <a name="presentation"></a><span data-ttu-id="52248-552">簡報</span><span class="sxs-lookup"><span data-stu-id="52248-552">Presentation</span></span>

<span data-ttu-id="52248-553">這些是簡報的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-553">These are properties common to presentations.</span></span> <span data-ttu-id="52248-554">若要將搜尋限制為只搜尋簡報，語法為：</span><span class="sxs-lookup"><span data-stu-id="52248-554">To limit the search to presentations only, the syntax is:</span></span>

`kind:presentation <property>:<value>`

<span data-ttu-id="52248-555">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-555">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-556">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-556">Property</span></span>    | <span data-ttu-id="52248-557">用法</span><span class="sxs-lookup"><span data-stu-id="52248-557">Use</span></span>        | <span data-ttu-id="52248-558">範例</span><span class="sxs-lookup"><span data-stu-id="52248-558">Example</span></span>           |
|-------------|------------|-------------------|
| <span data-ttu-id="52248-559">投影片計數</span><span class="sxs-lookup"><span data-stu-id="52248-559">Slide count</span></span> | <span data-ttu-id="52248-560">slidecount</span><span class="sxs-lookup"><span data-stu-id="52248-560">slidecount</span></span> | <span data-ttu-id="52248-561">slidecount： >20</span><span class="sxs-lookup"><span data-stu-id="52248-561">slidecount:>20</span></span> |



 

### <a name="music"></a><span data-ttu-id="52248-562">音樂</span><span class="sxs-lookup"><span data-stu-id="52248-562">Music</span></span>

<span data-ttu-id="52248-563">這些是音樂檔案的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-563">These are properties common to music files.</span></span> <span data-ttu-id="52248-564">若要將搜尋限制為僅限音樂，語法為：</span><span class="sxs-lookup"><span data-stu-id="52248-564">To limit the search to music only, the syntax is:</span></span>

`kind:music <property>:<value>`

<span data-ttu-id="52248-565">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-565">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-566">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-566">Property</span></span> | <span data-ttu-id="52248-567">用法</span><span class="sxs-lookup"><span data-stu-id="52248-567">Use</span></span>                | <span data-ttu-id="52248-568">範例</span><span class="sxs-lookup"><span data-stu-id="52248-568">Example</span></span>                  |
|----------|--------------------|--------------------------|
| <span data-ttu-id="52248-569">位元速率</span><span class="sxs-lookup"><span data-stu-id="52248-569">Bit rate</span></span> | <span data-ttu-id="52248-570">位元速率，費率</span><span class="sxs-lookup"><span data-stu-id="52248-570">bitrate, rate</span></span>      | <span data-ttu-id="52248-571">位元速率：192</span><span class="sxs-lookup"><span data-stu-id="52248-571">bitrate:192</span></span>              |
| <span data-ttu-id="52248-572">演出者</span><span class="sxs-lookup"><span data-stu-id="52248-572">Artist</span></span>   | <span data-ttu-id="52248-573">演出者、寄件者</span><span class="sxs-lookup"><span data-stu-id="52248-573">artist, by or from</span></span> | <span data-ttu-id="52248-574">演出者： John Singer</span><span class="sxs-lookup"><span data-stu-id="52248-574">artist:John Singer</span></span>       |
| <span data-ttu-id="52248-575">持續時間</span><span class="sxs-lookup"><span data-stu-id="52248-575">Duration</span></span> | <span data-ttu-id="52248-576">duration</span><span class="sxs-lookup"><span data-stu-id="52248-576">duration</span></span>           | <span data-ttu-id="52248-577">持續時間：3</span><span class="sxs-lookup"><span data-stu-id="52248-577">duration:3</span></span>               |
| <span data-ttu-id="52248-578">專輯</span><span class="sxs-lookup"><span data-stu-id="52248-578">Album</span></span>    | <span data-ttu-id="52248-579">專輯</span><span class="sxs-lookup"><span data-stu-id="52248-579">album</span></span>              | <span data-ttu-id="52248-580">專輯：「最大點擊次數」</span><span class="sxs-lookup"><span data-stu-id="52248-580">album:"greatest hits"</span></span>    |
| <span data-ttu-id="52248-581">Genre</span><span class="sxs-lookup"><span data-stu-id="52248-581">Genre</span></span>    | <span data-ttu-id="52248-582">genre</span><span class="sxs-lookup"><span data-stu-id="52248-582">genre</span></span>              | <span data-ttu-id="52248-583">genre:rock</span><span class="sxs-lookup"><span data-stu-id="52248-583">genre:rock</span></span>               |
| <span data-ttu-id="52248-584">Track</span><span class="sxs-lookup"><span data-stu-id="52248-584">Track</span></span>    | <span data-ttu-id="52248-585">追蹤</span><span class="sxs-lookup"><span data-stu-id="52248-585">track</span></span>              | <span data-ttu-id="52248-586">追蹤：12</span><span class="sxs-lookup"><span data-stu-id="52248-586">track:12</span></span>                 |
| <span data-ttu-id="52248-587">Year</span><span class="sxs-lookup"><span data-stu-id="52248-587">Year</span></span>     | <span data-ttu-id="52248-588">year</span><span class="sxs-lookup"><span data-stu-id="52248-588">year</span></span>               | <span data-ttu-id="52248-589">year： > 1980 < 1990</span><span class="sxs-lookup"><span data-stu-id="52248-589">year:> 1980 < 1990</span></span> |



 

### <a name="picture"></a><span data-ttu-id="52248-590">Picture</span><span class="sxs-lookup"><span data-stu-id="52248-590">Picture</span></span>

<span data-ttu-id="52248-591">這些是圖片的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-591">These are properties common to pictures.</span></span> <span data-ttu-id="52248-592">若要限制僅搜尋圖片，語法為：</span><span class="sxs-lookup"><span data-stu-id="52248-592">To limit the search to pictures only, the syntax is:</span></span>

`kind:picture <property>:<value>`

<span data-ttu-id="52248-593">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-593">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-594">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-594">Property</span></span>     | <span data-ttu-id="52248-595">用法</span><span class="sxs-lookup"><span data-stu-id="52248-595">Use</span></span>         | <span data-ttu-id="52248-596">範例</span><span class="sxs-lookup"><span data-stu-id="52248-596">Example</span></span>               |
|--------------|-------------|-----------------------|
| <span data-ttu-id="52248-597">攝影機製作</span><span class="sxs-lookup"><span data-stu-id="52248-597">Camera make</span></span>  | <span data-ttu-id="52248-598">cameramake</span><span class="sxs-lookup"><span data-stu-id="52248-598">cameramake</span></span>  | <span data-ttu-id="52248-599">cameramake：範例</span><span class="sxs-lookup"><span data-stu-id="52248-599">cameramake:sample</span></span>     |
| <span data-ttu-id="52248-600">攝影機模型</span><span class="sxs-lookup"><span data-stu-id="52248-600">Camera model</span></span> | <span data-ttu-id="52248-601">cameramodel</span><span class="sxs-lookup"><span data-stu-id="52248-601">cameramodel</span></span> | <span data-ttu-id="52248-602">cameramodel：範例</span><span class="sxs-lookup"><span data-stu-id="52248-602">cameramodel:sample</span></span>    |
| <span data-ttu-id="52248-603">維度</span><span class="sxs-lookup"><span data-stu-id="52248-603">Dimensions</span></span>   | <span data-ttu-id="52248-604">dimensions</span><span class="sxs-lookup"><span data-stu-id="52248-604">dimensions</span></span>  | <span data-ttu-id="52248-605">維度：8X10</span><span class="sxs-lookup"><span data-stu-id="52248-605">dimensions:8X10</span></span>       |
| <span data-ttu-id="52248-606">Orientation</span><span class="sxs-lookup"><span data-stu-id="52248-606">Orientation</span></span>  | <span data-ttu-id="52248-607">orientation</span><span class="sxs-lookup"><span data-stu-id="52248-607">orientation</span></span> | <span data-ttu-id="52248-608">方向：橫向</span><span class="sxs-lookup"><span data-stu-id="52248-608">orientation:landscape</span></span> |
| <span data-ttu-id="52248-609">拍攝日期</span><span class="sxs-lookup"><span data-stu-id="52248-609">Date taken</span></span>   | <span data-ttu-id="52248-610">datetaken</span><span class="sxs-lookup"><span data-stu-id="52248-610">datetaken</span></span>   | <span data-ttu-id="52248-611">datetaken：昨天</span><span class="sxs-lookup"><span data-stu-id="52248-611">datetaken:yesterday</span></span>   |
| <span data-ttu-id="52248-612">寬度</span><span class="sxs-lookup"><span data-stu-id="52248-612">Width</span></span>        | <span data-ttu-id="52248-613">width</span><span class="sxs-lookup"><span data-stu-id="52248-613">width</span></span>       | <span data-ttu-id="52248-614">寬度：1600</span><span class="sxs-lookup"><span data-stu-id="52248-614">width:1600</span></span>            |
| <span data-ttu-id="52248-615">高度</span><span class="sxs-lookup"><span data-stu-id="52248-615">Height</span></span>       | <span data-ttu-id="52248-616">身高</span><span class="sxs-lookup"><span data-stu-id="52248-616">height</span></span>      | <span data-ttu-id="52248-617">高度：1200</span><span class="sxs-lookup"><span data-stu-id="52248-617">height:1200</span></span>           |



 

### <a name="video"></a><span data-ttu-id="52248-618">影片</span><span class="sxs-lookup"><span data-stu-id="52248-618">Video</span></span>

<span data-ttu-id="52248-619">這些是影片的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="52248-619">These are properties common to videos.</span></span> <span data-ttu-id="52248-620">若要限制僅搜尋影片，語法為：</span><span class="sxs-lookup"><span data-stu-id="52248-620">To limit the search to videos only, the syntax is:</span></span>

`kind:video <property>:<value>`

<span data-ttu-id="52248-621">其中 `<property>` 是下面列出的屬性，而且 `<value>` 是使用者指定的搜尋詞彙。</span><span class="sxs-lookup"><span data-stu-id="52248-621">where `<property>` is a property listed below and `<value>` is the user-specified search term.</span></span>



| <span data-ttu-id="52248-622">屬性</span><span class="sxs-lookup"><span data-stu-id="52248-622">Property</span></span> | <span data-ttu-id="52248-623">用法</span><span class="sxs-lookup"><span data-stu-id="52248-623">Use</span></span>           | <span data-ttu-id="52248-624">範例</span><span class="sxs-lookup"><span data-stu-id="52248-624">Example</span></span>                                |
|----------|---------------|----------------------------------------|
| <span data-ttu-id="52248-625">Name</span><span class="sxs-lookup"><span data-stu-id="52248-625">Name</span></span>     | <span data-ttu-id="52248-626">name、subject</span><span class="sxs-lookup"><span data-stu-id="52248-626">name, subject</span></span> | <span data-ttu-id="52248-627">name： "家人度假給海灘 05"</span><span class="sxs-lookup"><span data-stu-id="52248-627">name:"Family Vacation to the Beach 05"</span></span> |
| <span data-ttu-id="52248-628">分機</span><span class="sxs-lookup"><span data-stu-id="52248-628">Ext</span></span>      | <span data-ttu-id="52248-629">ext、fileext</span><span class="sxs-lookup"><span data-stu-id="52248-629">ext, fileext</span></span>  | <span data-ttu-id="52248-630">ext:.avi</span><span class="sxs-lookup"><span data-stu-id="52248-630">ext:.avi</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="52248-631">相關主題</span><span class="sxs-lookup"><span data-stu-id="52248-631">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="52248-632">**參考**</span><span class="sxs-lookup"><span data-stu-id="52248-632">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="52248-633">認知類型</span><span class="sxs-lookup"><span data-stu-id="52248-633">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="52248-634">SchemaTable</span><span class="sxs-lookup"><span data-stu-id="52248-634">SchemaTable</span></span>](-search-2x-wds-schematable.md)
</dt> <dt>

[<span data-ttu-id="52248-635">從命令列呼叫 WDS</span><span class="sxs-lookup"><span data-stu-id="52248-635">Calling WDS from the Command Line</span></span>](-search-2x-wds-fromcommandline.md)
</dt> <dt>

[<span data-ttu-id="52248-636">從 Web Pages 呼叫 WDS</span><span class="sxs-lookup"><span data-stu-id="52248-636">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





