---
description: GetBorderColour 方法會抓取目前的視窗框線色彩 m \_ BorderColour。
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: 'CBaseControlWindow. GetBorderColour 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994340"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>CBaseControlWindow. GetBorderColour 方法

方法會抓取 `GetBorderColour` 目前的視窗框線色彩 **m \_ BorderColour**。

## <a name="syntax"></a>語法


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回框線的色彩。

## <a name="remarks"></a>備註

應用程式可以設定目的地矩形來顯示影片。 這個矩形應該相對於視窗的工作區。 如果這樣做 (預設為一律繪製整個視窗) ，則會有一個圍繞影片的區域;亦即框線。 框線色彩可透過 [**CBaseControlWindow：:p 的 ui \_ 邊框**](cbasecontrolwindow-put-bordercolor.md) 型成員函式來設定。 這個屬性會影響框線的色彩。 除非您是透過 [**IVideoWindow：： get \_**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) CBaseControlWindow，否則請使用此成員函式，而不是使用 [**：： get \_ 邊框**](cbasecontrolwindow-get-bordercolor.md)式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




