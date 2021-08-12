---
description: NotifyMediaType 方法會通知目前媒體類型的 CDrawImage 物件。
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: 'CDrawImage. NotifyMediaType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3df1f904bb5c2acfc328e8779da6135f901de9601cea6735de21b2e76aeea9c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656789"
---
# <a name="cdrawimagenotifymediatype-method"></a>CDrawImage. NotifyMediaType 方法

`NotifyMediaType`方法會通知目前媒體類型的 **CDrawImage** 物件。

## <a name="syntax"></a>語法


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaType* 
</dt> <dd>

[**CMediaType**](cmediatype.md)物件的指標，或為 **Null** 以清除媒體類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當媒體類型變更時，擁有篩選應呼叫這個方法。 一般來說，當 pin 首次連接，以及動態格式變更之後，就會發生這種情況。

**CDrawImage** 物件會將 *pMediaType* 指標儲存在 **m \_ pMediaType** 成員變數中。 因此，如果呼叫端需要釋放 **CMediaType** 物件，則應該再次呼叫這個方法來更新 **CDrawImage** 物件，其方式是使用新的指標或 **Null** 值。 否則，當 **CDrawImage** 物件嘗試參考舊指標時，就會發生錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




