---
description: CompleteConnect 方法會通知視窗，轉譯器的輸入針腳已連接。
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: 'CBaseWindow. CompleteConnect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e04e0adf1d11a4878d860dd5c8a1eea9395095c71d8b5c86d6023a24ccdb28c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016706"
---
# <a name="cbasewindowcompleteconnect-method"></a>CBaseWindow. CompleteConnect 方法

`CompleteConnect`方法會通知視窗，轉譯器的輸入針腳已連接。

## <a name="syntax"></a>語法


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會重設視窗啟用旗標， ([**CBaseWindow：： m \_ BActivated**](cbasewindow-m-bactivated.md)) 設為 **FALSE**。 當影片轉譯器完成連接的連接時，它可能會呼叫 [**CBaseWindow：： ActivateWindow**](cbasewindow-activatewindow.md) 方法來設定視窗的大小和位置。 若要強制 **ActivateWindow** 重新計算這些屬性，請先呼叫 `CompleteConnect` 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




