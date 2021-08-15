---
description: '\#從 FOURCCMap 物件中抓取 FOURCC&160; DWORD。'
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'FOURCCMap：： GetFOURCC 方法 (Fourcc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 381625f5d0a585f212c8f7b076d1cd58ea5215958bf09025e1db864ce2f624b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015716"
---
# <a name="fourccmapgetfourcc-method"></a>FOURCCMap：： GetFOURCC 方法

從 [**FOURCCMap**](fourccmap.md)物件中抓取 **FOURCC** 的 **DWORD** 。

## <a name="syntax"></a>語法


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **FOURCC** **DWORD** 值。 請注意，如果您所建立的 **GUID** 原本並非衍生自 **FOURCC**，則傳回值基本上會是隨機的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Fourcc (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FOURCCMap 類別**](fourccmap.md)
</dt> </dl>

 

 




