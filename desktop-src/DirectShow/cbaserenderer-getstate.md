---
description: '>getstate 方法會 (執行中、已停止或已暫停的) 來抓取篩選的狀態。'
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: 'CBaseRenderer. >getstate 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997643"
---
# <a name="cbaserenderergetstate-method"></a>CBaseRenderer. >getstate 方法

`GetState`方法會 (執行中、已停止或已暫停) 來抓取篩選的狀態。

## <a name="syntax"></a>語法


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwMilliSecsTimeout* 
</dt> <dd>

逾時間隔（以毫秒為單位）。

</dd> <dt>

*State* 
</dt> <dd>

變數的指標，此變數會接收 [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員，以指出篩選的狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                | Description                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                                            |
| <dl> <dt>**VFW \_ S \_ 州 \_ 中繼**</dt> </dl> | 篩選正在轉換成指定的狀態。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>                  | **Null** 指標引數。<br/>                          |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseFilter：： >getstate**](cbasefilter-getstate.md) 方法。 當轉譯器暫停時，它不會完成狀態轉換，直到它收到要轉譯的樣本為止。 如果超時時間在狀態轉換完成之前過期，則方法會傳回 VFW \_ S \_ 狀態 \_ 中繼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




