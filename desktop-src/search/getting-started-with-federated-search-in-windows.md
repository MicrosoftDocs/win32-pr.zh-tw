---
description: 使用 OpenSearch 技術對遠端資料存放區進行搜尋同盟的 Windows 7 支援，可讓使用者從 Windows 檔案總管記憶體取遠端資料並與其互動。
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: 在 Windows 中使用同盟搜尋開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c1f887ff2bdba279cdd25e4910162dd9263d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511085"
---
# <a name="getting-started-with-federated-search-in-windows"></a><span data-ttu-id="b71b2-103">在 Windows 中使用同盟搜尋開始使用</span><span class="sxs-lookup"><span data-stu-id="b71b2-103">Getting Started with Federated Search in Windows</span></span>

<span data-ttu-id="b71b2-104">使用 OpenSearch 技術對遠端資料存放區進行搜尋同盟的 Windows 7 支援，可讓使用者從 Windows 檔案總管記憶體取遠端資料並與其互動。</span><span class="sxs-lookup"><span data-stu-id="b71b2-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="b71b2-105">您可以建立可使用 Windows 同盟搜尋來搜尋的 web 資料存放區，並透過 Windows 檔案總管啟用豐富的遠端資料源整合，而不需要撰寫或部署任何 Windows 用戶端程式代碼。</span><span class="sxs-lookup"><span data-stu-id="b71b2-105">You can build a web-based data store that can be searched using Windows federated search and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="b71b2-106">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="b71b2-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b71b2-107">什麼是同盟搜尋？</span><span class="sxs-lookup"><span data-stu-id="b71b2-107">What is Federated Search?</span></span>](#what-is-federated-search)
-   [<span data-ttu-id="b71b2-108">建立同盟搜尋的步驟</span><span class="sxs-lookup"><span data-stu-id="b71b2-108">Steps for Building Federated Search</span></span>](#steps-for-building-federated-search)
-   [<span data-ttu-id="b71b2-109">同盟搜尋的運作方式</span><span class="sxs-lookup"><span data-stu-id="b71b2-109">How Federated Search Works</span></span>](#how-federated-search-works)
-   [<span data-ttu-id="b71b2-110">在 RSS 或 Atom 中傳送查詢並傳回搜尋結果</span><span class="sxs-lookup"><span data-stu-id="b71b2-110">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [<span data-ttu-id="b71b2-111">同盟搜尋範例</span><span class="sxs-lookup"><span data-stu-id="b71b2-111">Federated Search Examples</span></span>](#federated-search-examples)
-   [<span data-ttu-id="b71b2-112">其他資源</span><span class="sxs-lookup"><span data-stu-id="b71b2-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="b71b2-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b71b2-113">Related topics</span></span>](#related-topics)

## <a name="what-is-federated-search"></a><span data-ttu-id="b71b2-114">什麼是同盟搜尋？</span><span class="sxs-lookup"><span data-stu-id="b71b2-114">What is Federated Search?</span></span>

<span data-ttu-id="b71b2-115">Windows 7 支援透過 [OpenSearch](https://github.com/dewitt/opensearch) 通訊協定，將外部來源連接到 windows 用戶端。</span><span class="sxs-lookup"><span data-stu-id="b71b2-115">Windows 7 supports the connection of external sources to the Windows client through the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="b71b2-116">這可讓使用者搜尋遠端資料存放區，並從 Windows 檔案總管內查看結果。</span><span class="sxs-lookup"><span data-stu-id="b71b2-116">This enables users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="b71b2-117">[OpenSearch](https://github.com/dewitt/opensearch) v1.1 標準定義了簡單的檔案格式，可用來描述用戶端應該如何查詢資料存放區的 web 服務，以及服務應該如何傳回結果以供用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="b71b2-117">The [OpenSearch](https://github.com/dewitt/opensearch) v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span> <span data-ttu-id="b71b2-118">Windows 同盟搜尋會連接到接收 [OpenSearch](https://github.com/dewitt/opensearch) 查詢的 web 服務，並以 RSS 或 Atom XML 格式傳回結果。</span><span class="sxs-lookup"><span data-stu-id="b71b2-118">Windows federated search connects to web services that receive [OpenSearch](https://github.com/dewitt/opensearch) queries, and returns results in either the RSS or Atom XML format.</span></span>

<span data-ttu-id="b71b2-119">下列螢幕擷取畫面說明從遠端搜尋 SharePoint 網站之後所取得的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="b71b2-119">The following screen shot illustrates the search results obtained after remotely searching a SharePoint site.</span></span>

![顯示 windows explorer 中所顯示的 sharepoint 網站搜尋結果的螢幕擷取畫面](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a><span data-ttu-id="b71b2-121">建立同盟搜尋的步驟</span><span class="sxs-lookup"><span data-stu-id="b71b2-121">Steps for Building Federated Search</span></span>

<span data-ttu-id="b71b2-122">若要建立同盟搜尋，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b71b2-122">To build federated search, perform the following steps:</span></span>

1.  <span data-ttu-id="b71b2-123">提供可傳回 RSS 或 Atom 格式之結果的 [OpenSearch](https://github.com/dewitt/opensearch)相容 web 服務，讓您可以從 Windows 檔案總管搜尋資料存放區。</span><span class="sxs-lookup"><span data-stu-id="b71b2-123">Enable your data store to be searched from Windows Explorer by providing an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service that can return results in RSS or Atom format.</span></span>
2.  <span data-ttu-id="b71b2-124">建立 .osdx) 檔案的 OpenSearch ( 描述，以描述如何連接至 web 服務，以及如何對應 RSS 或 Atom XML 中的任何自訂元素。</span><span class="sxs-lookup"><span data-stu-id="b71b2-124">Create an OpenSearch Description (.osdx) file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML.</span></span>
3.  <span data-ttu-id="b71b2-125">使用 .osdx 檔案將搜尋連接器部署至 Windows 用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="b71b2-125">Deploy the search connectors to Windows client computers with an .osdx file.</span></span>

<span data-ttu-id="b71b2-126">下圖說明建立同盟搜尋的步驟。</span><span class="sxs-lookup"><span data-stu-id="b71b2-126">The following diagram illustrates the steps for building federated search.</span></span>

![建立同盟搜尋的流程圖表](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a><span data-ttu-id="b71b2-128">同盟搜尋的運作方式</span><span class="sxs-lookup"><span data-stu-id="b71b2-128">How Federated Search Works</span></span>

<span data-ttu-id="b71b2-129">Windows 檔案總管和您的 [OpenSearch](https://github.com/dewitt/opensearch) web 服務之間的通訊是透過 Windows 資料層執行。</span><span class="sxs-lookup"><span data-stu-id="b71b2-129">Communication between Windows Explorer and your [OpenSearch](https://github.com/dewitt/opensearch) web service is performed through the Windows Data Layer.</span></span> <span data-ttu-id="b71b2-130">Windows 資料層可透過 Windows 存放區提供者與不同類型的資料存放區進行通訊。</span><span class="sxs-lookup"><span data-stu-id="b71b2-130">The Windows Data Layer can communicate with different types of data stores through Windows Store Providers.</span></span> <span data-ttu-id="b71b2-131">每個提供者都專門與支援特定通訊協定並具有特定功能的資料存放區進行通訊。</span><span class="sxs-lookup"><span data-stu-id="b71b2-131">Each provider specializes in communicating with data stores that support a particular protocol and have specific capabilities.</span></span> <span data-ttu-id="b71b2-132">例如，下圖說明瞭 [OpenSearch](https://github.com/dewitt/opensearch) 提供者如何與提供支援 [OpenSearch](https://github.com/dewitt/opensearch) 標準之 web 服務的資料存放區進行通訊。</span><span class="sxs-lookup"><span data-stu-id="b71b2-132">For example, the following illustration sows how the [OpenSearch](https://github.com/dewitt/opensearch) provider communicates with data stores that provide a web service that supports the [OpenSearch](https://github.com/dewitt/opensearch) standard.</span></span>

![顯示從用戶端上的 windows explorer 透過遠端伺服器上的 opensearch 資料存放區進行通訊的圖表](images/windowssearchfederationfunctionality.png)

<span data-ttu-id="b71b2-134">若要讓您的資料存放區支援 Windows 7 中的同盟搜尋，您必須執行一些工作。</span><span class="sxs-lookup"><span data-stu-id="b71b2-134">To enable your data store to support federated search in Windows 7, you must perform a number of tasks.</span></span> <span data-ttu-id="b71b2-135">下表列出啟用資料存放區的工作、完成每項工作所需的作業，以及可在何處找到檔。</span><span class="sxs-lookup"><span data-stu-id="b71b2-135">The following table lists tasks for enabling your data store, what is required to accomplish each task, and where to find documentation.</span></span>



| <span data-ttu-id="b71b2-136">Task</span><span class="sxs-lookup"><span data-stu-id="b71b2-136">Task</span></span>                                                                                                     | <span data-ttu-id="b71b2-137">需求</span><span class="sxs-lookup"><span data-stu-id="b71b2-137">Requirement</span></span>                                                                                                                                                                                            | <span data-ttu-id="b71b2-138">文件</span><span class="sxs-lookup"><span data-stu-id="b71b2-138">Documentation</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b71b2-139">讓 Windows 檔案總管搜尋您的資料存放區。</span><span class="sxs-lookup"><span data-stu-id="b71b2-139">Enable your data store to be searched by Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="b71b2-140">建立與 OpenSearch 相容的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="b71b2-140">Build an OpenSearch-compatible web service.</span></span><br/> <span data-ttu-id="b71b2-141"> ( .osdx) 檔案中建立 [OpenSearch 描述]。</span><span class="sxs-lookup"><span data-stu-id="b71b2-141">Create an OpenSearch Description (.osdx) file.</span></span><br/>                                                                                       | [<span data-ttu-id="b71b2-142">在 Windows 同盟搜尋中連接您的 web 服務</span><span class="sxs-lookup"><span data-stu-id="b71b2-142">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/> [<span data-ttu-id="b71b2-143">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="b71b2-143">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/> |
| <span data-ttu-id="b71b2-144">主動將 web 服務部署至企業內的使用者。</span><span class="sxs-lookup"><span data-stu-id="b71b2-144">Actively deploy your web service to users within an enterprise.</span></span><br/>                               | <span data-ttu-id="b71b2-145">將 .osdx 檔案提供給您的使用者、將它複製到本機，然後透過快捷方式讓使用者存取。</span><span class="sxs-lookup"><span data-stu-id="b71b2-145">Supply an .osdx file to your users, copy it locally, and make it accessible to the user via a shortcut.</span></span><br/>                                                                                     | [<span data-ttu-id="b71b2-146">在 Windows 同盟搜尋中部署搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="b71b2-146">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)<br/>                                                                                                              |
| <span data-ttu-id="b71b2-147">在 Windows 檔案總管中列舉搜尋結果，以回應查詢。</span><span class="sxs-lookup"><span data-stu-id="b71b2-147">Enumerate search results in Windows Explorer in response to a query.</span></span><br/>                          | <span data-ttu-id="b71b2-148">執行可接受查詢字串，並以 RSS 或 Atom 格式傳回結果的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="b71b2-148">Implement a web service that accepts a query string and returns results in RSS or Atom format.</span></span><br/>                                                                                              | [<span data-ttu-id="b71b2-149">在 Windows 同盟搜尋中連接您的 web 服務</span><span class="sxs-lookup"><span data-stu-id="b71b2-149">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/>                                                                                                            |
| <span data-ttu-id="b71b2-150">讓使用者將您的資料存放區新增至其 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="b71b2-150">Enable users to add your data store to their Windows Explorer.</span></span><br/>                                | <span data-ttu-id="b71b2-151">建立 .osdx 檔案，並將它提供給您的使用者。</span><span class="sxs-lookup"><span data-stu-id="b71b2-151">Create an .osdx file and supply it to your users.</span></span><br/>                                                                                                                                           | [<span data-ttu-id="b71b2-152">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="b71b2-152">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="b71b2-153">在 Windows 檔案總管中，將您的專案顯示為類似檔的專案。</span><span class="sxs-lookup"><span data-stu-id="b71b2-153">Display your items as file-like items in Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="b71b2-154">使用 **主機殼** 或媒體來傳回檔案或內容資料流程的 URL **： content** 元素</span><span class="sxs-lookup"><span data-stu-id="b71b2-154">Return a URL to the file or content stream by using **enclosure** or **media:content** elements</span></span><br/> <span data-ttu-id="b71b2-155">提供用戶端電腦可識別的副檔名或 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="b71b2-155">Supply a file name extension or a MIME type that the client computer recognizes.</span></span><br/> | [<span data-ttu-id="b71b2-156">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="b71b2-156">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="b71b2-157">除了 RSS 或 Atom 標準所定義的屬性外，也會顯示 Windows 檔案總管中的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="b71b2-157">Display custom properties in Windows Explorer, beyond those defined in RSS or Atom standards.</span></span><br/> | <span data-ttu-id="b71b2-158">在 RSS/Atom 輸出中使用另一個 XML 命名空間，以提供額外的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b71b2-158">Provide additional metadata by using another XML namespace in your RSS/Atom output.</span></span><br/> <span data-ttu-id="b71b2-159">將屬性對應新增至 .osdx 檔案。</span><span class="sxs-lookup"><span data-stu-id="b71b2-159">Add a property map to your .osdx file.</span></span><br/>                                                       | [<span data-ttu-id="b71b2-160">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="b71b2-160">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="b71b2-161">自訂 Windows 檔案總管中的專案所顯示的屬性。</span><span class="sxs-lookup"><span data-stu-id="b71b2-161">Customize the properties that are displayed for your items in Windows Explorer.</span></span><br/>               | <span data-ttu-id="b71b2-162">將 proplist 對應新增至 .osdx 檔案。</span><span class="sxs-lookup"><span data-stu-id="b71b2-162">Add proplist mappings to your .osdx file.</span></span><br/>                                                                                                                                                   | [<span data-ttu-id="b71b2-163">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="b71b2-163">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="b71b2-164">在預覽窗格中顯示專案的自訂網頁流覽。</span><span class="sxs-lookup"><span data-stu-id="b71b2-164">Display a custom webpage view of your items in the preview pane.</span></span><br/>                              | <span data-ttu-id="b71b2-165">傳回相異的連結與主機殼值。</span><span class="sxs-lookup"><span data-stu-id="b71b2-165">Return distinct link and enclosure values.</span></span><br/> <span data-ttu-id="b71b2-166">將 URL 值對應至 **WebPreviewUrl** Windows Shell 屬性。</span><span class="sxs-lookup"><span data-stu-id="b71b2-166">Map a URL value to the **System.WebPreviewUrl** Windows Shell property.</span></span><br/>                                                               | [<span data-ttu-id="b71b2-167">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="b71b2-167">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="b71b2-168">在 Windows 檔案總管中顯示 [命令列] 按鈕，此按鈕會將查詢向前復原到您的網站。</span><span class="sxs-lookup"><span data-stu-id="b71b2-168">Display a command bar button in Windows Explorer that rolls the query over to your website.</span></span><br/>   | <span data-ttu-id="b71b2-169">`Url format="text/html"`在 .osdx 檔案中提供範本。</span><span class="sxs-lookup"><span data-stu-id="b71b2-169">Provide a `Url format="text/html"` template in the .osdx file.</span></span><br/>                                                                                                                              | [<span data-ttu-id="b71b2-170">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="b71b2-170">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="b71b2-171">在 RSS 或 Atom 中傳送查詢並傳回搜尋結果</span><span class="sxs-lookup"><span data-stu-id="b71b2-171">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="b71b2-172">當使用者在 Windows 檔案總管右上角的 [搜尋] 方塊中輸入字詞時，查詢會傳送至 [ [OpenSearch](https://github.com/dewitt/opensearch) 提供者]，然後將查詢傳送到遠端資料存放區。</span><span class="sxs-lookup"><span data-stu-id="b71b2-172">When the user types a term into the search box in the upper-right corner of Windows Explorer, the query is sent to the [OpenSearch](https://github.com/dewitt/opensearch) provider, which then sends the query to the remote data store.</span></span> <span data-ttu-id="b71b2-173">遠端 web 服務會回應查詢，方法是在 XML 檔（通常稱為摘要）中提供結果，其中有兩種支援的格式 (RSS 或 Atom) 。</span><span class="sxs-lookup"><span data-stu-id="b71b2-173">The remote web service responds to the query by providing results in an XML document, typically referred to as a feed, in one of two supported formats (RSS or Atom).</span></span> <span data-ttu-id="b71b2-174">摘要中的每個結果專案都包含 XML 子項目，以代表或描述專案中繼資料，例如標題、URL、描述、縮圖影像等等。</span><span class="sxs-lookup"><span data-stu-id="b71b2-174">Each result item in the feed includes XML child elements to represent or describe item metadata, such as the title, URL, description, thumbnail image, and so forth.</span></span> <span data-ttu-id="b71b2-175">[ [OpenSearch](https://github.com/dewitt/opensearch) 提供者] 負責將 XML 元素值對應至 windows 應用程式可以使用的 windows Shell 系統屬性。</span><span class="sxs-lookup"><span data-stu-id="b71b2-175">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span>

## <a name="federated-search-examples"></a><span data-ttu-id="b71b2-176">同盟搜尋範例</span><span class="sxs-lookup"><span data-stu-id="b71b2-176">Federated Search Examples</span></span>

<span data-ttu-id="b71b2-177">下列範例 ( 的 [OpenSearch]) 檔案 `ShortName` 是由和元素所組成 `Url` ，這是透過 [OpenSearch] 通訊協定將外部資料存放區連接到 Windows 用戶端的最低必要子項目。</span><span class="sxs-lookup"><span data-stu-id="b71b2-177">The following example OpenSearch Description (.osdx) file consists of `ShortName` and `Url` elements, which are the minimum required child elements to connect an external data store to the Windows client through the OpenSearch protocol.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



<span data-ttu-id="b71b2-178">下列範例說明如何以 RSS 格式來搜尋可供 web 使用的資料存放區，以及如何指定要傳回的一個搜尋專案：</span><span class="sxs-lookup"><span data-stu-id="b71b2-178">The following example illustrates how to make a web-enabled data store searchable in RSS format, and how to specify that one search item be returned:</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="b71b2-179">下列範例說明如何將屬性對應至預設的系統屬性，以便排序和分組顯示的專案：</span><span class="sxs-lookup"><span data-stu-id="b71b2-179">The following example illustrates how to map properties to default system properties so that displayed items are sorted and grouped:</span></span>


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



<span data-ttu-id="b71b2-180">下列範例說明如何將縮圖影像顯示新增至 Windows 檔案總管中的每個專案：</span><span class="sxs-lookup"><span data-stu-id="b71b2-180">The following example illustrates how to adds a thumbnail image display to each item in Windows Explorer:</span></span>


```
<media:thumbnail>    
```



## <a name="additional-resources"></a><span data-ttu-id="b71b2-181">其他資源</span><span class="sxs-lookup"><span data-stu-id="b71b2-181">Additional Resources</span></span>

<span data-ttu-id="b71b2-182">如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](-search-federated-search-overview.md)的「其他資源」。</span><span class="sxs-lookup"><span data-stu-id="b71b2-182">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b71b2-183">相關主題</span><span class="sxs-lookup"><span data-stu-id="b71b2-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b71b2-184">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="b71b2-184">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="b71b2-185">在 Windows 同盟搜尋中連接您的 web 服務</span><span class="sxs-lookup"><span data-stu-id="b71b2-185">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="b71b2-186">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="b71b2-186">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="b71b2-187">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="b71b2-187">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="b71b2-188">遵循 Windows 同盟搜尋的最佳作法</span><span class="sxs-lookup"><span data-stu-id="b71b2-188">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="b71b2-189">在 Windows 同盟搜尋中部署搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="b71b2-189">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 




