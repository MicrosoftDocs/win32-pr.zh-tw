---
description: 旗標，指定物件是否以精確的批次傳遞範例。
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'COutputQueue：： m_bBatchExact 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5859744c3670ccc789ae5d87a619b3b32c3731580d473ff8cc6d775348771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087248"
---
# <a name="coutputqueuem_bbatchexact-member"></a>COutputQueue：： m \_ bBatchExact 成員

旗標，指定物件是否以精確的批次傳遞範例。

## <a name="syntax"></a>語法


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>備註

如果值為 **TRUE**，則物件會等到它擁有完整的媒體樣本批次，再傳遞任何。 否則，它會在抵達時傳遞範例。 [**COutputQueue：： m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)成員變數定義批次大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




