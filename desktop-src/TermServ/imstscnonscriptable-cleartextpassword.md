---
title: IMsTscNonScriptable ClearTextPassword 屬性
description: 以純文字格式設定遠端桌面 ActiveX 控制項密碼。
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- ClearTextPassword 屬性遠端桌面服務
- ClearTextPassword 屬性遠端桌面服務，IMsTscNonScriptable 介面
- IMsTscNonScriptable 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、ClearTextPassword 屬性
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686440"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>IMsTscNonScriptable：： ClearTextPassword 屬性

以純文字格式設定遠端桌面 ActiveX 控制項密碼。

此屬性是唯寫的。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>屬性值

要用來連接的密碼（以純文字格式指定）。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

密碼會傳遞至安全加密 RDP 通道中的伺服器。 設定純文字密碼之後，無法以純文字格式抓取。

只有當遠端桌面 ActiveX 控制項不是處於線上狀態時，才能設定 **ClearTextPassword** 屬性。 如果控制項已連接，則設定這個屬性會失敗。 若要檢查連接狀態，請取出 [**IMsTscAx：： connected**](imstscax-connected.md) 屬性。

您也可以呼叫這個方法來設定純文字密碼，然後將它轉換成可移植編碼的密碼或二進位 (nonportable) 編碼的密碼。 不過請注意，編碼的密碼不應被安全地加密。

如果您第一次呼叫此方法來設定純文字格式的密碼，則可以將密碼轉換成編碼格式。

**將純文字密碼轉換成編碼格式**

1.  在 **ClearTextPassword** 屬性中，以純文字格式設定密碼。
2.  若要以二進位格式取出密碼 (nonportable) 編碼格式，請取出 [**BinaryPassword**](imstscnonscriptable-binarypassword.md) 屬性和 [**BinarySalt**](imstscnonscriptable-binarysalt.md) 屬性。 編碼的密碼部分和 salt 部分都需要以二進位編碼格式設定密碼。
3.  若要以可移植的編碼格式取得密碼，請取出 [**PortablePassword**](imstscnonscriptable-portablepassword.md) 方法和 [**PortableSalt**](imstscnonscriptable-portablesalt.md) 屬性。 這兩個元件都需要以可移植編碼格式設定密碼。

遵循上述三個步驟之後，您可以藉由設定 [**BinaryPassword**](imstscnonscriptable-binarypassword.md) 和 [**BinarySalt**](imstscnonscriptable-binarysalt.md) 屬性，或 [**PortablePassword**](imstscnonscriptable-portablepassword.md) 和 [**PortableSalt**](imstscnonscriptable-portablesalt.md) 屬性來設定編碼格式的密碼。 這兩個元件都是必要的。

若要啟用自動登入，您也必須設定使用者 [**名稱**](imstscax-username.md) 和 [**網域**](imstscax-domain.md) 屬性。 如果密碼無法驗證使用者，則會在伺服器上顯示 [Windows 登入] 對話方塊，提示使用者輸入密碼。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable 定義為 c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





