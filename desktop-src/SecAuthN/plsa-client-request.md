---
description: 不透明的資料類型。
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: 'PLSA_CLIENT_REQUEST (Ntsecpkg) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192951"
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
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Ntsecpkg。h</dt> </dl> |



 

 
