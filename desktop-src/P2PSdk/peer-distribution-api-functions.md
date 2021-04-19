---
description: Microsoft 對等散發服務支援取用者角色和發行者角色案例的功能。
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: 對等散發 API 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2532ad8bf5cbb14e18bd16a14bb1be2d79c1791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000282"
---
# <a name="peer-distribution-api-functions"></a>對等散發 API 函數

Microsoft 對等散發服務支援取用者角色和發行者角色案例的功能。

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>下列函式在「用戶端」和「伺服器」案例中都很常見。



| 一般函數                                                                                       | Description                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | 建立新的 **PEERDIST \_ 實例 \_ 控制碼** 實例，必須傳遞給所有其他對等散發 api。 |
| [**PeerDistShutdown**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | 釋放呼叫 [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)所配置的資源。                         |
| [**PeerDistGetStatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | 傳回對等散發服務的目前狀態。                                                        |
| [**PeerDistGetStatusEx**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | 傳回對等散發服務的目前狀態和功能。                                   |
| [**PeerDistGetOverlappedResult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | 捕獲非同步作業的結果。                                                               |
| [**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | 要求對等散發服務在狀態變更發生時通知呼叫者。                      |
| [**PeerDistRegisterForStatusChangeNotificationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | 要求對等散發服務在狀態變更發生時通知呼叫者。                      |
| [**PeerDistUnregisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | 取消註冊與所提供控制碼相關聯之會話的狀態變更通知。                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>只有在「用戶端」案例中才支援下列函數。



| 用戶端函數                                                                             | Description                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | 開啟並傳回要參考該內容的 **PEERDIST \_ 內容 \_ 控制碼** 。                                                                                                                                                                                                                                                                     |
| [**PeerDistClientCloseContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | 關閉 **PEERDIST \_ 內容 \_ 控制碼**。                                                                                                                                                                                                                                                                                                        |
| [**PeerDistClientGetInformationByHandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | 從對等散發服務取得特定內容控制碼的其他資訊。                                                                                                                                                                                                                                               |
| [**PeerDistClientAddContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | 新增與 **PEERDIST \_ 內容 \_ 控制碼** 相關聯的內容資訊。 可與任何內容資訊相關聯的 **PEERDIST \_ 內容 \_ 控制碼** 。                                                                                                                                                                        |
| [**PeerDistClientCompleteContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | 指出內容資訊的結尾。                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientAddData**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | 用來將內容提供給本機快取。 這通常會在本機網路上找不到資料時完成，如 [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) 或 [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) 完成時所示，但 **發生錯誤 \_ 超時** 或錯誤的 **\_ \_ \_ 資料遺失**。 |
| [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | 提供內容資料流程的隨機存取。                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | 提供內容資料流程的順序存取。                                                                                                                                                                                                                                                                                                |
| [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | 移除先前已新增至本機對等散發系統的內容。                                                                                                                                                                                                                                                            |
| [**PeerDistClientCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | 取消與重 [迭結構相關](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 聯的非同步作業，以及 [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)所傳回的內容控制碼。                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>只有在「伺服器」案例中才支援下列函數。



| 伺服器函數                                                                             | Description                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | 建立可與 [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)搭配使用的 **PEERDIST \_ 資料流程 \_ 控制碼**，以建立內容資料流程的內容資訊。 |
| [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | 將資料加入至由 PeerDist 資料流程控制碼所參考的資料流程。                                                                                                                                  |
| [**PeerDistServerPublishCompleteStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | 呼叫以表示所有資料都已新增至資料流程。                                                                                                                                     |
| [**PeerDistServerCloseStreamHandle**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | 關閉資料流程控制碼。                                                                                                                                                                          |
| [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Unpublishes 對等散發服務中先前發行的內容。                                                                                                                         |
| [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | 開啟已發佈內容的 **PEERDIST \_ CONTENTINFO \_ 控制碼** 。                                                                                                                                   |
| [**PeerDistServerOpenContentInformationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | 開啟已發佈內容的 **PEERDIST \_ CONTENTINFO \_ 控制碼** 。                                                                                                                                   |
| [**PeerDistServerRetrieveContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | 抓取與已發佈內容相關聯的內容資訊。                                                                                                                               |
| [**PeerDistServerCloseContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **PEERDIST \_PeerDistServerOpenContentInformation 開啟的 CONTENTINFO \_ 控制碼**。 [](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)                                                                  |
| [**PeerDistServerCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | 取消與內容 [識別碼和重](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 迭結構相關聯的非同步作業。                                             |



 

 

 
