---
description: 表示網格的緩衝區配置中單一專案的相關資訊。
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MeshDataBufferLayoutEntry 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 40360e73f480b4c12dcb24311c26fd9718093705
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625354"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry 結構

表示網格的緩衝區配置中單一專案的相關資訊。

## <a name="syntax"></a>語法


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>成員

**pName**  
包含專案名稱的 COM 字串。

**numComponents**  
組成此專案)  (值的同質元件數目。

**isPosition**  
如果專案是位置，則為 true;否則為 false。

**format**  
專案 (註冊) 的資料格式。 如需詳細資訊，請參閱註冊 \_ 格式列舉。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



