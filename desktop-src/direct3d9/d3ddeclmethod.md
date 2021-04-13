---
description: 定義頂點宣告方法，這是鑲嵌 (所執行的預先定義作業，或是在鑲嵌) 期間，頂點資料上的任何程式性幾何常式。
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: 'D3DDECLMETHOD 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322731"
---
# <a name="d3ddeclmethod-enumeration"></a>D3DDECLMETHOD 列舉

定義頂點宣告方法，這是鑲嵌 (所執行的預先定義作業，或是在鑲嵌) 期間，頂點資料上的任何程式性幾何常式。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ 預設值**
</dt> <dd>

預設值。 鑲嵌會) 依原樣複製 (曲線資料的頂點資料，而不會有其他計算。 使用鑲嵌時，會插入這個元素。 否則，會將頂點資料複製到輸入暫存器中。 輸入和輸出類型可以是任何值，但一律是相同的類型。

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ PARTIALU**
</dt> <dd>

以 U 方向計算矩形或三角形 patch 上某個點的正切函數。 輸入類型可以是下列其中一項：

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

輸出類型一律為 D3DDECLTYPE \_ FLOAT3。

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**
</dt> <dd>

以 V 方向計算矩形或三角形 patch 上某個點的正切函數。 輸入類型可以是下列其中一項：

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

輸出類型一律為 D3DDECLTYPE \_ FLOAT3。

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**
</dt> <dd>

藉由採用兩個正切的交叉乘積，計算矩形或三角形 patch 上某個點的法線。 輸入類型可以是下列其中一項：

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

輸出類型一律為 D3DDECLTYPE \_ FLOAT3。

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ UV**
</dt> <dd>

將 U、V 值複製到矩形或三角形 patch 上的某個點。 這會導致2D 浮點數。 輸入類型必須設定為 D3DDECLTYPE \_ 未使用。 輸出資料類型一律為 D3DDECLTYPE \_ FLOAT2。 輸入資料流程和位移也是未使用的 (但必須設定為 0) 。

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD \_ 查閱**
</dt> <dd>

查閱置換圖。 輸入類型可以是下列其中一項：

-   D3DDECLTYPE \_ FLOAT2
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4

紋理對應查閱只會使用. x 和. y 元件。 輸出類型一律為 D3DDECLTYPE \_ FLOAT1。 裝置必須支援置換對應。 如需置換對應的詳細資訊，請參閱 [ (Direct3D 9) 的置換對應 ](displacement-mapping.md)。 如果啟用了 N 個修補程式，則只有 N 個修補程式資料的可程式化管線才支援這個常數。

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**
</dt> <dd>

查閱 presampled 置換地圖。 輸入類型必須設定為 D3DDECLTYPE \_ 未使用; 資料流程索引和資料流程位移必須設定為0。 這項作業的輸出類型一律為 D3DDECLTYPE \_ FLOAT1。 裝置必須支援置換對應。 如需置換對應的詳細資訊，請參閱 [ (Direct3D 9) 的置換對應 ](displacement-mapping.md)。 如果啟用了 N 個修補程式，則只有 N 個修補程式資料的可程式化管線才支援這個常數。 這個方法只能搭配 D3DDECLUSAGE \_ 範例使用。

</dd> </dl>

## <a name="remarks"></a>備註

鑲嵌會查看方法，以判斷在鑲嵌期間要從頂點資料計算的資料。 網格資料應使用預設值。 修補程式可以使用任何其他已實的類型。

頂點資料是使用 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 結構的陣列來宣告。 陣列中的每個元素都包含一個頂點宣告方法。

除了使用 D3DDECLMETHOD \_ 預設值， \_ \_ 當啟用 N 個修補程式時，一般網格可以使用 D3DDECLMETHOD LOOKUP 和 D3DDECLMETHOD LOOKUPPRESAMPLED 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




