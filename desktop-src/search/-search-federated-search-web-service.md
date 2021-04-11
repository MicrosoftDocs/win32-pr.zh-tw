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
# <a name="connecting-your-web-service-in-windows-federated-search"></a>在 Windows 同盟搜尋中連接您的 Web 服務

本主題說明在資料存放區與 Windows 同盟搜尋之間連接 web 服務，以及如何在 RSS 或 Atom 中傳送查詢和傳回搜尋結果所牽涉到的步驟。

本主題的組織方式如下：

-   [連接您的 web 服務](#connect-your-web-service)
-   [註冊現有的遠端資料存放區](#register-an-existing-remote-data-store)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="connect-your-web-service"></a>連接您的 web 服務

**若要將資料存放區的 web 服務連接到同盟搜尋，請執行下列步驟：**

1.  建立 .osdx 檔案。
2.  將 .osdx 檔案提供給使用者，讓他們可以開啟 .osdx 檔案，依需求新增服務。
3.  產生搜尋連接器，並在您的企業中主動加以部署。

## <a name="register-an-existing-remote-data-store"></a>註冊現有的遠端資料存放區

使用者藉由開啟 ( .osdx) 檔案中的 [OpenSearch 描述]，向 Windows 同盟搜尋註冊新的遠端資料存放區。 當使用者這樣做時，會發生下列事件：

1.  Searchconnector-ms 檔案 (搜尋連接器) 會建立在 Windows 搜尋資料夾 (% userprofile%/Searches) 。
2.  Searchconnector-ms 檔案的快捷方式建立于連結資料夾 (% userprofile%/Links) 。
3.  快捷方式會出現在 Windows 檔案總管導覽的 [我的最 **愛] 窗格** 中，讓使用者流覽至新的資料存放區，然後查詢 web 服務。

> [!Note]  
> 當使用者開啟 .osdx 檔案時，您可以將已經有與 Windows 同盟搜尋相容的 [OpenSearch](https://github.com/dewitt/opensearch) web 服務的資料存放區新增至 Windows 檔案總管。

 

## <a name="additional-resources"></a>其他資源

如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](/previous-versions//dd742958(v=vs.85))的「其他資源」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 中的同盟搜尋](-search-federated-search-overview.md)
</dt> <dt>

[在 Windows 中使用同盟搜尋開始使用](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[在 Windows 同盟搜尋中啟用資料存放區](-search-federated-search-data-store.md)
</dt> <dt>

[在 Windows 同盟搜尋中建立 OpenSearch 描述檔案](-search-federated-search-osdx-file.md)
</dt> <dt>

[遵循 Windows 同盟搜尋的最佳作法](-search-fedsearch-best.md)
</dt> <dt>

[在 Windows 同盟搜尋中部署搜尋連接器](-search-federated-search-deploying.md)
</dt> </dl>

 

 
