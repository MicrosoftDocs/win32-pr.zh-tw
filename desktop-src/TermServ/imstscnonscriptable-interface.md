---
title: IMsTscNonScriptable 介面
description: 包含與遠端桌面 ActiveX 控制項的密碼應用程式相關的屬性和方法。
ms.assetid: b4a68e02-cce6-4fbe-98b4-0627c10f3f37
ms.tgt_platform: multiple
keywords:
- IMsTscNonScriptable 介面遠端桌面服務
- IMsTscNonScriptable 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsTscNonScriptable
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92372f7ea9479f7fcdd632546a0bd7dd2f0b465e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968142"
---
# <a name="imstscnonscriptable-interface"></a>IMsTscNonScriptable 介面

包含與遠端桌面 ActiveX 控制項的密碼應用程式相關的屬性和方法。

**IMsTscNonScriptable** 介面的主要用途是在遠端桌面 ActiveX 控制項裝載于自訂寫入容器的案例中，設定遠端桌面工作階段主機 (RD 工作階段主機) 伺服器的自動密碼登入存取。 當設定自動登入時，使用者在連接時不會收到 [Windows 登入] 對話方塊。

在某些平臺上， **IMsTscNonScriptable** 介面的方法可以用來指定三種支援格式的密碼：

-   純文字
-   可移植的編碼
-   二進位 (nonportable) 編碼

請注意，編碼格式的密碼是由兩個部分所組成：

-   編碼的密碼部分。
-   Salt 值部分。

這兩個元件都必須設定編碼的密碼。 編碼的密碼部分和 salt 值部分都不應視為安全加密。

可編寫腳本的純文字密碼存取權可透過可編寫腳本之介面 [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)的 [**ClearTextPassword**](imsrdpclientadvancedsettings-cleartextpassword.md)屬性取得。

**IMsTscNonScriptable** 介面只能透過 vtable 來存取。

## <a name="members"></a>成員

**IMsTscNonScriptable** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMsTscNonScriptable** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IMsTscNonScriptable** 介面具有這些方法。



| 方法                                                     | 描述                                           |
|:-----------------------------------------------------------|:------------------------------------------------------|
| [**ResetPassword**](imstscnonscriptable-resetpassword.md) | 重設控制項中的所有密碼狀態。<br/> |



 

### <a name="properties"></a>屬性

**IMsTscNonScriptable** 介面具有這些屬性。



| 屬性                                                                      | 存取類型           | Description                                                                  |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------|
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>       | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>               | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                   |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/> | 唯寫<br/> | 以純文字格式的遠端桌面 ActiveX 控制項密碼。<br/> |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>   | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>           | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                   |



 

## <a name="remarks"></a>備註

提供密碼給遠端桌面 ActiveX 控制項是選擇性的。 如果您提供密碼給控制項，則在使用 [**Connect**](imstscax-connect.md) 方法的呼叫起始連接之前，您應該只將上述三種格式的其中一種套用至控制項。

> [!Note]  
> 您也可以使用遠端桌面服務設定工具 (的設定，在伺服器上啟用自動登入。 ) 系統管理員可以使用此工具，在需要自動登入的情況下，將特定密碼指派給連線。

 

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

下列介面已擴充 **IMsTscNonScriptable** 介面，每個新介面都會繼承先前介面的所有方法和屬性：

-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient 定義為791fa017-2de3-492e-acc5-53c67a2b94d0<br/> CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient2 定義為9059F30F-4EB1-4BD2-9FDC-36F43A218F4A<br/> CLSID \_ MsRdpClient2a 定義為971127BB-259F-48C2-BD75-5F97A3331551<br/> CLSID \_ MsRdpClient2NotSafeForScripting 定義為3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> CLSID \_ MsRdpClient3 定義為7584C670-2274-4EFB-B00B-D6AABA6D3850<br/> CLSID \_ MsRdpClient3a 定義為6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting 定義為 ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID \_ MsRdpClient4 定義為4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a 定義為54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting 定義為6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> CLSID \_ MsRdpClient5 定義為4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting 定義為4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 定義為7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting 定義為 D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> CLSID \_ MsRdpClientNotSafeForScripting 定義為7CACBD7B-0D99-468F-AC33-22E495C0AFE5<br/> CLSID \_ MsTscAx 定義為 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/> CLSID \_ MsTscAxNotSafeForScripting 定義為 A41A4187-5A86-4E26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsTscNonScriptable 定義為 C1E6743A-41C1-4A74-832A-0DD06C1C7A0E<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsTscAx：： Connect**](imstscax-connect.md)
</dt> </dl>

 

