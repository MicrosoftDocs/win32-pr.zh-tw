---
title: EAPHost 要求者 Run-Time 函式
description: 瞭解 EAPHost 要求者執行時間函數，例如 EapHostPeerBeginSession 和 EapHostPeerGetResult。
ms.assetid: b1c473ba-9a12-4929-b4d0-27262117e9c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97481347535de03cb1d3c04f341f382c270f0ae89482060e9952c38cfbdc5b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785326"
---
# <a name="eaphost-supplicant-run-time-functions"></a>EAPHost 要求者 Run-Time 函式

EAP 要求者 API 執行時間函數如下所示。



| 函式                                                                     | 描述                                                                                                                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                   | 啟動 EAP 驗證會話。                                                                                                                                                                                |
| [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection)             | 停止對呼叫要求者所提供之 [**NotificationHandler**](/previous-versions/windows/desktop/api) 的所有未來回呼，以在先前的 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)呼叫中 EAPHost。 |
| [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)                       | 終止 EAPHost 與呼叫要求者之間的目前 EAP 驗證會話。                                                                                                                          |
| [**EapHostPeerFreeEapError**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror)                   | 釋放 EAPHost Api 所傳回的所有 EAP 錯誤特定記憶體。                                                                                                                                                        |
| [**EapHostFreeRuntimeMemory**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory)                    | 釋放執行時間 Api 所使用的記憶體空間。                                                                                                                                                                         |
| [**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)                 | 從 EAPHost 取得要求者目前的 EAP 驗證狀態。                                                                                                                                             |
| [**EapHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity)                     | 從內部方法要求身分識別資訊。                                                                                                                                                                |
| [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) | 從 EAPHost 取得 EAP 驗證屬性的陣列。                                                                                                                                                      |
| [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)                         | 取得指定 EAP 驗證會話的驗證結果。                                                                                                                                      |
| [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket)                 | 從 EAPHost 取得要傳送給驗證器的封包。                                                                                                                                                          |
| [**EapHostPeerGetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)                   | 針對要求者的 [**EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) api 中所使用的 EAPHost，取得要求者的使用者介面內容。                             |
| [**EapHostPeerInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize)                       | 初始化要求者的 EAPHost。 [**EapHostInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) 和 [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) 必須以成對的方式呼叫。                                      |
| [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) | 從伺服器收到 EAP 封包之後，將 EAP 封包傳送至 EAPHost。                                                                                                                             |
| [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) | 提供更新的 EAP 驗證屬性給 EAPHost。                                                                                                                                                           |
| [**EapHostPeerSetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext)                   | 提供新的或更新的使用者介面內容給 EAPHost 上載入的 EAP 對等方法。                                                                                                                           |
| [**EapHostPeerUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize)                   | Unitializes 要求者的 EapHost。 [**EapHostInitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) 和 [**EapHostUninitialize**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) 必須以成對的方式呼叫。                                      |



 

 

 




