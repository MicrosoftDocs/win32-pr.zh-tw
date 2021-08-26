---
description: SetPalette 方法會安裝視窗的調色板。 這個方法沒有任何參數。
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: CBaseWindow. SetPalette 方法 (Winutil .h) -沒有參數
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
ms.openlocfilehash: f15df65f6e427e467c14654a0e2745b84d774a5226b9a526193fc546261c5a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052148"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>CBaseWindow. SetPalette 方法 (Winutil .h) -沒有參數

`SetPalette`方法會安裝視窗的調色板。

## <a name="syntax"></a>語法


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | 描述                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | **GdiFlush** 的內部呼叫傳回錯誤。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                            |



 

## <a name="remarks"></a>備註

已選取 [**CBaseWindow：： m \_ hPalette**](cbasewindow-m-hpalette.md) 成員變數所指定的調色板。 呼叫端必須確保 **m \_ hPalette** 的有效性。

如果 [**CBaseWindow：： m \_ bNoRealize**](cbasewindow-m-bnorealize.md) 成員變數的值為 **FALSE** (預設) ，這個方法會選取並意識到這個調色板。 否則，它會選取元件，但不會察覺到。 物件不會刪除任何先前使用的調色板。 呼叫端負責刪除調色板。

任何執行緒都可以安全地呼叫這個方法，而不只是擁有視窗的執行緒。 視窗會將私用訊息傳送至本身，以觸發對 [**CBaseWindow：： OnPaletteChange**](cbasewindow-onpalettechange.md) 方法的呼叫。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | Winutil (包含： .h)  |
| 程式庫|  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




