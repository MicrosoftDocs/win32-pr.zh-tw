---
description: 用來序列化狀態變更的重要區段指標。
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'CBaseFilter：： m_pLock 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc8d3b627e6cd8c3ae4821864f6980db5acd251c721bb8841be40e04377ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659791"
---
# <a name="cbasefilterm_plock-member"></a>CBaseFilter：： m \_ pLock 成員

用來序列化狀態變更的重要區段指標。

## <a name="syntax"></a>語法


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>備註

這個變數會在類別的函式中初始化;請參閱 [**CBaseFilter：： CBaseFilter**](cbasefilter-cbasefilter.md)。

在狀態轉換期間，或當方法存取數個作業的狀態時，請保留此重要區段。 基底類別會保存下列方法中的重要區段：

-   [**CBaseFilter::FindPin**](cbasefilter-findpin.md)
-   [**CBaseFilter::GetSyncSource**](cbasefilter-getsyncsource.md)
-   [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md)
-   [**CBaseFilter：： IsActive**](cbasefilter-isactive.md)
-   [**CBaseFilter::SetSyncSource**](cbasefilter-setsyncsource.md)
-   [**CBaseFilter：:P ause**](cbasefilter-pause.md)
-   [**CBaseFilter：： Run**](cbasefilter-run.md)
-   [**CBaseFilter：： Stop**](cbasefilter-stop.md)

請勿在串流作業期間保留此重要區段， (也就是將範例傳遞給下游篩選) 時。 使用不同的重要區段序列化串流作業。 否則，它可能會造成鎖死。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> <dt>

[執行緒和重要區段](threads-and-critical-sections.md)
</dt> </dl>

 

 




