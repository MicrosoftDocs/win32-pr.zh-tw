---
title: RemoteDesktopClient 類別
description: 會執行 Microsoft Windows Store 應用程式的遠端桌面用戶端控制-第1版。
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- RemoteDesktopClient 類別遠端桌面服務
- RemoteDesktopClient 類別遠端桌面服務，說明
topic_type:
- apiref
api_name:
- RemoteDesktopClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb10b23f52f53e2d89fd5a81449818a8fe374116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934110"
---
# <a name="remotedesktopclient-class"></a>RemoteDesktopClient 類別

實行 Microsoft Windows Store 應用程式遠端桌面用戶端控制-第1版

這個類別會執行下列介面。

-   [**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)

**RemoteDesktopClient** 具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**RemoteDesktopClient** 類別有這些方法。



| 方法                                                                                      | 描述                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | 將事件處理常式附加至事件。<br/>                                                                                                                  |
| [**連接**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | 使用目前在遠端桌面通訊協定 (RDP) 應用程式容器用戶端控制上設定的屬性來起始連線。<br/>                         |
| [**DeleteSavedCredentials**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | 刪除指定遠端電腦的已儲存認證。<br/>                                                                                            |
| [**Vemap.detachevent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | 從事件卸離事件處理常式。<br/>                                                                                                                |
| [**中斷連線**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | 中斷使用中連接。<br/>                                                                                                                      |
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | 當用戶端控制項收到系統管理訊息時呼叫。<br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | 當用戶端控制項自動重新連接到遠端會話時呼叫。<br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | 當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。<br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | 當用戶端控制項已連線到遠端會話時呼叫。<br/>                                                                                       |
| [**OnConnecting**](iremotedesktopclientevents-onconnecting.md)                             | 當用戶端控制項嘗試建立遠端會話的連接時呼叫。<br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | 在用戶端控制項顯示的對話方塊關閉之後呼叫。<br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | 在控制項顯示對話方塊之前呼叫。<br/>                                                                                                        |
| [**OnDisconnected**](iremotedesktopclientevents-ondisconnected.md)                         | 當用戶端控制項與遠端會話中斷連接時呼叫。<br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | 在遠端會話中按下特殊按鍵組合時呼叫。<br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | 當用戶端控制項成功登入遠端會話時呼叫。<br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | 在網路狀態變更時呼叫。<br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | 當遠端桌面大小變更時呼叫。<br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | 當用戶端控制項更新其狀態時呼叫。<br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | 當觸控指標游標已移動，且 [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) 屬性設定為 true 時呼叫。<br/> |
| [**重新連接**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | 起始自動重新連線遠端桌面通訊協定 (RDP) 應用程式容器用戶端控制項，以將會話納入新的寬度和高度。<br/>   |
| [**UpdateSessionDisplaySettings**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | 更新遠端桌面通訊協定 (RDP) 應用程式容器用戶端控制的寬度和高度設定。<br/>                                               |



 

### <a name="properties"></a>屬性

**RemoteDesktopClient** 類別具有這些屬性。



| 屬性                                                             | 存取類型          | Description                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**行動**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | 唯讀<br/> | 抓取遠端桌面通訊協定 (RDP) 應用程式容器用戶端的動作物件。<br/>                                                                    |
| [**設定**](iremotedesktopclient-settings.md)<br/>         | 唯讀<br/> | 抓取遠端桌面通訊協定 (RDP) 應用程式容器用戶端的設定物件。<br/>                                                                   |
| [**TouchPointer**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | 唯讀<br/> | 包含遠端桌面通訊協定 (RDP) 應用程式容器用戶端的 [**RemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) 物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                     |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient 定義為 EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面 ActiveX 控制項類別](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

