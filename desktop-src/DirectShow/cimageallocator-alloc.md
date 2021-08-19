---
description: 配置方法會為緩衝區配置記憶體。 這個方法會覆寫 CBaseAllocator：：分配方法。
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: 'CImageAllocator 方法 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bdf4c36bcf66d46a5c5ee7df16ac04a4461bd3a88de91e175b81e89ce496e1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076238"
---
# <a name="cimageallocatoralloc-method"></a>CImageAllocator 方法

`Alloc`方法會為緩衝區配置記憶體。 這個方法會覆寫 [**CBaseAllocator：：分配**](cbaseallocator-alloc.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                   | 描述                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | Success<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足<br/> |



 

## <a name="remarks"></a>備註

當篩選準則認可配置器時， [**CBaseAllocator：： Commit**](cbaseallocator-commit.md) 方法會呼叫這個方法。

這個方法會建立媒體範例的清單，這些範例會實作為 [**CImageSample**](cimagesample.md) 物件。 每個範例都包含 GDI 與裝置無關的點陣圖（使用 GDI **CreateDIBSection** 函式）。

在內部，這個方法會呼叫 [**CImageAllocator：： CreateDIB**](cimageallocator-createdib.md) 來建立每個 DIB，並呼叫 [**CImageAllocator：： CreateImageSample**](cimageallocator-createimagesample.md) 來建立每個範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageAllocator 類別**](cimageallocator.md)
</dt> </dl>

 

 




