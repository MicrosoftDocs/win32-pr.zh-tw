---
title: 材質類型
description: 使用下列語法來宣告材質變數。
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- 材質類型 HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/07/2020
ms.locfileid: "103681528"
---
# <a name="texture-type"></a>材質類型

使用下列語法來宣告材質變數。

|                |
|----------------|
| **類型名稱;** |

## <a name="parameters"></a>參數
| 項目                                                                                     | 描述                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**類型**<br/> | 下列其中一種類型：材質 (不具類型，適用于回溯相容性) 、Texture1D、Texture1DArray、Texture2D、Texture2DArray、Texture3D、TextureCube。 元素大小必須符合 4 32 位數量。<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/> | 可唯一識別變數名稱的 ASCII 字串。<br/>                                                                                                                                                   |
## <a name="remarks"></a>備註

使用材質有三個部分。

1.  宣告材質變數。 這是使用上述語法完成的。 例如，這些都是有效的宣告。

    ```
    texture g_MeshTexture;
    ```

    \- 或 -

    ```
    Texture2D g_MeshTexture;
    ```

2.  宣告和初始化取樣器物件。 這是在 Direct3D 9 和 Direct3D 10 中略有不同的語法來完成。 如需有關取樣器物件語法的詳細資訊，請參閱 [ (DIRECTX HLSL) 的取樣器類型 ](dx-graphics-hlsl-sampler.md)。
3.  在著色器中叫用材質函數。

Direct3D 9 與 Direct3D 10 之間的差異：

Direct3D 9 使用 [內部紋理](dx-graphics-hlsl-intrinsic-functions.md) 函式來執行材質作業。 此範例來自 [BasicHLSL 範例](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) ，並使用 [tex2D (s，t)  (DirectX HLSL) ](dx-graphics-hlsl-tex2d.md) 來執行材質取樣。

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

Direct3D 10 會改為使用樣板 [化紋理物件](dx-graphics-hlsl-to-type.md) 。 以下是對等的材質運算範例。

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a>另請參閱

[ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
