---
description: 說明如何讓您的資料存放區可供 OpenSearch web 服務存取，以及如何避免可能的阻礙。
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: 在 Windows 同盟搜尋中啟用資料存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cef227cb82c64f391ec61b2a7fef0fe35acf131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973024"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a><span data-ttu-id="67167-103">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="67167-103">Enabling Your Data Store in Windows Federated Search</span></span>

<span data-ttu-id="67167-104">說明如何讓您的資料存放區可供 [OpenSearch](https://github.com/dewitt/opensearch) web 服務存取，以及如何避免可能的阻礙。</span><span class="sxs-lookup"><span data-stu-id="67167-104">Explains how to enable your data store to be accessed by an [OpenSearch](https://github.com/dewitt/opensearch) web service, and how to avoid potential barriers for doing so.</span></span>

<span data-ttu-id="67167-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="67167-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="67167-106">接受搜尋要求的條件</span><span class="sxs-lookup"><span data-stu-id="67167-106">Conditions for Search Request Acceptance</span></span>](#conditions-for-search-request-acceptance)
    -   [<span data-ttu-id="67167-107">支援的查詢語法</span><span class="sxs-lookup"><span data-stu-id="67167-107">Supported Query Syntax</span></span>](#supported-query-syntax)
    -   [<span data-ttu-id="67167-108">支援的驗證通訊協定</span><span class="sxs-lookup"><span data-stu-id="67167-108">Supported Authentication Protocols</span></span>](#supported-authentication-protocols)
-   [<span data-ttu-id="67167-109">在 RSS 或 Atom 中傳送查詢並傳回搜尋結果</span><span class="sxs-lookup"><span data-stu-id="67167-109">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [<span data-ttu-id="67167-110">RSS 摘要輸出的範例</span><span class="sxs-lookup"><span data-stu-id="67167-110">Example of an RSS Feed Output</span></span>](#example-of-an-rss-feed-output)
-   [<span data-ttu-id="67167-111">自動對應至 Windows Shell 屬性</span><span class="sxs-lookup"><span data-stu-id="67167-111">Automatic Mapping to Windows Shell Properties</span></span>](#automatic-mapping-to-windows-shell-properties)
-   [<span data-ttu-id="67167-112">瞭解如何對檔案類型 Windows 地圖專案</span><span class="sxs-lookup"><span data-stu-id="67167-112">Understanding How Windows Maps Items to File Types</span></span>](#understanding-how-windows-maps-items-to-file-types)
-   [<span data-ttu-id="67167-113">避免啟用資料存放區的潛在阻礙</span><span class="sxs-lookup"><span data-stu-id="67167-113">Avoiding Potential Barriers to Enabling a Data Store</span></span>](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [<span data-ttu-id="67167-114">其他資源</span><span class="sxs-lookup"><span data-stu-id="67167-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="67167-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="67167-115">Related topics</span></span>](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a><span data-ttu-id="67167-116">接受搜尋要求的條件</span><span class="sxs-lookup"><span data-stu-id="67167-116">Conditions for Search Request Acceptance</span></span>

<span data-ttu-id="67167-117">您在 web 伺服器上建立的 [OpenSearch](https://github.com/dewitt/opensearch) web 服務 **必須** 滿足下列兩個需求：</span><span class="sxs-lookup"><span data-stu-id="67167-117">The [OpenSearch](https://github.com/dewitt/opensearch) web service you create on your web server **must** fulfill the following two requirements:</span></span>

-   <span data-ttu-id="67167-118">能夠接受 `GET URL` 來自用戶端的查詢。</span><span class="sxs-lookup"><span data-stu-id="67167-118">Be able to accept a `GET URL` query from the client.</span></span>
-   <span data-ttu-id="67167-119">允許在 URL 中內嵌搜尋字詞。</span><span class="sxs-lookup"><span data-stu-id="67167-119">Permit the search terms to be embedded in the URL.</span></span>

    <span data-ttu-id="67167-120">下列範例顯示如何將搜尋字詞內嵌在 URL 中。</span><span class="sxs-lookup"><span data-stu-id="67167-120">The following example shows how a search term can be embedded in a URL.</span></span>

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> <span data-ttu-id="67167-121">聯合搜尋不支援 `POST` 將要求傳送至 web 服務。</span><span class="sxs-lookup"><span data-stu-id="67167-121">Federated search does not support sending `POST` requests to a web service.</span></span>

 

<span data-ttu-id="67167-122">如需有關建立 URL 的詳細資訊，請參閱在 [Windows 同盟搜尋中建立 OpenSearch 描述](-search-federated-search-osdx-file.md)檔案的「URL 範本參數」。</span><span class="sxs-lookup"><span data-stu-id="67167-122">For more information about constructing a URL, see "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

### <a name="supported-query-syntax"></a><span data-ttu-id="67167-123">支援的查詢語法</span><span class="sxs-lookup"><span data-stu-id="67167-123">Supported Query Syntax</span></span>

<span data-ttu-id="67167-124">在 Windows 7 中不需要特定的查詢語法。</span><span class="sxs-lookup"><span data-stu-id="67167-124">There is no specific query syntax expected in Windows 7.</span></span> <span data-ttu-id="67167-125">[OpenSearch 提供者] 會接受使用者在 Windows 檔案總管的輸入方塊中輸入的任何詞彙，然後將其編碼成 URL。</span><span class="sxs-lookup"><span data-stu-id="67167-125">The OpenSearch provider accepts whatever terms the user enters in the input box in Windows Explorer, and encodes it into the URL.</span></span> <span data-ttu-id="67167-126">它會根據在 [Windows 同盟搜尋中建立 OpenSearch 描述](-search-federated-search-osdx-file.md)檔案的「Url 範本參數」中所述的 url 範本來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="67167-126">It does so according to the URL template described in "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

<span data-ttu-id="67167-127">使用者預期會將不同的詞彙視為隱含以 and 連結在一起。</span><span class="sxs-lookup"><span data-stu-id="67167-127">Users expect that separate terms are treated as implicitly ANDed together.</span></span> <span data-ttu-id="67167-128">例如，「Microsoft Windows」的查詢應該只傳回包含「Windows」和「Microsoft」的結果。</span><span class="sxs-lookup"><span data-stu-id="67167-128">For example, a query for "Microsoft Windows" should return only results that contain both "Windows" and "Microsoft".</span></span>

### <a name="supported-authentication-protocols"></a><span data-ttu-id="67167-129">支援的驗證通訊協定</span><span class="sxs-lookup"><span data-stu-id="67167-129">Supported Authentication Protocols</span></span>

<span data-ttu-id="67167-130">Windows 同盟搜尋支援以 Windows 為基礎的驗證，並可透過下列通訊協定提供認證給 web 服務：</span><span class="sxs-lookup"><span data-stu-id="67167-130">Windows Federated Search supports Windows-based authentication, and can provide credentials to web services via the following protocols:</span></span>

-   <span data-ttu-id="67167-131">NTLM。</span><span class="sxs-lookup"><span data-stu-id="67167-131">NTLM.</span></span>
-   <span data-ttu-id="67167-132">Kerberos。</span><span class="sxs-lookup"><span data-stu-id="67167-132">Kerberos.</span></span>
-   <span data-ttu-id="67167-133">基本 (僅透過 HTTPs) 。</span><span class="sxs-lookup"><span data-stu-id="67167-133">Basic (only over https).</span></span>
-   <span data-ttu-id="67167-134">其他安全性支援提供者 (Ssp) 安裝在可提供額外查詢容量的 Windows 上。</span><span class="sxs-lookup"><span data-stu-id="67167-134">Other Security Support Providers (SSPs) installed on Windows that provide additional querying capacity.</span></span> <span data-ttu-id="67167-135">請參閱 [SSP 介面](../secauthn/sspi.md) SDK 檔，以隨時掌握其他 ssp 的可能加法。</span><span class="sxs-lookup"><span data-stu-id="67167-135">See the [SSP Interface](../secauthn/sspi.md) SDK documentation to keep abreast of the potential addition of other SSPs.</span></span>

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="67167-136">在 RSS 或 Atom 中傳送查詢並傳回搜尋結果</span><span class="sxs-lookup"><span data-stu-id="67167-136">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="67167-137">[ [OpenSearch](https://github.com/dewitt/opensearch) 提供者] 負責將 XML 元素值對應至 windows 應用程式可以使用的 windows Shell 系統屬性。</span><span class="sxs-lookup"><span data-stu-id="67167-137">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span> <span data-ttu-id="67167-138">但是，您不限於標準 RSS 或 Atom 專案的預設對應，而且可以在 Windows 命名空間中包含每個屬性的自訂 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="67167-138">But you are not limited to the default mappings of standard RSS or Atom elements, and can include custom XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="67167-139">例如，您可以在 **專案專案** 內加入自己的自訂 XML 專案，以提供其他的中繼資料給 Windows。</span><span class="sxs-lookup"><span data-stu-id="67167-139">For example, you can add your own custom XML elements within the **item** element to provide additional metadata to Windows.</span></span> <span data-ttu-id="67167-140">您也可以從其他 XML 命名空間（例如 iTunes）對應元素。</span><span class="sxs-lookup"><span data-stu-id="67167-140">You can also map elements from other XML namespaces, such as iTunes</span></span>

### <a name="example-of-an-rss-feed-output"></a><span data-ttu-id="67167-141">RSS 摘要輸出的範例</span><span class="sxs-lookup"><span data-stu-id="67167-141">Example of an RSS Feed Output</span></span>

<span data-ttu-id="67167-142">下列 RSS 摘要輸出範例會傳回一個專案。</span><span class="sxs-lookup"><span data-stu-id="67167-142">The following example RSS feed output returns one item.</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="67167-143">如需有關屬性對應的詳細資訊，請參閱在 [windows 同盟搜尋中建立 OpenSearch 描述](-search-federated-search-osdx-file.md)檔案的「Windows 同盟搜尋中的擴充元素」和「自訂屬性對應」章節。</span><span class="sxs-lookup"><span data-stu-id="67167-143">For more detailed information about property mapping, see the "Extended Elements in WIndows Federated Search" and "Custom Property Mappings" sections in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="automatic-mapping-to-windows-shell-properties"></a><span data-ttu-id="67167-144">自動對應至 Windows Shell 屬性</span><span class="sxs-lookup"><span data-stu-id="67167-144">Automatic Mapping to Windows Shell Properties</span></span>

<span data-ttu-id="67167-145">在 RSS 摘要的專案內，您可以選擇包含自動對應至 Windows Shell 系統屬性的其他 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="67167-145">Within the items in your RSS feed, you can choose to include other XML elements that automatically map to Windows Shell system properties.</span></span> <span data-ttu-id="67167-146">若要這樣做，請包含以 Windows Shell 屬性命名的元素，並在前面加上 Windows Shell system 命名空間。</span><span class="sxs-lookup"><span data-stu-id="67167-146">To do so, include an element named after the Windows Shell property and prefixed with the Windows Shell system namespace.</span></span> <span data-ttu-id="67167-147">下列範例說明命名空間宣告 `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` ，以及包含屬性對應的元素 `win:System.Contact.PrimaryEmailAddress` ：</span><span class="sxs-lookup"><span data-stu-id="67167-147">The following example illustrates the namespace declaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` and the inclusion of an element for the property mapping `win:System.Contact.PrimaryEmailAddress`:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



<span data-ttu-id="67167-148">此處使用的命名空間前置詞 (`"win"`) 是建議的作法; 您可以使用任何前置詞。</span><span class="sxs-lookup"><span data-stu-id="67167-148">The namespace prefix used here (`"win"`) is a suggestion; you can use any prefix.</span></span> <span data-ttu-id="67167-149">不過，您必須使用確切的 Windows Shell 屬性名稱，且必須包含 (URI) 的確切統一資源識別項，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="67167-149">However, you must use the exact Windows Shell property names, and must include the exact Uniform Resource Identifier (URI), as shown in the following example:</span></span>


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



<span data-ttu-id="67167-150">**關於 Windows Shell 系統屬性**</span><span class="sxs-lookup"><span data-stu-id="67167-150">**About Windows Shell System Properties**</span></span>

<span data-ttu-id="67167-151">Windows 會定義完整的 [系統屬性](../properties/props.md) 清單，以及每個屬性所需的實數值型別格式。</span><span class="sxs-lookup"><span data-stu-id="67167-151">Windows defines a complete list of [System Properties](../properties/props.md) and the value type format required for each property.</span></span> <span data-ttu-id="67167-152">例如，[ [FileExtension](../properties/props-system-fileextension.md) ] 視窗 Shell 屬性的檔指定值必須包含開頭的點 ( ".docx"，而不是 ".docx" ) 。</span><span class="sxs-lookup"><span data-stu-id="67167-152">The documentation for the [System.FileExtension](../properties/props-system-fileextension.md) Window Shell property, for example, specifies that the value must contain the leading dot (".docx" and not "docx").</span></span>

<span data-ttu-id="67167-153">**日期和時間值**</span><span class="sxs-lookup"><span data-stu-id="67167-153">**Date and Time Values**</span></span>

<span data-ttu-id="67167-154">慣用的日期和時間格式為 ISO-8601，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="67167-154">The preferred date and time format is ISO-8601, as shown in the following example:</span></span>


```
2008-01-16T 19:20:30:.45+01:00
```



<span data-ttu-id="67167-155">.NET 開發人員應該使用 DateTime 類別搭配 `ToString("R") ` 來輸出正確的格式。</span><span class="sxs-lookup"><span data-stu-id="67167-155">.NET developers should use the DateTime class with `ToString("R") `to output the correct format.</span></span>

<span data-ttu-id="67167-156">如需有關屬性對應的詳細資訊，請參閱在 [windows 同盟搜尋中建立 OpenSearch 描述](-search-federated-search-osdx-file.md)檔案中的「Windows 同盟搜尋中的擴充元素」。</span><span class="sxs-lookup"><span data-stu-id="67167-156">For more detailed information about property mapping, see "Extended Elements in Windows Federated Search" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="understanding-how-windows-maps-items-to-file-types"></a><span data-ttu-id="67167-157">瞭解如何對檔案類型 Windows 地圖專案</span><span class="sxs-lookup"><span data-stu-id="67167-157">Understanding How Windows Maps Items to File Types</span></span>

<span data-ttu-id="67167-158">在 Windows 檔案總管 UI 內搜尋，可讓使用者在 RSS 專案指向遠端儲存的檔案時，將結果視為檔案。</span><span class="sxs-lookup"><span data-stu-id="67167-158">Searching within the Windows Explorer UI permits users to treat results as files when an RSS item points to a file stored remotely.</span></span> <span data-ttu-id="67167-159">使用者可以拖放專案至桌面，Windows 檔案總管 UI 會顯示正確的圖示，並提供適當的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="67167-159">The user can drag and drop items to the desktop, and the Windows Explorer UI displays the correct icon and provides the appropriate shortcut menu.</span></span> <span data-ttu-id="67167-160">如果 RSS 專案未指向遠端儲存的檔案，則會將該檔案視為連結，而使用者可以在其上執行動作，例如建立快捷方式或在瀏覽器中開啟它。</span><span class="sxs-lookup"><span data-stu-id="67167-160">If the RSS item does not point to a remotely stored file, the file is treated as a link, and users can perform actions on it such as creating a shortcut or opening it in the browser.</span></span>

<span data-ttu-id="67167-161">下列流程圖顯示 Windows 如何判斷專案的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="67167-161">The following flowchart shows how Windows determines an item's file type.</span></span>

![流程圖：顯示從專案到決策的路徑，以將其視為 web 連結類型專案或檔案類型](images/determineanitemfiletype.png)

<span data-ttu-id="67167-163">[OpenSearch](https://github.com/dewitt/opensearch)提供者會執行下列步驟，將專案對應至檔案類型：</span><span class="sxs-lookup"><span data-stu-id="67167-163">The [OpenSearch](https://github.com/dewitt/opensearch) provider performs the following steps to map an item to a file type:</span></span>

-   <span data-ttu-id="67167-164">識別是否應將專案視為檔案或網頁連結。</span><span class="sxs-lookup"><span data-stu-id="67167-164">Identify whether the item should be treated as a file or a web link.</span></span>
-   <span data-ttu-id="67167-165">識別要使用的正確副檔名。</span><span class="sxs-lookup"><span data-stu-id="67167-165">Identify the correct file name extension to use.</span></span>

<span data-ttu-id="67167-166">例如，如果專案有使用檔案系統路徑的連結 URL (例如 `file:///\\server\share\etc\item.ext`) ，則 [ [OpenSearch](https://github.com/dewitt/opensearch) 提供者] 會將連結視為檔案，並依此) 範例中的路徑 ( 中使用的副檔名來決定類型。</span><span class="sxs-lookup"><span data-stu-id="67167-166">For example, if the item has a link URL that uses a file system path (such as `file:///\\server\share\etc\item.ext`), the [OpenSearch](https://github.com/dewitt/opensearch) provider treats the link as a file and determines the type by the file name extension used in the path (.ext in this example).</span></span>

<span data-ttu-id="67167-167">如果專案使用標準 RSS 主機殼或 **MediaRSS media： content** 元素，則 [OpenSearch](https://github.com/dewitt/opensearch) 提供者會假設該專案為檔案，並識別副檔名，如下所示：</span><span class="sxs-lookup"><span data-stu-id="67167-167">If the item uses the standard RSS enclosure or **MediaRSS media:content** element, the [OpenSearch](https://github.com/dewitt/opensearch) provider assumes that the item is a file and identifies the file name extension as follows:</span></span>

-   <span data-ttu-id="67167-168">如果已對應專案的 [FileExtension](../properties/props-system-fileextension.md) Windows Shell 屬性，則提供者會使用該副檔名。</span><span class="sxs-lookup"><span data-stu-id="67167-168">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has been mapped for the item, the provider uses that file name extension.</span></span>
-   <span data-ttu-id="67167-169">如果 [FileExtension](../properties/props-system-fileextension.md) Windows Shell 屬性尚未對應，則提供者會使用主機殼或 content 元素中指定的 **類型** 屬性。</span><span class="sxs-lookup"><span data-stu-id="67167-169">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has not been mapped, the provider uses the **Type** attribute specified in the enclosure or content element.</span></span> <span data-ttu-id="67167-170">這個元素應該包含 `MIMEType` 字串，例如 `"image/jpeg"` 。</span><span class="sxs-lookup"><span data-stu-id="67167-170">This element should contain a `MIMEType` string, such as `"image/jpeg"`.</span></span> <span data-ttu-id="67167-171">如果與在 `MIMEType` 用戶端電腦上註冊的副檔名相關聯，該專案就會被視為該類型的檔案。</span><span class="sxs-lookup"><span data-stu-id="67167-171">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the item is regarded as a file of that type.</span></span> <span data-ttu-id="67167-172">如果未 `MIMEType` 與用戶端電腦上註冊的副檔名建立關聯，則會將該專案視為 web 連結類型。</span><span class="sxs-lookup"><span data-stu-id="67167-172">If the `MIMEType` is not associated with a file name extension registered on the client computer, the item is treated as a web link type.</span></span> <span data-ttu-id="67167-173">[OpenSearch](https://github.com/dewitt/opensearch)提供者不會嘗試剖析 **Url** 屬性來尋找副檔名。</span><span class="sxs-lookup"><span data-stu-id="67167-173">The [OpenSearch](https://github.com/dewitt/opensearch) provider does not attempt to parse the **Url** attribute to locate the file name extension.</span></span>
-   <span data-ttu-id="67167-174">如果與在 `MIMEType` 用戶端電腦上註冊的副檔名相關聯，則提供者會判斷副檔名是否為已知的 web 檔案類型 ( .htm、.html、.asp、.aspx、php、.asp、.stm) 。</span><span class="sxs-lookup"><span data-stu-id="67167-174">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the provider determines whether the file name extension is a known web file type (.htm, .html, .asp, .aspx, .php, .swf, .stm).</span></span> <span data-ttu-id="67167-175">如果是，則會將檔案類型視為 web 連結類型;否則，它會被視為一種檔案類型。</span><span class="sxs-lookup"><span data-stu-id="67167-175">If so, the file type is regarded as a web link type; otherwise, it is regarded as a file type.</span></span> <span data-ttu-id="67167-176">例如，如果與 `MIMEType "text/html"` .htm 副檔名相關聯，該專案會被視為 web 連結，而不是 .htm 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="67167-176">For example, if the `MIMEType "text/html"` is associated with the .htm file name extension, that item is regarded as a web link instead of as an .htm file type.</span></span>

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a><span data-ttu-id="67167-177">避免啟用資料存放區的潛在阻礙</span><span class="sxs-lookup"><span data-stu-id="67167-177">Avoiding Potential Barriers to Enabling a Data Store</span></span>

<span data-ttu-id="67167-178">某些資料存放區不提供與 [OpenSearch](https://github.com/dewitt/opensearch)相容的 web 服務，但仍可連接到 Windows 同盟搜尋。</span><span class="sxs-lookup"><span data-stu-id="67167-178">Some data stores do not provide an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service but can still be connected to Windows Federated Search.</span></span> <span data-ttu-id="67167-179">這類資料存放區包括：</span><span class="sxs-lookup"><span data-stu-id="67167-179">Such data stores include:</span></span>

-   <span data-ttu-id="67167-180">Windows 7 同盟搜尋中不支援的驗證方法的遠端索引。</span><span class="sxs-lookup"><span data-stu-id="67167-180">Remote indexes with authentication methods that are not supported in Windows 7 Federated Search.</span></span>

    <span data-ttu-id="67167-181">範例包括表單架構驗證和其他自訂驗證方法。</span><span class="sxs-lookup"><span data-stu-id="67167-181">Examples include forms-based authentication and other custom authentication methods.</span></span>

-   <span data-ttu-id="67167-182">如果高價值的公用存放區具有公用 web Api，則任何人都可以撰寫與 [OpenSearch](https://github.com/dewitt/opensearch)相容的另一個 web 服務，並在幕後呼叫這些 api。</span><span class="sxs-lookup"><span data-stu-id="67167-182">If a high-value public store has public web APIs, anyone can write another web service that is [OpenSearch](https://github.com/dewitt/opensearch)-compatible and calls those APIs behind the scenes.</span></span>

    <span data-ttu-id="67167-183">範例包括國會和醫療研究資料庫的程式庫。</span><span class="sxs-lookup"><span data-stu-id="67167-183">Examples include the Library of Congress, and medical research databases.</span></span>

-   <span data-ttu-id="67167-184">專屬的企業資料存放區或索引，以及舊版內容管理存放區，可能無法執行前端。</span><span class="sxs-lookup"><span data-stu-id="67167-184">Proprietary enterprise data stores or indexes, and legacy content management stores, for which it might be impossible to implement a front end.</span></span>

<span data-ttu-id="67167-185">不過，有一些替代方法可避免阻礙啟用資料存放區。</span><span class="sxs-lookup"><span data-stu-id="67167-185">However, there are alternatives that can avoid barriers to enabling a data store.</span></span> <span data-ttu-id="67167-186">以下是其中一些替代方案：</span><span class="sxs-lookup"><span data-stu-id="67167-186">The following are some of those alternatives:</span></span>

<span data-ttu-id="67167-187">**當您無法修改現有資料來源的 web 服務，或 web 服務提供自訂 API 時，撰寫中間人 web 服務：**</span><span class="sxs-lookup"><span data-stu-id="67167-187">**To write a middle-man web service when you cannot modify the web service for the existing data source, or the web service provides a custom API:**</span></span>

1.  <span data-ttu-id="67167-188">撰寫可接受 Windows 7 查詢的中間人 web 服務。</span><span class="sxs-lookup"><span data-stu-id="67167-188">Write a middle-man web service that can accept a Windows 7 query.</span></span>
2.  <span data-ttu-id="67167-189">連接到您的資料來源，並取出查詢結果。</span><span class="sxs-lookup"><span data-stu-id="67167-189">Connect to your data source, and retrieve the query results.</span></span>
3.  <span data-ttu-id="67167-190">以 RSS 或 Atom 格式重新格式化結果。</span><span class="sxs-lookup"><span data-stu-id="67167-190">Reformat the results in RSS or Atom format.</span></span>
4.  <span data-ttu-id="67167-191">將結果傳回到 Windows 7 用戶端。</span><span class="sxs-lookup"><span data-stu-id="67167-191">Return the results to the Windows 7 client.</span></span>
5.  <span data-ttu-id="67167-192">請注意，對於 enterprise data services 和許多網際網路資料服務，您可能需要代表 web 服務傳遞使用者認證，以根據使用者的許可權來執行結果修剪。</span><span class="sxs-lookup"><span data-stu-id="67167-192">Note that for enterprise data services and many Internet data services, you may need to pass the user credentials through on behalf of the web service to perform result trimming based on the user's permissions.</span></span>

<span data-ttu-id="67167-193">**當您無法啟用公用資料存放區時，若要使用現有的搜尋引擎：**</span><span class="sxs-lookup"><span data-stu-id="67167-193">**To use an existing search engine when you cannot enable a public data store:**</span></span>

1.  <span data-ttu-id="67167-194">使用已使用 RSS 支援 [OpenSearch](https://github.com/dewitt/opensearch) 的公用搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="67167-194">Use a public search engine that already supports [OpenSearch](https://github.com/dewitt/opensearch) with RSS.</span></span> <span data-ttu-id="67167-195">若要這麼做，您可以為使用者提供 .osdx 檔案，該檔案的 URL 範本會將結果限制為只有特定網域的結果。</span><span class="sxs-lookup"><span data-stu-id="67167-195">You can do so by providing your users with an .osdx file that has a URL template that restricts results to only those for your specific domain.</span></span>
2.  <span data-ttu-id="67167-196">請參閱下列的 [OpenSearch](https://github.com/dewitt/opensearch) 描述範例，以針對 live.com 使用查詢來僅搜尋適用于 Windows 的說明內容。</span><span class="sxs-lookup"><span data-stu-id="67167-196">See the following example of an [OpenSearch](https://github.com/dewitt/opensearch) description for searching only the Help content for Windows by using a query against live.com.</span></span>

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

<span data-ttu-id="67167-197">**當您無法啟用專屬的企業資料存放區或索引時，若要使用支援 OpenSearch 的現有索引伺服器：**</span><span class="sxs-lookup"><span data-stu-id="67167-197">**To use an existing indexing server that supports OpenSearch when you cannot enable proprietary enterprise data stores or indexes:**</span></span>

1.  <span data-ttu-id="67167-198">選取支援 [OpenSearch](https://github.com/dewitt/opensearch) 的現有索引伺服器來為您的內容編制索引，例如 SharePoint 搜尋伺服器。</span><span class="sxs-lookup"><span data-stu-id="67167-198">Select an existing indexing server that supports [OpenSearch](https://github.com/dewitt/opensearch) to index your content, such as the SharePoint Search Server.</span></span>
2.  <span data-ttu-id="67167-199">使用 URL 範本內的關鍵字語法，建立 .osdx 檔案，將 SharePoint 索引的結果限制為只有來自您伺服器的結果。</span><span class="sxs-lookup"><span data-stu-id="67167-199">Create an .osdx file that restricts the results from the SharePoint index to only those from your server by using their KeyWord syntax within the URL template.</span></span>

<span data-ttu-id="67167-200">**如果伺服器端專用解決方案無法運作，則撰寫用戶端資料存放區：**</span><span class="sxs-lookup"><span data-stu-id="67167-200">**To write a client-side data store if a server-side-only solution does not work:**</span></span>

1.  <span data-ttu-id="67167-201">撰寫[位於 Windows](https://github.com/dewitt/opensearch)的 opensearch 提供者與外部資料源之間的客戶[端資料來源](https://github.com/dewitt/opensearch)。</span><span class="sxs-lookup"><span data-stu-id="67167-201">Write a client-side [OpenSearch](https://github.com/dewitt/opensearch) data source that sits between the Windows [OpenSearch](https://github.com/dewitt/opensearch) provider and the external data source.</span></span>
2.  <span data-ttu-id="67167-202">使用 Windows SDK 中的 [IOpenSearchSource 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) API 來建立適當設定的 searchconnector-ms 檔案，讓 Windows 檔案總管可以使用查詢參數來呼叫您的實作為。</span><span class="sxs-lookup"><span data-stu-id="67167-202">Use the [IOpenSearchSource Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) API in the Windows SDK to create an appropriately configured .searchconnector-ms file through which Windows Explorer can call your implementation with the query parameters.</span></span> <span data-ttu-id="67167-203">然後，您的實作為會傳回以 RSS 或 Atom 格式格式化的結果。</span><span class="sxs-lookup"><span data-stu-id="67167-203">Your implementation can then return results formatted in RSS or Atom format.</span></span> <span data-ttu-id="67167-204">這麼做可讓您的執行程式提供自訂驗證 UI，並使用其專屬的 API 連接到資料來源。</span><span class="sxs-lookup"><span data-stu-id="67167-204">Doing so enables your implementation to provide custom authentication UI and to connect to the data source using its proprietary API.</span></span>

> [!Note]  
> <span data-ttu-id="67167-205">開啟 .osdx 檔案會在% userprofile%/searches 目錄中建立 searchconnector-ms 檔案 (搜尋) 連接器，並在% userprofile%/links 目錄中放置該檔案的連結。</span><span class="sxs-lookup"><span data-stu-id="67167-205">Opening an .osdx file creates a .searchconnector-ms file (search connector) in the %userprofile%/searches directory and places a link to it in the %userprofile%/links directory.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="67167-206">其他資源</span><span class="sxs-lookup"><span data-stu-id="67167-206">Additional Resources</span></span>

<span data-ttu-id="67167-207">如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](/previous-versions//dd742958(v=vs.85))的「其他資源」。</span><span class="sxs-lookup"><span data-stu-id="67167-207">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67167-208">相關主題</span><span class="sxs-lookup"><span data-stu-id="67167-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67167-209">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="67167-209">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="67167-210">在 Windows 中使用同盟搜尋開始使用</span><span class="sxs-lookup"><span data-stu-id="67167-210">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="67167-211">在 Windows 同盟搜尋中連接您的 web 服務</span><span class="sxs-lookup"><span data-stu-id="67167-211">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="67167-212">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="67167-212">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="67167-213">遵循 Windows 同盟搜尋的最佳作法</span><span class="sxs-lookup"><span data-stu-id="67167-213">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="67167-214">在 Windows 同盟搜尋中部署搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="67167-214">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
