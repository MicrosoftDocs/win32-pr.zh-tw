---
description: RecordFrameLateness 方法會記錄轉譯發生的及時時間，並收集屬性頁面的統計資料。
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: 'CBaseVideoRenderer. RecordFrameLateness 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975979"
---
# <a name="cbasevideorendererrecordframelateness-method"></a>CBaseVideoRenderer. RecordFrameLateness 方法

`RecordFrameLateness`方法會記錄轉譯發生的及時時間，並收集屬性頁的統計資料。

## <a name="syntax"></a>語法


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*trLate* 
</dt> <dd>

值，指出取樣超過其到期時間的延遲時間（以參考時間單位為單位）。

</dd> <dt>

*trFrame* 
</dt> <dd>

在參考時間單位中的幀時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




