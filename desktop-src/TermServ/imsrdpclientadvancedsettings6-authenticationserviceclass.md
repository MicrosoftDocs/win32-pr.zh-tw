---
title: IMsRdpClientAdvancedSettings6 AuthenticationServiceClass 屬性
description: 指定服務主體名稱 (SPN) 用來向伺服器進行驗證。
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- AuthenticationServiceClass 屬性遠端桌面服務
- AuthenticationServiceClass 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，AuthenticationServiceClass 屬性
- AuthenticationServiceClass 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，AuthenticationServiceClass 屬性
- AuthenticationServiceClass 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，AuthenticationServiceClass 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.put_AuthenticationServiceClass
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618b55d1489f46e0e1119186bd5003fb68dbfebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685912"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a>IMsRdpClientAdvancedSettings6：： AuthenticationServiceClass 屬性

指定服務主體名稱 (SPN) 用來向伺服器進行驗證。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a>屬性值

指定要使用的服務主體名稱。

## <a name="remarks"></a>備註

只有遠端桌面連線6.1 和7.0 用戶端支援此屬性。

服務主體名稱 (Spn) 與服務執行所在的安全性內容 (使用者或群組) 相關聯的安全性主體。 Spn 是用來支援用戶端應用程式與服務之間的相互驗證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





