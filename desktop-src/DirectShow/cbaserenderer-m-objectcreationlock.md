---
description: 鎖定以保護在篩選內建立物件。
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'CBaseRenderer：： m_ObjectCreationLock 成員 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b0925aab0345d5eed8da19e12f355c417d66c1f36a1384a05950a87d4c95b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429308"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>CBaseRenderer：： m \_ ObjectCreationLock 成員

鎖定以保護在篩選內建立物件。 當篩選建立輸入 pin ([**CBaseRenderer：： m \_ PInputPin**](cbaserenderer-m-pinputpin.md)) 或 [**CRendererPosPassThru**](crendererpospassthru.md) 物件 ([**CBaseRenderer：： m \_ pPosition**](cbaserenderer-m-pposition.md)) 時，會保留這個鎖定。 此鎖定可防止多個執行緒同時嘗試建立這些物件的其中一個。

## <a name="syntax"></a>Syntax


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




