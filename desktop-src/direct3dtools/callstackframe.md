---
description: 代表呼叫堆疊上框架的相關資訊。
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CallStackFrame 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c6cb4b0e32213165149d7df8c7bf334049e37399
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631336"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>CallStackFrame 結構

代表呼叫堆疊上框架的相關資訊。

## <a name="syntax"></a>語法


```C++
} CallStackFrame;
```

## <a name="members"></a>成員

**functionName**  
COM 字串，其中包含相關聯的函式名稱。

**sourceFile**  
COM 字串，其中包含相關原始程式檔的 filepath。

**moduleName**  
COM 字串，其中包含相關聯程式碼模組的名稱。

**lineNumber**  
關聯的行號。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



