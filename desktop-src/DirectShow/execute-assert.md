---
description: 評估 debug 和 retail 組建中的運算式。 在 [偵錯工具] 組建中，如果運算式為 FALSE，則會顯示診斷訊息。
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: 'EXECUTE_ASSERT 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 871a8e4a04ec1dc31f3240b539a943c9c1733f083166fa4b7e6f6b52d14a466c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401788"
---
# <a name="execute_assert-macro"></a>EXECUTE \_ ASSERT 宏

評估 debug 和 retail 組建中的運算式。 在 [偵錯工具] 組建中，如果運算式為 **FALSE**，則會顯示診斷訊息。

## <a name="syntax"></a>語法


```C++
void EXECUTE_ASSERT(
    cond
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

與 [**ASSERT**](assert.md) 宏不同的是，此宏會評估零售組建中的運算式。 在偵錯工具組建中，如果運算式為 **FALSE**，則宏會顯示訊息方塊，其中包含運算式的文字、原始程式檔的名稱，以及行號。 使用者可以忽略判斷提示、輸入偵錯工具，或結束應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Assert 和中斷點宏](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




