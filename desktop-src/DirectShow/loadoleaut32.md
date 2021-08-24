---
description: LoadOLEAut32 函式會將 Automation 動態連結程式庫 (OleAut32.dll) 載入。
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: 'LoadOLEAut32 函式 (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ca5832246e90e1df207754dc33380547b8193829394d81e6b2b757fccf79a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502308"
---
# <a name="loadoleaut32-function"></a>LoadOLEAut32 函式

**LoadOLEAut32** 函式會將 Automation 動態連結程式庫 (OleAut32.dll) 載入。

## <a name="syntax"></a>語法


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

傳回 Automation DLL 實例的控制碼。

## <a name="remarks"></a>備註

當 [**CBaseObject**](cbaseobject.md) 的函式終結 OleAut32.dll 載入的物件時，它會卸載程式庫（如果仍載入）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COM Helper 函數**](com-helper-functions.md)
</dt> </dl>

 

 




