---
description: 指出品質是否已變更的旗標。
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'CTransformFilter：： m_bQualityChanged 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454d8bad4ced2291b061b09992ad450d9e483f269e3fd72b192adbbacb077d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953607"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>CTransformFilter：： m \_ bQualityChanged 成員

指出品質是否已變更的旗標。 當篩選器第一次卸載範例時，它會將 [**EC \_ 品質 \_ 變更**](ec-quality-change.md) 事件傳送至篩選圖形管理員，並將此旗標設定為 **TRUE**。 除非篩選器停止並重新啟動，否則它不會再次傳送此事件，即使在此情況下，仍會繼續卸載範例。

## <a name="syntax"></a>Syntax


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




