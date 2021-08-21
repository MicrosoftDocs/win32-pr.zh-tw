---
description: 包含緩衝區之記憶體區塊的指標。
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: 'CMemAllocator：： m_pBuffer 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fa9c56c5a90c1fa3fde7dda4bca82cd3f473a591db9e2e24f0b1d141c6aa33e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155980"
---
# <a name="cmemallocatorm_pbuffer-member"></a>CMemAllocator：： m \_ pBuffer 成員

包含緩衝區之記憶體區塊的指標。

## <a name="syntax"></a>語法


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a>備註

範例緩衝區會計算為此指標的位移。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMemAllocator 類別**](cmemallocator.md)
</dt> </dl>

 

 




