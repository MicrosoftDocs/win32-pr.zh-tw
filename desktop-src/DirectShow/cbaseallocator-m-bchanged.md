---
description: 指出緩衝區需求是否已變更的旗標。
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'CBaseAllocator：： m_bChanged 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999668"
---
# <a name="cbaseallocatorm_bchanged-member"></a>CBaseAllocator：： m \_ bChanged 成員

指出緩衝區需求是否已變更的旗標。 [**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md)方法會將值設定為 **TRUE**。 在衍生類別中，純虛擬方法 [**CBaseAllocator：：**](cbaseallocator-alloc.md) 配置應將值設回 **FALSE**。 一旦配置了緩衝區，就不需要重新配置它們，而 *m \_ BChanged* 為 **FALSE**。

## <a name="syntax"></a>Syntax


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




