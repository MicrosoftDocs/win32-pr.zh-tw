---
description: 保護串流狀態的重要區段。 如需詳細資訊，請參閱篩選開發人員的資料流程。
ms.assetid: f77c3129-ca25-47b8-8a6e-3a07169701af
title: 'CTransformFilter：： m_csReceive 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csReceive
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 542f108cee8dbe761040ef8474ae7cec565e0b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995410"
---
# <a name="ctransformfilterm_csreceive-member"></a>CTransformFilter：： m \_ csReceive 成員

保護串流狀態的重要區段。 如需詳細資訊，請參閱 [篩選開發人員的](data-flow-for-filter-developers.md)資料流程。

## <a name="syntax"></a>Syntax


```C++
CCritSec m_csReceive;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




