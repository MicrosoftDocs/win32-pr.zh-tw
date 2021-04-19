---
description: IsCursorHidden 方法會抓取 m \_ bCursorHidden 資料成員的目前狀態。
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: 'CBaseControlWindow. IsCursorHidden 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996514"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a>CBaseControlWindow. IsCursorHidden 方法

方法會抓取 `IsCursorHidden` **m \_ bCursorHidden** 資料成員的目前狀態。

## <a name="syntax"></a>語法


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CursorHidden* 
</dt> <dd>

**M \_ bCursorHidden** 值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用參數呼叫時，如果資料指標是隱藏的，則會傳回 OATRUE，如果資料指標是可見的，則會傳回 OAFALSE。

## <a name="remarks"></a>備註

內建物件應該在沒有 *CursorHidden* 參數的情況下呼叫此成員函式，以避免鎖定重要區段。 外部物件會透過 [**IVideoWindow：： IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden)方法，使用 *CursorHidden* 參數存取這個成員函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




