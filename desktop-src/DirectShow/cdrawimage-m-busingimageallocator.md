---
description: M \_ bUsingImageAllocator 成員變數會指出釘選連接的配置器是否為 CImageAllocator 物件。 如果該值為 TRUE，則配置器是 CImageAllocator 物件 (或衍生自該類別) 。
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'CDrawImage：： m_bUsingImageAllocator 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf60184758598872577e0c6b293f8eb0b72c5bf7305f1516a4dd6b5a4a639b94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657106"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>CDrawImage：： m \_ bUsingImageAllocator 成員

`m_bUsingImageAllocator`成員變數會指出釘選連接的配置器是否為 **CImageAllocator** 物件。 如果該值為 **TRUE**，則配置器是 **CImageAllocator** 物件 (或衍生自該類別) 。

## <a name="syntax"></a>語法


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>備註

當此值為 **TRUE** 時， **CDrawImage** 物件可以使用 GDI **BitBlt** 和 **StretchBlt** 函式來轉譯影像，而不是使用較慢的 **SetDIBitsToDevice** 和 **StretchDIBits** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




