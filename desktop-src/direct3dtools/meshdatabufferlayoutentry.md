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
ms.openlocfilehash: 44cc67402c69b690ba9070fa51bf8d26f316faa7d10ac991226db2c05b6d6a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282269"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



