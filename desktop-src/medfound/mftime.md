---
description: 定義100毫微秒的單位。
ms.assetid: 9273ff1f-382e-4c58-b571-4852545915b3
title: 'MFTIME (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e82c99c3c4a42b652c04595d086951c3c1a71a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989866"
---
# <a name="mftime"></a>MFTIME

定義100毫微秒的單位。


```C++
typedef LONGLONG MFTIME;
```



## <a name="examples"></a>範例


```C++
const MFTIME ONE_SECOND = 10000000; // One second.
const LONG   ONE_MSEC = 1000;       // One millisecond

// Convert 100-nanosecond units to milliseconds.

inline LONG MFTimeToMsec(const LONGLONG& time)
{
    return (LONG)(time / (ONE_SECOND / ONE_MSEC));
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎資料類型](media-foundation-datatypes.md)
</dt> </dl>

 

 




