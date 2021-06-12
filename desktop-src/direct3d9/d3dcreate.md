---
description: 查看一或多個旗標的組合，以控制裝置在 D3DCREATE 常數中的建立行為。
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c24529c725b8b7c7f71c53718d56ceb50603
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011281"
---
# <a name="d3dcreate"></a>D3DCREATE

一或多個旗標的組合，可控制裝置的建立行為。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#定義</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>應用程式會要求裝置驅動此主要介面卡擁有的所有標頭。 Nonmaster 介面卡上的旗標不合法。 如果設定此旗標，則傳遞至 <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> 的簡報參數應指向 <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>的陣列。 <strong>D3DPRESENT_PARAMETERS</strong>中的元素數目應等於<a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>結構的 NumberOfAdaptersInGroup 成員所定義的介面卡數目。 DirectX 執行時間會以 <strong>D3DCAPS9</strong>的 AdapterOrdinalInGroup 成員所指定的數位順序，將每個元素指派給每個標頭。</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D 將會管理資源，而不是驅動程式。 對於資源錯誤（例如，視訊記憶體不足），Direct3D 呼叫將不會失敗。</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>如同 D3DCREATE_DISABLE_DRIVER_MANAGEMENT，Direct3D 將會管理資源，而不是驅動程式。 不同于 D3DCREATE_DISABLE_DRIVER_MANAGEMENT，D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX 會針對像是視頻記憶體不足的狀況傳回錯誤。</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>使執行時間不會為 Printscreen、Ctrl-Printscreen 和 Alt-Printscreen 註冊快速鍵，以抓取桌面或視窗內容。 
<table>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 此旗標僅適用于 Direct3D 9Ex。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_PSGP_THREADING</td>
<td>限制對主要應用程式執行緒的計算。 如果未設定旗標，則執行時間可能會在背景工作執行緒中執行軟體頂點處理和其他計算，以改善多處理器系統上的效能。 
<table>
<tbody>
<tr class="odd">
<td>Windows XP 與 Windows Vista 之間的差異：<br/> 此旗標適用于 Windows Vista、Windows Server 2008 和 Windows 7。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCREATE_ENABLE_PRESENTSTATS</td>
<td>可收集裝置上目前的統計資料。 對 <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> 的呼叫將會傳回有效的資料。 
<table>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 此旗標僅適用于 Direct3D 9Ex。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_FPU_PRESERVE</td>
<td>將 Direct3D 浮點數計算的有效位數設定為呼叫執行緒所使用的有效位數。 如果您未指定此旗標，Direct3D 預設為單精確度舍入至最接近的模式，原因有兩個：
<ul>
<li>雙精確度模式將會降低 Direct3D 效能。</li>
<li>Direct3D 的部分假設浮點單位例外狀況是遮罩的;取消遮罩這些例外狀況可能會導致未定義的行為。</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>指定硬體頂點處理。</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>指定混合 (軟體和硬體) 頂點處理。 針對 Windows 10，1607版和更新版本，不建議使用此設定。 請參閱 D3DCREATE_SOFTWARE_VERTEXPROCESSING。</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>指定軟體頂點處理。 針對 Windows 10，1607版和更新版本，不建議使用此設定。 使用 D3DCREATE_HARDWARE_VERTEXPROCESSING。
<div class="alert">
<blockquote>
[!Note]<br />
除非硬體頂點處理無法使用，否則不建議在 Windows 10、1607版 (和) 更新版本中使用軟體頂點處理，因為軟體頂點處理的效率大幅減少，同時改善了實施的安全性。
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>指出應用程式要求 Direct3D 為多執行緒安全。 這會讓 Direct3D 執行緒更頻繁地取得其全域 <a href="/windows/desktop/Sync/critical-section-objects">重要區段</a> 的擁有權，而這可能會降低效能。 如果應用程式在一個執行緒中處理視窗訊息，而在另一個執行緒中進行 Direct3D API 呼叫，則應用程式必須在建立裝置時使用此旗標。 您也必須在卸載 d3d9.dll 之前終結此視窗。</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>指出 Direct3D 不得以任何方式改變焦點視窗。
<div class="alert">
<blockquote>
[!Note]<br />
如果設定此旗標，應用程式必須完全支援所有焦點管理事件，例如 ALT + TAB 和滑鼠點擊事件。
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>指定 Direct3D 不支援 Get * 呼叫可儲存在狀態欄塊中的任何事物。 它也會告知 Direct3D 不要提供任何模擬服務來處理頂點。 這表示，如果裝置不支援頂點處理，則應用程式只能使用轉換後的頂點。</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>在全螢幕應用程式期間允許螢幕保護裝置。 如果沒有這個旗標，Direct3D 將會停用螢幕保護裝置，只要呼叫的應用程式是全螢幕。 如果呼叫的應用程式已經是螢幕保護裝置，此旗標不會有任何作用。 
<table>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 此旗標僅適用于 Direct3D 9Ex。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

D3DCREATE \_ 硬體 \_ VERTEXPROCESSING、D3DCREATE \_ MIXED \_ VERTEXPROCESSING 和 D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING 都是互斥的旗標。 呼叫 [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)時，必須指定至少一個頂點處理旗標。

## <a name="constant-information"></a>常數資訊



| 需求                         |  值          |
|--------------------------|------------|
| 標頭                   | D3D9。h     |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
