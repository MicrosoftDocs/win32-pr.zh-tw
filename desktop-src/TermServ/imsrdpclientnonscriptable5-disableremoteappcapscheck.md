---
title: IMsRdpClientNonScriptable5 DisableRemoteAppCapsCheck 屬性
description: 指定遠端桌面 ActiveX 控制項是否不應檢查伺服器的 RemoteApp 功能。
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- DisableRemoteAppCapsCheck 屬性遠端桌面服務
- DisableRemoteAppCapsCheck 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，DisableRemoteAppCapsCheck 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467021"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a>IMsRdpClientNonScriptable5：:D isableRemoteAppCapsCheck 屬性

指定遠端桌面 ActiveX 控制項是否不應檢查伺服器的 RemoteApp 功能。 如果這個屬性包含 **VARIANT \_ TRUE**，控制項就不應該檢查伺服器的 RemoteApp 功能。 如果這個屬性包含 **VARIANT \_ FALSE**，控制項可以檢查伺服器的 RemoteApp 功能。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a>屬性值

指定新的屬性值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                             |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 定義為 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





