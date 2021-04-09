---
title: WDS 傳輸提供者函式
description: 使用者定義內容提供者可以將下列回呼函數公開給多播伺服器。
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675436"
---
# <a name="wds-transport-provider-functions"></a>WDS 傳輸提供者函式

使用者定義內容提供者可以將下列回呼函數公開給多播伺服器。



| 函式                                                                               | 描述                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [*WdsTransportProviderCloseContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | 關閉控制碼所指定的內容資料流程。                                                                          |
| [*WdsTransportProviderCloseInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | 關閉由控制碼所指定之內容提供者的實例。                                                         |
| [*WdsTransportProviderCompareContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | 將指定的內容名稱和實例與開啟的內容資料流程進行比較，以判斷它們是否相同。             |
| [*WdsTransportProviderCreateInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | 開啟內容提供者的新實例。                                                                             |
| [*WdsTransportProviderDumpState*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | 指示傳輸提供者將其狀態的摘要以及任何其他相關資訊列印到追蹤記錄檔。 |
| [*WdsTransportProviderGetContentMetadata*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | 抓取開啟內容資料流程的中繼資料。                                                                          |
| [*WdsTransportProviderGetContentSize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | 抓取開啟內容資料流程的大小。                                                                           |
| [*WdsTransportProviderInitialize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | 初始化內容提供者。                                                                                         |
| [*WdsTransportProviderOpenContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | 開啟內容資料流程的新靜態視圖。                                                                            |
| [*WdsTransportProviderReadContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | 從開啟的內容資料流程讀取內容。                                                                              |
| [*WdsTransportProviderRefreshSettings*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | 指示傳輸提供者重新讀取任何相關的設定。                                                       |
| [*WdsTransportProviderShutdown*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | Shutsdown 內容提供者。                                                                                         |
| [*WdsTransportProviderUserAccessCheck*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | 根據使用者的權杖，指定內容資料流程的存取權。                                                           |



 

 

 




