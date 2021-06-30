---
title: D3D12 的 Helper 函式
description: 這些 helper 函式特別有助於處理子資源，而且會在 d3dx12 中宣告。
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Helper 函式
- d3dx12。h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10736d91da0e2c4efa2a3c981ab5c4f64e2af86d
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102130"
---
# <a name="helper-functions-for-d3d12"></a>D3D12 的 Helper 函式

這些 helper 函式特別有助於處理子資源，而且會在 **d3dx12** 中宣告。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                             | 描述                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommandListCast**](commandlistcast.md)<br/>                                     | 這個函式範本會將任何命令清單的常數指標轉換成 ID3D12CommandList 的 const 指標。<br/>                                                                                                                               |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md)<br/>                                   | 計算材質的 subresource 索引。 <br/>                                                                                                                                                                                                  |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md)<br/>                         | 輸出對應至指定之 subresource 索引的 mip 配量、陣列配量和平面配量。 <br/>                                                                                                                                        |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md)<br/>                           | 針對指定的虛擬配接器 (**ID3D12Device**) ，取得指定之 DXGI 格式的平面數目。 <br/>                                                                                                                               |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md)<br/>                                     | 指出版面配置是否為不透明。<br/>                                                                                                                                                                                                         |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md)<br/>                       | 傳回子物件類型，這個物件對應至傳入之子物件類型的基類。<br/>                                                                                                                                                  |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md)<br/>                    | 剖析管線狀態資料流程描述，針對每個已剖析的子物件實例呼叫使用者定義的回呼。<br/>                                                                                                                                 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md)<br/> | 有助於啟用根簽章1.1 功能（如果有的話），而且不需要維護兩個程式碼路徑來建立根簽章。 此 helper 方法會在版本1.1 不受支援時，重建版本1.0 的根簽章。<br/> |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md)<br/>                     | 傳回要用於資料上傳的緩衝區所需大小。 <br/>                                                                                                                                                                              |
| [**Memcpysubresource**](memcpysubresource.md)<br/>                                         | 逐列複製 subresource 資料列。 <br/>                                                                                                                                                                                                               |
| [**Updatesubresources**](updatesubresources1.md)<br/>                                      | 更新子資源，所有 subresource 陣列都應該填入，通常是藉由呼叫 [**ID3D12Device：： GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)。 <br/>                                                                  |
| [**Updatesubresources (堆積配置)**](updatesubresources2.md)<br/>                    | 以堆積配置的執行更新子資源。 <br/>                                                                                                                                                                                    |
| [**Updatesubresources (堆疊配置)**](updatesubresources3.md)<br/>                   | 使用堆疊配置執行更新子資源。 <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 參考](direct3d-12-reference.md)
</dt> <dt>

[D3D12 的 Helper 結構和函式](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





