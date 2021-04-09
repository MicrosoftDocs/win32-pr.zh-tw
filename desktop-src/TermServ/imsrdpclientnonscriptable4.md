---
title: IMsRdpClientNonScriptable4 介面
description: 提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。 衍生自 IMsRdpClientNonScriptable3 介面。
ms.assetid: 570a5722-94b9-4195-846a-10233d56002d
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable4 介面遠端桌面服務
- IMsRdpClientNonScriptable4 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aedea56733a2a98db4b966bd91d9337e38e61d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935134"
---
# <a name="imsrdpclientnonscriptable4-interface"></a>IMsRdpClientNonScriptable4 介面

提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。 衍生自 [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md) 介面。 這個介面的方法只能透過 vtable 存取;它們無法用於可編寫腳本的用戶端。

## <a name="members"></a>成員

**IMsRdpClientNonScriptable4** 介面繼承自 [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)。 **IMsRdpClientNonScriptable4** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientNonScriptable4** 介面具有這些屬性。



| 屬性                                                                                                         | 存取類型           | Description                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowCredentialSaving**](imsrdpclientnonscriptable4-allowcredentialsaving.md)<br/>                     | 讀取/寫入<br/> | 指定 [認證] 對話方塊是否顯示啟用儲存認證的核取方塊。<br/>                                                                                        |
| [**LaunchedViaClientShellInterface**](imsrdpclientnonscriptable4-launchedviaclientshellinterface.md)<br/> | 讀取/寫入<br/> | 指定使用者是否使用 RD Web 存取介面啟動用戶端控制項。<br/>                                                                                                  |
| [**MarkRdpSettingsSecure**](imsrdpclientnonscriptable4-markrdpsettingssecure.md)<br/>                     | 讀取/寫入<br/> | 指定是否將 RDP 設定標示為安全。<br/>                                                                                                                                          |
| [**PromptForCredsOnClient**](imsrdpclientnonscriptable4-promptforcredsonclient.md)<br/>                   | 讀取/寫入<br/> | 指定用戶端控制項是否顯示提示輸入認證的對話方塊。<br/>                                                                                                      |
| [**PublisherCertificateChain**](imsrdpclientnonscriptable4-publishercertificatechain.md)<br/>             | 讀取/寫入<br/> | 指定發行者的憑證鏈。 此鏈會儲存在類型為 VT BYREF 的變數中 \_ ，其中包含指向 [**CERT \_ 鏈 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) 結構的指標。<br/> |
| [**RedirectionWarningType**](imsrdpclientnonscriptable4-redirectionwarningtype.md)<br/>                   | 讀取/寫入<br/> | 控制重新導向對話方塊的存在和外觀。<br/>                                                                                                                           |
| [**TrustedZoneSite**](imsrdpclientnonscriptable4-trustedzonesite.md)<br/>                                 | 讀取/寫入<br/> | 指定使用者啟動連線的網站是否位於用戶端電腦的 [信任的網站] 清單中。<br/>                                                                |
| [**WarnAboutPrinterRedirection**](imsrdpclientnonscriptable4-warnaboutprinterredirection.md)<br/>         | 讀取/寫入<br/> | 指定在啟動會話之前，重新導向對話方塊是否顯示印表機重新導向的相關訊息。<br/>                                                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient6 定義為7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting 定義為 D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

