---
description: OnRenderStart 方法會設定轉譯的資訊。
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: 'CBaseVideoRenderer. OnRenderStart 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995629"
---
# <a name="cbasevideorendereronrenderstart-method"></a>CBaseVideoRenderer. OnRenderStart 方法

`OnRenderStart`方法會設定轉譯的資訊。

## <a name="syntax"></a>語法


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

媒體範例的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此成員函式會從系統抓取目前的時鐘時間，並將它儲存在繪圖完成時要使用的成員變數中。 函數也會執行效能記錄。 此成員函式應該只在開始繪製之前呼叫。

此成員函式會覆寫 [**CBaseRenderer：： OnRenderStart**](cbaserenderer-onrenderstart.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




