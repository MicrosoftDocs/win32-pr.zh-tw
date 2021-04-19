---
description: 配置方法會為緩衝區配置記憶體。
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: 'CMemAllocator 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000788"
---
# <a name="cmemallocatoralloc-method"></a>CMemAllocator 方法

`Alloc`方法會為緩衝區配置記憶體。

## <a name="syntax"></a>語法


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                       | Description                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 成功。<br/>                          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | 記憶體不足。<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | 未設定緩衝區需求。<br/> |



 

## <a name="remarks"></a>備註

[**CBaseAllocator：： Commit**](cbaseallocator-commit.md)方法會呼叫這個方法。 它會針對 [**CMemAllocator：： SetProperties**](cmemallocator-setproperties.md) 方法中提供的緩衝區需求，配置足夠的連續記憶體區塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMemAllocator 類別**](cmemallocator.md)
</dt> </dl>

 

 




