---
description: CompleteConnect 方法會完成輸入 pin 與另一個 pin 的連接。
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: 'CBaseRenderer. CompleteConnect 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 833e19a6e7b100aac5322a54455c04c263569e33b3422d5957e5eeee15bbd283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157839"
---
# <a name="cbaserenderercompleteconnect-method"></a>CBaseRenderer. CompleteConnect 方法

`CompleteConnect`方法會完成輸入 pin 與另一個 pin 的連接。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pReceivePin* 
</dt> <dd>

輸出釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

篩選器的輸入圖釘會從其本身的方法中呼叫這個方法 `CompleteConnect` ，以完成 pin 連接。  (如需詳細資訊，請參閱 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md)。 ) 篩選準則會呼叫 [**CBaseRenderer：： SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) 方法來啟用 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




