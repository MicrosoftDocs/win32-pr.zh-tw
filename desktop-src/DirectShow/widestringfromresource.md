---
description: WideStringFromResource 函式會從資源檔載入具有指定資源識別碼的寬字元字串。
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: 'WideStringFromResource 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798f915536c491d32ccab7e7dbdc9b506d8b5df22b4459818472307e62356b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071812"
---
# <a name="widestringfromresource-function"></a>WideStringFromResource 函式

`WideStringFromResource`函數會從資源檔載入具有指定資源識別碼的寬字元字串。

## <a name="syntax"></a>語法


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
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

屬性頁通常會透過其 COM 介面呼叫，而不論二進位檔的建立方式為何，都使用寬字元字串。 此函數可讓您將資源字串轉換成寬字元字串。 此函式會將資源轉換為寬字元字串 (如果它在載入後尚未) 的話。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性頁 Helper 函數](property-page-helper-functions.md)
</dt> </dl>

 

 




