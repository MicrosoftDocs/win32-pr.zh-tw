---
description: 指定視窗是否張貼或傳送其損毀訊息的旗標。
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'CBaseWindow：： m_bDoPostToDestroy 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993444"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>CBaseWindow：： m \_ bDoPostToDestroy 成員

指定視窗是否張貼或傳送其損毀訊息的旗標。 若 **為 TRUE**， [**CBaseWindow：:D onewithwindow**](cbasewindow-donewithwindow.md) 方法會使用 **PostMessage** 函式，將私用的終結訊息傳送給自己。 如果 **為 FALSE**，則 **DoneWithWindow** 會使用 **SendMessage** 函數來傳送訊息。 依預設，此值為 **FALSE**。

## <a name="syntax"></a>Syntax


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




