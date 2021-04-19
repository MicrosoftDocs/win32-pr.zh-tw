---
description: GetColourMask 方法會抓取目前顯示格式的色彩遮罩。
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: 'CImageDisplay. GetColourMask 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000988"
---
# <a name="cimagedisplaygetcolourmask-method"></a>CImageDisplay. GetColourMask 方法

方法會抓取 `GetColourMask` 目前顯示格式的色彩遮罩。

## <a name="syntax"></a>語法


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMaskRed* 
</dt> <dd>

接收紅色元件遮罩之變數的指標。

</dd> <dt>

*pMaskGreen* 
</dt> <dd>

接收綠色元件遮罩之變數的指標。

</dd> <dt>

*pMaskBlue* 
</dt> <dd>

接收藍色元件遮罩之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




