---
description: Receive 方法會接收資料流程中的下一個媒體範例。
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: 'CBaseRenderer 的 Receive 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983256"
---
# <a name="cbaserendererreceive-method"></a>CBaseRenderer 接收方法

`Receive`方法會接收資料流程中的下一個媒體範例。

## <a name="syntax"></a>語法


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

輸入 pin 會在從上游篩選器收到範例時呼叫這個方法。

如果篩選器正在執行，這個方法會執行下列步驟：

1.  排定轉譯 ([**CBaseRenderer：:P reparereceive**](cbaserenderer-preparereceive.md)) 的範例。
2.  等候排程的時間 ([**CBaseRenderer：： WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) 。
3.  轉譯 ([**CBaseRenderer：： Render**](cbaserenderer-render.md)) 的範例。
4.  釋放範例 ([**CBaseRenderer：： ClearPendingSample**](cbaserenderer-clearpendingsample.md)) 。

如果已暫停篩選，則方法會執行下列步驟：

1.  通知衍生類別 ([**CBaseRenderer：： OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)) 提供範例。
2.  等候排程的時間。
3.  呈現範例。
4.  釋放範例。

暫停時，方法會在步驟2中等候，直到篩選切換到執行中狀態。 在該時間點，篩選會排定範例。

在基類中， **OnReceiveFirstSample** 方法不會執行任何動作。 衍生的類別可以覆寫它。 例如，當影片轉譯器暫停時，會將第一個範例顯示為靜止影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




