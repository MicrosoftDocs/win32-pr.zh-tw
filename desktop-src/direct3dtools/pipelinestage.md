---
description: 表示管線階段，包括所使用之著色器的詳細資料。
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PipeLineStage 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935783"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>PipeLineStage 結構

表示管線階段，包括所使用之著色器的詳細資料。

## <a name="syntax"></a>語法


```C++
} PipeLineStage;
```

## <a name="members"></a>成員

**StageId**  
管線階段的識別碼。

**可偵錯**  
如果管線階段支援調試，則為 true。否則為 false。

**StageName**  
包含管線階段名稱的 COM 字串。

**GuaranteedOutput**  
如果管線階段一律具有管線輸出，則為 true。否則為 false。

**DebugEntryPoint**  
包含著色器進入點名稱的 COM 字串（如果有的話）。

**ShaderFile**  
COM 字串，其中包含著色器原始程式檔的 filepath。

**ShaderByteStreamPtr**  
著色器位元組資料流程的 FILEPTR。 這會傳回，以便進行 debug。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



