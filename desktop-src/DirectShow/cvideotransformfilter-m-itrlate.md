---
description: 表示樣本抵達轉譯器的延遲時間（以參考時間單位為單位）。 語法。
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'CVideoTransformFilter：： m_itrLate 成員 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba2d14d19849768538184e54de5ca84b9495371783d57231ab9ad6aa7738718
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075948"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>CVideoTransformFilter：： m \_ itrLate 成員

表示樣本抵達轉譯器的延遲時間（以參考時間單位為單位）。 Syntax

## <a name="syntax"></a>語法


```C++
int m_itrLate;
```



## <a name="remarks"></a>備註

當篩選從下游收到品質訊息時，它會將延遲值儲存在此變數中。 當篩選器卸載框架時，它會藉由減去每個畫面格的持續時間來更新此值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Vtrans (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CVideoTransformFilter 類別**](cvideotransformfilter.md)
</dt> </dl>

 

 




