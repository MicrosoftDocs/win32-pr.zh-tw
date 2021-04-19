---
description: 參考計數。
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'CUnknown：： m_cRef 成員 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94ff5d88ca48feeb46a8b0411a55d6261aefcf6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984383"
---
# <a name="cunknownm_cref-member"></a>CUnknown：： m \_ cRef 成員

參考計數。

## <a name="syntax"></a>語法


```C++
LONG m_cRef;
```



## <a name="remarks"></a>備註

如果您覆寫 [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) 或 [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) 方法，請使用這個成員變數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




