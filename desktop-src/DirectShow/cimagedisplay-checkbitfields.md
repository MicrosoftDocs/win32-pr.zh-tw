---
description: CheckBitFields 方法會驗證 VIDEOINFO 結構中的色遮罩。
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: 'CImageDisplay. CheckBitFields 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995202"
---
# <a name="cimagedisplaycheckbitfields-method"></a>CImageDisplay. CheckBitFields 方法

`CheckBitFields`方法會驗證 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構中的色遮罩。

## <a name="syntax"></a>語法


```C++
BOOL CheckBitFields(
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

如果色彩遮罩有效，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法會確認每個色彩元件的色彩遮罩長度介於1到8個位之間，而且每個色彩遮罩都是連續的位序列。 只有當 **biCompression** 成員設定為 BI 位欄位時，才會呼叫這個方法 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




