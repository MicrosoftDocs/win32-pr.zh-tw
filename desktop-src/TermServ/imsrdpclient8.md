---
title: IMsRdpClient8 介面
description: 提供設定和使用用戶端控制項所需的方法和屬性。 衍生自 IMsRdpClient7 介面。
ms.assetid: 5ff54392-48f2-49a9-a264-88db08ec1770
ms.tgt_platform: multiple
keywords:
- IMsRdpClient8 介面遠端桌面服務
- IMsRdpClient8 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClient8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63dbdffbad87f9860bc063ab7f83883e0f902ea1ef7e4d2e91d452b2b832a699
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871358"
---
# <a name="imsrdpclient8-interface"></a>IMsRdpClient8 介面

提供設定和使用用戶端控制項所需的方法和屬性。 衍生自 [**IMsRdpClient7**](imsrdpclient7.md) 介面。

## <a name="members"></a>成員

**IMsRdpClient8** 介面繼承自 [**IMsRdpClient7**](imsrdpclient7.md)。 **IMsRdpClient8** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IMsRdpClient8** 介面具有這些方法。



| 方法                                                                    | 描述                                                                                                                                                                                 |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**連線**](imstscax-connect.md)                                       | 使用目前在控制項上設定的屬性起始連接。<br/>                                                                                                        |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)           | 針對每個指定的虛擬通道名稱建立用戶端虛擬通道物件。<br/>                                                                                            |
| [**中斷連線**](imstscax-disconnect.md)                                 | 中斷使用中連接。<br/>                                                                                                                                               |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)          | 抓取會話中斷連接事件的錯誤描述。<br/>                                                                                                               |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                      | 抓取指定狀態碼的狀態文字。<br/>                                                                                                                         |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md) | 抓取為虛擬通道設定的選項。<br/>                                                                                                                                 |
| [**重新連接**](imsrdpclient8-reconnect.md)                              | 重新連接到具有新桌面寬度和高度的遠端會話。<br/>                                                                                                          |
| [**RequestClose**](imsrdpclient-requestclose.md)                         | 要求遠端桌面 ActiveX 控制項正常關機。<br/>                                                                                                              |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)             | 透過先前使用 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法建立的虛擬通道，將資料傳送至 RD 工作階段主機伺服器。<br/> |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                | 使動作在遠端會話中執行。<br/>                                                                                                                          |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md) | 設定遠端桌面 ActiveX 控制項的虛擬通道選項。<br/>                                                                                                         |



 

### <a name="properties"></a>屬性

**IMsRdpClient8** 介面具有這些屬性。



| 屬性                                                                             | 存取類型           | 描述                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | 唯讀<br/>  | 捕獲 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。<br/>                                                                                                                                          |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) 介面的指標。 介面可以用來設定用戶端控制項的 advanced 設定。<br/>                                             |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) 介面的指標。 介面可以用來設定用戶端控制項的 advanced 設定。<br/>                                                     |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) 介面的指標。<br/>                                                                                                                                |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) 介面的指標。<br/>                                                                                                                                 |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) 介面。<br/>                                                                                                                                             |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | 唯讀<br/>  | 捕獲 [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) 介面。<br/>                                                                                                                                             |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | 唯讀<br/>  | 抓取支援 [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) 介面的物件。<br/>                                                                                                                     |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | 唯讀<br/>  | 包含支援 [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) 介面的物件。<br/>                                                                                                                      |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | 唯讀<br/>  | 抓取目前控制項的最大加密強度。<br/>                                                                                                                                                                           |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | 讀取/寫入<br/> | 色彩深度 (控制項連接的每圖元) 位數。<br/>                                                                                                                                                                           |
| [**連線**](imstscax-connected.md)<br/>                                   | 唯讀<br/>  | 抓取目前控制項的連接狀態。<br/>                                                                                                                                                                                      |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | 讀取/寫入<br/> | 包含控制項處於連接狀態時，在控制項的工作區中顯示的文字。<br/>                                                                                                                          |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | 讀取/寫入<br/> | 指定控制項連接時，顯示在控制項中央的文字。<br/>                                                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | 讀取/寫入<br/> | 以圖元為單位，指定初始遠端桌面上的目前控制項高度（以圖元為單位）。<br/>                                                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | 讀取/寫入<br/> | 以圖元為單位，指定初始遠端桌面上的目前控制項寬度（以圖元為單位）。<br/>                                                                                                                                                            |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | 讀取/寫入<br/> | 指定在連接結束之前，顯示在控制項中央的文字。<br/>                                                                                                                                                  |
| [**域**](imstscax-domain.md)<br/>                                         | 讀取/寫入<br/> | 指定目前使用者登入的網域。<br/>                                                                                                                                                                                     |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | 唯讀<br/>  | 包含控制項中斷連接原因的延伸資訊。<br/>                                                                                                                                                                 |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | 讀取/寫入<br/> | 判斷用戶端控制項是否處於全螢幕模式。<br/>                                                                                                                                                                               |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | 唯寫<br/> | 指定當控制項處於全螢幕模式時，所顯示的視窗標題。<br/>                                                                                                                                                               |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | 唯讀<br/>  | 指出控制項是否已顯示水準捲軸。<br/>                                                                                                                                                                        |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | 唯讀<br/>  | 抓取可編寫腳本的用戶端設定介面 [**IMsRdpClientShell**](imsrdpclientshell.md)。<br/>                                                                                                                                           |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | 唯讀<br/>  | 抓取支援 [**ITSRemoteProgram**](itsremoteprogram.md) 介面的物件。<br/>                                                                                                                                               |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | 唯讀<br/>  | 抓取支援 [**ITSRemoteProgram2**](itsremoteprogram2.md) 介面的物件。<br/>                                                                                                                                             |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | 唯讀<br/>  | 捕獲 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) 介面指標。<br/>                                                                                                                                            |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | 唯讀<br/>  | 捕獲 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面的指標。 這個介面可以用來設定用戶端控制項的安全設定。<br/>                                               |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | 唯讀<br/>  | 抓取支援 [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) 介面的物件。<br/>                                                                                                                       |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | 唯讀<br/>  | 指出 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) 介面是否可供使用。 亦即，包含控制項的網頁目前是否為其中一個允許的 Internet Explorer URL 安全性區域。<br/> |
| [**伺服器**](imstscax-server.md)<br/>                                         | 讀取/寫入<br/> | 指定目前控制項所連接的伺服器名稱。<br/>                                                                                                                                                                 |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | 讀取/寫入<br/> | 指出控制項是否會在啟動時立即建立 RD 工作階段主機的伺服器連接。<br/>                                                                                                                                |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | 唯讀<br/>  | 抓取透過腳本傳遞至 [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) 介面的內容。<br/>                                                                                                         |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | 唯讀<br/>  | 捕獲 [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) 介面。<br/>                                                                                                                                           |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | 唯讀<br/>  | 抓取支援 [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) 介面的物件。<br/>                                                                                                                   |
| [**使用者**](imstscax-username.md)<br/>                                     | 讀取/寫入<br/> | 指定使用者名稱登入認證。<br/>                                                                                                                                                                                                   |
| [**版本**](imstscax-version.md)<br/>                                       | 唯讀<br/>  | 指定目前控制項的版本號碼。<br/>                                                                                                                                                                                        |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | 唯讀<br/>  | 指出控制項是否顯示垂直捲動條。<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>備註

下列介面已擴充 **IMsRdpClient8** 介面，每個新介面都會繼承先前介面的所有方法和屬性：

-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient8 定義為4247E044-9271-43A9-BC49-E2AD9E855D62<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

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

 

 





