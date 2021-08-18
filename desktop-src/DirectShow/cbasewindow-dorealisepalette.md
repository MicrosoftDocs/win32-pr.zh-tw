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
ms.openlocfilehash: ce593939ec9f8aa3f2675c95e7a70363465aabb6f501fde79de839c533a1d249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757478"
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



| 傳回碼                                                                             | 描述                                                    |
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

 

 




