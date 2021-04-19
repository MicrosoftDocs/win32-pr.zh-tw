---
description: PreparePalette 方法會根據擁有篩選器中的媒體類型來設定調色板。
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: 'CImagePalette. PreparePalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992801"
---
# <a name="cimagepalettepreparepalette-method"></a>CImagePalette. PreparePalette 方法

`PreparePalette`方法會根據擁有篩選準則的媒體類型來設定調色板。

## <a name="syntax"></a>語法


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pmtNew* 
</dt> <dd>

新媒體類型的指標。 格式區塊必須是 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。

</dd> <dt>

*pmtOld* 
</dt> <dd>

舊媒體類型的指標。 如果是第一次設定媒體類型，這個參數可以是空的型別，而且沒有格式區塊。 否則，格式區塊必須是 **VIDEOINFOHEADER** 結構。

</dd> <dt>

*szDevice* 
</dt> <dd>

字串的指標，其中包含由 GDI **EnumDisplayDevices** 函式所傳回之顯示裝置的名稱。 若要使用主顯示器裝置，請將此參數設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已 \_ 更新調色板，則傳回，如果調色板未變更，則傳回 \_ FALSE。

## <a name="remarks"></a>備註

如果需要更新調色板，這個方法會執行下列動作：

-   呼叫 [**CImagePalette：： MakePalette**](cimagepalette-makepalette.md) 來建立新的邏輯調色板。
-   將 [**EC \_ 調色板 \_ 已變更**](ec-palette-changed.md) 事件傳送至篩選圖形管理員。
-   在 **CBaseWindow** 物件上呼叫 [**CBaseWindow：： SetPalette**](cbasewindow-setpalette.md) 。
-   在 **CDrawImage** 物件上呼叫 [**CDrawImage：： IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImagePalette 類別**](cimagepalette.md)
</dt> </dl>

 

 




