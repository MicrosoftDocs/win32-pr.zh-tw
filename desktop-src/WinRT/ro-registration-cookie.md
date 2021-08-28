---
description: 代表藉由呼叫 RoRegisterActivationFactories 函式註冊的啟用 factory。
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: 'RO_REGISTRATION_COOKIE (Roapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efc7d3364f02c11750e6b42ddec6d2a3dee3f83368d277bc979a22ea3a0854a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741595"
---
# <a name="ro_registration_cookie"></a>RO \_ 註冊 \_ COOKIE

代表藉由呼叫 [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) 函式註冊的啟用 factory。


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>備註

當已向 Windows 執行階段註冊可啟動的類別 factory 時， [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)函數會傳回 **RO \_ 註冊 \_ COOKIE** 。 [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)函式會使用 cookie 來移除 class factory。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Roapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
