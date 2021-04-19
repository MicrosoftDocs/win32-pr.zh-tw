---
description: GetBitMasks 方法會抓取指定 VIDEOINFO 格式的色彩遮罩。
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: 'CImageDisplay. GetBitMasks 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998643"
---
# <a name="cimagedisplaygetbitmasks-method"></a>CImageDisplay. GetBitMasks 方法

方法會抓取 `GetBitMasks` 指定 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 格式的色彩遮罩。

## <a name="syntax"></a>語法


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

**VIDEOINFO** 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回三個 **DWORD** 值的陣列。

## <a name="remarks"></a>備註

如果 **biCompression** 成員是 BI \_ 位欄位，此方法會傳回 **dwBitMasks** 成員中所提供之色彩遮罩的指標。 如果 **biCompression** 成員是 BI \_ RGB，則方法會傳回對應于位深度的色彩遮罩。 如果方法失敗 (例如，位深度小於 16) ，則方法會傳回陣列 {0,0,0} 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




