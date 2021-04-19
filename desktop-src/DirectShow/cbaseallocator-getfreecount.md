---
description: GetFreeCount 方法會抓取未使用的媒體樣本數目。
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: 'CBaseAllocator. GetFreeCount 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993533"
---
# <a name="cbaseallocatorgetfreecount-method"></a>CBaseAllocator. GetFreeCount 方法

`GetFreeCount`方法會抓取未使用的媒體樣本數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*plBuffersFree* 
</dt> <dd>

接收未使用的樣本數目之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會實 [**IMemAllocatorCallbackTemp：： GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) 方法。 配置器不會公開 IMemAllocatorCallbackTemp 介面，除非 CBaseAllocator 函式中的 *fEnableReleaseCallback* 旗標設為 **TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




