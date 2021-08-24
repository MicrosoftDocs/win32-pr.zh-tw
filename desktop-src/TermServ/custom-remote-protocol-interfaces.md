---
title: 遠端桌面通訊協定提供者介面
description: 遠端桌面通訊協定提供者 API 所支援的介面。
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bde36cb70f937559dce20a73a485ec109a2cf6c6ae6c687655963c70e6ce22b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681228"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>遠端桌面通訊協定提供者介面

遠端桌面通訊協定提供者 API 支援下列介面。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

公開遠端桌面服務服務所呼叫的方法，以設定用戶端連接。

</dd> <dt>

[**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

公開方法，這些方法會提供用戶端連接狀態的相關資訊，以及針對用戶端執行動作的資訊。 此介面是由遠端桌面服務服務所執行，並由通訊協定呼叫。

</dd> <dt>

[**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

公開遠端桌面服務服務用來在連接順序期間執行授權交握的方法。

</dd> <dt>

[**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

公開方法，要求通訊協定開始和停止接聽用戶端連接要求。

</dd> <dt>

[**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

公開方法，以通知用戶端已連線的遠端桌面服務服務。

</dd> <dt>

[**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

公開遠端桌面服務服務所呼叫的方法，以更新登入狀態，並決定如何指示登入錯誤訊息。

</dd> <dt>

[**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

公開遠端桌面服務服務用來與通訊協定提供者進行通訊的方法。

</dd> <dt>

[**IWRdsProtocolSettings**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

公開用來取得和新增原則相關設定的方法。

</dd> <dt>

[**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

公開由通訊協定呼叫的方法，以通知遠端桌面服務服務啟動或停止陰影的目標端。

</dd> <dt>

[**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

公開通知通訊協定提供者有關會話遮蔽狀態的方法。

</dd> <dt>

[**IWRdsRemoteFXGraphicsConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

公開與用戶端連接上的圖形操作相關的方法。

</dd> <dt>

[已淘汰的桌面通訊協定提供者介面](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

下列介面已被取代，不應該再使用。 針對新的專案，請改用遠端桌面通訊協定提供者介面介面。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[遠端桌面通訊協定提供者參考](custom-remote-protocol-reference.md)
</dt> <dt>

[遠端桌面通訊協定提供者列舉](custom-remote-protocol-enumerations.md)
</dt> <dt>

[遠端桌面通訊協定提供者結構](custom-remote-protocol-structures.md)
</dt> <dt>

[遠端桌面通訊協定提供者聯集](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




