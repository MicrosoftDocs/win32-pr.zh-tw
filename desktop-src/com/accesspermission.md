---
title: AccessPermission
description: 描述可存取此類別實例之主體 (ACL) 的存取控制清單。 只有未呼叫 CoInitializeSecurity 的應用程式才會使用此 ACL。
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- AccessPermission 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641512d34b963879ceb3d1a6266a017836879b224b228edb3ad62d61300fb03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551342"
---
# <a name="accesspermission"></a>AccessPermission

描述可存取此類別實例之主體 (ACL) 的存取控制清單。 只有未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式才會使用此 ACL。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>備註

這是 **REG \_ 二進位** 值。 它包含描述存取控制清單 (ACL) 的資料，這些主體可存取此類別的實例。 收到連接到這個類別之現有物件的要求時，會由在模擬呼叫端時呼叫的應用程式檢查 ACL。 如果存取檢查失敗，則不允許連接。 如果這個命名值不存在，就會測試 [**DefaultAccessPermission**](defaultaccesspermission.md) ACL，以判斷是否允許連接。

針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 或未使用 [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) 介面來指定 AppID 的應用程式，應用程式二進位檔的可執行檔必須對應到應用程式的 appid （如 [**AppID**](appid.md)中所述）。 這是必要的，如此 COM 才能找出應用程式的 AppID。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 