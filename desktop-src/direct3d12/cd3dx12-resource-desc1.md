---
title: 'CD3DX12_RESOURCE_DESC1 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) 結構。
keywords:
- CD3DX12_RESOURCE_DESC1 結構
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 87fe62c475e1d961258671355c4c9be133bf0a41
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813241"
---
# <a name="cd3dx12_resource_desc1-structure"></a>CD3DX12_RESOURCE_DESC1 結構

協助程式結構，可讓您輕鬆地初始化 [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) 結構。

## <a name="syntax"></a>語法

```cpp
struct CD3DX12_RESOURCE_DESC1 : public D3D12_RESOURCE_DESC1
{
    CD3DX12_RESOURCE_DESC1();
    explicit CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1& o) noexcept;
    CD3DX12_RESOURCE_DESC1(
        D3D12_RESOURCE_DIMENSION dimension,
        UINT64 alignment,
        UINT64 width,
        UINT height,
        UINT16 depthOrArraySize,
        UINT16 mipLevels,
        DXGI_FORMAT format,
        UINT sampleCount,
        UINT sampleQuality,
        D3D12_TEXTURE_LAYOUT layout,
        D3D12_RESOURCE_FLAGS flags,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        UINT64 width,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex1D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex2D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        UINT sampleCount = 1,
        UINT sampleQuality = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex3D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 depth,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    inline UINT16 Depth() const noexcept;
    inline UINT16 ArraySize() const noexcept;
    inline UINT8 PlaneCount(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT Subresources(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice) noexcept;
};
inline bool operator==(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
inline bool operator!=(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
```

## <a name="members"></a>成員

`CD3DX12_RESOURCE_DESC1`

預設建構函式。 建立新的、未初始化的 **CD3DX12_RESOURCE_DESC1** 實例。

`CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1&)`

建立新實例的函式， **CD3DX12_RESOURCE_DESC1** 以 [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) 結構的內容初始化。

`CD3DX12_RESOURCE_DESC1(D3D12_RESOURCE_DIMENSION, UINT64, UINT64, UINT, UINT16, UINT16, DXGI_FORMAT, UINT, UINT, D3D12_TEXTURE_LAYOUT, D3D12_RESOURCE_FLAGS, UINT = 0, UINT = 0, UINT = 0)`

建立新實例的函式， **CD3DX12_RESOURCE_DESC1** 以傳遞給它的參數初始化。

`Buffer(const D3D12_RESOURCE_ALLOCATION_INFO&, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE)`

靜態函式，它會使用這些值來進行初始化 **CD3DX12_RESOURCE_DESC1** 的新實例。

|資料成員|值|
|-|-|
|尺寸|D3D12_RESOURCE_DIMENSION_BUFFER|
|對齊|*resAllocInfo*。對準|
|寬度|*resAllocInfo*。SizeInBytes|
|高度|1|
|DepthOrArraySize|1|
|MipLevels|1|
|格式|DXGI_FORMAT_UNKNOWN|
|SampleDesc 計數|1|
|SampleDesc 品質|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Flags|*flags*|
|SamplerFeedbackMipRegion 寬度|0|
|SamplerFeedbackMipRegion 高度|0|
|SamplerFeedbackMipRegion 深度|0|

`Buffer(UINT64, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, UINT64 = 0)`

靜態函式，它會使用這些值來進行初始化 **CD3DX12_RESOURCE_DESC1** 的新實例。

|資料成員|值|
|-|-|
|尺寸|D3D12_RESOURCE_DIMENSION_BUFFER|
|對齊|*對準*|
|寬度|*width* (寬度)|
|高度|1|
|DepthOrArraySize|1|
|MipLevels|1|
|格式|DXGI_FORMAT_UNKNOWN|
|SampleDesc 計數|1|
|SampleDesc 品質|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Flags|*flags*|
|SamplerFeedbackMipRegion 寬度|0|
|SamplerFeedbackMipRegion 高度|0|
|SamplerFeedbackMipRegion 深度|0|

`Tex1D(DXGI_FORMAT, UINT64, UINT16 = 1, UINT16 = 0, D3D12_RESOURCE_FLAGS D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

靜態函式，它會使用這些值來進行初始化 **CD3DX12_RESOURCE_DESC1** 的新實例。

|資料成員|值|
|-|-|
|尺寸|D3D12_RESOURCE_DIMENSION_TEXTURE1D|
|對齊|*對準*|
|寬度|*width* (寬度)|
|高度|1|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|格式|*format*|
|SampleDesc 計數|1|
|SampleDesc 品質|0|
|Layout|*佈局*|
|Flags|*flags*|
|SamplerFeedbackMipRegion 寬度|0|
|SamplerFeedbackMipRegion 高度|0|
|SamplerFeedbackMipRegion 深度|0|

`Tex2D(DXGI_FORMAT, UINT64, UINT, UINT16 = 1, UINT16 = 0, UINT = 1, UINT = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0, UINT = 0, UINT = 0, UINT = 0)`

靜態函式，它會使用這些值來進行初始化 **CD3DX12_RESOURCE_DESC1** 的新實例。

|資料成員|值|
|-|-|
|尺寸|D3D12_RESOURCE_DIMENSION_TEXTURE2D|
|對齊|*對準*|
|寬度|*width* (寬度)|
|高度|*height* (高度)|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|格式|*format*|
|SampleDesc 計數|*sampleCount*|
|SampleDesc 品質|*sampleQuality*|
|Layout|*佈局*|
|Flags|*flags*|
|SamplerFeedbackMipRegion 寬度|*samplerFeedbackMipRegionWidth*|
|SamplerFeedbackMipRegion 高度|*samplerFeedbackMipRegionHeight*|
|SamplerFeedbackMipRegion 深度|*samplerFeedbackMipRegionDepth*|

`Tex3D(DXGI_FORMAT, UINT64, UINT, UINT16, UINT16 = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

靜態函式，它會使用這些值來進行初始化 **CD3DX12_RESOURCE_DESC1** 的新實例。

|資料成員|值|
|-|-|
|尺寸|D3D12_RESOURCE_DIMENSION_TEXTURE3D|
|對齊|*對準*|
|寬度|*width* (寬度)|
|高度|*height* (高度)|
|DepthOrArraySize|*深度*|
|MipLevels|*mipLevels*|
|格式|*format*|
|SampleDesc 計數|1|
|SampleDesc 品質|0|
|Layout|*佈局*|
|Flags|*flags*|
|SamplerFeedbackMipRegion 寬度|0|
|SamplerFeedbackMipRegion 高度|0|
|SamplerFeedbackMipRegion 深度|0|

`Depth`

傳回包含資源深度的 **UINT16** 。

`ArraySize`

傳回包含資源陣列大小的 **UINT16** 。

`PlaneCount(ID3D12Device*)`

傳回 **UINT8** ，其中包含資源格式的平面計數。

`Subresources(ID3D12Device*)`

傳回包含資源中子資源數目的 **UINT** 。

`CalcSubresource(UINT, UINT, UINT)`

Caculates 並傳回包含資源之 subresource 索引的 **UINT** （以傳遞給它的參數為基礎）。

`operator==(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

如果兩個參數的成員相等，則為可傳回的免費函 `true` 式; 否則為 `false` 。

`operator!=(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

`true`如果兩個參數的成員不相等，則為傳回的自由函數; 否則為 `false` 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [D3DX12_RESOURCE_DESC1](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1)
* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
