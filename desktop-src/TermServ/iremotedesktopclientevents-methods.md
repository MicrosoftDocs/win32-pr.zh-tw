---
title: IRemoteDesktopClientEvents 方法
description: IRemoteDesktopClientEvents 介面會公開下列方法。
ms.assetid: D8035924-736D-495D-BF78-950DAEB69774
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85a3c5df2f8a083e8fe41da53035f4de43b58e5ef1e7948dee8e93f617e17bdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124998"
---
# <a name="iremotedesktopclientevents-methods"></a>IRemoteDesktopClientEvents 方法

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)介面會公開下列方法。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**OnConnecting 方法**](iremotedesktopclientevents-onconnecting.md)
</dt> <dd>

當用戶端控制項嘗試建立遠端會話的連接時呼叫。

</dd> <dt>

[**OnConnected 方法**](iremotedesktopclientevents-onconnected.md)
</dt> <dd>

當用戶端控制項已連線到遠端會話時呼叫。

</dd> <dt>

[**OnLoginCompleted 方法**](iremotedesktopclientevents-onlogincompleted.md)
</dt> <dd>

當用戶端控制項成功登入遠端會話時呼叫。

</dd> <dt>

[**OnDisconnected 方法**](iremotedesktopclientevents-ondisconnected.md)
</dt> <dd>

當用戶端控制項與遠端會話中斷連接時呼叫。

</dd> <dt>

[**OnStatusChanged 方法**](iremotedesktopclientevents-onstatuschanged.md)
</dt> <dd>

當用戶端控制項更新其狀態時呼叫。

</dd> <dt>

[**OnAutoReconnecting 方法**](iremotedesktopclientevents-onautoreconnecting.md)
</dt> <dd>

當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。

</dd> <dt>

[**OnAutoReconnected 方法**](iremotedesktopclientevents-onautoreconnected.md)
</dt> <dd>

當用戶端控制項自動重新連接到遠端會話時呼叫。

</dd> <dt>

[**OnDialogDisplaying 方法**](iremotedesktopclientevents-ondialogdisplaying.md)
</dt> <dd>

在控制項顯示對話方塊之前呼叫。

</dd> <dt>

[**OnDialogDismissed 方法**](iremotedesktopclientevents-ondialogdismissed.md)
</dt> <dd>

在用戶端控制項顯示的對話方塊關閉之後呼叫。

</dd> <dt>

[**OnNetworkStatusChanged 方法**](iremotedesktopclientevents-onnetworkstatuschanged.md)
</dt> <dd>

在網路狀態變更時呼叫。

</dd> <dt>

[**OnAdminMessageReceived 方法**](iremotedesktopclientevents-onadminmessagereceived.md)
</dt> <dd>

當用戶端控制項收到系統管理訊息時呼叫。

</dd> <dt>

[**OnKeyCombinationPressed 方法**](iremotedesktopclientevents-onkeycombinationpressed.md)
</dt> <dd>

在遠端會話中按下特殊按鍵組合時呼叫。

</dd> <dt>

[**OnRemoteDesktopSizeChanged 方法**](iremotedesktopclientevents-onremotedesktopsizechanged.md)
</dt> <dd>

當遠端桌面大小變更時呼叫。

</dd> <dt>

[**OnTouchPointerCursorMoved 方法**](iremotedesktopclientevents-ontouchpointercursormoved.md)
</dt> <dd>

當觸控指標游標已移動，且 [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) 屬性設定為 true 時呼叫。

</dd> </dl>

 

 