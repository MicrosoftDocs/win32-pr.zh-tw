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
ms.openlocfilehash: bb365c0af23868f05c624144de239828ce7c1d6cabacd3bf774c59d566348ff5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502718"
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

 

 




