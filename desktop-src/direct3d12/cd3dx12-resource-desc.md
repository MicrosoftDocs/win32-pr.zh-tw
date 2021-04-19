---
title: 'CD3DX12_RESOURCE_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 資源 \_ DESC 結構。
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- CD3DX12_RESOURCE_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991497"
---
# <a name="cd3dx12_resource_desc-structure"></a>CD3DX12 \_ 資源 \_ DESC 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 資源 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 資源 \_ DESC ()**
</dt> <dd>

建立 CD3DX12 資源 DESC 的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ 資源 \_ desc (const D3D12 \_ 資源 \_ desc& o)**
</dt> <dd>

建立 CD3DX12 資源 desc 的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 資源 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 資源 \_ DESC (D3D12 \_ 資源 \_ 的維度維度、uint64 對齊、uint64 寬度、UINT 高度、Uint16 depthOrArraySize、uint16 mipLevels、DXGI \_ 格式格式、UINT SAMPLECOUNT、uint sampleQuality、D3D12 \_ 材質配置版面配置 \_ 、D3D12 \_ 資源旗標 \_ 旗標)**
</dt> <dd>

建立 CD3DX12 資源 DESC 的新實例 \_ \_ ，並初始化下列參數：

[**D3D12 \_資源 \_ 維度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) 維度

UINT64 對齊

UINT64 寬度

UINT 高度

UINT16 depthOrArraySize

UINT16 mipLevels

[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式

UINT sampleCount

UINT sampleQuality

[**D3D12 \_材質 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) 配置版面配置

[**D3D12 \_資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標

</dd> <dt>

**靜態內嵌緩衝區 (const D3D12 \_ 資源 \_ 分配 \_ 資訊& resAllocInfo、D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

 (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無

</dd> <dt>

**靜態內嵌緩衝區 (UINT64 寬度，D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無，UINT64 對齊 = 0)**
</dt> <dd>

指定初始化下列參數的函式：

UINT64 寬度

 (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無

 (opt) UINT64 對齊 = 0

</dd> <dt>

**靜態內嵌 Tex1D (DXGI \_ 格式格式、UINT64 寬度、UINT16 arraySize = 1、UINT16 mipLevels = 0、D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無、D3D12 \_ 紋理配置版面配置 \_ = D3D12 \_ 紋理配置未知、 \_ \_ UINT64 對齊 = 0)**
</dt> <dd>

指定初始化下列參數的函式：

[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式

UINT64 寬度

 (opt) UINT16 arraySize = 1

 (opt) UINT16 mipLevels = 0

 (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無

 (opt) [**D3D12 \_ 材質 \_ 版面**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) 配置版面配置 = D3D12 \_ 材質配置 \_ \_ 不明

 (opt) UINT64 對齊 = 0

</dd> <dt>

**靜態內嵌 Tex2D (DXGI \_ 格式格式、UINT64 寬度、UINT 高度、UINT16 arraySize = 1、UINT16 mipLevels = 0、UINT sampleCount = 1、UINT sampleQuality = 0、D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無、D3D12 的 \_ 材質配置版面配置 = D3D12 紋理配置未知、 \_ \_ \_ \_ UINT64 對齊 = 0)**
</dt> <dd>

指定初始化下列參數的函式：

[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式

UINT64 寬度

UINT 高度

 (opt) UINT16 arraySize = 1

 (opt) UINT16 mipLevels = 0

 (opt) UINT sampleCount = 1

 (opt) UINT sampleQuality = 0

 (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無

 (opt) [**D3D12 \_ 材質 \_ 版面**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) 配置版面配置 = D3D12 \_ 材質配置 \_ \_ 不明

 (opt) UINT64 對齊 = 0

</dd> <dt>

**靜態內嵌 Tex3D (DXGI \_ 格式格式、UINT64 寬度、UINT 高度、uint16 深度、Uint16 mipLevels = 0、D3D12 \_ 資源 \_ 旗標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無、D3D12 \_ 紋理配置版面配置 \_ = D3D12 \_ 紋理配置未知、 \_ \_ UINT64 對齊 = 0)**
</dt> <dd>

指定初始化下列參數的函式：

[**DXGI \_格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式

UINT64 寬度

UINT 高度

UINT16 深度

 (opt) UINT16 mipLevels = 0

 (opt) [**D3D12 \_ 資源 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) 標旗標 = D3D12 \_ 資源 \_ 旗標 \_ 無

 (opt) [**D3D12 \_ 材質 \_ 版面**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) 配置版面配置 = D3D12 \_ 材質配置 \_ \_ 不明

 (opt) UINT64 對齊 = 0

</dd> <dt>

**內嵌深度 () 常數**
</dt> <dd>

如果 Dimension = = [**D3D12 \_ 資源 \_ 維度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)TEXTURE3D，則會傳回 \_ DepthOrArraySize。 如果 Dimension！ = D3D12 \_ 資源 \_ 維度 \_ TEXTURE3D，則傳回1。

</dd> <dt>

**內嵌 ArraySize () 常數**
</dt> <dd>

如果 Dimension！ = D3D12 \_ 資源 \_ 維度 \_ TEXTURE3D，則傳回 DepthOrArraySize。 如果 Dimension = = D3D12 \_ 資源 \_ 維度 \_ TEXTURE3D，則傳回1。 請參閱 [**D3D12 \_ 資源 \_ 維度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D。

</dd> <dt>

**內嵌 PlaneCount (ID3D12Device \* pDevice) const**
</dt> <dd>

傳回 D3D12GetFormatPlaneCount (pDevice，格式) 。 請參閱 [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) 和 [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)。

</dd> <dt>

**內嵌子資源 (ID3D12Device \* pDevice) const**
</dt> <dd>

傳回計算為 MipLevels \* ArraySize () \* PlaneCount (pDevice) 的子資源數目。

</dd> <dt>

**內嵌 CalcSubresource (UINT MipSlice、UINT ArraySlice、UINT PlaneSlice)**
</dt> <dd>

使用 [**D3D12CalcSubresource**](d3d12calcsubresource.md)計算 subresource 索引。

</dd> <dt>

**operator const D3D12 \_ 資源 \_ DESC& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> <dt>

**operator = = (const D3D12 \_ 資源 \_ DESC& l，const D3D12 \_ resource \_ desc& r)**
</dt> <dd>

如果每個結構的所有成員都相同，則傳回 true。

</dd> <dt>

**operator！ = (const D3D12 \_ 資源 \_ desc& l，const D3D12 \_ resource \_ desc& r)**
</dt> <dd>

如果每個結構的所有成員都相同，則傳回 false。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 資源 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

