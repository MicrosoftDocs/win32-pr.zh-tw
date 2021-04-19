---
description: DoRealisePalette 方法會發現視窗的目前調色板。
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: 'CBaseWindow. DoRealisePalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991555"
---
# <a name="cbasewindowdorealisepalette-method"></a>CBaseWindow. DoRealisePalette 方法

方法會發現 `DoRealisePalette` 視窗的目前調色板。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bForceBackground* 
</dt> <dd>

布林值，指定是否要將調色板強制為背景調色板。 如需詳細資訊，請參閱 Platform SDK 中的 **SelectPalette** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | Description                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | **GdiFlush** 的內部呼叫傳回錯誤。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                            |



 

## <a name="remarks"></a>備註

[**CBaseWindow：： OnPaletteChange**](cbasewindow-onpalettechange.md)方法會呼叫這個方法。 若要設定新的調色板，請呼叫 [**CBaseWindow：： SetPalette**](cbasewindow-setpalette.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




