---
title: IRemoteDesktopClientEvents 介面
description: 提供從伺服器接收用戶端控制項事件相關資訊的方法。
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- IRemoteDesktopClientEvents 介面遠端桌面服務
- IRemoteDesktopClientEvents 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025099"
---
# <a name="iremotedesktopclientevents-interface"></a>IRemoteDesktopClientEvents 介面

提供從伺服器接收用戶端控制項事件相關資訊的方法。 事件包括連線和中斷連接、全螢幕模式要求、成功登入，以及錯誤狀況。

## <a name="members"></a>成員

**IRemoteDesktopClientEvents** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IRemoteDesktopClientEvents** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IRemoteDesktopClientEvents** 介面具有這些方法。



| 方法                                                                                      | 描述                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | 當用戶端控制項收到系統管理訊息時呼叫。 <br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | 當用戶端控制項自動重新連接到遠端會話時呼叫。 <br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | 當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。 <br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | 當用戶端控制項已連線到遠端會話時呼叫。<br/>                                                                                        |
| [**OnConnecting**](iremotedesktopclientevents-onconnecting.md)                             | 當用戶端控制項嘗試建立遠端會話的連接時呼叫。 <br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | 在用戶端控制項顯示的對話方塊關閉之後呼叫。 <br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | 在控制項顯示對話方塊之前呼叫。 <br/>                                                                                                        |
| [**OnDisconnected**](iremotedesktopclientevents-ondisconnected.md)                         | 當用戶端控制項與遠端會話中斷連接時呼叫。 <br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | 在遠端會話中按下特殊按鍵組合時呼叫。 <br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | 當用戶端控制項成功登入遠端會話時呼叫。 <br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | 在網路狀態變更時呼叫。 <br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | 當遠端桌面大小變更時呼叫。 <br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | 當用戶端控制項更新其狀態時呼叫。 <br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | 當觸控指標游標已移動，且 [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) 屬性設定為 true 時呼叫。 <br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                           |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                 |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient 定義為 EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/>       |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面 ActiveX 控制項參考](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

