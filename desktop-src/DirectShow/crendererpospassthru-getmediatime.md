---
description: CRendererPosPassThru. GetMediaTime 方法-GetMediaTime 方法會抓取目前樣本上的時間戳記。
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: 'CRendererPosPassThru. GetMediaTime 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3b8eb4bdd9426d589476265133234bdf3c2d5cfc691bfaced743cc4e75769c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084118"
---
# <a name="crendererpospassthrugetmediatime-method"></a>CRendererPosPassThru. GetMediaTime 方法

方法會抓取 `GetMediaTime` 目前樣本上的時間戳記。

## <a name="syntax"></a>語法


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStartTime* 
</dt> <dd>

接收開始時間之變數的指標，以目前時間格式的單位為單位。

</dd> <dt>

*pEndTime* 
</dt> <dd>

接收結束時間之變數的指標，以目前時間格式的單位為單位。 可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                  | 描述                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 不支援轉換成此格式。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數。<br/>                  |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CPosPassThru：： GetMediaTime**](cpospassthru-getmediatime.md) 方法。 時間戳記值會藉由呼叫 [**CPosPassThru：： ConvertTimeFormat**](cpospassthru-converttimeformat.md) 方法轉換為目前的時間格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




