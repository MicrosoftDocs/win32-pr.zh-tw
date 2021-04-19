---
description: StringFromResource 函式會從資源檔載入具有指定資源識別碼的字串。
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: 'StringFromResource 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983179"
---
# <a name="stringfromresource-function"></a>StringFromResource 函式

`StringFromResource`函數會從資源檔載入具有指定資源識別碼的字串。

## <a name="syntax"></a>語法


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBuffer* 
</dt> <dd>

對應至 *iResourceID* 之字串的指標。

</dd> <dt>

*iResourceID* 
</dt> <dd>

要取出之字串的資源識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回與 *pBuffer* 相同的字串。 如果函式不成功，則會傳回 null 字串。

## <a name="remarks"></a>備註

*PBuffer* 緩衝區必須至少為 STR 的 \_ 最大 \_ 長度位元組。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性頁 Helper 函數](property-page-helper-functions.md)
</dt> </dl>

 

 




