---
description: GetPositions 方法會抓取目前的位置和停止位置，相對於資料流程的總持續時間。 這個方法會實 IMediaSeeking：： GetPositions 方法。
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: 'CPosPassThru. GetPositions 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999281"
---
# <a name="cpospassthrugetpositions-method"></a>CPosPassThru. GetPositions 方法

方法會抓取 `GetPositions` 目前的位置和停止位置，相對於資料流程的總持續時間。 這個方法會實 [**IMediaSeeking：： GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCurrent* 
</dt> <dd>

變數的指標，此變數會接收目前的位置，以目前時間格式的單位為單位。

</dd> <dt>

*pStop* 
</dt> <dd>

接收停止位置之變數的指標，以目前時間格式的單位為單位。

</dd> </dl>

## <a name="return-value"></a>傳回值

從連接的 pin 傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




