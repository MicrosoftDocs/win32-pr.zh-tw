---
description: 評估運算式，並在運算式為 FALSE 時引發中斷點例外狀況。 運算式的文字、原始程式檔的名稱，以及使用 DbgLog 宏記錄行號的行號。 在零售組建中略過。
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: 'KASSERT 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976268"
---
# <a name="kassert-macro"></a>KASSERT 宏

評估運算式，並在運算式為 **FALSE** 時引發中斷點例外狀況。 運算式的文字、原始程式檔的名稱，以及使用 [**DbgLog**](dbglog.md) 宏記錄行號的行號。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void KASSERT(
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

與 [**assert**](assert.md) 和 [**EXECUTE \_ assert**](execute-assert.md) 宏不同的是，此宏不會顯示提示使用者的訊息方塊。 在 debug 組建中，如果運算式為 **FALSE**，宏會自動造成中斷點例外狀況發生。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Assert 和中斷點宏](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




