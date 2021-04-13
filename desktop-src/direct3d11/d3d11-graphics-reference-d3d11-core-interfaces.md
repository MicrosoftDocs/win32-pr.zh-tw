---
title: Direct3D 11 核心介面
description: 本節包含核心介面的相關資訊。
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- 介面，Direct3D 11 核心
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104463849"
---
# <a name="direct3d-11-core-interfaces"></a>Direct3D 11 核心介面

本節包含核心介面的相關資訊。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a><br/></td>
<td>此介面會封裝以非同步方式從 GPU 取得資料的方法。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a><br/></td>
<td>Blend 介面會保存您可以系結至 <a href="d3d10-graphics-programming-guide-output-merger-stage.md">輸出合併階段</a>之混合狀態的描述。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a><br/></td>
<td>Blend 介面會保存您可以系結至 <a href="d3d10-graphics-programming-guide-output-merger-stage.md">輸出合併階段</a>之混合狀態的描述。 這個 blend 狀態介面支援邏輯作業以及混合作業。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a><br/></td>
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a>介面會封裝要播放之圖形命令的清單。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a><br/></td>
<td>此介面會封裝用來測量 GPU 效能的方法。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a><br/></td>
<td>深度樣板狀態介面會保存深度範本狀態的描述，您可以將其系結至 <a href="d3d10-graphics-programming-guide-output-merger-stage.md">輸出合併階段</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a><br/></td>
<td>裝置介面代表虛擬配接器;它是用來建立資源。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a><br/></td>
<td>裝置介面代表虛擬配接器;它是用來建立資源。 <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>中的方法。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a><br/></td>
<td>裝置介面代表虛擬配接器;它是用來建立資源。 <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>中的方法。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a><br/></td>
<td>裝置介面代表虛擬配接器;它是用來建立資源。 <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>中的方法。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a><br/></td>
<td>裝置介面代表虛擬配接器;它是用來建立資源。 <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>中的方法，例如 <strong>RegisterDeviceRemovedEvent</strong> 和 <strong>UnregisterDeviceRemoved</strong>。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a><br/></td>
<td>裝置介面代表虛擬配接器;它是用來建立資源。 <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>中的方法。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a><br/></td>
<td>裝置子系介面可存取裝置所使用的資料。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a><br/></td>
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>>id3d11devicecoNtext</strong></a>介面表示產生轉譯命令的裝置內容。<br/>
<blockquote>
[!Note]<br />
此介面的最新版本 <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceCoNtext4</strong></a> 引進 Windows 10 Creators Update 中。 瞄準 Windows 10 Creators Update 的應用程式應該使用 <strong>ID3D11DeviceCoNtext4</strong> 介面，而不是 <strong>ID3D11Device</strong>。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a><br/></td>
<td>裝置內容介面代表裝置內容;它是用來呈現命令。 <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceCoNtext1</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>>id3d11devicecoNtext</strong></a>中的方法。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a><br/></td>
<td>裝置內容介面代表裝置內容;它是用來呈現命令。 <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceCoNtext2</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceCoNtext1</strong></a>中的方法。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceCoNtext3</strong></a><br/></td>
<td>裝置內容介面代表裝置內容;它是用來呈現命令。 <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceCoNtext3</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceCoNtext2</strong></a>中的方法。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceCoNtext4</strong></a><br/></td>
<td>裝置內容介面代表裝置內容;它是用來呈現命令。 <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceCoNtext4</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceCoNtext3</strong></a>中的方法。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceCoNtextState</strong></a><br/></td>
<td><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceCoNtextState</strong></a>介面代表內容狀態物件，其保存有關 Microsoft Direct3D 裝置的狀態和行為資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a><br/></td>
<td>代表用來同步處理 CPU 的物件，以及一或多個 Gpu。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a><br/></td>
<td>輸入配置介面會保存如何將在記憶體中配置的頂點資料摘要至<a href="overviews-direct3d-11-graphics-pipeline.md">圖形管線</a>的<a href="d3d10-graphics-programming-guide-input-assembler-stage.md">輸入組合語言階段</a>的定義。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a><br/></td>
<td>為多執行緒應用程式的重要區段提供執行緒保護。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a><br/></td>
<td>述詞介面會根據上一次繪製呼叫的結果，判斷是否應該處理幾何。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a><br/></td>
<td>查詢介面會從 GPU 查詢資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a><br/></td>
<td>表示查詢物件，用來從圖形處理器 (GPU) 查詢資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a><br/></td>
<td>轉譯器狀態介面會保存您可以系結至轉譯器 <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">階段</a>的轉譯器狀態原因。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a><br/></td>
<td>轉譯器狀態介面會保存您可以系結至轉譯器 <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">階段</a>的轉譯器狀態原因。 此轉譯器狀態介面支援強制取樣計數。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a><br/></td>
<td>轉譯器狀態介面會保存您可以系結至轉譯器 <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">階段</a>的轉譯器狀態原因。 此轉譯器狀態介面支援強制取樣計數和保守的點陣化模式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a><br/></td>
<td>取樣器狀態介面會保存取樣器狀態的描述，您可以系結至 <a href="overviews-direct3d-11-graphics-pipeline.md">管線</a> 的任何著色器階段，以供材質範例作業參考。<br/></td>
</tr>
</tbody>
</table>



 

Direct3D 11 的執行介面：

-   [資源](d3d11-graphics-reference-resource-interfaces.md)
-   [著色器](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心參考](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

