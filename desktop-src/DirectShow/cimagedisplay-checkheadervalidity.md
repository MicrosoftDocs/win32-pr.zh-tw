---
description: CheckHeaderValidity 方法會驗證 BITMAPINFOHEADER 結構。 這個方法僅適用于未壓縮的 RGB 類型，不適用於壓縮類型或 YUV 類型。
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: 'CImageDisplay. CheckHeaderValidity 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995626"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>CImageDisplay. CheckHeaderValidity 方法

`CheckHeaderValidity`方法會驗證 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構。 這個方法僅適用于未壓縮的 RGB 類型，不適用於壓縮類型或 YUV 類型。

## <a name="syntax"></a>語法


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInput* 
</dt> <dd>

包含 **BITMAPINFOHEADER** 結構之 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 **BITMAPINFOHEADER** 有效，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法會檢查影像維度是否為非負值;壓縮類型為 BI \_ RGB 或 bi \_ 位欄位; 色彩深度和色彩遮罩有效; **biPlanes** 成員等於 1; **biSize** 和 **biSizeImage** 成員是正確的。 它也會檢查調色板專案中的常見錯誤（如果有的話）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




