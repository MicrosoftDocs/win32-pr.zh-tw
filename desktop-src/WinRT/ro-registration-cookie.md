---
description: 代表藉由呼叫 RoRegisterActivationFactories 函式註冊的啟用 factory。
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: 'RO_REGISTRATION_COOKIE (Roapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995820"
---
# <a name="ro_registration_cookie"></a>RO \_ 註冊 \_ COOKIE

代表藉由呼叫 [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) 函式註冊的啟用 factory。


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>備註

當已向 Windows 執行階段註冊可啟動的類別 factory 時， [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) 函數會傳回 **RO \_ 註冊 \_ COOKIE** 。 [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)函式會使用 cookie 來移除 class factory。

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

 

 
