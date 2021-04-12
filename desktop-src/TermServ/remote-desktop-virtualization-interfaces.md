---
title: 遠端桌面虛擬化介面
description: 遠端桌面虛擬化 API 支援下列介面。
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315739"
---
# <a name="remote-desktop-virtualization-interfaces"></a>遠端桌面虛擬化介面

遠端桌面虛擬化 API 支援下列介面。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**ITsSbBaseNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

公開向遠端桌面連線代理人 (RD 連線代理人) 報告狀態和錯誤訊息的方法。

</dd> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

公開方法和屬性，這些方法和屬性會儲存來自遠端桌面連線 (RDC) 用戶端的連入連線要求的狀態資訊。

</dd> <dt>

[**ITsSbClientConnectionPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

可以用來適當地定義用戶端連接的自訂屬性。

</dd> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

公開方法和屬性，其中包含裝載目的電腦之環境的相關資訊。 此介面可用來儲存裝載虛擬機器之實體伺服器的相關資訊。

</dd> <dt>

[**ITsSbEnvironmentPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

可以用來定義適當的裝載目的電腦之環境的自訂屬性。

</dd> <dt>

[**ITsSbFilterPluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

篩選外掛程式存放區

</dd> <dt>

[**ITsSbGenericNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

公開向 RD 連線代理人報告完成並取得等候時間的方法。

</dd> <dt>

[**ITsSbGlobalStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

公開查詢已新增至 RD 連線代理人存放區之目的電腦、會話、環境和伺服器陣列的方法。

</dd> <dt>

[**ITsSbLoadBalanceResult**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

公開方法和屬性，這些方法和屬性會儲存負載平衡演算法所傳回的目標名稱。

</dd> <dt>

[**ITsSbLoadBalancing**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

公開可用來提供自訂負載平衡演算法的方法。

</dd> <dt>

[**ITsSbLoadBalancingNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

公開方法，以將負載平衡演算法的結果傳回 RD 連線代理人。

</dd> <dt>

[**ITsSbOrchestration**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

公開 RD 連線代理人用來確保在將用戶端重新導向至該目標之前，已備妥目標的方法。

</dd> <dt>

[**ITsSbOrchestrationNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

公開將 [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) 物件傳回 RD 連線代理人的方法，以成功準備連接的目標。

</dd> <dt>

[**ITsSbPlacement**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

公開可在裝載虛擬機器) 的電腦上準備環境 (的方法。

</dd> <dt>

[**ITsSbPlacementNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

公開方法，以傳回 RD 連線代理人環境的相關資訊。

</dd> <dt>

[**ITsSbPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

公開初始化和終止外掛程式的方法。

</dd> <dt>

[**ITsSbPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

公開通知 RD 連線代理人有關外掛程式初始化或終止的方法。

</dd> <dt>

[**ITsSbPluginPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

可以用來定義適當的自訂外掛程式屬性。

</dd> <dt>

[**ITsSbPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

可以用來定義適當的自訂屬性。

</dd> <dt>

[**ITsSbProvider**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

公開方法，以建立遠端桌面虛擬化所使用之物件的預設執行。

</dd> <dt>

[**ITsSbProvisioning**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

公開建立和維護虛擬機器的方法。

</dd> <dt>

[**ITsSbProvisioningPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

公開通知 RD 連線代理人有關布建虛擬機器的方法。

</dd> <dt>

[**ITsSbResourceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

公開 RD 連線代理人用來通知外掛程式發生在會話、目標和用戶端連線物件中之任何狀態變更的方法。

</dd> <dt>

[**ITsSbResourceNotificationEx**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

公開 RD 連線代理人用來通知外掛程式發生在會話、目標和用戶端連線物件中之任何狀態變更的方法。

</dd> <dt>

[**ITsSbResourcePlugin**](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

公開擴充 RD 連線代理人功能的方法。

</dd> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

公開可讓資源外掛程式儲存物件（例如會話和目標）的方法。

</dd> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> <dd>

公開可讓資源外掛程式儲存物件（例如會話和目標）的方法。

</dd> <dt>

[**ITsSbServiceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

公開 RD 連線代理人用來通知外掛程式 RD 連線代理人本身發生之狀態變更的方法。

</dd> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

公開屬性，這些屬性會儲存使用者會話的相關資訊。

</dd> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

公開屬性，這些屬性會儲存目標的設定和狀態資訊。

</dd> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dd>

公開屬性，這些屬性會儲存目標的設定和狀態資訊。

</dd> <dt>

[**ITsSbTargetPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

衍生自這個介面，以定義自訂目標屬性集。

</dd> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

公開遠端桌面連線代理人用來設定外掛程式佇列的屬性。

</dd> <dt>

[**ITsSbTaskPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

公開更新遠端桌面連線代理人外掛程式工作佇列的方法。

</dd> <dt>

[**ITsSbTaskPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

公開方法，以報告有關要 RD 連線代理人之工作的狀態和錯誤訊息。

</dd> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

用來擴充終端機服務會話代理人 (TS 會話代理人) 的功能。 當您想要提供可覆寫 TS 會話代理人重新導向邏輯的外掛程式時，請執行這個介面。

</dd> </dl>

 

 