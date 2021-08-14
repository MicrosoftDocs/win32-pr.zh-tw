---
title: NLM 介面
description: NLM 介面
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07751a3f28c713b699cf60aa391d7141b19db0fcafd3ef13437f951c944dcb04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798505"
---
# <a name="nlm-interfaces"></a>NLM 介面

以下是 NLM 介面。

| 介面                                                            | 描述                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumNetworkConnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | 提供網路連接的標準枚舉器。 它會列舉網路內的作用中、已中斷連接或所有網路連線。 這個介面可以從 [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) 介面取得。 |
| [**IEnumNetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | 列舉伺服器上所有可用的網路。 這個介面可以從 [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) 介面取得。                                                                                         |
| [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | 表示伺服器上的網路。 它也可以代表具有類似網路簽章的網路連接集合。                                                                                          |
| [**INetworkConnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | 代表單一網路連接。                                                                                                                                                                                  |
| [**INetworkConnectionCost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | 用來查詢目前的網路成本和與連接相關聯的資料方案狀態。                                                                                                                                    |
| [**INetworkConnectionCostEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | 用來通知應用程式的成本和通話方案狀態變更事件的連接。                                                                                                                               |
| [**INetworkConnectionEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | 用戶端所執行的接收介面，用來接收與網路連接相關的事件。 對於較細微層級事件（例如驗證變更）有興趣的應用程式，請執行此介面。       |
| [**INetworkCostManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | 用來查詢與用於全電腦網際網路連線的連線相關聯的全電腦成本和通話方案狀態資訊，或連接時路由至特定目的地的第一躍點。 |
| [**INetworkCostManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | 用來通知應用程式有全電腦成本和通話方案相關事件。                                                                                                                                         |
| [**INetworkEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | 用戶端用來接收網路相關事件的接收介面。 這些 Api 是在引發個別事件時自動呼叫的所有回呼函數。                                  |
| [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | 提供一組方法來執行網路清單管理功能。                                                                                                                                                  |
| [**INetworkListManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | 用戶端所執行的接收介面，用來接收與網路清單管理員相關的事件。 對更細微層級事件（例如網際網路連線能力）有興趣的應用程式，可執行介面。   |



 

 

 




