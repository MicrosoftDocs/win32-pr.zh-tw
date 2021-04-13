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
# <a name="deploying-search-connectors-in-windows-federated-search"></a>在 Windows 同盟搜尋中部署搜尋連接器

本主題說明如何藉由開啟 ( .osdx) 檔中的 OpenSearch 描述、如何部署 .osdx 檔案，以及如何追蹤您的 [opensearch](https://github.com/dewitt/opensearch) 服務使用方式，來向同盟搜尋註冊新的遠端資料存放區。

本主題的組織方式如下：

-   [Searchconnector-ms (Search Connector) File](#the-searchconnector-ms-search-connector-file)
-   [部署方法](#deployment-methods)
    -   [提取部署](#pull-deployment)
    -   [推送部署](#push-deployment)
-   [追蹤使用量](#tracking-usage)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>Searchconnector-ms (Search Connector) File

只要開啟 .osdx 檔案，以描述如何連線至 web 服務，以及如何對應 RSS 或 Atom XML 中的任何自訂元素，就會使用同盟搜尋來註冊新的遠端資料存放區。 當使用者開啟 .osdx 檔案時，您可以將已經有與同盟搜尋相容的 [OpenSearch](https://github.com/dewitt/opensearch) web 服務的資料存放區新增至 Windows 檔案總管。

當您將 .osdx 給使用者，且使用者開啟 .osdx 檔案之後，就會發生下列事件。

1.  Searchconnector-ms 檔案會建立在 **Windows 搜尋** 資料夾 (% userprofile%/Searches) 。
2.  Searchconnector-ms 檔案的快捷方式建立于 **連結** 資料夾 (% userprofile%/Links) 。
3.  快捷方式會出現在 Windows 檔案總管導覽的 [我的最 **愛] 窗格** 中，讓使用者流覽至新的資料存放區，並查詢 web 服務。

## <a name="deployment-methods"></a>部署方法

有兩種方式可以部署搜尋連接器、提取部署和推送部署。

### <a name="pull-deployment"></a>提取部署

提取部署描述任何類型的部署，使用者可在其中使用此計畫來安裝搜尋連接器。 提取部署的一般方法如下：

-   將 .osdx 檔案附加至電子郵件。
-   將檔案張貼在網頁上。
-   在內部網路網站上提供動態連結;例如，根據使用者選擇或網站內目前的範圍產生自訂 .osdx 檔案。

如果是使用者在瀏覽器中按一下連結時所要下載的檔案，則必須將裝載 web 服務的 web 伺服器設定為以檔案形式傳遞 .osdx。 因此，您必須設定網頁伺服器上的 MIME 類型，將 .osdx 檔案視為 `"application/opensearchdescription+xml"` 。 （選擇性）您可以使用 Microsoft 提供的圖示來識別搜尋連接器連結。

### <a name="push-deployment"></a>推送部署

推送部署描述任何不依賴使用者計畫來安裝搜尋連接器的部署類型。 推送部署的一般方法如下：

-   群組原則喜好設定 (GPP) 
-   登入指令檔
-   漫遊設定檔
-   建立映像

## <a name="tracking-usage"></a>追蹤使用量

若要在使用者從 Windows 檔案總管中搜尋時，追蹤您的 [OpenSearch](https://github.com/dewitt/opensearch) 服務使用量，請篩選您的 web 伺服器記錄檔，以取得這個使用者代理程式字串： `Windows-Search+(Windows+NT+6.1)` 。

## <a name="additional-resources"></a>其他資源

如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](/previous-versions//dd742958(v=vs.85))的「其他資源」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 中的同盟搜尋](-search-federated-search-overview.md)
</dt> <dt>

[在 Windows 中使用同盟搜尋開始使用](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[在 Windows 同盟搜尋中連接您的 web 服務](-search-federated-search-web-service.md)
</dt> <dt>

[在 Windows 同盟搜尋中啟用資料存放區](-search-federated-search-data-store.md)
</dt> <dt>

[在 Windows 同盟搜尋中建立 OpenSearch 描述檔案](-search-federated-search-osdx-file.md)
</dt> <dt>

[遵循 Windows 同盟搜尋的最佳作法](-search-fedsearch-best.md)
</dt> </dl>

 

 
