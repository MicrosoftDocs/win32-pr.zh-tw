---
description: UsingDifferentAllocators 方法會判斷輸入和輸出圖釘是否使用不同的配置器。
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: 'CTransInPlaceFilter. UsingDifferentAllocators 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984445"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>CTransInPlaceFilter. UsingDifferentAllocators 方法

`UsingDifferentAllocators`方法會判斷輸入和輸出圖釘是否使用不同的配置器。

## <a name="syntax"></a>語法


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果輸入和輸出圖釘使用不同的配置器，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




