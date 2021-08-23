---
title: IMsRdpClient10 介面
description: 提供設定和使用用戶端控制項所需的方法和屬性。 衍生自 IMsRdpClient9 介面。
ms.assetid: 601f70aa-85f1-4180-921b-9f1bb31d4def
ms.tgt_platform: multiple
keywords:
- IMsRdpClient10 介面遠端桌面服務
- IMsRdpClient10 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClient10
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561541f170fbe6dc5342b359e5deae69d0c92469ad2d692ee4ea3b9d59904885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737238"
---
# <a name="imsrdpclient10-interface"></a>IMsRdpClient10 介面

提供設定和使用用戶端控制項所需的方法和屬性。 衍生自 [**IMsRdpClient9**](imsrdpclient9.md) 介面。

## <a name="members"></a>成員

**IMsRdpClient10** 介面繼承自 [**IMsRdpClient9**](imsrdpclient9.md)。 **IMsRdpClient10** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IMsRdpClient10** 介面具有這些方法。



| 方法                                                                             | 描述                                                                         |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                   | 附加事件。<br/>                                                       |
| [**Vemap.detachevent**](imsrdpclient9-detachevent.md)                                   | 卸離事件。<br/>                                                       |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | 抓取會話中斷連接事件的錯誤描述。<br/>       |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | 抓取指定狀態碼的狀態文字。<br/>                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | 抓取為虛擬通道設定的選項。<br/>                         |
| [**重新連接**](imsrdpclient8-reconnect.md)                                       | 重新連接到具有新桌面寬度和高度的遠端會話。<br/>  |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | 要求遠端桌面 ActiveX 控制項正常關機。<br/>      |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | 使動作在遠端會話中執行。<br/>                  |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | 設定遠端桌面 ActiveX 控制項的虛擬通道選項。<br/> |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | 同步處理會話顯示設定。<br/>                                   |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | 更新會話顯示設定。<br/>                                        |



 

### <a name="properties"></a>屬性

**IMsRdpClient10** 介面具有這些屬性。



| 屬性                                                                             | 存取類型           | 描述                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) 介面的指標。 介面可以用來設定用戶端控制項的 advanced 設定。<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) 介面的指標。 介面可以用來設定用戶端控制項的 advanced 設定。<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) 介面的指標。<br/>                                                                                    |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) 介面的指標。<br/>                                                                                     |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) 介面。<br/>                                                                                                 |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) 介面。<br/>                                                                                                 |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | 唯讀<br/>  | 抓取支援 [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) 介面的物件。<br/>                                                                         |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | 唯讀<br/>  | 包含支援 [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) 介面的物件。<br/>                                                                          |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | 讀取/寫入<br/> | 色彩深度 (控制項連接的每圖元) 位數。<br/>                                                                                                                               |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | 讀取/寫入<br/> | 包含控制項處於連接狀態時，在控制項的工作區中顯示的文字。<br/>                                                                              |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | 唯讀<br/>  | 包含控制項中斷連接原因的延伸資訊。<br/>                                                                                                                     |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | 讀取/寫入<br/> | 判斷用戶端控制項是否處於全螢幕模式。<br/>                                                                                                                                   |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | 唯讀<br/>  | 抓取可編寫腳本的用戶端設定介面 [**IMsRdpClientShell**](imsrdpclientshell.md)。<br/>                                                                                               |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | 唯讀<br/>  | 抓取支援 [**ITSRemoteProgram**](itsremoteprogram.md) 介面的物件。<br/>                                                                                                   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | 唯讀<br/>  | 抓取支援 [**ITSRemoteProgram2**](itsremoteprogram2.md) 介面的物件。<br/>                                                                                                 |
| [**RemoteProgram3**](imsrdpclient10-remoteprogram3.md)<br/>                   | 唯讀<br/>  | 支援 [**ITSRemoteProgram3**](itsremoteprogram3.md) 介面的物件。<br/>                                                                                                           |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | 唯讀<br/>  | 捕獲 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面的指標。 這個介面可以用來設定用戶端控制項的安全設定。<br/>   |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | 唯讀<br/>  | 抓取支援 [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) 介面的物件。<br/>                                                                           |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | 唯讀<br/>  | 抓取透過腳本傳遞至 [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) 介面的內容。<br/>                                                             |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | 唯讀<br/>  | 捕獲 [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) 介面。<br/>                                                                                               |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | 唯讀<br/>  | 抓取支援 [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) 介面的物件。<br/>                                                                       |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | 唯讀<br/>  | 抓取支援 [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) 介面的物件。<br/>                                                                       |



 

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                                                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                                                                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> |
| IID<br/>                      | IID \_ IMsRdpClient10 定義為7ED92C39-EB38-4927-A70A-708AC5A59321<br/>                                                                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

