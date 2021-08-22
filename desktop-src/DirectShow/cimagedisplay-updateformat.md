---
description: UpdateFormat 方法會填入 VIDEOINFO 結構的一些選擇性成員。
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: 'CImageDisplay. UpdateFormat 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e46065aae630132a1d7fd38a6d331009a537af18c12687fcbecd22dd7bf78b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119257198"
---
# <a name="cimagedisplayupdateformat-method"></a>CImageDisplay. UpdateFormat 方法

`UpdateFormat`方法會填入 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構的一些選擇性成員。

## <a name="syntax"></a>語法


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

**VIDEOINFO** 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會將 **biClrUsed**、 **biClrImportant** 和 **biSizeImage** 成員設定為正確的值，並清除來源和目標矩形。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




