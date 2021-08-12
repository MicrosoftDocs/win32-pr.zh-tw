---
description: GetDestinationPosition 方法會在一個不可部分完成的作業中抓取目的地矩形。
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: 'CBaseControlVideo. GetDestinationPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b077548e6a427e70d098cbece93cdc033972cf48a664dd85cd0dfab747d88c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661138"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a>CBaseControlVideo. GetDestinationPosition 方法

`GetDestinationPosition`方法會在一個不可部分完成的作業中抓取目的地矩形。

## <a name="syntax"></a>語法


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pLeft* 
</dt> <dd>

目的地矩形左座標的指標。

</dd> <dt>

*pTop* 
</dt> <dd>

目的地矩形的上方座標指標。

</dd> <dt>

*pWidth* 
</dt> <dd>

目的地矩形的寬度指標。

</dd> <dt>

*pHeight* 
</dt> <dd>

目的地矩形高度的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。



| 傳回碼                                                                                           | 描述                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ 失敗**</dt> </dl>                | 失敗。<br/>                                                              |
| <dl> <dt>**E \_ 指標**</dt> </dl>             | **Null** 指標引數。<br/>                                            |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 無法執行作業，因為沒有連接的釘選。<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | 成功。<br/>                                                              |



 

## <a name="remarks"></a>備註

這個成員函式可以用來取代對 [**CBaseControlVideo：： get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)、 [**CBaseControlVideo：： get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)、 [**CBaseControlVideo：： get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)和 [**CBaseControlVideo：： get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) 成員函式的個別呼叫。 應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。 來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。 目的地矩形相對於現正播放之視窗的工作區。 視窗的左上角是座標 (0，0) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




