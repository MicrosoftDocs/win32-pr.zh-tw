---
title: 2008年11月 Direct3D 11 Tech Preview 的新功能
description: 此版本的 Direct3D 11 包含新功能、工具和檔。
ms.assetid: 7d259764-b826-4609-b415-2093cc6df874
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a49529882eafaf092a866d1b172de62fe15c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375417"
---
# <a name="whats-new-in-the-nov-2008-direct3d-11-tech-preview"></a>2008年11月 Direct3D 11 Tech Preview 的新功能

此版本的 Direct3D 11 包含新功能、工具和檔。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>項目</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>鑲嵌<br/></td>
<td>Direct3D 11 提供額外的管線階段，以支援高序位基本專案的 <a href="direct3d-11-advanced-stages-tessellation.md">即時鑲嵌</a> 。 利用廣泛的程式設計功能，這項功能可讓您使用許多不同的方法來評估高序位介面，包括使用近似值技術、貝塞爾修補程式、適應性鑲嵌和置換對應的細分表面。 這項功能僅適用于 Direct3D 11 類別的硬體，因此為了評估這項功能，您必須使用參考轉譯器。 如需鑲嵌式運作方式的示範，請參閱透過範例瀏覽器提供的 <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> 範例。<br/></td>
</tr>
<tr class="even">
<td><span id="Compute_Shader"></span><span id="compute_shader"></span><span id="COMPUTE_SHADER"></span>計算著色器<br/></td>
<td><a href="direct3d-11-advanced-stages-compute-shader.md">計算著色器</a>是一種與 Direct3D 11 管線無關的額外階段，可在 GPU 上啟用一般用途計算。 除了統一著色器核心提供的所有著色器功能之外，計算著色器也支援透過未排序的存取權，以散佈的方式讀取和寫入資源、執行中線程群組內的共用記憶體集區、同步處理原始物件、不可部分完成的運算子，以及許多其他先進的資料平行功能。 您已在此版本中啟用 Direct3D 11 計算著色器的變異，可在 Direct3D 10 類別硬體上運作。 因此，您可以在實際的硬體上開發計算著色器，但需要更新的驅動程式。 Direct3D 11 計算著色器的完整功能主要是為了支援 Direct3D 11 類別的硬體，因此為了評估完整的功能，您必須使用參考轉譯器，才能使用此類硬體。 如需計算著色器運作方式的示範，請參閱透過範例瀏覽器提供的 <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> 範例。<br/></td>
</tr>
<tr class="odd">
<td><span id="Multithreaded_Rendering"></span><span id="multithreaded_rendering"></span><span id="MULTITHREADED_RENDERING"></span>多執行緒轉譯<br/></td>
<td>Direct3D 11 中的 Direct3D 10 主要 API 差異在於新增 <a href="overviews-direct3d-11-render-multi-thread.md">延遲</a>的內容，可讓您在多個核心上進行可調整的 direct3d 命令執行。 延後的內容會捕捉和組合動作，例如狀態變更，以及繪製可以在稍後於實際裝置上執行的提交。 藉由在多個執行緒上利用延遲的內容，應用程式可以將 Direct3D11 執行時間和驅動程式所需的 CPU 額外負荷分散至多個核心，以更有效地使用使用者的電腦設定。 這項功能可用於目前的 Direct3D 10 硬體以及參考轉譯器。 如需 API 使用方式的示範，請參閱透過範例瀏覽器提供的 <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a> 範例。<br/></td>
</tr>
<tr class="even">
<td><span id="Dynamic_Shader_Linkage_"></span><span id="dynamic_shader_linkage_"></span><span id="DYNAMIC_SHADER_LINKAGE_"></span>動態著色器連結 <br/></td>
<td>為了解決在效能上特製化著色器中所見到的組合爆炸問題，Direct3D 11 引進了一種有限形式的執行時間 <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking">著色器連結</a> ，可在應用程式執行期間提供近乎理想的著色器特製化。 這是藉由在著色器指派給管線時，在著色器程式碼中指定特定函式的實作為達成，讓驅動程式能夠快速地內嵌原生著色器指令，而不是強制驅動程式以新的設定重新編譯中繼語言為原生指令。 著色器開發會透過將類別和介面引入 HLSL 來公開。 如需示範，請參閱透過範例瀏覽器提供的 <a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">動態著色器連結 11</a> 範例。<br/></td>
</tr>
<tr class="odd">
<td><span id="Windows_Advanced_Rasterizer__WARP_"></span><span id="windows_advanced_rasterizer__warp_"></span><span id="WINDOWS_ADVANCED_RASTERIZER__WARP_"></span>Windows Advanced (的變形) <br/></td>
<td>此 SDK 透過 Direct3D 11 提供，最後也透過 Direct3D 10.1 提供，變形是一種快速、多核心的調整轉譯器，其完全符合 Direct3D 10.1。 利用這項技術就像在裝置建立時傳遞 D3D_DRIVER_TYPE_WARP 旗標一樣簡單。<br/></td>
</tr>
<tr class="even">
<td><span id="Direct3D_10_and_Direct3D_11_on_Direct3D_9_Hardware__D3D10_Level_9_"></span><span id="direct3d_10_and_direct3d_11_on_direct3d_9_hardware__d3d10_level_9_"></span><span id="DIRECT3D_10_AND_DIRECT3D_11_ON_DIRECT3D_9_HARDWARE__D3D10_LEVEL_9_"></span>Direct3d 9 硬體上的 Direct3D 10 和 Direct3D 11 (D3D10 Level 9) <br/></td>
<td>此 SDK 透過 Direct3D 11 提供，最後也透過 Direct3D 10.1 提供，Direct3D API 最多可以 Direct3D 9 硬體為目標，以及 Direct3D 10、Direct3D 10.1 和 Direct3D 11 硬體。 這是藉由提供功能層級機制來達成，這會根據功能將硬體分組為六個類別：9_1、9_2、9_3、10_0、10_1 和11_0。 只有當卡片完全符合該層級時，才會符合功能層級，而且每個層級都是其下的嚴格超級組。 功能的模擬最少，可確保不會發生未預期的效能懸崖。 因此，Direct3D 9 層級目標無法使用幾何著色器之類的功能。 <br/></td>
</tr>
<tr class="odd">
<td><span id="Runtime_Binaries"></span><span id="runtime_binaries"></span><span id="RUNTIME_BINARIES"></span>執行時間二進位檔<br/></td>
<td>可在 Windows 7 和 Windows Vista SP1 上使用的 Direct3D 11 tech preview 中提供的所有執行時間二進位檔都會與 SDK 一起安裝，並標示為搶鮮 &quot; 版（Beta） &quot; 元件 (例如 D3D11_beta.DLL) 。 所有搶鮮版（Beta）標記的元件都是 bombed 時間。 若要建立專案來評估這些新元件，您必須連結到其對等的 Beta 標記的匯入程式庫 (例如 D3D11_Beta .lib) 。 如果您有 Windows 7 的 PDC 複本，則與組建 Windows SDK 中提供的標頭、程式庫和 pdb，適用于使用 Windows 7 提供的 Direct3D 11 元件進行開發。 請將此 SDK 中的標頭、程式庫和 pdb 保留使用於此處提供的搶鮮版（Beta）元件。<br/></td>
</tr>
<tr class="even">
<td><span id="D3DX11"></span><span id="d3dx11"></span>D3DX11<br/></td>
<td>D3DX11 目前支援適用于 Direct3D 11 資源的材質載入、著色器編譯、資料載入和背景工作執行緒函數。 未來，此元件將提供更多 D3DX10 所提供的技術。 著色器編譯功能也會透過 Direct3D 編譯器元件直接提供，如下所述。<br/></td>
</tr>
<tr class="odd">
<td><span id="HLSL_and_Direct3D_Compiler"></span><span id="hlsl_and_direct3d_compiler"></span><span id="HLSL_AND_DIRECT3D_COMPILER"></span>HLSL 和 Direct3D 編譯器<br/></td>
<td>HLSL 編譯器有數項新功能，可支援 Direct3D 11 提供的新技術。 這包括透過介面和類別的物件導向程式設計、資源載入的直接索引編制語法，以及可確保使用特定變數執行的所有作業都遵守嚴格浮點數規則的 ' 精確 ' 關鍵字。 幾乎所有新的語言功能在現有的著色器目標上都有有效的功能。 除了支援所有 Direct3D 9、Direct3D 10、Direct3D 10.1 和 Direct3D 11 著色器之外，HLSL 編譯器也支援為 Direct3D 10 層級9目標撰寫著色器所需的特殊目標。 您現在可以透過 D3DCompiler 和 D3DCompiler，直接在 D3DX10 和 D3DX11 外部存取 D3D 編譯器。 使用這些新檔案時，應用程式不需要連結至 D3DX 來執行執行時間編譯，而且如果只需要 D3DX 的功能，應用程式就不需要包含編譯器。<br/></td>
</tr>
<tr class="even">
<td><span id="D3D11_Reference_Rasterizer"></span><span id="d3d11_reference_rasterizer"></span><span id="D3D11_REFERENCE_RASTERIZER"></span>D3D11 參考轉譯器<br/></td>
<td>參考轉譯器提供了一種黃金標準的點陣化執行，可評估硬體中尚無法使用的 Direct3D 11 功能。 參考轉譯器也提供一種方式，以驗證特定硬體實作為點陣標準的精確度。 參考轉譯器的設計是為了正確性，而不是效能。 若要建立參考裝置，只要在裝置建立時傳遞 D3D_DRIVER_TYPE_REFERENCE 旗標即可。 <br/></td>
</tr>
<tr class="odd">
<td><span id="D3D11_SDK_Layers"></span><span id="d3d11_sdk_layers"></span><span id="D3D11_SDK_LAYERS"></span>D3D11 SDK 層級<br/></td>
<td>Direct3D11 SDK 層提供一種機制，可在開發期間追蹤 Direct3D 11 執行時間的操作。 目前，這是用來提供有用的偵錯工具資訊，不僅包含不適當用途的錯誤，也會提供建議最佳作法使用執行時間的警告，而且通常會提供深入且有用的偵錯工具資訊。 強烈建議您在開發期間隨時開啟 D3D11 SDK 層的偵錯工具輸出，而應用程式在執行期間不會產生任何偵錯工具輸出，而是在其發行或搭配適用于 Windows 的 PIX 進行程式碼剖析時使用。 啟用 debug 層就像在裝置建立時傳遞 D3D11_CREATE_DEVICE_DEBUG 旗標一樣簡單。 強烈建議開發人員在 debug 組建中使用圖層。 不建議在設定檔或發行組建中使用圖層。<br/></td>
</tr>
<tr class="even">
<td><span id="New_Samples"></span><span id="new_samples"></span><span id="NEW_SAMPLES"></span>新範例<br/></td>
<td>此版本有四個新的範例。<br/>
<ul>
<li><a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">動態著色器連結 11</a>範例示範如何使用著色器模型5著色器介面，以及在執行時間連結著色器介面方法的 Direct3D 11 支援。</li>
<li><a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a>範例會示範如何在) 上 (CS 設定和執行計算著色器，這是 Direct3D 11 最令人興奮的新功能之一。 雖然此範例只會利用 CS 來執行 HDR 語氣對應，但是概念應該可以輕鬆擴充至其他的後置處理演算法，以及更一般的計算。</li>
<li><a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a>範例示範如何在多個執行緒之間分割轉譯，但負荷極低。</li>
<li>新的 <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> 範例與 DirectX SDK 中的 SubD10 範例非常類似，不同之處在于它已增強，可利用三種新的 Direct3D 11 管線階段：輪廓著色器、鑲嵌和網域著色器。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[先前版本中引進的功能](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

 

