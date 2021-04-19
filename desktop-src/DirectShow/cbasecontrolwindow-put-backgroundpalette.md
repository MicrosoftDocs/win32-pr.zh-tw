---
description: Put \_ BackgroundPalette 方法會設定旗標，以在背景中實現調色板。
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: 'CBaseControlWindow.put_BackgroundPalette 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989612"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a>CBaseControlWindow. put \_ BackgroundPalette 方法

`put_BackgroundPalette`方法會設定旗標，以在背景中實現調色板。

## <a name="syntax"></a>語法


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BackgroundPalette* 
</dt> <dd>

自動化布林值旗標 (0 是 off，1是) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

若要在另一個應用程式或檔內播放影片，應用程式可能會想要使用自己的調色板。 它可以將此旗標設定為1，要求影片使用目前的前景調色板，而不是它自己的背景調色板。 如果此設定為0，則視窗將會安裝並瞭解它自己慣用的調色板。 要求視窗使用不同的調色板將會造成嚴重的效能負面影響。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




