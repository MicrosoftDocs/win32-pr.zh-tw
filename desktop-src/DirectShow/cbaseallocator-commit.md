---
description: Commit 方法會為緩衝區配置記憶體。 這個方法會實 IMemAllocator：： Commit 方法。
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: 'CBaseAllocator 的 Commit 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba9c373a15d5200d6466fef5c519a59a1052c8e5854ebe38c5a8b027d21188a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087578"
---
# <a name="cbaseallocatorcommit-method"></a>CBaseAllocator Commit 方法

方法會配置 `Commit` 緩衝區的記憶體。 這個方法會實 [**IMemAllocator：： Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Commit();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下列清單中的值。



| 傳回碼                                                                                       | 描述                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 成功。<br/>                                |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | 未指定緩衝區需求。<br/> |



 

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先呼叫 [**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md) 方法來指定緩衝區需求。

這個方法會呼叫虛擬方法 [**CBaseAllocator：：**](cbaseallocator-alloc.md) allocate 來配置緩衝區的記憶體。 衍生類別可以覆寫 **分配**。 如果取消認可作業暫止，則會將其取消。

您必須在呼叫 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法之前呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




