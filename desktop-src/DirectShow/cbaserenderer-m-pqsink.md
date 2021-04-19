---
description: 物件的指標，該物件會接收品質控制訊息。
ms.assetid: bf4fd84c-9522-4686-9fb1-17a2ce3e5a16
title: 'CBaseRenderer：： m_pQSink 成員 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pQSink
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 331504ffaeb74d84382b65d1332f6dbe7c9556dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000423"
---
# <a name="cbaserendererm_pqsink-member"></a>CBaseRenderer：： m \_ pQSink 成員

物件的指標，該物件會接收品質控制訊息。

## <a name="syntax"></a>語法


```C++
IQualityControl *m_pQSink;
```



## <a name="remarks"></a>備註

基類不會執行品質控制項。 此成員變數預設為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




