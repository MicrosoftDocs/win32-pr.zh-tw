---
description: 表示著色器偵錯工具要求的相關資訊。
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DebugShaderRequestInfo 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510058"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo 結構

表示著色器偵錯工具要求的相關資訊。

## <a name="syntax"></a>語法


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a>成員

**階段**  
要進行調試的管線階段。

**eventID**  
要進行偵錯工具之圖形事件的識別碼。

**frameNumber**  
要進行調試的框架。

**頂點**  
要調試的頂點。

**像素**  
要調試的圖元。

**groupCoordinates**  
要進行偵錯工具之群組的座標。

**threadCoordinates**  
要進行偵錯工具之執行緒的座標

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



