---
description: 本主題說明在資料存放區與 Windows 同盟搜尋之間連接 web 服務，以及如何在 RSS 或 Atom 中傳送查詢和傳回搜尋結果所牽涉到的步驟。
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: 在 Windows 同盟搜尋中連接您的 Web 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112461"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a><span data-ttu-id="4b198-103">在 Windows 同盟搜尋中連接您的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="4b198-103">Connecting Your Web Service in Windows Federated Search</span></span>

<span data-ttu-id="4b198-104">本主題說明在資料存放區與 Windows 同盟搜尋之間連接 web 服務，以及如何在 RSS 或 Atom 中傳送查詢和傳回搜尋結果所牽涉到的步驟。</span><span class="sxs-lookup"><span data-stu-id="4b198-104">This topic describes the steps involved in connecting a web service between your data store and Windows Federated Search, and how to send queries and return search results in RSS or Atom.</span></span>

<span data-ttu-id="4b198-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="4b198-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="4b198-106">連接您的 web 服務</span><span class="sxs-lookup"><span data-stu-id="4b198-106">Connect Your web Service</span></span>](#connect-your-web-service)
-   [<span data-ttu-id="4b198-107">註冊現有的遠端資料存放區</span><span class="sxs-lookup"><span data-stu-id="4b198-107">Register an Existing Remote Data Store</span></span>](#register-an-existing-remote-data-store)
-   [<span data-ttu-id="4b198-108">其他資源</span><span class="sxs-lookup"><span data-stu-id="4b198-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="4b198-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b198-109">Related topics</span></span>](#related-topics)

## <a name="connect-your-web-service"></a><span data-ttu-id="4b198-110">連接您的 web 服務</span><span class="sxs-lookup"><span data-stu-id="4b198-110">Connect Your web Service</span></span>

<span data-ttu-id="4b198-111">**若要將資料存放區的 web 服務連接到同盟搜尋，請執行下列步驟：**</span><span class="sxs-lookup"><span data-stu-id="4b198-111">**To connect the web service of your data store to federated search, perform the following steps:**</span></span>

1.  <span data-ttu-id="4b198-112">建立 .osdx 檔案。</span><span class="sxs-lookup"><span data-stu-id="4b198-112">Create an .osdx file.</span></span>
2.  <span data-ttu-id="4b198-113">將 .osdx 檔案提供給使用者，讓他們可以開啟 .osdx 檔案，依需求新增服務。</span><span class="sxs-lookup"><span data-stu-id="4b198-113">Supply the .osdx file to users so that they can add the service on demand by opening the .osdx file.</span></span>
3.  <span data-ttu-id="4b198-114">產生搜尋連接器，並在您的企業中主動加以部署。</span><span class="sxs-lookup"><span data-stu-id="4b198-114">Generate a search connector and actively deploy it in your enterprise.</span></span>

## <a name="register-an-existing-remote-data-store"></a><span data-ttu-id="4b198-115">註冊現有的遠端資料存放區</span><span class="sxs-lookup"><span data-stu-id="4b198-115">Register an Existing Remote Data Store</span></span>

<span data-ttu-id="4b198-116">使用者藉由開啟 ( .osdx) 檔案中的 [OpenSearch 描述]，向 Windows 同盟搜尋註冊新的遠端資料存放區。</span><span class="sxs-lookup"><span data-stu-id="4b198-116">A user registers a new remote data store with Windows Federated Search by opening an OpenSearch Description (.osdx) file.</span></span> <span data-ttu-id="4b198-117">當使用者這樣做時，會發生下列事件：</span><span class="sxs-lookup"><span data-stu-id="4b198-117">When the user does so, the following events occur:</span></span>

1.  <span data-ttu-id="4b198-118">Searchconnector-ms 檔案 (搜尋連接器) 會建立在 Windows 搜尋資料夾 (% userprofile%/Searches) 。</span><span class="sxs-lookup"><span data-stu-id="4b198-118">A .searchconnector-ms file (search connector) is created in the Windows Searches folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="4b198-119">Searchconnector-ms 檔案的快捷方式建立于連結資料夾 (% userprofile%/Links) 。</span><span class="sxs-lookup"><span data-stu-id="4b198-119">A shortcut to the .searchconnector-ms file is created in the Links folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="4b198-120">快捷方式會出現在 Windows 檔案總管導覽的 [我的最 **愛] 窗格** 中，讓使用者流覽至新的資料存放區，然後查詢 web 服務。</span><span class="sxs-lookup"><span data-stu-id="4b198-120">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store, and query the web service.</span></span>

> [!Note]  
> <span data-ttu-id="4b198-121">當使用者開啟 .osdx 檔案時，您可以將已經有與 Windows 同盟搜尋相容的 [OpenSearch](https://github.com/dewitt/opensearch) web 服務的資料存放區新增至 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="4b198-121">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with Windows Federated Search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="4b198-122">其他資源</span><span class="sxs-lookup"><span data-stu-id="4b198-122">Additional Resources</span></span>

<span data-ttu-id="4b198-123">如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](/previous-versions//dd742958(v=vs.85))的「其他資源」。</span><span class="sxs-lookup"><span data-stu-id="4b198-123">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b198-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b198-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b198-125">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="4b198-125">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="4b198-126">在 Windows 中使用同盟搜尋開始使用</span><span class="sxs-lookup"><span data-stu-id="4b198-126">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="4b198-127">在 Windows 同盟搜尋中啟用資料存放區</span><span class="sxs-lookup"><span data-stu-id="4b198-127">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="4b198-128">在 Windows 同盟搜尋中建立 OpenSearch 描述檔案</span><span class="sxs-lookup"><span data-stu-id="4b198-128">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="4b198-129">遵循 Windows 同盟搜尋的最佳作法</span><span class="sxs-lookup"><span data-stu-id="4b198-129">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="4b198-130">在 Windows 同盟搜尋中部署搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="4b198-130">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
