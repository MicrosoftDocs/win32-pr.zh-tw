---
description: 不透明的資料類型。
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: 'PLSA_CLIENT_REQUEST (Ntsecpkg) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792b81516e434469750b4ddd667bf6ddb82df31f4f13f82588d281f743bc8835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921037"
---
# <a name="plsa_client_request"></a>PLSA \_ 用戶端 \_ 要求

**PLSA \_ 用戶端 \_ 要求** 資料類型是不透明的資料類型。

[*本地安全機構*](../secgloss/l-gly.md) (LSA) 在內部使用它來維護與個別要求相關的用戶端資訊。


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Ntsecpkg。h</dt> </dl> |



 

 
