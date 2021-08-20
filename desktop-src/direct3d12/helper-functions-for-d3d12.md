---
title: Direct3D 12 的 Helper 函式
description: 這些 helper 函式有助於處理子資源，而且會在中宣告 `d3dx12.h` 。
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Helper 函式
- d3dx12。h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9434bf916d7cb92116cdf4f7f6d86363b2eb51
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813191"
---
# <a name="helper-functions-for-direct3d-12"></a>Direct3D 12 的 Helper 函式

這些 helper 函式有助於處理子資源，而且會在中宣告 `d3dx12.h` 。

`d3dx12.h` 可以與 Direct3D 12 標頭分開使用。 您可以 `d3dx12.h` 從 [D3D12 Helper 程式庫](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h)進行下載。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**CommandListCast**](commandlistcast.md) | 這個函式範本會將任何命令清單的常數指標轉換成 ID3D12CommandList 的 const 指標。 |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md) | 計算材質的 subresource 索引。 |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md) | 輸出對應至指定之 subresource 索引的 mip 配量、陣列配量和平面配量。 |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) | 針對指定的虛擬配接器 (**ID3D12Device**) ，取得指定之 DXGI 格式的平面數目。 |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md) | 指出版面配置是否為不透明。 |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md) | 傳回子物件類型，這個物件對應至傳入之子物件類型的基類。 |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md) | 剖析管線狀態資料流程描述，針對每個已剖析的子物件實例呼叫使用者定義的回呼。 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md) | 有助於啟用根簽章1.1 功能（如果有的話），而且不需要維護兩個程式碼路徑來建立根簽章。 此 helper 方法會在版本1.1 不受支援時，重建版本1.0 的根簽章。 |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md) | 傳回要用於資料上傳的緩衝區所需大小。 |
| [**Memcpysubresource**](memcpysubresource.md) | 逐列複製 subresource 資料列。 |
| [**Updatesubresources**](updatesubresources1.md) | 更新子資源，所有 subresource 陣列都應該填入，通常是藉由呼叫 [**ID3D12Device：： GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)。 |
| [**Updatesubresources (堆積配置)**](updatesubresources2.md) | 以堆積配置的執行更新子資源。 |
| [**Updatesubresources (堆疊配置)**](updatesubresources3.md) | 使用堆疊配置執行更新子資源。 |

## <a name="related-topics"></a>相關主題

* [Direct3D 12 參考](direct3d-12-reference.md)
* [D3D12 的 Helper 結構和函式](helper-structures-and-functions-for-d3d12.md)
