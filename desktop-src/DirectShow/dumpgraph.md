---
description: DumpGraph 函式會將篩選圖形的相關資訊傳送至偵錯工具的輸出位置。 在零售組建中略過。
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: 'DumpGraph 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994344"
---
# <a name="dumpgraph-function"></a>DumpGraph 函式

`DumpGraph`函數會將篩選圖形的相關資訊傳送至偵錯工具輸出位置。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGraph* 
</dt> <dd>

篩選圖形管理員上 [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) 介面的指標。

</dd> <dt>

*dwLevel* 
</dt> <dd>

記錄層級。 函數會產生 \_ 具有指定記錄層級的記錄追蹤訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Debug Output 函數](debug-output-functions.md)
</dt> </dl>

 

 




