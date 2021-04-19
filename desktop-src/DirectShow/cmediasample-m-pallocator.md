---
description: 建立此範例的配置器指標。
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'CMediaSample：： m_pAllocator 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991540"
---
# <a name="cmediasamplem_pallocator-member"></a>CMediaSample：： m \_ pAllocator 成員

建立此範例的配置器指標。

## <a name="syntax"></a>語法


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>備註

雖然此範例會保留配置器的指標，但不會保留參考計數。 取而代之的是，配置器會在 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法中遞增自己的參考計數，並在 [**IMemAllocator：： ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) 方法中自行發行。 這可保證配置器將可供使用，只要另一個物件正在使用範例即可。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




