---
description: 本主題說明如何藉由開啟 ( .osdx) 檔中的 OpenSearch 描述、如何部署 .osdx 檔案，以及如何追蹤您的 OpenSearch 服務使用方式，來向同盟搜尋註冊新的遠端資料存放區。
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: 在 Windows 同盟搜尋中部署搜尋連接器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468805"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a><span data-ttu-id="67633-103">在 Windows 同盟搜尋中部署搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="67633-103">Deploying Search Connectors in Windows Federated Search</span></span>

<span data-ttu-id="67633-104">本主題說明如何藉由開啟 ( .osdx) 檔中的 OpenSearch 描述、如何部署 .osdx 檔案，以及如何追蹤您的 [opensearch](https://github.com/dewitt/opensearch) 服務使用方式，來向同盟搜尋註冊新的遠端資料存放區。</span><span class="sxs-lookup"><span data-stu-id="67633-104">This topic explains how a user registers a new remote data store with federated search by opening an OpenSearch Description (.osdx) file, how to deploy an .osdx file, and how to track usage of your [OpenSearch](https://github.com/dewitt/opensearch) service.</span></span>

<span data-ttu-id="67633-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="67633-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="67633-106">Searchconnector-ms (Search Connector) File</span><span class="sxs-lookup"><span data-stu-id="67633-106">The .searchconnector-ms (Search Connector) File</span></span>](#the-searchconnector-ms-search-connector-file)
-   [<span data-ttu-id="67633-107">部署方法</span><span class="sxs-lookup"><span data-stu-id="67633-107">Deployment Methods</span></span>](#deployment-methods)
    -   [<span data-ttu-id="67633-108">提取部署</span><span class="sxs-lookup"><span data-stu-id="67633-108">Pull Deployment</span></span>](#pull-deployment)
    -   [<span data-ttu-id="67633-109">推送部署</span><span class="sxs-lookup"><span data-stu-id="67633-109">Push Deployment</span></span>](#push-deployment)
-   [<span data-ttu-id="67633-110">追蹤使用量</span><span class="sxs-lookup"><span data-stu-id="67633-110">Tracking Usage</span></span>](#tracking-usage)
-   [<span data-ttu-id="67633-111">其他資源</span><span class="sxs-lookup"><span data-stu-id="67633-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="67633-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="67633-112">Related topics</span></span>](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a><span data-ttu-id="67633-113">Searchconnector-ms (Search Connector) File</span><span class="sxs-lookup"><span data-stu-id="67633-113">The .searchconnector-ms (Search Connector) File</span></span>

<span data-ttu-id="67633-114">只要開啟 .osdx 檔案，以描述如何連線至 web 服務，以及如何對應 RSS 或 Atom XML 中的任何自訂元素，就會使用同盟搜尋來註冊新的遠端資料存放區。</span><span class="sxs-lookup"><span data-stu-id="67633-114">Merely opening the .osdx file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML registers your new remote data store with federated search.</span></span> <span data-ttu-id="67633-115">當使用者開啟 .osdx 檔案時，您可以將已經有與同盟搜尋相容的 [OpenSearch](https://github.com/dewitt/opensearch) web 服務的資料存放區新增至 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="67633-115">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with federated search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

<span data-ttu-id="67633-116">當您將 .osdx 給使用者，且使用者開啟 .osdx 檔案之後，就會發生下列事件。</span><span class="sxs-lookup"><span data-stu-id="67633-116">After you have given the .osdx to your user and the user opens the .osdx file, the following events occur.</span></span>

1.  <span data-ttu-id="67633-117">Searchconnector-ms 檔案會建立在 **Windows 搜尋** 資料夾 (% userprofile%/Searches) 。</span><span class="sxs-lookup"><span data-stu-id="67633-117">A .searchconnector-ms file is created in the **Windows Searches** folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="67633-118">Searchconnector-ms 檔案的快捷方式建立于 **連結** 資料夾 (% userprofile%/Links) 。</span><span class="sxs-lookup"><span data-stu-id="67633-118">A shortcut to the .searchconnector-ms file is created in the **Links** folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="67633-119">快捷方式會出現在 Windows 檔案總管導覽的 [我的最 **愛] 窗格** 中，讓使用者流覽至新的資料存放區，並查詢 web 服務。</span><span class="sxs-lookup"><span data-stu-id="67633-119">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store and query the web service.</span></span>

## <a name="deployment-methods"></a><span data-ttu-id="67633-120">部署方法</span><span class="sxs-lookup"><span data-stu-id="67633-120">Deployment Methods</span></span>

<span data-ttu-id="67633-121">有兩種方式可以部署搜尋連接器、提取部署和推送部署。</span><span class="sxs-lookup"><span data-stu-id="67633-121">There are two ways to deploy search connectors, pull deployment and push deployment.</span></span>

### <a name="pull-deployment"></a><span data-ttu-id="67633-122">提取部署</span><span class="sxs-lookup"><span data-stu-id="67633-122">Pull Deployment</span></span>

<span data-ttu-id="67633-123">提取部署描述任何類型的部署，使用者可在其中使用此計畫來安裝搜尋連接器。</span><span class="sxs-lookup"><span data-stu-id="67633-123">Pull deployment describes any type of deployment in which the end user takes the initiative to install the search connectors.</span></span> <span data-ttu-id="67633-124">提取部署的一般方法如下：</span><span class="sxs-lookup"><span data-stu-id="67633-124">Common methods of pull deployment are:</span></span>

-   <span data-ttu-id="67633-125">將 .osdx 檔案附加至電子郵件。</span><span class="sxs-lookup"><span data-stu-id="67633-125">Attaching the .osdx file in an email.</span></span>
-   <span data-ttu-id="67633-126">將檔案張貼在網頁上。</span><span class="sxs-lookup"><span data-stu-id="67633-126">Posting the file on a webpage.</span></span>
-   <span data-ttu-id="67633-127">在內部網路網站上提供動態連結;例如，根據使用者選擇或網站內目前的範圍產生自訂 .osdx 檔案。</span><span class="sxs-lookup"><span data-stu-id="67633-127">Providing a dynamic link on your intranet site; for example, one that generates custom .osdx files based on user choices or the current scope within the site.</span></span>

<span data-ttu-id="67633-128">如果是使用者在瀏覽器中按一下連結時所要下載的檔案，則必須將裝載 web 服務的 web 伺服器設定為以檔案形式傳遞 .osdx。</span><span class="sxs-lookup"><span data-stu-id="67633-128">For the file to be downloaded when the user clicks the link in their browser, the web server hosting the web service must be configured to deliver the .osdx as a file.</span></span> <span data-ttu-id="67633-129">因此，您必須設定網頁伺服器上的 MIME 類型，將 .osdx 檔案視為 `"application/opensearchdescription+xml"` 。</span><span class="sxs-lookup"><span data-stu-id="67633-129">Hence, you must configure the MIME Types on the web server to treat .osdx files as `"application/opensearchdescription+xml"`.</span></span> <span data-ttu-id="67633-130">（選擇性）您可以使用 Microsoft 提供的圖示來識別搜尋連接器連結。</span><span class="sxs-lookup"><span data-stu-id="67633-130">Optionally, you can use the icon supplied by Microsoft to identify search connector link.</span></span>

### <a name="push-deployment"></a><span data-ttu-id="67633-131">推送部署</span><span class="sxs-lookup"><span data-stu-id="67633-131">Push Deployment</span></span>

<span data-ttu-id="67633-132">推送部署描述任何不依賴使用者計畫來安裝搜尋連接器的部署類型。</span><span class="sxs-lookup"><span data-stu-id="67633-132">Push deployment describes any type of deployment that does not depend on user initiative to install the search connectors.</span></span> <span data-ttu-id="67633-133">推送部署的一般方法如下：</span><span class="sxs-lookup"><span data-stu-id="67633-133">Common methods of push deployment are:</span></span>

-   <span data-ttu-id="67633-134">群組原則喜好設定 (GPP) </span><span class="sxs-lookup"><span data-stu-id="67633-134">Group Policy Preferences (GPP)</span></span>
-   <span data-ttu-id="67633-135">登入指令檔</span><span class="sxs-lookup"><span data-stu-id="67633-135">Logon script</span></span>
-   <span data-ttu-id="67633-136">漫遊設定檔</span><span class="sxs-lookup"><span data-stu-id="67633-136">Roaming profiles</span></span>
-   <span data-ttu-id="67633-137">建立映像</span><span class="sxs-lookup"><span data-stu-id="67633-137">Imaging</span></span>

## <a name="tracking-usage"></a><span data-ttu-id="67633-138">追蹤使用量</span><span class="sxs-lookup"><span data-stu-id="67633-138">Tracking Usage</span></span>

<span data-ttu-id="67633-139">若要在使用者從 Windows 檔案總管中搜尋時，追蹤您的 [OpenSearch](https://github.com/dewitt/opensearch) 服務使用量，請篩選您的 web 伺服器記錄檔，以取得這個使用者代理程式字串： `Windows-Search+(Windows+NT+6.1)` 。</span><span class="sxs-lookup"><span data-stu-id="67633-139">To track the usage of your [OpenSearch](https://github.com/dewitt/opensearch) service by users searching from Windows Explorer, filter your web server log files for this user agent string: `Windows-Search+(Windows+NT+6.1)`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67633-140">其他資源</span><span class="sxs-lookup"><span data-stu-id="67633-140">Additional Resources</span></span>

<span data-ttu-id="67633-141">如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](/previous-versions//dd742958(v=vs.85))的「其他資源」。</span><span class="sxs-lookup"><span data-stu-id="67633-141">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67633-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="67633-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67633-143">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="67633-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="67633-144">在 Windows 中使用同盟搜尋開始使用</span><span class="sxs-lookup"><span data-stu-id="67633-144">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="67633-145">在 Windows 同盟搜尋中連接您的 web 服務</span><span class="sxs-lookup"><span data-stu-id="67633-145">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="67633-146">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="67633-146">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="67633-147">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="67633-147">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="67633-148">遵循 Windows 同盟搜尋的最佳作法</span><span class="sxs-lookup"><span data-stu-id="67633-148">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> </dl>

 

 
