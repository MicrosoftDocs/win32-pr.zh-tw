---
description: CheckSizes 方法會根據目前的媒體類型來檢查配置器屬性。
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: 'CImageAllocator. CheckSizes 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 070c0cac981f73ea6fa7e3c0ecb620e262f744edd651571be9b592840ad23956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076228"
---
# <a name="cimageallocatorchecksizes-method"></a>CImageAllocator. CheckSizes 方法

`CheckSizes`方法會根據目前的媒體類型來檢查配置器屬性。

## <a name="syntax"></a>語法


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRequest* 
</dt> <dd>

配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，此結構描述所要求的配置器屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                           | 描述                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 要求的屬性與媒體類型相容。<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | 要求的屬性與媒體類型不相容。<br/> |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 未連接擁有的 pin。<br/>                                 |



 

## <a name="remarks"></a>備註

當方法傳回時，如果傳回值為 S \_ OK， *PRequest* 的 **cbBuffer** 成員就會包含實際的緩衝區大小。 這可能大於所要求的大小，但永遠不會較小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageAllocator 類別**](cimageallocator.md)
</dt> </dl>

 

 




