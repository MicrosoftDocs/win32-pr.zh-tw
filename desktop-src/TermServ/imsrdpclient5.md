---
title: IMsRdpClient5 介面
description: 提供設定和使用用戶端控制項所需的方法和屬性。 衍生自 IMsRdpClient4 介面。
ms.assetid: d3fc5e67-f4d9-4d80-b572-8fc3e660571e
ms.tgt_platform: multiple
keywords:
- IMsRdpClient5 介面遠端桌面服務
- IMsRdpClient5 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClient5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1005fba795c8926052dd8a42e13533e6b3319e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094111"
---
# <a name="imsrdpclient5-interface"></a>IMsRdpClient5 介面

提供設定和使用用戶端控制項所需的方法和屬性。 衍生自 [**IMsRdpClient4**](imsrdpclient4.md) 介面。

## <a name="members"></a>成員

**IMsRdpClient5** 介面繼承自 [**IMsRdpClient4**](imsrdpclient4.md)。 **IMsRdpClient5** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IMsRdpClient5** 介面具有這些方法。



| 方法                                                           | 描述                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------|
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) | 捕獲錯誤碼和錯誤訊息。<br/> |



 

### <a name="properties"></a>屬性

**IMsRdpClient5** 介面具有這些屬性。



| 屬性                                                                | 存取類型          | Description                                                                                         |
|:------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------|
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/> | 唯讀<br/> | 要 [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)的介面。<br/> |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>   | 唯讀<br/> | 入口網站啟動器的用戶端設定。<br/>                                         |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>         | 唯讀<br/> | 用戶端 RemoteApp 設定。<br/>                                                            |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/> | 唯讀<br/> | 用戶端 RD 閘道設定。<br/>                                                           |



 

## <a name="remarks"></a>備註

下列介面已擴充 **IMsRdpClient5** 介面，每個新介面都會繼承先前介面的所有方法和屬性：

-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient5 定義為4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting 定義為4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 定義為7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting 定義為 D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient5 定義為4eb5335b-6429-477d-b922-e06a28ecd8bf<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

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

 

 





