---
description: SetPalette 方法會安裝視窗的調色板。
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: 'CBaseWindow. SetPalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994210"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a>CBaseWindow. SetPalette 方法 (Winutil .h) 

`SetPalette`方法會安裝視窗的調色板。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPalette* 
</dt> <dd>

新調色板的控制碼。 不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | Description                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | **GdiFlush** 的內部呼叫傳回錯誤。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                            |



 

## <a name="remarks"></a>備註

如果 [**CBaseWindow：： m \_ bNoRealize**](cbasewindow-m-bnorealize.md) 成員變數的值為 **FALSE** (預設) ，這個方法會選取並意識到這個調色板。 否則，它會選取元件，但不會察覺到。 物件不會刪除任何先前使用的調色板。 呼叫端負責刪除調色板。

任何執行緒都可以安全地呼叫這個方法，而不只是擁有視窗的執行緒。 視窗會將私用訊息傳送至本身，以觸發對 [**CBaseWindow：： OnPaletteChange**](cbasewindow-onpalettechange.md) 方法的呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




