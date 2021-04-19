---
description: NotifyMediaType 方法會通知物件目前的媒體類型。
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: 'CImageAllocator. NotifyMediaType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001138"
---
# <a name="cimageallocatornotifymediatype-method"></a>CImageAllocator. NotifyMediaType 方法

`NotifyMediaType`方法會通知目前媒體類型的物件。

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

當媒體類型變更時，擁有篩選應呼叫這個方法。 一般來說，當 pin 首次連接，以及動態格式變更之後，就會發生這種情況。 配置器會使用媒體類型來驗證建議的配置器屬性，也會在建立媒體範例時使用。

**CImageAllocator** 物件會將 *pMediaType* 指標儲存在 **m \_ pMediaType** 成員變數中。 因此，如果呼叫端需要釋放 **CMediaType** 物件，則應該再次呼叫這個方法來更新配置器，方法是使用新的指標或 **Null** 值。 否則，當配置器嘗試參考舊指標時，就會發生錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageAllocator 類別**](cimageallocator.md)
</dt> </dl>

 

 




