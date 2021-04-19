---
description: 取得邊框 \_ 型方法會抓取目前的框線色彩。
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: 'CBaseControlWindow.get_BorderColor 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994599"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a>CBaseControlWindow. 取得 \_ 邊框方法

方法會抓取 `get_BorderColor` 目前的框線色彩。

## <a name="syntax"></a>語法


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*色彩* 
</dt> <dd>

目前框線色彩的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

應用程式可以設定應該顯示影片的目的地矩形。 這個矩形相對於視窗的工作區。 如果這樣做 (預設為一律繪製整個視窗) ，則會在影片周圍加上框線。 這個屬性會影響框線所使用的色彩。 雖然參數指定為 **LONG** 類型，但其實是 **COLORREF** 值。

此成員函式的目的是要透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面呼叫外部物件，因此會鎖定重要區段以與相關聯的篩選進行同步處理。 呼叫 [**CBaseControlWindow：： GetBorderColour**](cbasecontrolwindow-getbordercolour.md) 成員函式，以取得此屬性（如果不是從外部物件呼叫）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




