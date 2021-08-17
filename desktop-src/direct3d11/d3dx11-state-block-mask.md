---
title: 'D3DX11_STATE_BLOCK_MASK 結構 (D3dx11effect .h) '
description: 指出裝置狀態。
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- D3DX11_STATE_BLOCK_MASK 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8087f45ad94fe3e45f78a1be9d86b30f6f7e3f2c9161b9c4498865b12582436e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124933"
---
# <a name="d3dx11_state_block_mask-structure"></a>D3DX11 \_ 狀態 \_ 區塊 \_ 遮罩結構

指出裝置狀態。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a>成員

<dl> <dt>

**與**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存頂點著色器狀態的布林值。

</dd> <dt>

**VSSamplers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

頂點著色器取樣器的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。

</dd> <dt>

**VSShaderResources**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

頂點著色器資源的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。

</dd> <dt>

**VSConstantBuffers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

頂點著色器常數緩衝區的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個常數緩衝區位置。

</dd> <dt>

**VSInterfaces**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

頂點著色器介面的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。

</dd> <dt>

**房 協**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存輪廓著色器狀態的布林值。

</dd> <dt>

**HSSamplers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

輪廓著色器取樣器的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。

</dd> <dt>

**HSShaderResources**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

輪廓著色器資源的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。

</dd> <dt>

**HSConstantBuffers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

輪廓的陣列-著色器常數緩衝區。 陣列是多位元組的位元遮罩，其中每個位都代表一個常數緩衝區位置。

</dd> <dt>

**HSInterfaces**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

輪廓著色器介面的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。

</dd> <dt>

**DS**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存網域著色器狀態的布林值。

</dd> <dt>

**DSSamplers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

網域著色器取樣器的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。

</dd> <dt>

**DSShaderResources**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

網域著色器資源的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。

</dd> <dt>

**DSConstantBuffers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

網域著色器常數緩衝區的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個緩衝區位置。

</dd> <dt>

**DSInterfaces**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

網域著色器介面的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。

</dd> <dt>

**GS**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存幾何著色器狀態的布林值。

</dd> <dt>

**GSSamplers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

幾何的陣列-著色器取樣器。 陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。

</dd> <dt>

**GSShaderResources**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Geometry 的陣列-著色器資源。 陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。

</dd> <dt>

**GSConstantBuffers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Geometry 的陣列-著色器常數緩衝區。 陣列是多位元組的位元遮罩，其中每個位都代表一個緩衝區位置。

</dd> <dt>

**GSInterfaces**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Geometry-著色器介面的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。

</dd> <dt>

**PS**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存圖元著色器狀態的布林值。

</dd> <dt>

**PSSamplers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

圖元著色器取樣器的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。

</dd> <dt>

**PSShaderResources**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

圖元著色器資源的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。

</dd> <dt>

**PSConstantBuffers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

圖元著色器常數緩衝區的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個常數緩衝區位置。

</dd> <dt>

**PSInterfaces**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

圖元著色器介面的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。

</dd> <dt>

**PSUnorderedAccessViews**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

布林值，指出是否要儲存圖元著色器的未排序存取視圖。

</dd> <dt>

**CS**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存計算著色器狀態的布林值。

</dd> <dt>

**CSSamplers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

計算著色器取樣器的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個取樣器位置。

</dd> <dt>

**CSShaderResources**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

計算著色器資源的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。

</dd> <dt>

**CSConstantBuffers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

計算著色器常數緩衝區的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個常數緩衝區位置。

</dd> <dt>

**CSInterfaces**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

計算著色器介面的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個介面位置。

</dd> <dt>

**CSUnorderedAccessViews**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

布林值，指出是否要儲存計算著色器的未排序存取視圖。

</dd> <dt>

**IAVertexBuffers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

頂點緩衝區的陣列。 陣列是多位元組的位元遮罩，其中每個位都代表一個資源位置。

</dd> <dt>

**IAIndexBuffer**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存索引緩衝區狀態的布林值。

</dd> <dt>

**IAInputLayout**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存輸入配置狀態的布林值。

</dd> <dt>

**IAPrimitiveTopology**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存基本拓撲狀態的布林值。

</dd> <dt>

**OMRenderTargets**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存轉譯目標狀態的布林值。

</dd> <dt>

**OMDepthStencilState**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存深度樣板狀態的布林值。

</dd> <dt>

**OMBlendState**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存 blend 狀態的布林值。

</dd> <dt>

**RSViewports**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

布林值，指出是否要儲存區的狀態。

</dd> <dt>

**RSScissorRects**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存剪式矩形狀態的布林值。

</dd> <dt>

**RSRasterizerState**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存轉譯器狀態的布林值。

</dd> <dt>

**SOBuffers**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存資料流程輸出緩衝區狀態的布林值。

</dd> <dt>

**預測**
</dt> <dd>

類型： **[**位元組**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指出是否要儲存 predication 狀態的布林值。

</dd> </dl>

## <a name="remarks"></a>備註

狀態欄塊遮罩表示裝置會指出通過或技術有所變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx11effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11結構](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

