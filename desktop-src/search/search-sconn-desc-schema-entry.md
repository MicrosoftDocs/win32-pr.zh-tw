---
description: 介紹 Windows 檔案總管程式庫和同盟搜尋提供者所使用的搜尋連接器描述架構。
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: 搜尋連接器描述架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f502f67cdc933bf4d27a3475cd6adef70c00fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972603"
---
# <a name="search-connector-description-schema"></a><span data-ttu-id="5da78-103">搜尋連接器描述架構</span><span class="sxs-lookup"><span data-stu-id="5da78-103">Search Connector Description Schema</span></span>

<span data-ttu-id="5da78-104">介紹 Windows 檔案總管程式庫和同盟搜尋提供者所使用的搜尋連接器描述架構。</span><span class="sxs-lookup"><span data-stu-id="5da78-104">Introduces the Search Connector Description schema that is used by Windows Explorer libraries and federated search providers.</span></span> <span data-ttu-id="5da78-105">架構會指定搜尋連接器描述檔案的結構和需求 (\* searchConnector-ms) 和 Shell 程式庫描述)  (的 **searchConnectorDescriptionType** 元素。 \*</span><span class="sxs-lookup"><span data-stu-id="5da78-105">The schema specifies the structure and requirements for Search Connector Description files (\*.searchConnector-ms) and for **searchConnectorDescriptionType** elements of the Shell Library Description (\*.library-ms) files.</span></span>

<span data-ttu-id="5da78-106">本主題說明與同盟搜尋連接器相關的架構。</span><span class="sxs-lookup"><span data-stu-id="5da78-106">This topic describes the schema as it relates to federated search connectors.</span></span> <span data-ttu-id="5da78-107">如需程式庫和程式庫描述架構的詳細資訊，請參閱連結 [庫描述架構](../shell/library-schema-entry.md)。</span><span class="sxs-lookup"><span data-stu-id="5da78-107">For more information about libraries and the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>

<span data-ttu-id="5da78-108">本主題包含下列章節：</span><span class="sxs-lookup"><span data-stu-id="5da78-108">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="5da78-109">什麼是搜尋連接器？</span><span class="sxs-lookup"><span data-stu-id="5da78-109">What Are Search Connectors?</span></span>](#what-are-search-connectors)
-   [<span data-ttu-id="5da78-110">搜尋連接器描述檔案的運作方式為何？</span><span class="sxs-lookup"><span data-stu-id="5da78-110">How Do Search Connector Description Files Work?</span></span>](#search-connector-description-schema)
-   [<span data-ttu-id="5da78-111">什麼是搜尋連接器描述架構？</span><span class="sxs-lookup"><span data-stu-id="5da78-111">What Is the Search Connector Description Schema?</span></span>](#what-is-the-search-connector-description-schema)
-   [<span data-ttu-id="5da78-112">架構的主要部分有哪些？</span><span class="sxs-lookup"><span data-stu-id="5da78-112">What Are the Major Parts of the Schema?</span></span>](#what-are-the-major-parts-of-the-schema)
-   [<span data-ttu-id="5da78-113">搜尋連接器描述檔案的範例</span><span class="sxs-lookup"><span data-stu-id="5da78-113">Examples of Search Connector Description Files</span></span>](#examples-of-search-connector-description-files)
-   [<span data-ttu-id="5da78-114">其他資源</span><span class="sxs-lookup"><span data-stu-id="5da78-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="5da78-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="5da78-115">Related topics</span></span>](#related-topics)

## <a name="what-are-search-connectors"></a><span data-ttu-id="5da78-116">什麼是搜尋連接器？</span><span class="sxs-lookup"><span data-stu-id="5da78-116">What Are Search Connectors?</span></span>

<span data-ttu-id="5da78-117">搜尋連接器會將使用者連線到儲存在 web 服務或遠端儲存體位置中的資料。</span><span class="sxs-lookup"><span data-stu-id="5da78-117">Search connectors connect users with data stored in web services or remote storage locations.</span></span> <span data-ttu-id="5da78-118">在 Windows 7 中，使用者可以為位置（例如 web 服務）安裝搜尋連接器，讓他們直接從 Windows 檔案總管搜尋這些位置。</span><span class="sxs-lookup"><span data-stu-id="5da78-118">With Windows 7, users can install search connectors for locations, like web services, so that they search those locations directly from Windows Explorer.</span></span> <span data-ttu-id="5da78-119">搜尋連接器是搜尋連接器的描述檔案 (\* searchConnector-ms) ，可指定如何連線、傳送查詢，以及從位置接收結果。</span><span class="sxs-lookup"><span data-stu-id="5da78-119">Search connectors are Search Connector Description files (\*.searchConnector-ms) that specify how to connect to, send queries to, and receive results from the location.</span></span>

<span data-ttu-id="5da78-120">除了 web 服務之外，搜尋連接器還可以用來搜尋通訊協定處理常式所建立的本機索引範圍。</span><span class="sxs-lookup"><span data-stu-id="5da78-120">In addition to web services, search connectors can be used to search local index scopes created by protocol handlers.</span></span> <span data-ttu-id="5da78-121">例如，使用者可以使用該電子郵件存放區的搜尋連接器，在本機搜尋以 MAPI 通訊協定處理常式編制索引的電子郵件。</span><span class="sxs-lookup"><span data-stu-id="5da78-121">For example, users can search email indexed locally with the MAPI protocol handler by using a search connector for that email store.</span></span>

## <a name="how-do-search-connector-description-files-work"></a><span data-ttu-id="5da78-122">搜尋連接器描述檔案的運作方式為何？</span><span class="sxs-lookup"><span data-stu-id="5da78-122">How Do Search Connector Description Files Work?</span></span>

<span data-ttu-id="5da78-123">當使用者的系統上已安裝搜尋連接器描述檔案時，使用者可以開啟 Windows 檔案總管，在流覽窗格中按一下 [搜尋] 連接器，然後輸入搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="5da78-123">When Search Connector Description files are installed on users' systems, users can open Windows Explorer, click the search connector in the navigation pane, and enter a search query.</span></span> <span data-ttu-id="5da78-124">Windows 檔案總管使用搜尋連接器描述檔案中的資訊來傳送查詢，例如要使用的提供者和搜尋的範圍。</span><span class="sxs-lookup"><span data-stu-id="5da78-124">Windows Explorer sends the query using information from the Search Connector Description file, such as which provider to use and the scope of the search.</span></span> <span data-ttu-id="5da78-125">結果會以 RSS 或 Atom 摘要專案的形式傳回，並顯示給使用者，就像是一般的 Shell 專案一樣。</span><span class="sxs-lookup"><span data-stu-id="5da78-125">The results are returned as RSS or Atom feed items and displayed to users as if they were regular Shell items.</span></span>

<span data-ttu-id="5da78-126">您部署搜尋連接器描述檔案的方式取決於搜尋連接器支援的位置類型：</span><span class="sxs-lookup"><span data-stu-id="5da78-126">How you deploy your Search Connector Description file depends on the type of location the search connector supports:</span></span>

-   <span data-ttu-id="5da78-127">在 [OpenSearch 設定] (中， \* 為您的 web 服務 .osdx) 檔</span><span class="sxs-lookup"><span data-stu-id="5da78-127">In an OpenSearch configuration (\*.osdx) file for your web service</span></span>
-   <span data-ttu-id="5da78-128">在通訊協定處理常式安裝過程中</span><span class="sxs-lookup"><span data-stu-id="5da78-128">As part of your protocol handler installation</span></span>

<span data-ttu-id="5da78-129">當使用者開啟 .osdx 檔案或安裝通訊協定處理常式時，您應該確保發生下列情況：</span><span class="sxs-lookup"><span data-stu-id="5da78-129">You should ensure that the following things happen when a user opens the .osdx file or installs the protocol handler:</span></span>

-   <span data-ttu-id="5da78-130">Searchconnector-ms 檔案會建立在使用者的 **Windows 搜尋** 資料夾 (% userprofile%/Searches) 。</span><span class="sxs-lookup"><span data-stu-id="5da78-130">The .searchconnector-ms file is created in the users' **Windows Searches** folder (%userprofile%/Searches).</span></span>
-   <span data-ttu-id="5da78-131">在使用者的 [ **連結** ] 資料夾中建立 searchconnector-ms 檔案的快捷方式 (% userprofile%/Links) 。</span><span class="sxs-lookup"><span data-stu-id="5da78-131">A shortcut to the .searchconnector-ms file is created in the users' **Links** folder (%userprofile%/Links).</span></span>

## <a name="what-is-the-search-connector-description-schema"></a><span data-ttu-id="5da78-132">什麼是搜尋連接器描述架構？</span><span class="sxs-lookup"><span data-stu-id="5da78-132">What Is the Search Connector Description Schema?</span></span>

<span data-ttu-id="5da78-133">搜尋連接器描述架構是一種 XML 架構，可定義搜尋連接器描述檔案的結構 (\* searchConnector-ms) 。</span><span class="sxs-lookup"><span data-stu-id="5da78-133">The Search Connector Description schema is an XML schema that defines the structure of Search Connector Description files (\*.searchConnector-ms).</span></span> <span data-ttu-id="5da78-134">每個搜尋連接器都必須有搜尋連接器的描述檔案，該檔案會指定如何連線、傳送查詢，以及從位置接收結果。</span><span class="sxs-lookup"><span data-stu-id="5da78-134">Each search connector must have a Search Connector Description file that specifies how to connect to, send queries to, and receive results from the location.</span></span>

## <a name="what-are-the-major-parts-of-the-schema"></a><span data-ttu-id="5da78-135">架構的主要部分有哪些？</span><span class="sxs-lookup"><span data-stu-id="5da78-135">What Are the Major Parts of the Schema?</span></span>

<span data-ttu-id="5da78-136">下表列出架構的主要部分。</span><span class="sxs-lookup"><span data-stu-id="5da78-136">The following table lists the major parts of the schema.</span></span>



| <span data-ttu-id="5da78-137">子元素</span><span class="sxs-lookup"><span data-stu-id="5da78-137">Child elements</span></span>                                                                         | <span data-ttu-id="5da78-138">Description</span><span class="sxs-lookup"><span data-stu-id="5da78-138">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5da78-139">isSearchOnlyItem</span><span class="sxs-lookup"><span data-stu-id="5da78-139">isSearchOnlyItem</span></span>](search-schema-sconn-issearchonlyitem.md)                           | <span data-ttu-id="5da78-140">識別搜尋連接器支援的位置是否為僅限搜尋或搜尋和流覽。</span><span class="sxs-lookup"><span data-stu-id="5da78-140">Identifies whether the locations supported by the search connector are search-only or search and browse.</span></span>                                                                                |
| [<span data-ttu-id="5da78-141">isDefaultSaveLocation</span><span class="sxs-lookup"><span data-stu-id="5da78-141">isDefaultSaveLocation</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 | <span data-ttu-id="5da78-142">僅供程式庫使用。</span><span class="sxs-lookup"><span data-stu-id="5da78-142">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="5da78-143">isDefaultNonOwnerSaveLocation</span><span class="sxs-lookup"><span data-stu-id="5da78-143">isDefaultNonOwnerSaveLocation</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) | <span data-ttu-id="5da78-144">僅供程式庫使用。</span><span class="sxs-lookup"><span data-stu-id="5da78-144">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="5da78-145">description</span><span class="sxs-lookup"><span data-stu-id="5da78-145">description</span></span>](search-schema-sconn-description.md)                                     | <span data-ttu-id="5da78-146">描述搜尋連接器。</span><span class="sxs-lookup"><span data-stu-id="5da78-146">Describes the search connector.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="5da78-147">iconReference</span><span class="sxs-lookup"><span data-stu-id="5da78-147">iconReference</span></span>](search-schema-sconn-iconreference.md)                                 | <span data-ttu-id="5da78-148">識別搜尋連接器的自訂圖示位置。</span><span class="sxs-lookup"><span data-stu-id="5da78-148">Identifies the location of a custom icon for the search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="5da78-149">imageLink</span><span class="sxs-lookup"><span data-stu-id="5da78-149">imageLink</span></span>](search-schema-sconn-imagelink.md)                                         | <span data-ttu-id="5da78-150">識別搜尋連接器之自訂縮圖的位置。</span><span class="sxs-lookup"><span data-stu-id="5da78-150">Identifies the location of a custom thumbnail for the search connector.</span></span>                                                                                                                 |
| [<span data-ttu-id="5da78-151">作者</span><span class="sxs-lookup"><span data-stu-id="5da78-151">author</span></span>](search-schema-sconn-author.md)                                               | <span data-ttu-id="5da78-152">識別搜尋連接器的作者。</span><span class="sxs-lookup"><span data-stu-id="5da78-152">Identifies the author of the search connector.</span></span>                                                                                                                                          |
| [<span data-ttu-id="5da78-153">dateCreated</span><span class="sxs-lookup"><span data-stu-id="5da78-153">dateCreated</span></span>](search-schema-sconn-datecreated.md)                                     | <span data-ttu-id="5da78-154">識別建立搜尋連接器的日期。</span><span class="sxs-lookup"><span data-stu-id="5da78-154">Identifies the date that the search connector was created.</span></span>                                                                                                                              |
| [<span data-ttu-id="5da78-155">templateInfo</span><span class="sxs-lookup"><span data-stu-id="5da78-155">templateInfo</span></span>](search-schema-sconn-templateinfo.md)                                   | <span data-ttu-id="5da78-156">指定搜尋連接器的資料夾類型。</span><span class="sxs-lookup"><span data-stu-id="5da78-156">Specifies a folder type for the search connector.</span></span>                                                                                                                                       |
| [<span data-ttu-id="5da78-157">locationProvider</span><span class="sxs-lookup"><span data-stu-id="5da78-157">locationProvider</span></span>](search-schema-sconn-locationprovider.md)                           | <span data-ttu-id="5da78-158">指定此搜尋連接器要使用的搜尋提供者。</span><span class="sxs-lookup"><span data-stu-id="5da78-158">Specifies the search provider to be used by this search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="5da78-159">範圍 (scope)</span><span class="sxs-lookup"><span data-stu-id="5da78-159">scope</span></span>](search-schema-sconn-scope.md)                                                 | <span data-ttu-id="5da78-160">指定要在搜尋範圍中包含和排除的位置。</span><span class="sxs-lookup"><span data-stu-id="5da78-160">Specifies the locations to include in and exclude from the search scope.</span></span>                                                                                                                |
| [<span data-ttu-id="5da78-161">propertyStore</span><span class="sxs-lookup"><span data-stu-id="5da78-161">propertyStore</span></span>](search-schema-sconn-propertystore.md)                                 | <span data-ttu-id="5da78-162">指定此搜尋連接器之 XML 型 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 的位置。</span><span class="sxs-lookup"><span data-stu-id="5da78-162">Specifies the location of an XML-based [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) for this search connector.</span></span> <span data-ttu-id="5da78-163">**IPropertyStore** 支援搜尋連接器的 open 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5da78-163">The **IPropertyStore** supports the search connector's open metadata.</span></span> |
| [<span data-ttu-id="5da78-164">includeInStartMenuScope</span><span class="sxs-lookup"><span data-stu-id="5da78-164">includeInStartMenuScope</span></span>](search-schema-sconn-includeinstartmenuscope.md)             | <span data-ttu-id="5da78-165">指定搜尋連接器所表示的位置是否應包含在 [開始] 功能表的搜尋範圍內。</span><span class="sxs-lookup"><span data-stu-id="5da78-165">Specifies whether the location represented by the search connector should be included in the Start menu's search scope.</span></span>                                                                 |
| [<span data-ttu-id="5da78-166">域</span><span class="sxs-lookup"><span data-stu-id="5da78-166">domain</span></span>](search-schema-sconn-domain.md)                                               | <span data-ttu-id="5da78-167">識別搜尋連接器的最上層網域。</span><span class="sxs-lookup"><span data-stu-id="5da78-167">Identifies the search connector's top-level domain.</span></span>                                                                                                                                     |
| [<span data-ttu-id="5da78-168">supportsAdvancedQuerySyntax</span><span class="sxs-lookup"><span data-stu-id="5da78-168">supportsAdvancedQuerySyntax</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     | <span data-ttu-id="5da78-169">指定搜尋連接器是否支援 (AQS) 的 Advanced Query 語法。</span><span class="sxs-lookup"><span data-stu-id="5da78-169">Specifies whether the search connector supports Advanced Query Syntax (AQS).</span></span>                                                                                                            |
| [<span data-ttu-id="5da78-170">isIndexed</span><span class="sxs-lookup"><span data-stu-id="5da78-170">isIndexed</span></span>](search-schema-sconn-isindexed.md)                                         | <span data-ttu-id="5da78-171">指定搜尋連接器所表示的位置是否已編制索引。</span><span class="sxs-lookup"><span data-stu-id="5da78-171">Specifies whether the location represented by the search connector is indexed.</span></span>                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a><span data-ttu-id="5da78-172">搜尋連接器描述檔案的範例</span><span class="sxs-lookup"><span data-stu-id="5da78-172">Examples of Search Connector Description Files</span></span>

<span data-ttu-id="5da78-173">以下是同盟搜尋 web 服務的搜尋連接器描述檔案範例。</span><span class="sxs-lookup"><span data-stu-id="5da78-173">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



<span data-ttu-id="5da78-174">以下是 MAPI 通訊協定處理常式的搜尋連接器描述檔案範例。</span><span class="sxs-lookup"><span data-stu-id="5da78-174">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a><span data-ttu-id="5da78-175">其他資源</span><span class="sxs-lookup"><span data-stu-id="5da78-175">Additional Resources</span></span>

-   <span data-ttu-id="5da78-176">如需程式庫描述架構的詳細資訊，請參閱連結 [庫描述架構](../shell/library-schema-entry.md)。</span><span class="sxs-lookup"><span data-stu-id="5da78-176">For more information about the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>
-   <span data-ttu-id="5da78-177">如需安裝搜尋連接器的詳細資訊，請參閱 [Windows 中](-search-federated-search-overview.md)的同盟搜尋。</span><span class="sxs-lookup"><span data-stu-id="5da78-177">For more information on installing a search connector, see [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5da78-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="5da78-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5da78-179">**參考**</span><span class="sxs-lookup"><span data-stu-id="5da78-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5da78-180">searchConnectorDescriptionType 元素 (搜尋連接器架構) </span><span class="sxs-lookup"><span data-stu-id="5da78-180">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md)
</dt> <dt>

<span data-ttu-id="5da78-181">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="5da78-181">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5da78-182">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="5da78-182">OpenSearch</span></span>](http://www.opensearch.org/Home)
</dt> <dt>

[<span data-ttu-id="5da78-183">Microsoft 下載中心</span><span class="sxs-lookup"><span data-stu-id="5da78-183">Microsoft Download Center</span></span>](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
