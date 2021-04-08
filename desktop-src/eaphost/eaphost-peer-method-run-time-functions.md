---
title: EAPHost 對等方法 Run-Time 函式
description: 深入瞭解 EAPHost 對等方法的 API 執行時間函數。 查看函數清單，並查看其他可用的資源。
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfde4adc8d509fcd5d67f9a33bd0617d605716db
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842727"
---
# <a name="eaphost-peer-method-run-time-functions"></a>EAPHost 對等方法 Run-Time 函式

EAP 對等方法 API 執行時間函數如下所示。



| 函式                                                                   | 描述                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | 在對等 EAPHost 上啟動新的驗證會話。                                                                                                                                                                    |
| [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | 終止 EAPHost 與對等之間的目前 EAP 驗證會話。                                                                                                                                               |
| [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | 允許 EAP 方法開發人員提供方法所支援的各種連接屬性和使用者屬性。 EAPHost 會叫用此函式，以建立 EAP 方法的連接屬性和使用者屬性。 |
| [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | 取得正在呼叫之 EAP 方法的身分識別。                                                                                                                                                                    |
| [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | 取得一組函式指標，以便執行載入的 EAP 對等方法。                                                                                                                                     |
| [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | 從 EAP 方法取得 EAP 屬性的陣列。                                                                                                                                                                     |
| [**EapPeerGetResponsePacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | 從 EAP 方法取得回應封包。                                                                                                                                                                              |
| [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | 從 EAP 方法取得驗證會話的結果。                                                                                                                                                        |
| [**EapPeerGetUICoNtext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | 從 EAP 方法取得使用者介面內容。                                                                                                                                                                     |
| [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | 初始化對等方法的 EAPHost。                                                                                                                                                                                    |
| [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | 處理 EAPHost 從要求者收到的封包。                                                                                                                                                                   |
| [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | 提供新的或更新的使用者認證給 EAP 方法。                                                                                                                                                                 |
| [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | 提供 eap 屬性的更新陣列給 EAP 方法。                                                                                                                                                              |
| [**EapPeerSetUICoNtext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | 提供使用者介面內容給 EAP 方法。                                                                                                                                                                        |
| [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | 關閉 EAP 方法，並準備卸載其對應的 DLL。                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 對等方法設定函數](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




