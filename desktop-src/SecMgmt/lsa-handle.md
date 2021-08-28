---
description: 本機原則物件的控制碼。
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: 'LSA_HANDLE (Ntsecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c674708a1fe29dda1fa01ba56739cfb58f23a037055ae11c5a4e4ab60690de3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894572"
---
# <a name="lsa_handle"></a>LSA \_ 控制碼

**LSA \_ 控制碼** 資料類型是本機 [**原則**](policy-object.md)物件的控制碼。


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a>備註

您的應用程式必須先開啟 [**原則**](policy-object.md) 物件的控制碼，您才能使用本機原則 API。 若要這樣做，請呼叫 [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)。 此函式會傳回一個控制碼，讓您的應用程式可以在後續的 LSA 原則函式呼叫中指定。

每個控制碼都有一組相關聯的許可權，可決定您的應用程式可以使用控制碼在 [**原則**](policy-object.md) 物件上執行的作業。 您的應用程式一次可以開啟一個以上的 **原則** 物件控制碼。 當不再需要控制碼時，您的應用程式應該透過呼叫 [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)來關閉它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Ntsecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

