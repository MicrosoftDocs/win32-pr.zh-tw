---
description: 模組實例的控制碼。
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'CBaseWindow：： m_hInstance 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999141"
---
# <a name="cbasewindowm_hinstance-member"></a>CBaseWindow：： m \_ hInstance 成員

模組實例的控制碼。

## <a name="syntax"></a>語法


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>備註

DLL 進入點函數會使用模組實例的控制碼來設定全域變數。 **CBaseWindow** 類別會將此控制碼儲存在其函式方法中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




