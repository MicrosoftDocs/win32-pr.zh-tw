---
description: HideCursor 方法會隱藏或顯示資料指標。
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: 'CBaseControlWindow. HideCursor 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999266"
---
# <a name="cbasecontrolwindowhidecursor-method"></a>CBaseControlWindow. HideCursor 方法

`HideCursor`方法會隱藏或顯示資料指標。

## <a name="syntax"></a>語法


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*HideCursor* 
</dt> <dd>

值，指定是否要顯示資料指標。 設定為 [OATRUE] 可隱藏資料指標，或設定為 [OAFALSE] 以顯示資料指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




