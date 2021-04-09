---
title: IMsRdpClientAdvancedSettings7 RedirectDirectX 屬性
description: 不會使用此屬性。 |IMsRdpClientAdvancedSettings7 RedirectDirectX 屬性
ms.assetid: a027d8d7-994f-4b24-8c46-18651c8e200b
ms.tgt_platform: multiple
keywords:
- RedirectDirectX 屬性遠端桌面服務
- RedirectDirectX 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RedirectDirectX 屬性
- RedirectDirectX 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RedirectDirectX 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.RedirectDirectX
- IMsRdpClientAdvancedSettings7.get_RedirectDirectX
- IMsRdpClientAdvancedSettings7.put_RedirectDirectX
- IMsRdpClientAdvancedSettings8.RedirectDirectX
- IMsRdpClientAdvancedSettings8.get_RedirectDirectX
- IMsRdpClientAdvancedSettings8.put_RedirectDirectX
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f7da3ecea0c5a5a77a45b48ff24038a5517dc1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853735"
---
# <a name="imsrdpclientadvancedsettings7redirectdirectx-property"></a>IMsRdpClientAdvancedSettings7：： RedirectDirectX 屬性

不會使用此屬性。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectDirectX(
  [in]          VARIANT_BOOL fRedirectDirectX
);

HRESULT get_RedirectDirectX(
  [out, retval] VARIANT_BOOL *pfRedirectDirectX
);
```



## <a name="property-value"></a>屬性值

不會使用此屬性。

## <a name="error-codes"></a>錯誤碼

不會使用此屬性。 Setter 方法一律會傳回 **\_ FALSE** ，而 getter 方法一律會傳回 **E \_ >notimpl**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                                |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





