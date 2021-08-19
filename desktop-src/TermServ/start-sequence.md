---
title: 開始順序
description: 啟動自訂通訊協定的步驟。
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29dbb899905dd96e806ffe17a0eafd0091ad97b547ba9f172527ab0acc1b2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000540"
---
# <a name="start-sequence"></a>開始順序

若要啟動您的通訊協定提供者，遠端桌面服務服務：

-   從登錄中取出接聽程式的名稱和通訊協定管理員物件的 CLSID ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) 。 如需詳細資訊，請參閱 [註冊通訊協定管理員](registering-the-custom-protocol.md)。
-   呼叫 [**initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) 以初始化通訊協定管理員。
-   使用 CLSID 建立通訊協定管理員物件。 即使有多個接聽程式已為相同的通訊協定提供者註冊，服務還是只會建立一個通訊協定管理員物件。
-   呼叫 [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) 來指示通訊協定管理員物件建立 [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) 接聽程式物件，並將它傳回至服務。 通訊協定管理員物件必須先加入接聽程式物件的參考，才能將它傳回至服務。 當服務停止或刪除接聽程式時，服務會釋放物件。
-   在接聽程式物件上呼叫 [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) ，讓接聽程式可以開始接聽傳入連接。
-   呼叫 [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) 以停止接聽程式物件。
-   呼叫解除 [**初始化**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) 以將通訊協定管理員解除初始化。

當用戶端嘗試連接時，接聽程式會建立 [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) 物件。 接聽程式物件會呼叫 [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) 來通知遠端桌面服務服務，新的用戶端嘗試連線或重新連線，並在該呼叫中傳遞 **IWRdsProtocolConnection** 物件。 遠端桌面服務服務會接著傳回該呼叫中的 [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) 物件，讓通訊協定可以視需要與遠端桌面服務服務進行通訊。 服務會在傳回之前加入回呼物件的參考，而且當連接關閉時，通訊協定必須釋放該參考。

下圖顯示啟動期間各種物件之間的互動。

![rcm 開始順序](images/protocol-startsequence.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[方法呼叫順序](method-call-sequence.md)
</dt> <dt>

[連接順序](connection-sequence.md)
</dt> </dl>

 

 




