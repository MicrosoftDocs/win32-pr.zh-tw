---
description: 評估運算式，並在運算式為 FALSE 時顯示診斷訊息。 在零售組建中略過。
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: 'ASSERT 宏 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1c64ae2256ae132fccdca6e483fae3f79d28b0cda66d7701acbe95abb1222d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824427"
---
# <a name="assert-macro"></a>ASSERT 巨集

評估運算式，並在運算式為 **FALSE** 時顯示診斷訊息。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*待續* 
</dt> <dd>

要評估的運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個宏不會傳回值。

## <a name="remarks"></a>備註

在「偵錯工具組建」中，如果運算式為 **FALSE**，此宏會顯示訊息方塊，其中包含運算式的文字、原始程式檔的名稱，以及行號。 使用者可以忽略判斷提示、輸入偵錯工具，或結束應用程式。

## <a name="examples"></a>範例


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Assert 和中斷點宏](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




