---
description: 對等
ms.assetid: a85fe46c-ce5f-4978-aa37-a3666560426b
title: 對等
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c51f80d4013a7096d5ee4205d988ff96e736fb8fec720b4ba8b69d476ae3abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034304"
---
# <a name="peer-to-peer"></a>對等

## <a name="purpose"></a>目的

對等技術是用來協助跨分散式網路進行即時通訊和協同作業。

在對等模型中，如果沒有使用網際網路伺服器，每位電腦使用者都可以執行下列動作：

-   Exchange 資料
-   共用資源
-   尋找其他使用者
-   通訊
-   即時共同作業

藉由使用點對點技術，協調電腦 CPU 週期和存放裝置使用的應用程式，可以在連線到網際網路的小型或大型電腦群組之間共用資源。

## <a name="where-applicable"></a>適用時

開發人員可以使用對等基礎結構來建立各式各樣的分散式、臨機操作和點對點應用程式。

## <a name="developer-audience"></a>開發人員對象

使用對等基礎結構的開發人員應該熟悉 C 程式設計概念。 使用 PNRP Winsock 命名空間提供者的開發人員應該熟悉 Winsock API。

## <a name="run-time-requirements"></a>執行階段需求求

Windows Vista、Windows xp （含 service pack 2） (SP2) 和更新版本，以及適用于 Windows xp service pack 1 Windows SP1 (的 Advanced 網路套件，都支援對等基礎結構。 對等基礎結構需要安裝並起始 IPv6，才能讓對等網路應用程式運作。 只有 Windows Vista 才支援使用對等共同作業。

## <a name="in-this-section"></a>本節內容



| 主題                                                     | 描述                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [對等基礎結構](peer-infrastructure.md)<br/> | 對等基礎結構和對等名稱解析通訊協定的相關資訊 (PNRP) 。 <br/> |
| [對等共同作業](peer-collaboration.md)<br/>   | 對等共同作業 API 特定的資訊和參考資料。<br/>               |
| [對等分佈](peer-distribution.md)<br/>     | 對等散發 API 的特定資訊和參考資料。<br/>                |



 

## <a name="additional-resources"></a>其他資源

您可以在下列位置找到有關點對點技術的進一步資訊：

| 主題                                                                                                          | 描述                                                                                                               |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Windows對等網路資源](https://www.microsoft.com/p2p)                       | 存取已發佈的白皮書、範例和簡報，詳述對等網路技術。<br/> |
| [Microsoft 對等網路的 Blog](/archive/blogs/p2p/)                          | 閱讀來自 Microsoft 對等網路團隊的最新 blog 專案。<br/>                                 |
| [MSDN 對等網路論壇](https://social.msdn.microsoft.com/forums/peertopeer/threads/)                              | 討論對等技術，並與其他開發人員共同作業。<br/>                                    |
| [適用于 IT 專業人員的 TechNet 對等網路資源](https://technet.microsoft.com/library/bb742623.aspx) | 概念對等網路總覽，以及 IT Professional 角色特有的指引。 <br/>  |



 

 

