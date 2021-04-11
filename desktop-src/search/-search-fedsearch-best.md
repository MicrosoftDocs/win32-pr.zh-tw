---
description: 本主題列出您可以用來建立可使用 Windows 同盟搜尋來搜尋之 web 資料存放區的最佳作法，並將您的遠端資料源與 Windows 檔案總管整合，而不需要撰寫或部署任何 Windows 用戶端程式代碼。
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: 遵循 Windows 同盟搜尋的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112460"
---
# <a name="following-best-practices-in-windows-federated-search"></a><span data-ttu-id="c804c-103">遵循 Windows 同盟搜尋的最佳作法</span><span class="sxs-lookup"><span data-stu-id="c804c-103">Following Best Practices in Windows Federated Search</span></span>

<span data-ttu-id="c804c-104">本主題列出您可以用來建立可使用 Windows 同盟搜尋來搜尋之 web 資料存放區的最佳作法，並將您的遠端資料源與 Windows 檔案總管整合，而不需要撰寫或部署任何 Windows 用戶端程式代碼。</span><span class="sxs-lookup"><span data-stu-id="c804c-104">This topic lists the best practices through which you can build a web-based data store that can be searched using Windows federated search, and integrates your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="c804c-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="c804c-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c804c-106">Windows 同盟搜尋的最佳作法</span><span class="sxs-lookup"><span data-stu-id="c804c-106">Best Practices for Windows Federated Search</span></span>](#best-practices-for-windows-federated-search)
-   [<span data-ttu-id="c804c-107">建立 RSS 輸出的最佳作法</span><span class="sxs-lookup"><span data-stu-id="c804c-107">Best Practices for Creating RSS Output</span></span>](#best-practices-for-creating-rss-output)
-   [<span data-ttu-id="c804c-108">其他資源</span><span class="sxs-lookup"><span data-stu-id="c804c-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="c804c-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="c804c-109">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a><span data-ttu-id="c804c-110">Windows 同盟搜尋的最佳作法</span><span class="sxs-lookup"><span data-stu-id="c804c-110">Best Practices for Windows Federated Search</span></span>

<span data-ttu-id="c804c-111">在 Windows 7 中使用 [OpenSearch](https://github.com/dewitt/opensearch) 的最佳作法如下：</span><span class="sxs-lookup"><span data-stu-id="c804c-111">Best practices for working with [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 are as follows:</span></span>

-   <span data-ttu-id="c804c-112">支援 *{startIndex}* 和 *{count}* 個參數，而且除非您傳回最後一個結果，否則務必一律傳回所要求的專案數。</span><span class="sxs-lookup"><span data-stu-id="c804c-112">Support the *{startIndex}* and *{count}* parameters, and be sure to always return the number of items requested unless you are returning the last of the results.</span></span>
-   <span data-ttu-id="c804c-113">如果您知道副檔名，請將其對應至 [FileExtension](../properties/props-system-fileextension.md) Windows Shell 屬性。</span><span class="sxs-lookup"><span data-stu-id="c804c-113">If you know the file name extension, map it to the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property.</span></span> <span data-ttu-id="c804c-114">使用副檔名是識別 MIME 類型之檔案類型的較佳方式。</span><span class="sxs-lookup"><span data-stu-id="c804c-114">Using file name extensions is a better way to identify a file type than MIME type.</span></span>
-   <span data-ttu-id="c804c-115">確定您在 RSS 中指定的 MIME 類型或副檔名，符合在要求專案內容時裝載專案之 web 伺服器的 HTTP 標頭中所傳回的檔案名和 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="c804c-115">Ensure that the MIME type or file name extension that you specify in the RSS matches the file name and MIME type returned in the HTTP header by the web server that hosts the item when the item content is requested.</span></span>
-   <span data-ttu-id="c804c-116">如果您要傳回檔案專案，請盡可能傳回檔案大小。</span><span class="sxs-lookup"><span data-stu-id="c804c-116">If you are returning file items, return a file size whenever possible.</span></span> <span data-ttu-id="c804c-117">這樣可確保 [下載進度] 對話方塊正確無誤。</span><span class="sxs-lookup"><span data-stu-id="c804c-117">This ensures that the download progress dialog box is accurate.</span></span>
-   <span data-ttu-id="c804c-118">確認對結果集結尾以外的專案所提出的要求不會傳回任何結果。</span><span class="sxs-lookup"><span data-stu-id="c804c-118">Verify that requests for items beyond the end of the results set return no results.</span></span>
    > [!Note]  
    > <span data-ttu-id="c804c-119">不要重複結果。</span><span class="sxs-lookup"><span data-stu-id="c804c-119">Do not repeat results.</span></span>

     

-   <span data-ttu-id="c804c-120">請勿將 HTML 標籤放在不屬於的位置。</span><span class="sxs-lookup"><span data-stu-id="c804c-120">Do not put HTML tags where they don't belong.</span></span> <span data-ttu-id="c804c-121">根據 RSS 規格，它們在 [描述] 欄位中是有效的，但不在 [標題] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="c804c-121">Per the RSS specification, they are valid in the description field, but not in the title field.</span></span>
-   <span data-ttu-id="c804c-122">請勿建立網頁專案的主機殼。</span><span class="sxs-lookup"><span data-stu-id="c804c-122">Do not create enclosures for webpage items.</span></span> <span data-ttu-id="c804c-123">例如，如果您建立主機殼並對應 .aspx 的副檔名，則會 Windows 檔案總管將檔案下載至網際網路快取，並從該處執行該檔案。</span><span class="sxs-lookup"><span data-stu-id="c804c-123">For example, if you create an enclosure and map a file name extension of .aspx, the file is downloaded by Windows Explorer to the Internet cache and executed from there.</span></span> <span data-ttu-id="c804c-124">Web 瀏覽器不會處理 .aspx 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="c804c-124">Web browsers do not handle the .aspx file type.</span></span> <span data-ttu-id="c804c-125">使用者會收到 **開啟檔案** 對話方塊，或者檔案可能會由 Microsoft Visual Studio 之類的應用程式開啟。</span><span class="sxs-lookup"><span data-stu-id="c804c-125">The user would get an **Open with** dialog box, or the file might be opened by an application like Microsoft Visual Studio.</span></span> <span data-ttu-id="c804c-126">只要針對網頁傳回 link 元素，即可避免此情況。</span><span class="sxs-lookup"><span data-stu-id="c804c-126">Avoid this by returning a link element only for webpages.</span></span>
-   <span data-ttu-id="c804c-127">使用 URL 範本搭配，在 .osdx 檔案中提供 web 向前復原 URL `format="text\html"` 。</span><span class="sxs-lookup"><span data-stu-id="c804c-127">Provide a web roll-over URL in the .osdx file using a URL template with `format="text\html"`.</span></span>
-   <span data-ttu-id="c804c-128">將自訂元素 URL 值對應至 [ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell 屬性，以提供父資料夾、容器或網頁的 url。</span><span class="sxs-lookup"><span data-stu-id="c804c-128">Provide a URL to the parent folder, container, or webpage by mapping a custom element URL value to the [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell property.</span></span>

## <a name="best-practices-for-creating-rss-output"></a><span data-ttu-id="c804c-129">建立 RSS 輸出的最佳作法</span><span class="sxs-lookup"><span data-stu-id="c804c-129">Best Practices for Creating RSS Output</span></span>

<span data-ttu-id="c804c-130">建立 RSS 輸出的最佳作法如下：</span><span class="sxs-lookup"><span data-stu-id="c804c-130">Best practices for creating RSS output are as follows:</span></span>

-   <span data-ttu-id="c804c-131">每個專案都必須傳回 `link` `enclosure` (或相等的 URL 或值，例如 `media:content`) </span><span class="sxs-lookup"><span data-stu-id="c804c-131">Each item MUST return a URL `link` or `enclosure` value (or equivalent, such as `media:content`)</span></span>
-   <span data-ttu-id="c804c-132">請勿在 **title** 屬性中包含任何 HTML 格式標記，否則這些標記會出現在標題中，並顯示在 Windows 檔案總管中。</span><span class="sxs-lookup"><span data-stu-id="c804c-132">Do not include any HTML formatting tags in the **title** attribute, or those tags will appear in the title and be displayed in Windows Explorer.</span></span>
-   <span data-ttu-id="c804c-133">針對 **description** 元素：</span><span class="sxs-lookup"><span data-stu-id="c804c-133">For the **description** element:</span></span>
    -   <span data-ttu-id="c804c-134">顯示足夠的資訊，讓使用者知道此結果可能相關的原因。</span><span class="sxs-lookup"><span data-stu-id="c804c-134">Show enough information so that the user knows why this result might be relevant.</span></span>
    -   <span data-ttu-id="c804c-135">請勿包含 HTML 格式。</span><span class="sxs-lookup"><span data-stu-id="c804c-135">Do not include HTML formatting.</span></span> <span data-ttu-id="c804c-136">[OpenSearch](https://github.com/dewitt/opensearch)提供者會移除格式，而這可能會導致您的描述產生小於預期的結果。</span><span class="sxs-lookup"><span data-stu-id="c804c-136">The [OpenSearch](https://github.com/dewitt/opensearch) provider removes the formatting, which might result in less than desirable results for your description.</span></span>
    -   <span data-ttu-id="c804c-137">請勿包含已經在其他元素中提供的中繼資料，例如，機殼檔案名、大小、修改日期等，因為 Windows 檔案總管已經顯示中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c804c-137">Do not include metadata that is already provided in other elements, such as enclosure file name, size, modified date, and so forth, because Windows Explorer already displays the metadata.</span></span> <span data-ttu-id="c804c-138">將它顯示在 **description** 元素中會是多餘的。</span><span class="sxs-lookup"><span data-stu-id="c804c-138">Displaying it in the **description** element would be redundant.</span></span>
-   <span data-ttu-id="c804c-139">針對主機殼或內容 Url：</span><span class="sxs-lookup"><span data-stu-id="c804c-139">For enclosure or content URLs:</span></span>
    -   <span data-ttu-id="c804c-140">將類型屬性指定為有效的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="c804c-140">Specify the type attribute as a valid MIME type.</span></span>
    -   <span data-ttu-id="c804c-141">指定檔案大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c804c-141">Specify the file size in bytes.</span></span>
-   <span data-ttu-id="c804c-142">如果您要使用 .NET 在 .NET 中執行 RSS 輸出 `DateTime` ，請在 Microsoft Internet Explorer 中測試您的摘要，以查看它是否有效，再將其部署至 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="c804c-142">If you are implementing RSS output in .NET using `DateTime`, test your feed in Microsoft Internet Explorer to see if it is valid before deploying it to Windows Explorer.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c804c-143">其他資源</span><span class="sxs-lookup"><span data-stu-id="c804c-143">Additional Resources</span></span>

<span data-ttu-id="c804c-144">如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](/previous-versions//dd742958(v=vs.85))的「其他資源」。</span><span class="sxs-lookup"><span data-stu-id="c804c-144">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c804c-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="c804c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c804c-146">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="c804c-146">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="c804c-147">在 Windows 中使用同盟搜尋開始使用</span><span class="sxs-lookup"><span data-stu-id="c804c-147">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="c804c-148">在 Windows 同盟搜尋中連接您的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="c804c-148">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="c804c-149">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="c804c-149">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="c804c-150">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="c804c-150">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="c804c-151">在 Windows 同盟搜尋中部署搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="c804c-151">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> <dt>

[<span data-ttu-id="c804c-152">擴充索引</span><span class="sxs-lookup"><span data-stu-id="c804c-152">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
