---
description: TimeStamp 資料類型保存安全性權杖的時間有效性的相關資訊。 TimeStamp 資料類型值的格式與 FILETIME 結構的值相同。
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: 'TimeStamp (Sspi. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e521818c9001213396c0046b92f8f0bd9727dddfeaf99b2e23b652a48f8ff95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786363"
---
# <a name="timestamp"></a>TimeStamp

**TimeStamp** 資料類型保存安全性權杖的時間有效性的相關資訊。 **TimeStamp** 資料類型值的格式與 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構的值相同。


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Sspi (包含 Security .h) </dt> </dl> |



 

 
