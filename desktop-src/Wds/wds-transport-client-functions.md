---
title: WDS 傳輸用戶端函式
description: 此模組會定義在內容接收器與傳輸用戶端之間組成介面的結構和函式。
ms.assetid: 20c3116b-3a0d-4048-b6f2-81c03e0a80ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8449f620eb04045d37e56499be998477d361871c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969478"
---
# <a name="wds-transport-client-functions"></a>WDS 傳輸用戶端函式

此模組會定義在內容接收器與傳輸用戶端之間組成介面的結構和函式。



| 函式                                                                              | 描述                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ WdsTransportClientReceiveContents*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents) | 表示已準備好要使用的資料區塊。                                                                                                                         |
| [*PFN \_ WdsTransportClientReceiveMetadata*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivemetadata) | 接收有關檔案的中繼資料資訊。                                                                                                                                 |
| [*PFN \_ WdsTransportClientSessionComplete*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete) | 指出會話已順利完成或發生錯誤。                                                                                                  |
| [*PFN \_ WdsTransportClientSessionStart*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstart)       | 指出檔案的檔案大小和其他伺服器端資訊給取用者。                                                                                   |
| [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex)   | 指出檔案的檔案大小和其他伺服器端資訊給取用者。                                                                                   |
| [**WdsTransportClientAddRefBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientaddrefbuffer)              | 遞增多播用戶端所擁有的緩衝區上的參考計數。                                                                                                   |
| [**WdsTransportClientCancelSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcancelsession)            | 釋放與用戶端中的會話相關聯的資源。                                                                                                             |
| [**WdsTransportClientCloseSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientclosesession)              | 釋放與用戶端中的會話相關聯的資源。                                                                                                             |
| [**WdsTransportClientCompleteReceive**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcompletereceive)        | 指出資料區塊上的所有處理都已完成，而且多播用戶端可能會從其快取中移除此資料區塊，以騰出空間供進一步接收。 |
| [**WdsTransportClientInitialize**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitialize)                  | 初始化多播用戶端。                                                                                                                                           |
| [**WdsTransportClientInitializeSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitializesession)    | 起始多播檔案傳輸。                                                                                                                                        |
| [**WdsTransportClientQueryStatus**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientquerystatus)                | 從多播用戶端抓取進行中或完整多播傳輸的目前狀態。                                                                    |
| [**WdsTransportClientRegisterCallback**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientregistercallback)      | 向多播用戶端註冊回呼。                                                                                                                             |
| [**WdsTransportClientReleaseBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientreleasebuffer)            | 遞減多播用戶端所擁有的緩衝區上的參考計數。                                                                                                   |
| [**WdsTransportClientShutdown**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientshutdown)                      | 關閉多播用戶端。                                                                                                                                            |
| [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)              | 起始多播檔案傳輸。                                                                                                                                        |
| [**WdsTransportClientWaitForCompletion**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientwaitforcompletion)    | 封鎖直到多播會話完成或達到指定的超時時間。                                                                                  |



 

 

 




