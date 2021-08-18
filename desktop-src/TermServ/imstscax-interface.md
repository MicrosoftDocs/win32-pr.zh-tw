---
title: IMsTscAx 介面
description: 可讓您連接並中斷用戶端控制項、建立虛擬通道物件，以及透過虛擬通道傳送資料。
ms.assetid: ca27393e-4f1f-4fc2-9dd0-34e8684bc8d4
ms.tgt_platform: multiple
keywords:
- IMsTscAx 介面遠端桌面服務
- IMsTscAx 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsTscAx
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cefdaa28d4331b1cc74c84de6b67d9d4d43336c90315c20bde8642ca9b9219c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125388"
---
# <a name="imstscax-interface"></a>IMsTscAx 介面

可讓您連接並中斷用戶端控制項、建立虛擬通道物件，以及透過虛擬通道傳送資料。 介面也包含取得和設定用戶端控制項相關屬性的方法。 您也可以透過 [**IMsRdpClient 介面**](imsrdpclient-interface.md)使用這些方法。

## <a name="members"></a>成員

**IMsTscAx** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IMsTscAx** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IMsTscAx** 介面具有這些方法。



| 方法                                                          | 描述                                                                                                                                                                                           |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**連線**](imstscax-connect.md)                             | 使用目前在控制項上設定的屬性起始連接。<br/>                                                                                                                  |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) | 針對每個指定的虛擬通道名稱建立用戶端虛擬通道物件。<br/>                                                                                                      |
| [**中斷連線**](imstscax-disconnect.md)                       | 中斷使用中連接。<br/>                                                                                                                                                         |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)   | 透過先前使用 [**IMsTscAx：： CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法建立的虛擬通道，將資料傳送至 RD 工作階段主機伺服器。<br/> |



 

### <a name="properties"></a>屬性

**IMsTscAx** 介面具有這些屬性。



| 屬性                                                                             | 存取類型           | 描述                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | 唯讀<br/>  | [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)介面指標。<br/>                       |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | 唯讀<br/>  | 目前控制項的最大加密強度。<br/>                                                        |
| [**連線**](imstscax-connected.md)<br/>                                   | 唯讀<br/>  | 目前控制項的連接狀態。<br/>                                                                   |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | 讀取/寫入<br/> | 控制項連接時，顯示在控制項中央的文字。<br/>                                 |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | 讀取/寫入<br/> | 目前的控制項在初始遠端桌面上的高度（以圖元為單位）。<br/>                                        |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | 讀取/寫入<br/> | 目前的控制項寬度（以圖元為單位），在初始的遠端桌面。<br/>                                         |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | 讀取/寫入<br/> | 在連接結束之前出現在控制項中央的文字。<br/>                               |
| [**域**](imstscax-domain.md)<br/>                                         | 讀取/寫入<br/> | 目前使用者登入的網域。<br/>                                                                  |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | 唯寫<br/> | 當控制項處於全螢幕模式時，所顯示的視窗標題。<br/>                                            |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | 唯讀<br/>  | 指出控制項是否已顯示水準捲軸。<br/>                                           |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | 唯讀<br/>  | [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)介面指標。<br/>                          |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | 唯讀<br/>  | 指出 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) 介面是否可供使用。<br/> |
| [**伺服器**](imstscax-server.md)<br/>                                         | 讀取/寫入<br/> | 目前控制項所連接的伺服器名稱。<br/>                                              |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | 讀取/寫入<br/> | 指出控制項是否會在啟動時立即建立 RD 工作階段主機的伺服器連接。<br/>   |
| [**使用者**](imstscax-username.md)<br/>                                     | 讀取/寫入<br/> | 使用者名稱登入認證。<br/>                                                                                |
| [**版本**](imstscax-version.md)<br/>                                       | 唯讀<br/>  | 目前控制項的版本號碼。<br/>                                                                     |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | 唯讀<br/>  | 指出控制項是否顯示垂直捲動條。<br/>                                                  |



 

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient 定義為791fa017-2de3-492e-acc5-53c67a2b94d0<br/> CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient2 定義為9059F30F-4EB1-4BD2-9FDC-36F43A218F4A<br/> CLSID \_ MsRdpClient2a 定義為971127BB-259F-48C2-BD75-5F97A3331551<br/> CLSID \_ MsRdpClient2NotSafeForScripting 定義為3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> CLSID \_ MsRdpClient3 定義為7584C670-2274-4EFB-B00B-D6AABA6D3850<br/> CLSID \_ MsRdpClient3a 定義為6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting 定義為 ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID \_ MsRdpClient4 定義為4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a 定義為54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting 定義為6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> CLSID \_ MsRdpClient5 定義為4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting 定義為4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 定義為7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting 定義為 D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> CLSID \_ MsRdpClientNotSafeForScripting 定義為7CACBD7B-0D99-468F-AC33-22E495C0AFE5<br/> CLSID \_ MsTscAx 定義為 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/> CLSID \_ MsTscAxNotSafeForScripting 定義為 A41A4187-5A86-4E26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

