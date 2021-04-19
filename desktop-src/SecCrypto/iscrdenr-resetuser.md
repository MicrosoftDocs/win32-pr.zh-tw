---
description: 從智慧卡控制項清除使用者名稱。
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: ISCrdEnr：： resetUser 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991918"
---
# <a name="iscrdenrresetuser-method"></a>ISCrdEnr：： resetUser 方法

**ResetUser** 方法會從智慧卡控制項中清除使用者名稱。

## <a name="syntax"></a>語法


```C++
HRESULT resetUser();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="remarks"></a>備註

這個方法會從記憶體中清除任何現有的使用者名稱和先前註冊的憑證。 但先前註冊的憑證並不會從智慧卡移除。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr：： getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




