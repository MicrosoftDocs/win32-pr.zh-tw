---
description: 取消認可方法將解除配置器。 這個方法會實 IMemAllocator：:D ecommit 方法。
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: 'CBaseAllocator. 取消認可方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998617"
---
# <a name="cbaseallocatordecommit-method"></a>CBaseAllocator. 取消認可方法

`Decommit`方法會解除配置配置器。 這個方法會實 [**IMemAllocator：:D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

呼叫這個方法之後，對 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法的呼叫將會失敗。 當範例釋出時，它們就會回到可用清單。 傳回最後一個範例時，配置器會呼叫 [**CBaseAllocator：： Free**](cbaseallocator-free.md) 方法，它會釋放已配置的記憶體。  (在基類中， **Free** 是純虛擬方法。 ) 

此外，這個方法會釋放 **GetBuffer** 呼叫封鎖的任何執行緒。 對 **GetBuffer** 的呼叫會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




