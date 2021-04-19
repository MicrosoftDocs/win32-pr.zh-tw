---
description: 函式方法。
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: 'CBaseWindow. CBaseWindow (Winutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1741f8596210afac676a7e81f57b46e18fbba9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983975"
---
# <a name="cbasewindowcbasewindow-constructor"></a>CBaseWindow. CBaseWindow 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bDoGetDC* 
</dt> <dd>

指定是否要取出裝置內容的布林值。

</dd> <dt>

*bPostToDestroy* 
</dt> <dd>

指定 [**CBaseWindow：： m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) 成員變數的布林值。

</dd> </dl>

## <a name="remarks"></a>備註

建立物件之後，請呼叫 [**CBaseWindow：:P reparewindow**](cbasewindow-preparewindow.md) 方法來建立視窗。 **PrepareWindow** 是虛擬方法。 它會呼叫 [**CBaseWindow：： InitialiseWindow**](cbasewindow-initialisewindow.md)，也是虛擬方法。 這些方法會與函式分開，讓衍生的類別可以在必要時加以覆寫。

如果 *bDoGetDC* 參數的值為 **TRUE**，則物件會 `CBaseWindow` (DC) 抓取視窗的裝置內容控制碼，並將其儲存在 [**CBaseWindow：： m \_ hdc**](cbasewindow-m-hdc.md) 成員變數中。 物件也會建立相容的記憶體 DC，它會儲存在 [**CBaseWindow：： m \_ MemoryDC**](cbasewindow-m-memorydc.md) 成員變數中。 這些動作會在 **InitialiseWindow** 方法中進行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




