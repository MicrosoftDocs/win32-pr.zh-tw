---
description: CheckPaletteHeader 方法會驗證 VIDEOINFO 結構中的調色板專案。
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: 'CImageDisplay. CheckPaletteHeader 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981388"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>CImageDisplay. CheckPaletteHeader 方法

`CheckPaletteHeader`方法會驗證 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構中的調色板專案。

## <a name="syntax"></a>語法


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInput* 
</dt> <dd>

**VIDEOINFO** 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果調色板專案有效，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果影像格式不是調色盤，方法會確認 **biClrUsed** 等於零。 否則，此方法會驗證 **biCompression** 旗標是否為 BI \_ RGB; **biClrImportant** 不大於 **biClrUsed**;而且，如果有色彩深度，則調色板專案的數目不會超過最大值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




