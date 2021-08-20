---
title: 2009年8月 Windows 7/Direct3D 11 SDK 的新功能
description: 此版本的 Windows 7/Direct3D 11 隨附于 DirectX SDK 中，並包含新功能、工具和檔。
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c51f350065134893ed2303d8854eb9d24fc7f58e8ab762f71da019d89d45b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608908"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a>2009年8月 Windows 7/Direct3D 11 SDK 的新功能

此版本的 Windows 7/Direct3D 11 隨附于 DirectX SDK 中，並包含新功能、工具和檔。



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
<td><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D<br/></td>
<td>Direct2D 是一種硬體加速、即時模式、2D 圖形 API，可為2D 幾何、點陣圖和文字提供高效能和高品質的呈現。 Direct2D API 是設計來與 Direct3D 和 GDI 順利互通。 此 SDK 可讓開發人員評估 API 並撰寫簡單的應用程式，並在正確設定的電腦上提供一些更先進的功能。 <br/> 適用于 Direct2D 的<a href="/windows/win32/direct2d/direct2d-portal">檔</a>和<a href="/previous-versions//dd372354(v=vs.85)">範例</a>目前可在 MSDN 上取得。<br/></td>
</tr>
<tr class="even">
<td><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br/></td>
<td>DirectWrite 支援高品質的文字轉譯、解析度無關的外框字型、完整的 Unicode 文字和版面配置支援等等，還有更多：<br/>
<ul>
<li>與裝置無關的文字版面配置系統，可改善檔和 UI 中的文字可讀性。<br/></li>
<li>高品質、子圖元、ClearType 文字轉譯，可使用 GDI Direct3D、Direct2D 或應用程式特定的轉譯技術。<br/></li>
<li>支援多重格式的文字。 <br/></li>
<li>支援 OpenType 字型的先進印刷樣式功能。<br/></li>
<li>支援 Windows 所支援之所有語言的文字版面配置和轉譯。<br/></li>
</ul>
此 SDK 可讓開發人員評估 API，並撰寫基本的應用程式以供示範之用。<br/> DirectWrite 的<a href="/windows/win32/directwrite/direct-write-portal">檔</a>和<a href="/windows/win32/directwrite/samples">範例</a>目前可在 MSDN 上取得。<br/></td>
</tr>
<tr class="odd">
<td><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1。1<br/></td>
<td><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">dxgi 1.1</a>建基於 dxgi 1.0，Windows Vista 和 Windows 7 都可使用。 DXGI 1.1 新增了數個新功能：<br/>
<ul>
<li>同步處理的共用的表面支援。 如此一來，在多個 D3D (之間，可以在 D3D10 和 D3D11) 裝置之間進行有效率的讀取和寫入介面共用。<br/></li>
<li>支援 BGRA 格式。 這可讓 GDI 轉譯至 Direct2D、Direct3D 10.1 或 Direct3D 11 裝置的目標相同 DXGI 介面。 <br/></li>
<li>最大幀延遲。 使用 <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1：： SetMaximumFrameLatency</strong></a> 和 <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1：： GetMaximumFrameLatency</strong></a>，標題可以控制提交轉譯之前，允許儲存在佇列中的框架數目。 延遲通常用來控制 CPU 如何選擇回應轉譯佇列中的使用者輸入和框架。<br/></li>
<li>介面卡列舉。 使用 <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1：： EnumAdapters1</strong></a>，標題可以列舉沒有任何監視器或輸出的本機介面卡，以及已附加輸出的介面卡。<br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>更新的範例<br/></td>
<td>此版本有數個新的和更新的範例。<br/>
<ul>
<li>新的 <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> 是可在 D3D10 或 D3D11 GPU 上執行的更先進計算著色器處理技術的圖例。</li>
<li><a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11 範例</a>已經過擴充，可使用計算著色器 (的色調對應) 來執行模糊和 bloom 效果，並提供比較的圖元著色器。</li>
<li><a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11 範例</a>已大幅更新，並有更複雜的藝術資產，以及每個執行緒的大量處理。</li>
<li><a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11 範例</a>已更新為新的臉部模型，且範例現在會利用範例內容匯出程式的相鄰計算功能。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[先前版本中引進的功能](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

