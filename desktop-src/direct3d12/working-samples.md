---
title: 工作範例
description: 可供下載的工作範例可供下載，以顯示一些 Direct3D 12 功能的使用方式。
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1b61ec374e21c9173797121ee90ec72e789de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103620"
---
# <a name="working-samples"></a>工作範例

可供下載的工作範例可供下載，以顯示一些 Direct3D 12 功能的使用方式。

## <a name="working-samples"></a>工作範例

您可以從 [GitHub/Microsoft/DirectX-Graphics 範例](https://github.com/Microsoft/DirectX-Graphics-Samples)下載以 Visual Studio 2015 專案的形式 (的工作範例) 。

> [!Note]  
> 在此位置提供的完整樣本清單會因新增和更新範例而有所不同。

 



<table>
<thead>
<tr class="header">
<th>範例標題</th>
<th>描述</th>
<th>桌上型</th>
<th>UWP</th>
<th>逐步解說</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HelloWorld<dl> HelloWindow<br />
HelloTriangle<br />
HelloBundles<br />
HelloConstBuffers<br />
HelloTexture<br />
</dl></td>
<td>HelloWorld 範例集包含下列簡單的專案，可協助您開始使用 Direct3D 12。<dl> 建立視窗以準備轉譯 Direct3D 12 內容。<br />
使用 Direct3D 12 呈現簡單的三角形。<br />
示範使用 Direct3D 12 進行轉譯的組合使用方式。<br />
示範如何使用常數緩衝區將資料傳遞至用來在 Direct3D 12 中轉譯的 GPU。<br />
示範如何使用 Direct3D 12 將材質套用至三角形。<br />
</dl></td>
<td>Y</td>
<td>Y</td>
<td><a href="creating-a-basic-direct3d-12-component.md">建立基本的 Direct3D 12 元件</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>示範框架緩衝和同步處理的最佳作法，以及使用套件組合來呈現簡單的網格。</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>如何建立多執行緒功能的應用程式範例。</td>
<td>Y</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyGravity</td>
<td>示範如何在相同的 GPU 上，使用多個引擎來執行非同步計算工作與3D 工作。</td>
<td>Y</td>
<td>Y</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">多引擎 n-內文重力模擬</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>示範使用查詢堆積和 predication 的遮蔽剔除。</td>
<td>Y</td>
<td>Y</td>
<td><a href="predication-queries.md">Predication 查詢</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>示範 DirectX 12 和 HLSL 的動態索引功能。</td>
<td>Y</td>
<td>Y</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">使用 HLSL 5.1 的動態索引</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>示範11on12 圖層的基本使用方式。 此範例會在 Direct3D 12 11on12 裝置上使用 Direct3D 11 API，以使用 D2D 轉譯文字。</td>
<td>Y</td>
<td>Y</td>
<td><a href="d2d-using-d3d11on12.md">使用 D3D11on12 的 D2D</a></td>
</tr>
<tr class="even">
<td>D3D12ExecuteIndirect</td>
<td>示範計算引擎會搭配執行間接功能來挑選，以只轉譯通過剔除測試的物件。</td>
<td>Y</td>
<td>Y</td>
<td><a href="indirect-drawing-and-gpu-culling-.md">間接繪圖和 GPU 剔除</a></td>
</tr>
<tr class="odd">
<td>D3D12PipelineStateCache</td>
<td>示範 (PSO) 快取的管線狀態物件。</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12Fullscreen</td>
<td>示範如何處理全螢幕到視窗間的轉換，以及在 DirectX 12 中調整視窗大小。</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12HeterogeneousMultiadapter</td>
<td>示範如何使用共用堆積，在多個異類 Gpu 之間共用工作負載。</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>示範如何使用保留的 () 資源的磚。 在此範例中，有一個包含完整 mip 鏈之保留資源的四個四個。</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>這是用來管理您的 Direct3D 12 堆積和認可資源的低整合成本解決方案，使用來自 Direct3D 11 的記憶體管理技術。</td>
<td>Y</td>
<td>Y</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>示範如何使用小型放置的資源，顯示使用放置的資源 (具有4K 對齊的記憶體節省，) 超出認可和保留的資源 (以64K 對齊) 。</td>
<td>Y</td>
<td>Y</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 程式設計指南](directx-12-programming-guide.md)
</dt> <dt>

[D3D12 程式碼逐步解說-解說](d3d12-code-walk-throughs.md)
</dt> </dl>

 

 




