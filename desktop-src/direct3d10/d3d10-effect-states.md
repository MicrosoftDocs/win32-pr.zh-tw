---
description: 效果狀態是運算式形式的成對名稱/值。
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: '效果狀態群組 (Direct3D 10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321672"
---
# <a name="effect-state-groups-direct3d-10"></a>效果狀態群組 (Direct3D 10) 

效果狀態是運算式形式的成對名稱/值。

## <a name="blend-state"></a>Blend 狀態

| | |
|-|-|
| **ALPHATOCOVERAGEENABLE**、 **BLENDENABLE**、 **SRCBLEND**、 **DESTBLEND**、 **BLENDOP**、 **SRCBLENDALPHA**、 **DESTBLENDALPHA**、 **BLENDOPALPHA**、 **RENDERTARGETWRITEMASK** | [ **D3D10 \_ BLEND \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>深度和樣板狀態

| | |
|-|-|
| **DEPTHENABLE**、 **DEPTHWRITEMASK**、 **DEPTHFUNC**、 **STENCILENABLE**、 **STENCILREADMASK**、 **STENCILWRITEMASK** | [ **D3D10 深度樣板 \_ \_ \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| FRONTFACESTENCILFAIL * *、 **FRONTFACESTENCILZFAIL**、 **FRONTFACESTENCILPASS**、 **FRONTFACESTENCILFUNC**、 **BACKFACESTENCILFAIL**、 **BACKFACESTENCILZFAIL**、 **BACKFACESTENCILPASS**、 **BACKFACESTENCILFUNC** | [ **D3D10 \_ 深度 \_ STENCILOP \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>轉譯器狀態

| | |
|-|-|
| FILLMODE | [**D3D10 \_ 填滿 \_ 模式**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| CULLMODE | [**D3D10 的 \_ 挑選 \_ 模式**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **FRONTCOUNTERCLOCKWISE**、 **DEPTHBIAS**、 **DEPTHBIASCLAMP**、 **SLOPESCALEDDEPTHBIAS**、 **ZCLIPENABLE**、 **SCISSORENABLE**、 **MULTISAMPLEENABLE**、 **ANTIALIASEDLINEENABLE** | D3D10 轉譯器 [ **\_ \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>取樣器狀態

| | |
|-|-|
| **Filter**、 **AddressU**、 **AddressV**、 **AddressW**、 **MipLODBias**、 **MaxAnisotropy**、 **ComparisonFunc**、 **邊框**、 **MinLOD**、 **MaxLOD** | [ **D3D10 取樣器 \_ \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

如需範例，請參閱 [ (DIRECTX HLSL) 的取樣器類型 ](../direct3dhlsl/dx-graphics-hlsl-sampler.md) 。

## <a name="effect-object-state"></a>效果物件狀態

| 此效果物件 | 對應至 |
|-|-|
| RASTERIZERSTATE | 轉譯器 [狀態](#rasterizer-state) 狀態物件。 |
| DEPTHSTENCILSTATE | [深度和樣板狀態](#depth-and-stencil-state)狀態物件。 |
| BLENDSTATE | [Blend 狀態](#blend-state)狀態物件。 |
| VERTEXSHADER | 已編譯的頂點著色器物件。 |
| 無效 | 編譯的圖元著色器物件。 |
| GEOMETRYSHADER | 已編譯的幾何著色器物件。 |
| DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK | [**D3D10 \_ PASS \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc)的成員。 |

## <a name="defining-and-using-state-objects"></a>定義和使用狀態物件

系統會以下列格式在 FX 檔案中宣告狀態物件。 *StateObjectType* 是上面所列的其中一個狀態， *而成員* 名稱是將擁有非預設值之任何成員的名稱。

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

例如，若要設定 AlphaToCoverageEnable，並將 BlendEnable \[ 0 設為 FALSE 的 blend 狀態物件 \] ，則會使用下列程式碼。 

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

使用 [ (Direct3D 10) 的效果技巧語法 ](d3d10-effect-technique-syntax.md)中所述的其中一種 SetStateGroup 函式，將狀態物件套用至技術傳遞。 例如，若要套用上面所述的 BlendState 物件，則會使用下列程式碼。

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

如需說明使用狀態的教學課程，請參閱 [狀態管理](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)。

## <a name="related-topics"></a>相關主題

* [效果技巧語法](d3d10-effect-technique-syntax.md)
* [ (Direct3D 10) 的效果格式 ](d3d10-effect-format.md)
