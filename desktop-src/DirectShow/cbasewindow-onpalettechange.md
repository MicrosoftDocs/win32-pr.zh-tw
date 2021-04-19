---
description: OnPaletteChange 方法會處理調色板變更訊息。
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: 'CBaseWindow. OnPaletteChange 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994211"
---
# <a name="cbasewindowonpalettechange-method"></a>CBaseWindow. OnPaletteChange 方法

`OnPaletteChange`方法會處理調色板變更訊息。

## <a name="syntax"></a>語法


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> <dt>

*訊息* 
</dt> <dd>

訊息識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已處理訊息，則傳回 0; 如果未處理訊息，則傳回1。

## <a name="remarks"></a>備註

這個方法會處理 WM \_ PALETTECHANGED 和 wm \_ QUERYNEWPALETTE 訊息。 它會呼叫 [**CBaseWindow：:D orealisepalette**](cbasewindow-dorealisepalette.md) 方法，以實現新的調色板。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




