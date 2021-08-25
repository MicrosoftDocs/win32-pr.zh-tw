---
title: IMsRdpClientNonScriptable5 介面
description: 在遠端桌面 ActiveX 控制項上，提供用戶端遠端會話的 nonscriptable 屬性存取。 衍生自 IMsRdpClientNonScriptable4 介面。
ms.assetid: 41b8c624-0451-4a7e-bc80-d0bf269e33c6
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable5 介面遠端桌面服務
- IMsRdpClientNonScriptable5 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb7f3407f0dc6b1bc8dc04c6c4a72cda95db6b6b1def088a18908a730b96600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009798"
---
# <a name="imsrdpclientnonscriptable5-interface"></a>IMsRdpClientNonScriptable5 介面

在遠端桌面 ActiveX 控制項上，提供用戶端遠端會話的 nonscriptable 屬性存取。 衍生自 [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md) 介面。 這個介面的方法只能透過 vtable 存取;它們無法用於可編寫腳本的用戶端。

藉由呼叫 [**IMsTscAx**](imstscax-interface.md)物件上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得這個介面的實例，並傳遞 **IID \_ IMsRdpClientNonScriptable5**。

## <a name="members"></a>成員

**IMsRdpClientNonScriptable5** 介面繼承自 [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)。 **IMsRdpClientNonScriptable5** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientNonScriptable5** 介面具有這些屬性。



| 屬性                                                                                                         | 存取類型           | 描述                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AllowPromptingForCredentials**](imsrdpclientnonscriptable5-allowpromptingforcredentials.md)<br/>       | 讀取/寫入<br/> | 指定遠端桌面 ActiveX 控制項是否可以提示使用者輸入認證。<br/>                    |
| [**DisableConnectionBar**](imsrdpclientnonscriptable5-disableconnectionbar.md)<br/>                       | 唯寫<br/> | 指定遠端桌面 ActiveX 控制項是否應該停用連接列。<br/>                      |
| [**DisableRemoteAppCapsCheck**](imsrdpclientnonscriptable5-disableremoteappcapscheck.md)<br/>             | 讀取/寫入<br/> | 指定遠端桌面 ActiveX 控制項是否不應檢查伺服器的 RemoteApp 功能。<br/> |
| [**GetRemoteMonitorsBoundingBox**](imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md)<br/>       | 唯讀<br/>  | 指定遠端監視的周框。<br/>                                                      |
| [**RemoteMonitorCount**](imsrdpclientnonscriptable5-remotemonitorcount.md)<br/>                           | 唯讀<br/>  | 指定遠端監視的數目。<br/>                                                                     |
| [**RemoteMonitorLayoutMatchesLocal**](imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md)<br/> | 唯讀<br/>  | 指定遠端監視配置是否與本機監視器版面配置相同。<br/>                             |
| [**UseMultimon**](imsrdpclientnonscriptable5-usemultimon.md)<br/>                                         | 讀取/寫入<br/> | 指定遠端桌面 ActiveX 控制項是否應該使用多個監視器。<br/>                           |
| [**WarnAboutDirectXRedirection**](imsrdpclientnonscriptable5-warnaboutdirectxredirection.md)<br/>         | 讀取/寫入<br/> | 不會使用此屬性。<br/>                                                                                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 定義為 4f6996d5-d7b1-412c-b0ff-063718566907<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

