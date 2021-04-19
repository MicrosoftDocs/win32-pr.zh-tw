---
description: M \_ pAlloc 成員變數是記憶體配置器的 IMemAllocator 介面指標。
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'CPullPin：： m_pAlloc 成員 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999652"
---
# <a name="cpullpinm_palloc-member"></a>CPullPin：： m \_ pAlloc 成員

`m_pAlloc`成員變數是記憶體配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)介面的指標。

## <a name="syntax"></a>語法


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>備註

[**CPullPin：:D ecideallocator**](cpullpin-decideallocator.md)方法會設定這個成員變數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




