---
description: 描述如何建立 ( 的 OpenSearch 描述，以將外部資料存放區連接到 Windows 用戶端的 .osdx) 檔。
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: 在 Windows 同盟搜尋中建立 OpenSearch 描述檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943280"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a><span data-ttu-id="3868f-103">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="3868f-103">Creating an OpenSearch Description File in Windows Federated Search</span></span>

<span data-ttu-id="3868f-104">描述如何建立 ( 的 OpenSearch 描述，以將外部資料存放區連接到 Windows 客戶 [端的 .osdx](https://github.com/dewitt/opensearch)) 檔。</span><span class="sxs-lookup"><span data-stu-id="3868f-104">Describes how to create an OpenSearch Description (.osdx) file to connect external data stores to the Windows Client via the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="3868f-105">同盟搜尋可讓使用者搜尋遠端資料存放區，並從 Windows 檔案總管內查看結果。</span><span class="sxs-lookup"><span data-stu-id="3868f-105">Federated search enables users to search a remote data store and view the results from within Windows Explorer.</span></span>

<span data-ttu-id="3868f-106">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="3868f-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3868f-107">OpenSearch 描述檔</span><span class="sxs-lookup"><span data-stu-id="3868f-107">OpenSearch Description File</span></span>](#opensearch-description-file)
    -   [<span data-ttu-id="3868f-108">必要的必要子項目</span><span class="sxs-lookup"><span data-stu-id="3868f-108">Mininum Required Child Elements</span></span>](#mininum-required-child-elements)
-   [<span data-ttu-id="3868f-109">Windows 同盟搜尋中的標準元素</span><span class="sxs-lookup"><span data-stu-id="3868f-109">Standard Elements in Windows Federated Search</span></span>](#standard-elements-in-windows-federated-search)
    -   [<span data-ttu-id="3868f-110">Shortname</span><span class="sxs-lookup"><span data-stu-id="3868f-110">Shortname</span></span>](#shortname)
    -   [<span data-ttu-id="3868f-111">說明</span><span class="sxs-lookup"><span data-stu-id="3868f-111">Description</span></span>](#description)
    -   [<span data-ttu-id="3868f-112">RSS/Atom 結果的 URL 範本</span><span class="sxs-lookup"><span data-stu-id="3868f-112">URL Template for RSS/Atom Results</span></span>](#url-template-for-rssatom-results)
    -   [<span data-ttu-id="3868f-113">Web 結果的 URL 範本</span><span class="sxs-lookup"><span data-stu-id="3868f-113">URL Template for web Results</span></span>](#url-template-for-web-results)
    -   [<span data-ttu-id="3868f-114">URL 範本參數</span><span class="sxs-lookup"><span data-stu-id="3868f-114">URL Template Parameters</span></span>](#url-template-parameters)
    -   [<span data-ttu-id="3868f-115">分頁的結果</span><span class="sxs-lookup"><span data-stu-id="3868f-115">Paged Results</span></span>](#paged-results)
    -   [<span data-ttu-id="3868f-116">使用專案索引進行分頁</span><span class="sxs-lookup"><span data-stu-id="3868f-116">Paging Using the Item Index</span></span>](#paging-using-the-item-index)
    -   [<span data-ttu-id="3868f-117">使用頁面索引進行分頁</span><span class="sxs-lookup"><span data-stu-id="3868f-117">Paging Using the Page Index</span></span>](#paging-using-the-page-index)
    -   [<span data-ttu-id="3868f-118">頁面大小</span><span class="sxs-lookup"><span data-stu-id="3868f-118">Page Size</span></span>](#page-size)
-   [<span data-ttu-id="3868f-119">Windows 同盟搜尋中的擴充元素</span><span class="sxs-lookup"><span data-stu-id="3868f-119">Extended Elements in Windows Federated Search</span></span>](#extended-elements-in-windows-federated-search)
    -   [<span data-ttu-id="3868f-120">最大結果計數</span><span class="sxs-lookup"><span data-stu-id="3868f-120">Maximum Result Count</span></span>](#maximum-result-count)
    -   [<span data-ttu-id="3868f-121">屬性對應</span><span class="sxs-lookup"><span data-stu-id="3868f-121">Property Mapping</span></span>](#property-mapping)
-   [<span data-ttu-id="3868f-122">預覽</span><span class="sxs-lookup"><span data-stu-id="3868f-122">Previews</span></span>](#previews)
-   [<span data-ttu-id="3868f-123">開啟檔案位置功能表項目</span><span class="sxs-lookup"><span data-stu-id="3868f-123">Open File Location Menu Item</span></span>](#open-file-location-menu-item)
-   [<span data-ttu-id="3868f-124">其他資源</span><span class="sxs-lookup"><span data-stu-id="3868f-124">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="3868f-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="3868f-125">Related topics</span></span>](#related-topics)

## <a name="opensearch-description-file"></a><span data-ttu-id="3868f-126">OpenSearch 描述檔</span><span class="sxs-lookup"><span data-stu-id="3868f-126">OpenSearch Description File</span></span>

<span data-ttu-id="3868f-127">適用于 Windows 同盟搜尋 ( .osdx) 檔的 OpenSearch 描述必須遵守下列規則：</span><span class="sxs-lookup"><span data-stu-id="3868f-127">An OpenSearch Description (.osdx) file for Windows Federated Search must abide by the following rules:</span></span>

-   <span data-ttu-id="3868f-128">這是由 [opensearch](https://github.com/dewitt/opensearch) 1.1 規格所定義的有效的 OpenSearch 描述檔。</span><span class="sxs-lookup"><span data-stu-id="3868f-128">Be a valid OpenSearch Description document, as defined by the [OpenSearch](https://github.com/dewitt/opensearch) 1.1 specification.</span></span>
-   <span data-ttu-id="3868f-129">請提供具有 RSS 或 Atom 格式類型的 URL 範本。</span><span class="sxs-lookup"><span data-stu-id="3868f-129">Provide a URL template with either an RSS or an Atom format type.</span></span>
-   <span data-ttu-id="3868f-130">從 web 下載時，請使用 .osdx 副檔名，或與 .osdx 副檔名相關聯。</span><span class="sxs-lookup"><span data-stu-id="3868f-130">Use the .osdx file name extension, or be associated with the .osdx file name extension when downloading from the web.</span></span> <span data-ttu-id="3868f-131">例如，伺服器不需要使用 .osdx。</span><span class="sxs-lookup"><span data-stu-id="3868f-131">For example, a server is not required to use .osdx.</span></span> <span data-ttu-id="3868f-132">伺服器可以傳回具有任何副檔名的檔案（例如 .xml），並將其視為 .osdx 檔案（如果它使用適用于 OpenSearch 描述檔的正確 MIME 型別， (. .osdx 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="3868f-132">A server can return the file with any file name extension, such as .xml for example, and treated as if it were an .osdx file if it uses the correct MIME Type for OpenSearch Description documents (.osdx files).</span></span>
-   <span data-ttu-id="3868f-133"> (建議的) 提供 **ShortName** 元素值。</span><span class="sxs-lookup"><span data-stu-id="3868f-133">Provide a **ShortName** element value (recommended).</span></span>

### <a name="mininum-required-child-elements"></a><span data-ttu-id="3868f-134">必要的必要子項目</span><span class="sxs-lookup"><span data-stu-id="3868f-134">Mininum Required Child Elements</span></span>

<span data-ttu-id="3868f-135">下列 .osdx 檔案是由 **ShortName** 和專案所組成 `Url` ，這些都是必要的最小子項目。</span><span class="sxs-lookup"><span data-stu-id="3868f-135">The following example .osdx file consists of **ShortName** and `Url` elements, which are the minimum required child elements.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a><span data-ttu-id="3868f-136">Windows 同盟搜尋中的標準元素</span><span class="sxs-lookup"><span data-stu-id="3868f-136">Standard Elements in Windows Federated Search</span></span>

<span data-ttu-id="3868f-137">除了最小的子項目之外，同盟搜尋也支援下列標準元素。</span><span class="sxs-lookup"><span data-stu-id="3868f-137">In addition to the minimum child elements, federated search supports the following standard elements.</span></span>

### <a name="shortname"></a><span data-ttu-id="3868f-138">Shortname</span><span class="sxs-lookup"><span data-stu-id="3868f-138">Shortname</span></span>

<span data-ttu-id="3868f-139">Windows 使用 **ShortName** 元素值，將 searchconnector-ms (搜尋連接器命名為當使用者開啟 .osdx 檔案時所建立的) 檔案。</span><span class="sxs-lookup"><span data-stu-id="3868f-139">Windows uses the **ShortName** element value to name the .searchconnector-ms (search connector) file that is created when the user opens the .osdx file.</span></span> <span data-ttu-id="3868f-140">Windows 可確保產生的檔案名只使用 Windows 檔案名中允許的字元。</span><span class="sxs-lookup"><span data-stu-id="3868f-140">Windows ensures that the generated file name uses only characters that are allowed in Windows file names.</span></span> <span data-ttu-id="3868f-141">如果未提供任何 **ShortName** 值，searchconnector-ms 檔案會嘗試改用 .osdx 檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="3868f-141">If no **ShortName** value is provided, the .searchconnector-ms file tries to use the file name of the .osdx file instead.</span></span>

<span data-ttu-id="3868f-142">下列程式碼說明如何在 .osdx 檔案中使用 **ShortName** 元素。</span><span class="sxs-lookup"><span data-stu-id="3868f-142">The following code illustrates how to use the **ShortName** element in an .osdx file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a><span data-ttu-id="3868f-143">Description</span><span class="sxs-lookup"><span data-stu-id="3868f-143">Description</span></span>

<span data-ttu-id="3868f-144">當使用者選取 searchconnector-ms 檔案時，Windows 會使用 **Description** 元素值來填入 [Windows 檔案總管詳細資料] 窗格中顯示的檔案描述。</span><span class="sxs-lookup"><span data-stu-id="3868f-144">Windows uses the **Description** element value to populate the file description shown in the Windows Explorer details pane when a user selects a .searchconnector-ms file.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a><span data-ttu-id="3868f-145">RSS/Atom 結果的 URL 範本</span><span class="sxs-lookup"><span data-stu-id="3868f-145">URL Template for RSS/Atom Results</span></span>

<span data-ttu-id="3868f-146">.Osdx 檔案必須包含一個 **url 格式** 專案和樣板屬性 (url **範本，)** 以 RSS 或 Atom 格式傳回結果。</span><span class="sxs-lookup"><span data-stu-id="3868f-146">The .osdx file must include one **Url format** element and **template** attribute (a URL template) that returns results in either RSS or Atom format.</span></span> <span data-ttu-id="3868f-147">格式屬性必須 `application/rss+xml` 針對 RSS 格式化的結果設定為，或 `application/atom+xml` 針對 Atom 格式的結果設定為，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="3868f-147">The format attribute must be set to `application/rss+xml` for RSS formatted results, or `application/atom+xml` for Atom formatted results, as shown in the following code.</span></span>

> [!Note]  
> <span data-ttu-id="3868f-148">**Url 格式** 元素和 **範本** 屬性通常稱為 url 範本。</span><span class="sxs-lookup"><span data-stu-id="3868f-148">The **Url format** element and **template** attribute are commonly known as a URL template.</span></span>

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a><span data-ttu-id="3868f-149">Web 結果的 URL 範本</span><span class="sxs-lookup"><span data-stu-id="3868f-149">URL Template for web Results</span></span>

<span data-ttu-id="3868f-150">如果有可在網頁瀏覽器中查看的搜尋結果版本，您應該提供 **Url format =** `text/html` element 和 **template** 屬性，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="3868f-150">If there is a version of the search results that can be viewed in a web browser, you should provide a **Url format=**`text/html` element, and **template** attribute, as shown in the following code.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



<span data-ttu-id="3868f-151">如果您提供 **Url 格式 = "text/html"** 元素和 **範本** 屬性，則按鈕會出現在 Windows 檔案總管命令列中，如下列螢幕擷取畫面所示，可讓使用者在執行查詢時，開啟網頁瀏覽器來查看搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="3868f-151">If you provide a **Url format="text/html"** element and **template** attribute, a button appears in the Windows Explorer command bar, as shown in the following screen shot, that enables the user to open a web browser to view the search results when the user performs a query.</span></span>

![顯示 [web 搜尋匯總] 按鈕的螢幕擷取畫面。](images/websearchroll-overcommandbarbutton.png)

<span data-ttu-id="3868f-153">在某些案例中，查詢回復至資料存放區的 web UI 是很重要的。</span><span class="sxs-lookup"><span data-stu-id="3868f-153">The roll-over of the query back to the data store's web UI is important in some scenarios.</span></span> <span data-ttu-id="3868f-154">例如，使用者可能會想要查看超過100的結果 (的 OpenSearch 提供者所要求的預設專案數) 。</span><span class="sxs-lookup"><span data-stu-id="3868f-154">For example, a user may want to view more than 100 results (the default number of items the OpenSearch provider requests).</span></span> <span data-ttu-id="3868f-155">若是如此，使用者可能也會想要使用僅適用于資料存放區網站的搜尋功能，例如使用不同的排序次序重新查詢，或使用相關的中繼資料來切換和篩選查詢。</span><span class="sxs-lookup"><span data-stu-id="3868f-155">If so, the user may also want to use search features that are available only on the data store's website, such as re-querying with a different sort order, or pivoting and filtering the query with related metadata.</span></span>

### <a name="url-template-parameters"></a><span data-ttu-id="3868f-156">URL 範本參數</span><span class="sxs-lookup"><span data-stu-id="3868f-156">URL Template Parameters</span></span>

<span data-ttu-id="3868f-157">OpenSearch 提供者一律會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="3868f-157">The OpenSearch provider performs always the following actions:</span></span>

1.  <span data-ttu-id="3868f-158">使用 URL 範本將要求傳送至 web 服務。</span><span class="sxs-lookup"><span data-stu-id="3868f-158">Uses the URL template to send the request to the web service.</span></span>
2.  <span data-ttu-id="3868f-159">將要求傳送至 web 服務之前，嘗試取代 URL 範本中找到的權杖，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3868f-159">Attempts to replace the tokens found in the URL template before sending the request to the web service, as follows:</span></span>
    -   <span data-ttu-id="3868f-160">取代下表所列的標準 OpenSearch 權杖。</span><span class="sxs-lookup"><span data-stu-id="3868f-160">Replaces the standard OpenSearch tokens that are listed in the following table.</span></span>
    -   <span data-ttu-id="3868f-161">移除下表中未列出的任何權杖。</span><span class="sxs-lookup"><span data-stu-id="3868f-161">Removes any tokens that are not listed in the following table.</span></span>



| <span data-ttu-id="3868f-162">支援的權杖</span><span class="sxs-lookup"><span data-stu-id="3868f-162">Supported token</span></span>  | <span data-ttu-id="3868f-163">由 OpenSearch 提供者使用的方式</span><span class="sxs-lookup"><span data-stu-id="3868f-163">How used by OpenSearch provider</span></span>                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3868f-164">SearchTerms</span><span class="sxs-lookup"><span data-stu-id="3868f-164">{searchTerms}</span></span>    | <span data-ttu-id="3868f-165">取代為使用者在 Windows 檔案總管搜尋輸入方塊中輸入的搜尋字詞。</span><span class="sxs-lookup"><span data-stu-id="3868f-165">Replaced with the search terms that the user types in the Windows Explorer search input box.</span></span><br/>                                         |
| <span data-ttu-id="3868f-166">StartIndex</span><span class="sxs-lookup"><span data-stu-id="3868f-166">{startIndex}</span></span>     | <span data-ttu-id="3868f-167">在「頁面」中取得結果時使用。</span><span class="sxs-lookup"><span data-stu-id="3868f-167">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="3868f-168">取代為要傳回的第一個結果專案的索引。</span><span class="sxs-lookup"><span data-stu-id="3868f-168">Replaced with the index for the first result item to return.</span></span><br/>                        |
| <span data-ttu-id="3868f-169">StartPage</span><span class="sxs-lookup"><span data-stu-id="3868f-169">{startPage}</span></span>      | <span data-ttu-id="3868f-170">在「頁面」中取得結果時使用。</span><span class="sxs-lookup"><span data-stu-id="3868f-170">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="3868f-171">取代為要傳回之搜尋結果集的頁碼。</span><span class="sxs-lookup"><span data-stu-id="3868f-171">Replaced with the page number of the set of search results to return.</span></span><br/>               |
| <span data-ttu-id="3868f-172">字數</span><span class="sxs-lookup"><span data-stu-id="3868f-172">{count}</span></span>          | <span data-ttu-id="3868f-173">在「頁面」中取得結果時使用。</span><span class="sxs-lookup"><span data-stu-id="3868f-173">Used when getting results in "pages".</span></span><br/> <span data-ttu-id="3868f-174">以每頁 Windows 檔案總管要求的搜尋結果數目取代。</span><span class="sxs-lookup"><span data-stu-id="3868f-174">Replaced with the number of search results per page that Windows Explorer requests.</span></span><br/> |
| <span data-ttu-id="3868f-175">語言</span><span class="sxs-lookup"><span data-stu-id="3868f-175">{language}</span></span>       | <span data-ttu-id="3868f-176">取代為字串，表示要傳送之查詢的語言。</span><span class="sxs-lookup"><span data-stu-id="3868f-176">Replaced with a string that indicates the language of the query being sent.</span></span><br/>                                                          |
| <span data-ttu-id="3868f-177">{inputEncoding}</span><span class="sxs-lookup"><span data-stu-id="3868f-177">{inputEncoding}</span></span>  | <span data-ttu-id="3868f-178">以字串取代 (這類「UTF-16」 ) ，表示要傳送之查詢的字元編碼。</span><span class="sxs-lookup"><span data-stu-id="3868f-178">Replaced with a string (such "UTF-16") that indicates the character encoding of the query being sent.</span></span><br/>                                |
| <span data-ttu-id="3868f-179">OutputEncoding</span><span class="sxs-lookup"><span data-stu-id="3868f-179">{outputEncoding}</span></span> | <span data-ttu-id="3868f-180">取代為字串 (例如 "UTF-16" ) ，表示所需的 web 服務回應字元編碼。</span><span class="sxs-lookup"><span data-stu-id="3868f-180">Replaced with a string (such as "UTF-16") that indicates the desired character encoding for the response from the web service.</span></span><br/>       |



 

### <a name="paged-results"></a><span data-ttu-id="3868f-181">分頁的結果</span><span class="sxs-lookup"><span data-stu-id="3868f-181">Paged Results</span></span>

<span data-ttu-id="3868f-182">您可能會想要限制每個要求傳回的結果數目。</span><span class="sxs-lookup"><span data-stu-id="3868f-182">You may want to limit the number of results returned per request.</span></span> <span data-ttu-id="3868f-183">您可以選擇一次傳回結果的「頁面」，或讓 OpenSearch 提供者依專案編號或頁碼取得額外的結果頁面。</span><span class="sxs-lookup"><span data-stu-id="3868f-183">You can opt to return a "page" of results at a time, or to have the OpenSearch provider get additional pages of results either by item number or page number.</span></span> <span data-ttu-id="3868f-184">例如，如果您每個頁面傳送二十個結果，則您傳送的第一個頁面會在專案索引1和頁面1開始：您傳送的第二個頁面會從專案索引21開始，在第2頁開始。</span><span class="sxs-lookup"><span data-stu-id="3868f-184">For example, if you send twenty results per page, the first page you send starts at item index 1 and at page 1; the second page you send starts at item index 21 and at page 2.</span></span> <span data-ttu-id="3868f-185">您可以使用 `{startItem}` URL 範本中的或標記，來定義要讓 OpenSearch 提供者要求專案的方式 `{startPage}` 。</span><span class="sxs-lookup"><span data-stu-id="3868f-185">You can define how you want the OpenSearch provider to request items by using either the `{startItem}` or the `{startPage}` token in the URL template.</span></span>

### <a name="paging-using-the-item-index"></a><span data-ttu-id="3868f-186">使用專案索引進行分頁</span><span class="sxs-lookup"><span data-stu-id="3868f-186">Paging Using the Item Index</span></span>

<span data-ttu-id="3868f-187">專案索引會識別結果頁面中的第一個結果專案。</span><span class="sxs-lookup"><span data-stu-id="3868f-187">An item index identifies the first result item in a page of results.</span></span> <span data-ttu-id="3868f-188">如果您想要讓用戶端使用專案索引來傳送要求，您可以使用 `{startIndex}` **Url** 專案 **範本** 屬性中的權杖，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="3868f-188">If you want clients to send requests using an item index, you can use the `{startIndex}` token in your **Url** element **template** attribute, as shown in the following code.</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



<span data-ttu-id="3868f-189">然後，[ [OpenSearch](https://github.com/dewitt/opensearch) 提供者] 會將 URL 中的權杖取代為起始索引值。</span><span class="sxs-lookup"><span data-stu-id="3868f-189">The [OpenSearch](https://github.com/dewitt/opensearch) provider then replaces the token in the URL with a starting index value.</span></span> <span data-ttu-id="3868f-190">第一個要求會從第一個專案開始，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="3868f-190">The first request starts with the first item, as illustrated in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1
```



<span data-ttu-id="3868f-191">藉由變更 `{startIndex}` 參數值併發出新的要求，OpenSearch 提供者可以取得其他專案。</span><span class="sxs-lookup"><span data-stu-id="3868f-191">The OpenSearch provider can get additional items by changing the `{startIndex}` parameter value and issuing a new request.</span></span> <span data-ttu-id="3868f-192">提供者會重複此程式，直到取得足夠的結果來滿足其限制，或達到結果的結尾。</span><span class="sxs-lookup"><span data-stu-id="3868f-192">The provider repeats this process until it gets enough results to satisfy its limit, or reaches the end of the results.</span></span> <span data-ttu-id="3868f-193">[OpenSearch 提供者] 會查看第一個結果頁面中的 web 服務所傳回的專案數，並將預期的頁面大小設定為該數位。</span><span class="sxs-lookup"><span data-stu-id="3868f-193">The OpenSearch provider looks at the number of items returned by the web service in the first page of results, and sets the expected page size to that number.</span></span> <span data-ttu-id="3868f-194">它會使用該數位來遞增 `{startIndex}` 後續要求的值。</span><span class="sxs-lookup"><span data-stu-id="3868f-194">It uses that number to increment the `{startIndex}` value for subsequent requests.</span></span> <span data-ttu-id="3868f-195">例如，如果 web 服務在第一個要求中傳回20個結果，則提供者會將預期的頁面大小設定為20。</span><span class="sxs-lookup"><span data-stu-id="3868f-195">For example, if the web service returns 20 results in the first request, then the provider sets the expected page size to 20.</span></span> <span data-ttu-id="3868f-196">在下一個要求中，提供者會以 `{startIndex}` 值21取代，以取得接下來的20個專案。</span><span class="sxs-lookup"><span data-stu-id="3868f-196">For the next request, the provider replaces `{startIndex}` with the value of 21 to get the next 20 items.</span></span>

> [!Note]  
> <span data-ttu-id="3868f-197">如果 web 服務所傳回的結果頁面所含的專案數少於預期的頁面大小，則 OpenSearch 提供者會假設它已收到最後一頁的結果，並停止發出要求。</span><span class="sxs-lookup"><span data-stu-id="3868f-197">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="paging-using-the-page-index"></a><span data-ttu-id="3868f-198">使用頁面索引進行分頁</span><span class="sxs-lookup"><span data-stu-id="3868f-198">Paging Using the Page Index</span></span>

<span data-ttu-id="3868f-199">頁面索引會識別指定的結果頁面。</span><span class="sxs-lookup"><span data-stu-id="3868f-199">A page index identifies the specified page of results.</span></span> <span data-ttu-id="3868f-200">如果您想要讓用戶端使用頁碼傳送要求，您可以使用 `{startPage}` **Url 格式** 專案 **範本** 屬性中的權杖來指出，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="3868f-200">If you want clients to send requests using a page number, you can use the `{startPage}` token in your **Url format** element **template** attribute to indicate that, as illustrated in the following example:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



<span data-ttu-id="3868f-201">然後，在 URL 中使用頁碼參數來取代權杖。</span><span class="sxs-lookup"><span data-stu-id="3868f-201">The OpenSearch provider then replaces the token in the URL with a page number parameter.</span></span> <span data-ttu-id="3868f-202">第一個要求會從第一頁開始，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="3868f-202">The first request starts with the first page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> <span data-ttu-id="3868f-203">如果 web 服務所傳回的結果頁面所含的專案數少於預期的頁面大小，則 OpenSearch 提供者會假設它已收到最後一頁的結果，並停止發出要求。</span><span class="sxs-lookup"><span data-stu-id="3868f-203">If a page of results returned by the web service has fewer items than the expected page size, then the OpenSearch provider assumes it has received the last page of results and stops making requests.</span></span>

 

### <a name="page-size"></a><span data-ttu-id="3868f-204">頁面大小</span><span class="sxs-lookup"><span data-stu-id="3868f-204">Page Size</span></span>

<span data-ttu-id="3868f-205">您可能會想要設定 web 服務，以允許要求指定頁面的大小，方法是在 URL 中使用某些參數。</span><span class="sxs-lookup"><span data-stu-id="3868f-205">You may want to configure your web service to permit a request to specify the size of the pages by using some parameter in the URL.</span></span> <span data-ttu-id="3868f-206">您必須使用權杖，在 .osdx 檔案中指定要求，如下所示 `{count}` ：</span><span class="sxs-lookup"><span data-stu-id="3868f-206">A request must be specified in the .osdx file by using the `{count}` token, as follows:</span></span>


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



<span data-ttu-id="3868f-207">然後 [，您](https://github.com/dewitt/opensearch) 可以在每個頁面的結果數目中設定所需的頁面大小，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="3868f-207">The [OpenSearch](https://github.com/dewitt/opensearch) provider can then set the desired page size, in number of results per page, as shown in the following example:</span></span>


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



<span data-ttu-id="3868f-208">根據預設，[OpenSearch 提供者] 會使用頁面大小50來提出要求。</span><span class="sxs-lookup"><span data-stu-id="3868f-208">By default the OpenSearch provider makes requests using a page size of 50.</span></span> <span data-ttu-id="3868f-209">如果您想要不同的頁面大小，則請勿提供 `{count}` 權杖，而是將所需的數位直接放在 **Url 範本** 專案中。</span><span class="sxs-lookup"><span data-stu-id="3868f-209">If you want a different page size, then do not provide a `{count}` token, and instead place the desired number directly in the **Url template** element.</span></span>

<span data-ttu-id="3868f-210">[OpenSearch 提供者] 會根據第一個要求傳回的結果數目來決定頁面大小。</span><span class="sxs-lookup"><span data-stu-id="3868f-210">The OpenSearch provider determines the page size based on the number of results returned on the first request.</span></span> <span data-ttu-id="3868f-211">如果所收到結果的第一頁的專案數少於所要求的計數，則提供者會重設任何後續頁面要求的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="3868f-211">If the first page of results received has fewer items than the count requested, the provider resets the page size for any subsequent page requests.</span></span> <span data-ttu-id="3868f-212">如果後續頁面要求傳回的專案數少於所要求的數目，則 OpenSearch 提供者會假設它已達到結果的結尾。</span><span class="sxs-lookup"><span data-stu-id="3868f-212">If subsequent page requests return fewer items than requested, the OpenSearch provider assumes that it has reached the end of the results.</span></span>

## <a name="extended-elements-in-windows-federated-search"></a><span data-ttu-id="3868f-213">Windows 同盟搜尋中的擴充元素</span><span class="sxs-lookup"><span data-stu-id="3868f-213">Extended Elements in Windows Federated Search</span></span>

<span data-ttu-id="3868f-214">除了標準元素之外，同盟搜尋也支援下列擴充元素： **MaximumResultCount** 和 **ResultsProcessing**。</span><span class="sxs-lookup"><span data-stu-id="3868f-214">In addition to the standard elements, federated search supports the following extended elements: **MaximumResultCount** and **ResultsProcessing**.</span></span>

<span data-ttu-id="3868f-215">由於在 [OpenSearch](https://github.com/dewitt/opensearch) v1.1 規格中不支援這些擴充的子項目，因此必須使用下列命名空間來新增這些專案：</span><span class="sxs-lookup"><span data-stu-id="3868f-215">Because these extended child elements are not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification, they must be added by using the following namespace:</span></span>


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a><span data-ttu-id="3868f-216">最大結果計數</span><span class="sxs-lookup"><span data-stu-id="3868f-216">Maximum Result Count</span></span>

<span data-ttu-id="3868f-217">依預設，搜尋連接器的限制為每個使用者查詢100個結果。</span><span class="sxs-lookup"><span data-stu-id="3868f-217">By default, search connectors are limited to 100 results per user query.</span></span> <span data-ttu-id="3868f-218">這項限制可以透過將 **MaximumResultCount** 元素包含在 OSD 檔案中進行自訂，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="3868f-218">This limit can be customized by including the **MaximumResultCount** element within the OSD file as shown in the following example:</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



<span data-ttu-id="3868f-219">上述範例會宣告最上層 OpenSearchDescription 專案中的命名空間前置詞 `ms-ose` ，然後在專案名稱中使用該前置詞做為前置詞。</span><span class="sxs-lookup"><span data-stu-id="3868f-219">The preceding example declares the namespace prefix `ms-ose` in the top-level **OpenSearchDescription** element, and then uses it as a prefix in the element name.</span></span> <span data-ttu-id="3868f-220">此宣告是必要的，因為在 [OpenSearch](https://github.com/dewitt/opensearch) v1.1 規格中不支援 **MaximumResultCount** 。</span><span class="sxs-lookup"><span data-stu-id="3868f-220">This declaration is required because the **MaximumResultCount** is not supported in the [OpenSearch](https://github.com/dewitt/opensearch) v1.1 specification.</span></span>

### <a name="property-mapping"></a><span data-ttu-id="3868f-221">屬性對應</span><span class="sxs-lookup"><span data-stu-id="3868f-221">Property Mapping</span></span>

<span data-ttu-id="3868f-222">當 web 服務以 RSS 或 Atom 摘要傳回結果時，OpenSearch 提供者必須將摘要中的專案中繼資料對應至 Windows Shell 可以使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="3868f-222">When results are returned by the web service as an RSS or Atom feed, the OpenSearch provider must map the item metadata in the feeds to properties that the Windows Shell can use.</span></span> <span data-ttu-id="3868f-223">下列螢幕擷取畫面說明了 OpenSearch 提供者如何對應一些預設的 RSS 元素。</span><span class="sxs-lookup"><span data-stu-id="3868f-223">The following screen shot illustrates how the OpenSearch provider maps some of the default RSS elements.</span></span>

![顯示內建 rss 與 windows shell 屬性對應的螢幕擷取畫面](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a><span data-ttu-id="3868f-225">預設對應</span><span class="sxs-lookup"><span data-stu-id="3868f-225">Default Mappings</span></span>

<span data-ttu-id="3868f-226">下表列出 RSS XML 元素與 Windows Shell 系統屬性的預設對應。</span><span class="sxs-lookup"><span data-stu-id="3868f-226">The default mappings of RSS XML elements to Windows Shell system properties, are listed in the following table.</span></span> <span data-ttu-id="3868f-227">XML 路徑相對於 item 元素。</span><span class="sxs-lookup"><span data-stu-id="3868f-227">XML paths are relative to the item element.</span></span> <span data-ttu-id="3868f-228">`"media:"`前置詞是由[Yahoo Search namespace](https://www.rssboard.org/media-rss)命名空間所定義。</span><span class="sxs-lookup"><span data-stu-id="3868f-228">The `"media:"` prefix is defined by the [Yahoo Search Namespace](https://www.rssboard.org/media-rss) namespace.</span></span>



| <span data-ttu-id="3868f-229">RSS XML 路徑</span><span class="sxs-lookup"><span data-stu-id="3868f-229">RSS XML path</span></span>                  | <span data-ttu-id="3868f-230">Windows Shell 屬性 (標準名稱) </span><span class="sxs-lookup"><span data-stu-id="3868f-230">Windows Shell property (canonical name)</span></span> |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="3868f-231">連結</span><span class="sxs-lookup"><span data-stu-id="3868f-231">Link</span></span>                          | <span data-ttu-id="3868f-232">System. ItemUrl</span><span class="sxs-lookup"><span data-stu-id="3868f-232">System.ItemUrl</span></span>                          |
| <span data-ttu-id="3868f-233">標題</span><span class="sxs-lookup"><span data-stu-id="3868f-233">Title</span></span>                         | <span data-ttu-id="3868f-234">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="3868f-234">System.ItemName</span></span>                         |
| <span data-ttu-id="3868f-235">作者</span><span class="sxs-lookup"><span data-stu-id="3868f-235">Author</span></span>                        | <span data-ttu-id="3868f-236">System.Author</span><span class="sxs-lookup"><span data-stu-id="3868f-236">System.Author</span></span>                           |
| <span data-ttu-id="3868f-237">pubDate</span><span class="sxs-lookup"><span data-stu-id="3868f-237">pubDate</span></span>                       | <span data-ttu-id="3868f-238">System. DateModified</span><span class="sxs-lookup"><span data-stu-id="3868f-238">System.DateModified</span></span>                     |
| <span data-ttu-id="3868f-239">Description</span><span class="sxs-lookup"><span data-stu-id="3868f-239">Description</span></span>                   | <span data-ttu-id="3868f-240">System. AutoSummary</span><span class="sxs-lookup"><span data-stu-id="3868f-240">System.AutoSummary</span></span>                      |
| <span data-ttu-id="3868f-241">類別</span><span class="sxs-lookup"><span data-stu-id="3868f-241">Category</span></span>                      | <span data-ttu-id="3868f-242">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="3868f-242">System.Keywords</span></span>                         |
| enclosure/@type               | <span data-ttu-id="3868f-243">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="3868f-243">System.MIMEType</span></span>                         |
| enclosure/@length             | <span data-ttu-id="3868f-244">System. Size</span><span class="sxs-lookup"><span data-stu-id="3868f-244">System.Size</span></span>                             |
| enclosure/@url                | <span data-ttu-id="3868f-245">System. >contenturl</span><span class="sxs-lookup"><span data-stu-id="3868f-245">System.ContentUrl</span></span>                       |
| <span data-ttu-id="3868f-246">媒體：類別</span><span class="sxs-lookup"><span data-stu-id="3868f-246">media:category</span></span>                | <span data-ttu-id="3868f-247">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="3868f-247">System.Keywords</span></span>                         |
| media:content/@fileSize       | <span data-ttu-id="3868f-248">System. Size</span><span class="sxs-lookup"><span data-stu-id="3868f-248">System.Size</span></span>                             |
| media:content/@type           | <span data-ttu-id="3868f-249">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="3868f-249">System.MIMEType</span></span>                         |
| media:content/@url            | <span data-ttu-id="3868f-250">System. >contenturl</span><span class="sxs-lookup"><span data-stu-id="3868f-250">System.ContentUrl</span></span>                       |
| media:group/content/@fileSize | <span data-ttu-id="3868f-251">System. Size</span><span class="sxs-lookup"><span data-stu-id="3868f-251">System.Size</span></span>                             |
| media:group/content/@type     | <span data-ttu-id="3868f-252">System. MIMEType</span><span class="sxs-lookup"><span data-stu-id="3868f-252">System.MIMEType</span></span>                         |
| media:group/content/@url      | <span data-ttu-id="3868f-253">System. >contenturl</span><span class="sxs-lookup"><span data-stu-id="3868f-253">System.ContentUrl</span></span>                       |
| media:thumbnail/@url          | <span data-ttu-id="3868f-254">System. ItemThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="3868f-254">System.ItemThumbnailUrl</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="3868f-255">除了標準 RSS 或 Atom 專案的預設對應之外，您還可以在 Windows 命名空間中包含每個屬性的其他 XML 元素，藉以對應其他 Windows Shell 系統屬性。</span><span class="sxs-lookup"><span data-stu-id="3868f-255">In addition to the default mappings of standard RSS or Atom elements, you can map other Windows Shell system properties by including additional XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="3868f-256">您也可以在 .osdx 檔案中新增自訂屬性對應，以從其他現有的 XML 命名空間（例如 MediaRSS、iTunes 等等）對應元素。</span><span class="sxs-lookup"><span data-stu-id="3868f-256">You can also map elements from other existing XML namespaces such as MediaRSS, iTunes, and so forth, by adding custom property mapping in the .osdx file.</span></span>

 

### <a name="custom-property-mappings"></a><span data-ttu-id="3868f-257">自訂屬性對應</span><span class="sxs-lookup"><span data-stu-id="3868f-257">Custom Property Mappings</span></span>

<span data-ttu-id="3868f-258">您可以藉由指定 .osdx 檔案中的對應，自訂將 RSS 輸出中的專案對應至 Windows Shell 系統屬性。</span><span class="sxs-lookup"><span data-stu-id="3868f-258">You can customize the mapping of elements from your RSS output to Windows Shell system properties by specifying the mapping in the .osdx file.</span></span>

<span data-ttu-id="3868f-259">RSS 輸出會指定：</span><span class="sxs-lookup"><span data-stu-id="3868f-259">The RSS output specifies:</span></span>

-   <span data-ttu-id="3868f-260">XML 命名空間和</span><span class="sxs-lookup"><span data-stu-id="3868f-260">An XML namespace, and</span></span>
-   <span data-ttu-id="3868f-261">若為專案的任何子項目，則為要對應的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="3868f-261">For any child element of an item, an element name to map against.</span></span>

<span data-ttu-id="3868f-262">.Osdx 檔案會識別命名空間中每個元素名稱的 Windows Shell 屬性。</span><span class="sxs-lookup"><span data-stu-id="3868f-262">The .osdx file identifies a Windows Shell property for each element name in a namespace.</span></span> <span data-ttu-id="3868f-263">您在 .osdx 檔案中定義的屬性對應會覆寫這些指定屬性的預設對應（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="3868f-263">The property mappings that you define in your .osdx file override the default mappings, if they exist, for those specified properties.</span></span>

<span data-ttu-id="3868f-264">下圖說明 RSS 擴充功能如何對應至 Windows 屬性 (正式名稱) 。</span><span class="sxs-lookup"><span data-stu-id="3868f-264">The following diagram illustrates how an RSS extension maps to Windows properties (canonical name).</span></span>

![圖表顯示 xml 命名空間和 xml 路徑的組合會產生正式名稱](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a><span data-ttu-id="3868f-266">RSS 結果和 OSD 屬性對應範例</span><span class="sxs-lookup"><span data-stu-id="3868f-266">Example RSS results and OSD Property Mapping</span></span>

<span data-ttu-id="3868f-267">下列範例 RSS 輸出會將 " `https://example.com/schema/2009` example" 前置詞識別為 XML 命名空間。</span><span class="sxs-lookup"><span data-stu-id="3868f-267">The following example RSS output identifies `https://example.com/schema/2009` as the XML namespace with the prefix "example".</span></span> <span data-ttu-id="3868f-268">這個前置詞必須在 **電子郵件** 元素之前再次出現。</span><span class="sxs-lookup"><span data-stu-id="3868f-268">This prefix must appear again before the **email** element.</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



<span data-ttu-id="3868f-269">在下列 .osdx 檔中，XML **電子郵件** 專案會對應至 Windows Shell 屬性 [系統. EmailAddress](../properties/props-system-contact-emailaddress.md)。</span><span class="sxs-lookup"><span data-stu-id="3868f-269">In the following example .osdx file, the XML **email** element maps to the Windows Shell property [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md).</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



<span data-ttu-id="3868f-270">有些屬性是無法對應的，因為它們的值可能會在稍後覆寫或無法編輯。</span><span class="sxs-lookup"><span data-stu-id="3868f-270">There are some properties that cannot be mapped because values for them are either overridden later or are not editable.</span></span> <span data-ttu-id="3868f-271">例如，無法對應 [ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) 或 [ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) ，因為它們是從連結或主機殼元素中提供的 URL 值計算而來。</span><span class="sxs-lookup"><span data-stu-id="3868f-271">For example, [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) or [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) cannot be mapped because they are calculated from the URL value provided in either the link or enclosure elements.</span></span>

### <a name="thumbnails"></a><span data-ttu-id="3868f-272">縮圖</span><span class="sxs-lookup"><span data-stu-id="3868f-272">Thumbnails</span></span>

<span data-ttu-id="3868f-273">您可以使用 **media：縮圖 url = ""** 元素，為任何專案提供縮圖影像 url。</span><span class="sxs-lookup"><span data-stu-id="3868f-273">Thumbnail image URLs can be provided for any item by using the **media:thumbnail url=""** element.</span></span> <span data-ttu-id="3868f-274">理想的解決方式是 150 x 150 圖元。</span><span class="sxs-lookup"><span data-stu-id="3868f-274">The ideal resolution is 150 x 150 pixels.</span></span> <span data-ttu-id="3868f-275">支援的最大縮圖為 256 x 256 圖元。</span><span class="sxs-lookup"><span data-stu-id="3868f-275">The largest thumbnails supported are 256 x 256 pixels.</span></span> <span data-ttu-id="3868f-276">提供較大的影像會佔用更多頻寬，讓使用者不會有額外的好處。</span><span class="sxs-lookup"><span data-stu-id="3868f-276">Providing larger images takes more bandwidth for no extra benefit to the user.</span></span>

### <a name="open-file-location-context-menu"></a><span data-ttu-id="3868f-277">開啟檔案位置內容功能表</span><span class="sxs-lookup"><span data-stu-id="3868f-277">Open File Location Context Menu</span></span>

<span data-ttu-id="3868f-278">Windows 會提供一個快捷方式功能表，名為 [結果專案的 **開啟檔案位置** ]。</span><span class="sxs-lookup"><span data-stu-id="3868f-278">Windows provides a shortcut menu named **Open file location** for result items.</span></span> <span data-ttu-id="3868f-279">如果使用者從該功能表選取專案，則會開啟所選取專案的「父系」 URL。</span><span class="sxs-lookup"><span data-stu-id="3868f-279">If the user selects an item from that menu, the "parent" URL for the selected item is opened.</span></span> <span data-ttu-id="3868f-280">如果 URL 是 web URL （例如 `https://...` ），則會開啟網頁瀏覽器並流覽至該 url。</span><span class="sxs-lookup"><span data-stu-id="3868f-280">If the URL is a web URL, such as `https://...`, the web browser is opened and navigated to that URL.</span></span> <span data-ttu-id="3868f-281">您的摘要應該提供每個專案的自訂 URL，以確保 Windows 會開啟有效的 URL。</span><span class="sxs-lookup"><span data-stu-id="3868f-281">Your feed should provide a custom URL for each item to ensure that Windows opens a valid URL.</span></span> <span data-ttu-id="3868f-282">這可以藉由在專案 XML 內的元素內包含 URL 來完成，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="3868f-282">This can be accomplished by including the URL within an element inside the item's XML, as illustrated in the following example:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



<span data-ttu-id="3868f-283">如果未在專案的 XML 中明確設定此屬性，則 OpenSearch 提供者會將它設定為專案 URL 的父資料夾。</span><span class="sxs-lookup"><span data-stu-id="3868f-283">If this property is not explicitly set in the item's XML, the OpenSearch provider sets it to the parent folder of the URL of the item.</span></span> <span data-ttu-id="3868f-284">在上述範例中，[OpenSearch 提供者] 會使用連結值，並將 [ [ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell] 屬性值設定為 `"https://example.com/"` 。</span><span class="sxs-lookup"><span data-stu-id="3868f-284">In the example above, the OpenSearch provider would use the link value, and set the [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell property value to `"https://example.com/"`.</span></span>

### <a name="customize-windows-explorer-views-with-property-description-lists"></a><span data-ttu-id="3868f-285">使用屬性描述清單自訂 Windows 檔案總管的視圖</span><span class="sxs-lookup"><span data-stu-id="3868f-285">Customize Windows Explorer Views with Property Description Lists</span></span>

<span data-ttu-id="3868f-286">某些 Windows 檔案總管 view 版面配置是由屬性描述清單或 proplists 所定義。</span><span class="sxs-lookup"><span data-stu-id="3868f-286">Some Windows Explorer view layouts are defined by property description lists, or proplists.</span></span> <span data-ttu-id="3868f-287">Proplist 是以分號分隔的屬性清單（例如 `"prop:System.ItemName; System.Author"` ），可用來控制 Windows 檔案總管中顯示結果的方式。</span><span class="sxs-lookup"><span data-stu-id="3868f-287">A proplist is a semicolon-delimited list of properties, such as `"prop:System.ItemName; System.Author"`, that is used to control how your results appear in Windows Explorer.</span></span>

<span data-ttu-id="3868f-288">下列螢幕擷取畫面說明可使用 proplists 自訂之 Windows 檔案總管的 UI 區域：</span><span class="sxs-lookup"><span data-stu-id="3868f-288">The UI areas of Windows Explorer that can be customized by using proplists are illustrated in the following screen shot:</span></span>

![顯示 windows explorer ui 區域的螢幕擷取畫面，可使用 proplists 來自訂](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

<span data-ttu-id="3868f-290">Windows 檔案總管的每個區域都有相關聯的 proplists 集合，其本身會指定為屬性。</span><span class="sxs-lookup"><span data-stu-id="3868f-290">Each area of Windows Explorer has an associated set of proplists, which themselves are specified as properties.</span></span> <span data-ttu-id="3868f-291">您可以針對結果集內的個別專案或一組結果中的所有專案，指定自訂 proplists。</span><span class="sxs-lookup"><span data-stu-id="3868f-291">You can specify custom proplists for individual items in your result sets or for all items in a set of results.</span></span>



| <span data-ttu-id="3868f-292">要自訂的 UI 區域</span><span class="sxs-lookup"><span data-stu-id="3868f-292">UI Area to customize</span></span>               | <span data-ttu-id="3868f-293">執行自訂的 Windows Shell 屬性</span><span class="sxs-lookup"><span data-stu-id="3868f-293">Windows Shell property that implements the customization</span></span> |
|------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="3868f-294">搜尋) 時 (內容視圖模式</span><span class="sxs-lookup"><span data-stu-id="3868f-294">Content view mode (when searching)</span></span> | <span data-ttu-id="3868f-295">PropList. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="3868f-295">System.PropList.ContentViewModeForSearch</span></span>                 |
| <span data-ttu-id="3868f-296">流覽) 時 (內容視圖模式</span><span class="sxs-lookup"><span data-stu-id="3868f-296">Content view mode (when browsing)</span></span>  | <span data-ttu-id="3868f-297">PropList. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="3868f-297">System.PropList.ContentViewModeForBrowse</span></span>                 |
| <span data-ttu-id="3868f-298">磚視圖模式</span><span class="sxs-lookup"><span data-stu-id="3868f-298">Tile view mode</span></span>                     | <span data-ttu-id="3868f-299">PropList. TileInfo</span><span class="sxs-lookup"><span data-stu-id="3868f-299">System.PropList.TileInfo</span></span>                                 |
| <span data-ttu-id="3868f-300">[詳細資料] 窗格</span><span class="sxs-lookup"><span data-stu-id="3868f-300">Details pane</span></span>                       | <span data-ttu-id="3868f-301">PropList. PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="3868f-301">System.PropList.PreviewDetails</span></span>                           |
| <span data-ttu-id="3868f-302">提示 (專案的停留工具提示) </span><span class="sxs-lookup"><span data-stu-id="3868f-302">Infotip (item's hover tooltip)</span></span>     | <span data-ttu-id="3868f-303">PropList</span><span class="sxs-lookup"><span data-stu-id="3868f-303">System.PropList.Infotip</span></span>                                  |



 

 

<span data-ttu-id="3868f-304">**若要為個別專案指定唯一的 proplist：**</span><span class="sxs-lookup"><span data-stu-id="3868f-304">**To specify a unique proplist for an individual item:**</span></span>

1.  <span data-ttu-id="3868f-305">在您的 RSS 輸出中，新增自訂元素，代表您要自訂的 proplist。</span><span class="sxs-lookup"><span data-stu-id="3868f-305">In your RSS output, add a custom element representing the proplist you want to customize.</span></span> <span data-ttu-id="3868f-306">例如，下列範例會設定 [詳細資料] 窗格的清單：</span><span class="sxs-lookup"><span data-stu-id="3868f-306">For example, the following example sets the list for the details pane:</span></span>
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  <span data-ttu-id="3868f-307">若要將屬性套用至搜尋結果中的每個專案，而不修改 RSS 輸出，請在 .osdx 檔案中的 **PropertyDefaultValues** 元素內指定 proplist，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="3868f-307">To apply a property to every item in the search results without modifying the RSS output, specify a proplist within an **ms-ose:PropertyDefaultValues** element in the .osdx file, as shown in the following example:</span></span>

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a><span data-ttu-id="3868f-308">屬性的內容視圖模式版面配置</span><span class="sxs-lookup"><span data-stu-id="3868f-308">Content View Mode Layout of Properties</span></span>

<span data-ttu-id="3868f-309">**PropList. ContentViewModeForSearch** 和 **PropList. ContentViewModeForBrowse** proplists 中指定的屬性清單會決定內容視圖模式中顯示的內容。</span><span class="sxs-lookup"><span data-stu-id="3868f-309">The list of properties specified in the **System.PropList.ContentViewModeForSearch** and **System.PropList.ContentViewModeForBrowse** proplists determines what is shown in Content view mode.</span></span> <span data-ttu-id="3868f-310">如需屬性清單的詳細資訊，請參閱 [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring)。</span><span class="sxs-lookup"><span data-stu-id="3868f-310">For more information about property lists, see [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).</span></span>

<span data-ttu-id="3868f-311">這些屬性會根據下列版面配置模式中顯示的數位來配置：</span><span class="sxs-lookup"><span data-stu-id="3868f-311">The properties are laid out according to the numbers shown in the following layout pattern:</span></span>

![顯示內容視圖中預設版面配置模式的螢幕擷取畫面](images/propertiesnumberslayoutpattern.png)

<span data-ttu-id="3868f-313">如果我們使用下列屬性清單，</span><span class="sxs-lookup"><span data-stu-id="3868f-313">If we use the following list of properties,</span></span>


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



<span data-ttu-id="3868f-314">接著，我們會看到下列畫面：</span><span class="sxs-lookup"><span data-stu-id="3868f-314">Then we see the following display:</span></span>

![顯示範例屬性版面配置的螢幕擷取畫面。](images/samplepropertylayout.png)

> [!Note]  
> <span data-ttu-id="3868f-316">為了獲得最佳可讀性，應標記最右側資料行中顯示的屬性。</span><span class="sxs-lookup"><span data-stu-id="3868f-316">For the best readability, the properties shown in the right-most column should be labeled.</span></span>

 

### <a name="property-list-flags"></a><span data-ttu-id="3868f-317">屬性清單旗標</span><span class="sxs-lookup"><span data-stu-id="3868f-317">Property List Flags</span></span>

<span data-ttu-id="3868f-318">只有在 proplists 檔中定義的其中一個旗標適用于內容查看模式配置中的專案顯示： ` "~"` 。</span><span class="sxs-lookup"><span data-stu-id="3868f-318">Only one of the flags defined in the proplists documentation applies to the display of items in Content View mode layouts:` "~"`.</span></span> <span data-ttu-id="3868f-319">在先前的範例中，Windows 檔案總管 view 會標記一些屬性，例如 `Tags: animals; zoo; lion` 。</span><span class="sxs-lookup"><span data-stu-id="3868f-319">In the previous examples, the Windows Explorer view labels some of the properties, such as `Tags: animals; zoo; lion`.</span></span> <span data-ttu-id="3868f-320">當您在清單中指定屬性時，這是預設行為。</span><span class="sxs-lookup"><span data-stu-id="3868f-320">That is the default behavior when you specify a property in the list.</span></span> <span data-ttu-id="3868f-321">例如，proplist `"System.Author"` 會顯示為 `"Authors: value"` 。</span><span class="sxs-lookup"><span data-stu-id="3868f-321">For example, the proplist has `"System.Author"` which is displayed as `"Authors: value"`.</span></span> <span data-ttu-id="3868f-322">當您想要隱藏屬性標籤時，請將放 `"~"` 在屬性名稱的前方。</span><span class="sxs-lookup"><span data-stu-id="3868f-322">When you want to hide the property label, place a `"~"` in front of the property name.</span></span> <span data-ttu-id="3868f-323">例如，如果 proplist 具有 `"~System.Size"` ，屬性只會顯示為一個值，而不會顯示標籤。</span><span class="sxs-lookup"><span data-stu-id="3868f-323">For example, if the proplist has `"~System.Size"`, the property is displayed as just a value, without the label.</span></span>

## <a name="previews"></a><span data-ttu-id="3868f-324">預覽</span><span class="sxs-lookup"><span data-stu-id="3868f-324">Previews</span></span>

<span data-ttu-id="3868f-325">當使用者在 Windows 檔案總管中選取結果專案，而且預覽窗格已開啟時，就會預覽專案的內容。</span><span class="sxs-lookup"><span data-stu-id="3868f-325">When the user selects a result item in Windows Explorer and the preview pane is open, the content of the item is previewed.</span></span>

<span data-ttu-id="3868f-326">預覽版中所要顯示的內容是由 URL 指定，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3868f-326">The content to show in the preview is specified by a URL, that is determined as follows:</span></span>

1.  <span data-ttu-id="3868f-327">如果已針對專案設定 **WebPreviewUrl** Windows Shell 屬性，請使用該 URL。</span><span class="sxs-lookup"><span data-stu-id="3868f-327">If the **System.WebPreviewUrl** Windows Shell property is set for the item, then use that URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="3868f-328">您必須使用 Windows Shell 命名空間在 RSS 中提供屬性，或在 .osdx 檔案中明確地對應。</span><span class="sxs-lookup"><span data-stu-id="3868f-328">The property needs to be provided in the RSS by using the Windows Shell namespace, or explicitly mapped in the .osdx file.</span></span>

     

2.  <span data-ttu-id="3868f-329">如果沒有，則改為使用連結 URL。</span><span class="sxs-lookup"><span data-stu-id="3868f-329">If not, then use the link URL instead.</span></span>

<span data-ttu-id="3868f-330">下列流程圖顯示此邏輯。</span><span class="sxs-lookup"><span data-stu-id="3868f-330">The following flowchart shows this logic.</span></span>

![流程圖顯示 windows explorer 如何選取要用於預覽的 url](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

<span data-ttu-id="3868f-332">預覽可能會使用不同于專案本身的 URL。</span><span class="sxs-lookup"><span data-stu-id="3868f-332">It is possible to use a different URL for the preview than for the item itself.</span></span> <span data-ttu-id="3868f-333">這表示，如果您為連結 URL 和主機殼提供不同的 Url，或 `media:content URL` Windows 檔案總管使用連結 url 來預覽專案，但是會使用其他 URL 進行檔案類型偵測、開啟、下載等等。</span><span class="sxs-lookup"><span data-stu-id="3868f-333">This means that if you provide different URLs for the link URL and the enclosure or `media:content URL`, Windows Explorer uses the link URL for previews of the item but uses the other URL for file type detection, opening, downloading, and so forth.</span></span>

<span data-ttu-id="3868f-334">Windows 檔案總管如何判斷要使用的 URL：</span><span class="sxs-lookup"><span data-stu-id="3868f-334">How Windows Explorer determines what URL to use:</span></span>

1.  <span data-ttu-id="3868f-335">如果您提供 ItemFolderPathDisplay 的對應，則 Windows 檔案總管會使用該 URL [。](../properties/props-system-itemfolderpathdisplay.md)</span><span class="sxs-lookup"><span data-stu-id="3868f-335">If you provide a mapping to [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), then Windows Explorer uses that URL</span></span>
2.  <span data-ttu-id="3868f-336">如果您未提供對應，則 Windows 檔案總管會識別連結和主機殼 Url 是否不同。</span><span class="sxs-lookup"><span data-stu-id="3868f-336">If you do not provide a mapping, then Windows Explorer identifies whether the link and enclosure URLs are different.</span></span> <span data-ttu-id="3868f-337">如果是的話，Windows 檔案總管使用連結 URL。</span><span class="sxs-lookup"><span data-stu-id="3868f-337">If so, then Windows Explorer uses the link URL.</span></span>
3.  <span data-ttu-id="3868f-338">如果 Url 相同或只有連結 URL，則 Windows 檔案總管會從完整的 URL 中移除檔案名，以剖析連結以尋找父容器。</span><span class="sxs-lookup"><span data-stu-id="3868f-338">If the URLs are the same or if there is only a link URL, then Windows Explorer parses the link to find the parent container by removing the file name from the full URL.</span></span>
    > [!Note]  
    > <span data-ttu-id="3868f-339">如果您認為 URL 剖析會導致服務的無作用連結，您應該提供屬性的明確對應。</span><span class="sxs-lookup"><span data-stu-id="3868f-339">If you recognize that the URL parsing would result in dead links for your service, you should provide an explicit mapping for the property.</span></span>

     

## <a name="open-file-location-menu-item"></a><span data-ttu-id="3868f-340">開啟檔案位置功能表項目</span><span class="sxs-lookup"><span data-stu-id="3868f-340">Open File Location Menu Item</span></span>

<span data-ttu-id="3868f-341">當您以滑鼠右鍵按一下專案時，就會出現 [ **開啟檔案位置** ] 功能表命令。</span><span class="sxs-lookup"><span data-stu-id="3868f-341">When a right-clicks an item, the **Open file location** menu command appears.</span></span> <span data-ttu-id="3868f-342">此命令會將使用者帶到容器或該專案的位置。</span><span class="sxs-lookup"><span data-stu-id="3868f-342">This command takes the user to the container for or location of that item.</span></span> <span data-ttu-id="3868f-343">例如，在 SharePoint 搜尋中，針對文件庫中的檔案選取此選項，就會在網頁瀏覽器中開啟文件庫根。</span><span class="sxs-lookup"><span data-stu-id="3868f-343">For example, in a SharePoint search, selecting this option for a file in a document library would open the document library root in the web browser.</span></span>

<span data-ttu-id="3868f-344">當使用者按一下 [ **開啟檔案位置**] 時，Windows 檔案總管會使用下列流程圖所示的邏輯，嘗試尋找父容器：</span><span class="sxs-lookup"><span data-stu-id="3868f-344">When a user clicks **Open file location**, Windows Explorer attempts to find a parent container, by using the logic shown in the following flowchart:</span></span>

![顯示 windows explorer 如何識別父容器的流程圖](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a><span data-ttu-id="3868f-346">其他資源</span><span class="sxs-lookup"><span data-stu-id="3868f-346">Additional Resources</span></span>

<span data-ttu-id="3868f-347">如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](/previous-versions//dd742958(v=vs.85))的「其他資源」。</span><span class="sxs-lookup"><span data-stu-id="3868f-347">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3868f-348">相關主題</span><span class="sxs-lookup"><span data-stu-id="3868f-348">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3868f-349">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="3868f-349">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="3868f-350">在 Windows 中使用同盟搜尋開始使用</span><span class="sxs-lookup"><span data-stu-id="3868f-350">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="3868f-351">在 Windows 同盟搜尋中連接您的 web 服務</span><span class="sxs-lookup"><span data-stu-id="3868f-351">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="3868f-352">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="3868f-352">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="3868f-353">遵循 Windows 同盟搜尋的最佳作法</span><span class="sxs-lookup"><span data-stu-id="3868f-353">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="3868f-354">在 Windows 同盟搜尋中部署搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="3868f-354">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
