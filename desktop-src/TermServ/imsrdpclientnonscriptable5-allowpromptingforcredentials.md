---
title: IMsRdpClientNonScriptable5 AllowPromptingForCredentials 屬性
description: 指定遠端桌面 ActiveX 控制項是否可以提示使用者輸入認證。
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- AllowPromptingForCredentials 屬性遠端桌面服務
- AllowPromptingForCredentials 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，AllowPromptingForCredentials 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea0fb854b5bb12533032cd6608228d81584cd8d9f4e99bccd8a5ba76b624f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138751"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a>IMsRdpClientNonScriptable5：： AllowPromptingForCredentials 屬性

指定遠端桌面 ActiveX 控制項是否可以提示使用者輸入認證。 如果此屬性包含 **VARIANT \_ TRUE**，就會提示使用者輸入認證。 如果此屬性包含 **VARIANT \_ FALSE**，則不會提示使用者輸入認證。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
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

 

 





