---
description: 媒體範例佇列。
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'COutputQueue：： m_List 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994297"
---
# <a name="coutputqueuem_list-member"></a>COutputQueue：： m \_ List 成員

媒體範例佇列。

## <a name="syntax"></a>語法


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>備註

這個成員變數是 [**CGenericList**](cgenericlist.md) 物件的指標，該物件會保存 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 指標。 **CSampleList** 類型的定義如下：

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




