---
description: CBaseMediaFilter. StreamTime 方法-StreamTime 方法會抓取目前的資料流程時間。
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: 'CBaseMediaFilter. StreamTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096246"
---
# <a name="cbasemediafilterstreamtime-method"></a>CBaseMediaFilter. StreamTime 方法

`StreamTime`方法會捕獲目前的資料流程時間。

## <a name="syntax"></a>語法


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rtStream* \[裁判\]
</dt> <dd>

[**CRefTime**](creftime.md)物件的參考，該物件會接收目前的資料流程時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                      | Description                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>             | 成功。<br/>                         |
| <dl> <dt>**VFW \_ E \_ NO \_ CLOCK**</dt> </dl> | 沒有可用的參考時鐘。<br/> |



 

## <a name="remarks"></a>備註

資料流程時間定義為目前的參考時間 (如參考時鐘所指定) 減去 [**CBaseMediaFilter：： m \_ tStart**](cbasemediafilter-m-tstart.md)) 所指定的開始時間 (。 媒體範例的時間戳記會指定應呈現的資料流程時間。 如果時間戳記小於目前資料流程時間的樣本尚未轉譯，則會延遲。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseMediaFilter 類別**](cbasemediafilter.md)
</dt> </dl>

 

 




