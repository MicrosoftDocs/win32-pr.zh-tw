---
description: 定義用於網格正切框架計算的設定。
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: 'D3DXTANGENT 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993877"
---
# <a name="d3dxtangent-enumeration"></a>D3DXTANGENT 列舉

定義用於網格正切框架計算的設定。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ WRAP \_ U**
</dt> <dd>

U 方向的材質座標值介於0和1之間。 在此情況下，將會選擇材質座標集合，以將三角形的周邊最小化。 請參閱 [ (Direct3D 9) 的材質包裝 ](texture-wrapping.md)。

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ WRAP \_ V**
</dt> <dd>

V 方向的材質座標值介於0和1之間。 在此情況下，將會選擇材質座標集合，以將三角形的周邊最小化。 請參閱 [ (Direct3D 9) 的材質包裝 ](texture-wrapping.md)。

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ WRAP \_ UV**
</dt> <dd>

您和 v 方向的材質座標值都介於0和1之間。 在此情況下，將會選擇材質座標集合，以將三角形的周邊最小化。 請參閱 [ (Direct3D 9) 的材質包裝 ](texture-wrapping.md)。

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT 不會 \_ \_ 標準化 \_ 部分**
</dt> <dd>

請勿標準化材質座標的部分衍生。 如果未正規化，部分衍生的小數位數會與3D 模型的尺規成正比，除以 (u，v) 空間中的三角形小數位數。 這個調整規模值會提供量值，以指定的方向伸展材品質。 產生的向量長度是部分衍生的長度的加權總和。

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ 不 \_ ORTHOGONALIZE**
</dt> <dd>

請勿將材質座標轉換成正笛卡兒座標。 與您的 D3DXTANGENT \_ ORTHOGONALIZE 彼此互斥 \_ \_ ，並 \_ \_ 從 V D3DXTANGENT ORTHOGONALIZE \_ 。

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**\_ \_ 從 V D3DXTANGENT \_ ORTHOGONALIZE**
</dt> <dd>

針對每個頂點個別計算紋理座標 v 的部分衍生，然後根據您的部分衍生，以與 v 和一般向量相關的局部衍生乘積來計算部分衍生。 與 D3DXTANGENT 互斥，不是 \_ \_ 來自 U 的 ORTHOGONALIZE 和 D3DXTANGENT \_ ORTHOGONALIZE \_ \_ 。

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**\_ \_ 從 U D3DXTANGENT \_ ORTHOGONALIZE**
</dt> <dd>

針對每個頂點個別計算材質座標 u 的部分衍生，然後計算以 v 作為標準向量交叉乘積的部分衍生，以及與您相關的部分衍生。 與 D3DXTANGENT 互斥，不是 \_ \_ 來自 V 的 ORTHOGONALIZE 和 D3DXTANGENT \_ ORTHOGONALIZE \_ \_ 。

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**\_ \_ 依區域的 D3DXTANGENT 權數 \_**
</dt> <dd>

根據附加至該頂點的三角形區域，加權計算的每個頂點一般或部分衍生向量的方向。 與 D3DXTANGENT \_ 權數相等互斥 \_ 。

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ 權數 \_ 等於**
</dt> <dd>

計算輸入網格每個三角形的單位長度一般向量。 依區域以 D3DXTANGENT \_ 權數互相排斥 \_ \_ 。

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ 風 \_ CW**
</dt> <dd>

頂點會依每個三角形的順向方向排序。 因此，計算出的一般向量方向，會從使用逆時針頂點順序計算的方向反轉180度。

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ 計算 \_ 法線**
</dt> <dd>

針對輸入網格的每個三角形計算每個頂點的一般向量，並忽略輸入網格中已存在的任何一般向量。

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ \_ 就地產生 \_**
</dt> <dd>

結果會儲存在原始的輸入網格中，而且不會使用輸出網格。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




