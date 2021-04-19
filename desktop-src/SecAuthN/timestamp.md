---
description: TimeStamp 資料類型保存安全性權杖的時間有效性的相關資訊。 TimeStamp 資料類型值的格式與 FILETIME 結構的值相同。
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: 'TimeStamp (Sspi. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978901"
---
# <a name="timestamp"></a>TimeStamp

**TimeStamp** 資料類型保存安全性權杖的時間有效性的相關資訊。 **TimeStamp** 資料類型值的格式與 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構的值相同。


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Sspi (包含 Security .h) </dt> </dl> |



 

 
