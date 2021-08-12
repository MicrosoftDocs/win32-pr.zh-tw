---
description: M \_ bModifiesData 成員變數會指出篩選準則是否修改接收的範例資料。 值是在 CTransInPlaceFilter 的函式中設定，但預設為 TRUE。
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'CTransInPlaceFilter：： m_bModifiesData 成員 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7461f7f62a6cbd1fea2ff18f6e8f2e4b73825ea04cb9e3b0a679ee7cf15fef90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654877"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>CTransInPlaceFilter：： m \_ bModifiesData 成員

`m_bModifiesData`成員變數會指出篩選準則是否修改接收的範例資料。 值是在 **CTransInPlaceFilter** 的函式中設定，但預設為 **TRUE**。

## <a name="syntax"></a>語法


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>備註

這個變數會影響篩選器如何協調配置器。 如果值為 **TRUE**，則篩選器無法針對這兩個 pin 連線使用唯讀配置器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




