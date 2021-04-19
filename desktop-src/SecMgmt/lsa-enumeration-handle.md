---
description: Lsa \_ \_ 函數會使用 lsa 列舉控制碼資料類型來列舉 TrustedDomain 物件： LsaEnumerateTrustedDomainsEx。
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: 'LSA_ENUMERATION_HANDLE (Ntsecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974470"
---
# <a name="lsa_enumeration_handle"></a>LSA \_ 列舉 \_ 控制碼

Lsa 函數會使用 **lsa \_ 列舉 \_ 控制碼** 資料類型來列舉 [**TrustedDomain**](trusteddomain-object.md) 物件： [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)。 這個函式的設計目的，是為了讓您可以進行多個呼叫，以列舉資料庫中特定類型的所有物件。

在初始列舉函式呼叫中，您會將指標傳遞至已初始化為零的 **LSA \_ 列舉 \_ 控制碼** 變數。 函數會更新此值。 如果函式傳回的值指出有更多要列舉的物件，請再次呼叫函式，並傳入更新的 **LSA \_ 列舉 \_ 控制碼** 值，以取得從先前列舉中斷的點繼續的列舉。


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Ntsecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




