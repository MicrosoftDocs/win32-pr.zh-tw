---
description: 判斷來源矩形是否有效。
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: 'CBaseControlVideo. CheckSourceRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf7ac41d626eceee048afc4671a5e171e7164adfbd9a941b1b70bc85ea988c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873008"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a>CBaseControlVideo. CheckSourceRect 方法

判斷來源矩形是否有效。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSourceRect* 
</dt> <dd>

要檢查的來源矩形指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果無效 \_ ，則傳回 E INVALIDARG，否則會傳回 >aad-userreadusingalternativesecurityid-noerror (S \_ OK) 。

## <a name="remarks"></a>備註

此成員函式會檢查所要求的來源矩形是否未超過可用的來源影片。 左邊和上座標不可為負值，而且寬度和高度不能超過影片的右邊和底部。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




