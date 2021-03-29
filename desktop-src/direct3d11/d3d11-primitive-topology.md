---
description: 管線如何解讀系結至輸入組合語言階段的頂點資料。 這些基本拓撲值會決定在螢幕上呈現頂點資料的方式。
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: D3D11 \_ 基本 \_ 拓撲列舉
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104991858"
---
# <a name="d3d11_primitive_topology-enumeration"></a>D3D11 \_ 基本 \_ 拓撲列舉

管線如何解讀系結至輸入組合語言階段的頂點資料。 這些基本拓撲值會決定在螢幕上呈現頂點資料的方式。

## <a name="syntax"></a>Syntax


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_ \_ 未定義 D3D11 基本拓撲 \_**
</dt> <dd>

IA 階段尚未以基本拓撲初始化。 除非已定義基本拓撲，否則 IA 階段將無法正常運作。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ POINTLIST**
</dt> <dd>

將頂點資料解讀為點清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ LINELIST**
</dt> <dd>

將頂點資料解讀為線條清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11 \_ 基本 \_ 拓撲 \_ LINESTRIP**
</dt> <dd>

將頂點資料解讀為行帶。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ TRIANGLELIST**
</dt> <dd>

將頂點資料解讀為三角形清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ 基本 \_ 拓撲 \_ TRIANGLESTRIP**
</dt> <dd>

將頂點資料解讀為三角形帶。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ 基本 \_ 拓撲 \_ LINELIST \_ 形容詞**
</dt> <dd>

將頂點資料解讀為具有相鄰資料的線條清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ 基本 \_ 拓撲 \_ LINESTRIP \_ 形容詞**
</dt> <dd>

以相鄰資料的行帶來解讀頂點資料。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ 基本 \_ 拓撲 \_ TRIANGLELIST \_ 形容詞**
</dt> <dd>

將頂點資料解讀為具有相鄰資料的三角形清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ 基本 \_ 拓撲 \_ TRIANGLESTRIP \_ 形容詞**
</dt> <dd>

使用相鄰資料將頂點資料解讀為三角形帶。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 1 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 2 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 3 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 4 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 5 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 6 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 7 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 8 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 9 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 10 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 11 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 12 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 13 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 14 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 15 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 16 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 17 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 18 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 19 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 20 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 21 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 22 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 23 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 24 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 25 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 26 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 27 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 28 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 29 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 30 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 31 \_ 控制 \_ 點 \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 32 \_ 控制點 \_ \_ PATCHLIST**
</dt> <dd>

將頂點資料解讀為修補程式清單。

</dd> </dl>

## <a name="remarks"></a>備註

**D3D11 \_ 基本 \_ 拓撲** 列舉是 D3D11 .h 標頭檔中定義的類型，做為 [**D3D \_ 基本 \_ 拓撲**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology)列舉，在 D3DCommon .h 標頭檔中完整定義。
