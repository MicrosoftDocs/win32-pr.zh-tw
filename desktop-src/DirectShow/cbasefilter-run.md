---
description: Run 方法會執行篩選。 這個方法會實 IMediaFilter：： Run 方法。
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: 'CBaseFilter： Run 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6259e6ce00b0a2f93e0b71d6b44d1c6ed4aa65eaadca21ed0a78f1d16d98a42b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793278"
---
# <a name="cbasefilterrun-method"></a>CBaseFilter 方法

`Run`方法會執行篩選。 這個方法會實 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法。

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

\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

如果篩選已停止，則這個方法會藉由呼叫 [**CBaseFilter：:P ause**](cbasefilter-pause.md) 方法來暫停篩選。 然後，它會在每個篩選器的連接釘上呼叫 [**CBasePin：： Run**](cbasepin-run.md) 方法。 最後，它會將 [**CBaseFilter：： m \_ state**](cbasefilter-m-state.md) 成員變數設定為 \_ 正在執行狀態。

資料流程時間的計算方式為目前的參考時間減去 *tStart*。 時間戳記為零的媒體範例應該在時間 *tStart* 時轉譯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




