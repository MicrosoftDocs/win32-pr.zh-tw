---
description: MakePalette 方法會從色彩表以影片格式建立邏輯調色板。
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: 'CImagePalette. MakePalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989699"
---
# <a name="cimagepalettemakepalette-method"></a>CImagePalette. MakePalette 方法

`MakePalette`方法會從色彩表以影片格式建立邏輯調色板。

## <a name="syntax"></a>語法


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

包含 color 資料表之 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的指標。

</dd> <dt>

*szDevice* 
</dt> <dd>

字串的指標，其中包含由 GDI **EnumDisplayDevices** 函式所傳回之顯示裝置的名稱。 若要使用主顯示器裝置，請將此參數設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回檔色板的控制碼。 否則，會傳回 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImagePalette 類別**](cimagepalette.md)
</dt> </dl>

 

 




