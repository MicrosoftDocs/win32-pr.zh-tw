---
description: Run 方法會執行物件。 這個方法會實 IMediaFilter：： Run 方法。
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: 'CBaseMediaFilter： Run 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995193"
---
# <a name="cbasemediafilterrun-method"></a>CBaseMediaFilter 方法

`Run`方法會執行物件。 這個方法會實 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStart* 
</dt> <dd>

對應于資料流程時間0的參考時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

如果物件已停止，這個方法會藉由呼叫 [**CBaseMediaFilter：:P ause**](cbasemediafilter-pause.md) 方法來暫停物件。 然後，它會將 [**CBaseMediaFilter：： m \_ state**](cbasemediafilter-m-state.md) 成員變數設定為正在執行狀態 \_ 。

資料流程時間的計算方式為目前的參考時間減去 *tStart*。 時間戳記為零的媒體範例應該在時間 *tStart* 時轉譯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseMediaFilter 類別**](cbasemediafilter.md)
</dt> </dl>

 

 




