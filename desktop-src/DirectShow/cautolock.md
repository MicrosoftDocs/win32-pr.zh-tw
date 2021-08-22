---
description: CAutoLock 類別會保留程式碼區塊範圍的重要區段。
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: 'CAutoLock 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b046111e3a7e22fcf9e380fae09bb2d2007a583e49c0507b8e214142505fe02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661700"
---
# <a name="cautolock-class"></a>CAutoLock 類別

`CAutoLock`類別會保留程式碼區塊範圍的重要區段。

這個類別會與 [**CCritSec**](ccritsec.md) 類別搭配使用，這是重要區段物件的包裝函式。 此 `CAutoLock` 函式會鎖定重要區段，並將它解除鎖定。 `CAutoLock`您可以使用物件做為區域變數，藉由確保所有程式碼路徑都能解除鎖定重要區段，來鎖定重要區段。

下列程式碼範例顯示如何使用這個類別：


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



此類別中的方法不是設計成要覆寫。



| 受保護的成員變數                 | 描述                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**m \_ pLock**](cautolock-m-plock.md)      | 此鎖定的重要區段。                                  |
| 公用方法                             | 描述                                                      |
| [**CAutoLock**](cautolock-cautolock.md)   | 函式方法。 鎖定指定的重要區段物件。 |
| [**~ CAutoLock**](cautolock--cautolock.md) | 函式方法。 解除鎖定重要區段物件。          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




