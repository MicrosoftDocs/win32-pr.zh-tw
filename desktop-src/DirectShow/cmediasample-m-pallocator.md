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
ms.openlocfilehash: 646c6fb7f8236aca87b5aebd1d30fd67750d960da4445d45bf45d8b601320274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156540"
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

 

 




