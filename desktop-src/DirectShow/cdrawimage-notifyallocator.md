---
description: NotifyAllocator 方法會通知 CDrawImage 物件，連接的配置器是否為 CImageAllocator 物件。
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: 'CDrawImage. NotifyAllocator 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996027"
---
# <a name="cdrawimagenotifyallocator-method"></a>CDrawImage. NotifyAllocator 方法

`NotifyAllocator`方法會通知 **CDrawImage** 物件，連接的配置器是否為 [**CImageAllocator**](cimageallocator.md)物件。

## <a name="syntax"></a>語法


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bUsingImageAllocator* 
</dt> <dd>

指出正在使用哪種配置器類型的布林值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當 pin 同意配置器之後，擁有篩選應呼叫這個方法。 如果篩選準則知道配置器是 **CImageAllocator** 物件，則應該使用 **TRUE** 值來呼叫此方法。  (通常只有當篩選準則擁有有問題的配置器時，才會知道此篩選準則 ) 。否則，它應該使用值 **FALSE** 來呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> <dt>

[**CDrawImage：:D rawImage**](cdrawimage-drawimage.md)
</dt> </dl>

 

 




