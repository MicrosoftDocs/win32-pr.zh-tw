---
description: PrepareWindow 方法會建立視窗。
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: 'CBaseWindow. PrepareWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991216"
---
# <a name="cbasewindowpreparewindow-method"></a>CBaseWindow. PrepareWindow 方法

`PrepareWindow`方法會建立視窗。

## <a name="syntax"></a>語法


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                            | Description         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 失敗。<br/> |



 

## <a name="remarks"></a>備註

建立物件之後，請呼叫這個方法。 這個方法會執行一些初始的簿記，然後呼叫 [**CBaseWindow：:D ocreatewindow**](cbasewindow-docreatewindow.md) 方法來建立視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




