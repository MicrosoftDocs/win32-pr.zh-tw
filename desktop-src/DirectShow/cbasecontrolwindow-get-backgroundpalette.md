---
description: Get \_ BackgroundPalette 方法會抓取背景旗標中的已實現調色板。
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: 'CBaseControlWindow.get_BackgroundPalette 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63ea3fa8ecbc6e644ccc5f4b1fac7a2fcd9c18270474f45dc08faa164f76cbec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660773"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>CBaseControlWindow. 取得 \_ BackgroundPalette 方法

方法會抓取 `get_BackgroundPalette` 背景旗標中的已實現調色板。

## <a name="syntax"></a>語法


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBackgroundPalette* 
</dt> <dd>

自動化布林值旗標的指標 (0 是 off，1是) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會實 [**IVideoWindow：： get \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) 方法。 如果影片將會在另一個應用程式或檔中播放，則應用程式可能會想要使用自己的調色板。 它可以將此旗標設定為1，要求影片使用目前的前景調色板，而不是其本身。 如果此設定為0，則視窗將會安裝並瞭解它自己慣用的調色板。 請注意，要求視窗使用不同的調色板將會造成嚴重的效能負面影響。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




