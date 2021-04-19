---
description: 深入瞭解：設定進程的預設 DPI 感知
title: '設定進程的預設 DPI 感知 (Windows) '
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: ff869974e6d9aa2eec2b3251832c061d7b6826da
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106997606"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>設定進程的預設 DPI 感知

Windows 上的桌面應用程式可以在不同的 DPI 感知模式下執行。 這些模式會啟用不同的 DPI 縮放比例行為，而且可以使用不同的座標空間。 如需 DPI 感知的詳細資訊，請參閱 [Windows 上的高 DPI 桌面應用程式開發。](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) 請務必明確地設定流程的預設 DPI 感知模式，以避免非預期的行為。

有兩個主要方法可指定進程的預設 DPI 感知：

1 \) 透過應用程式資訊清單設定

\)透過 API 呼叫以程式設計方式2

我們建議您透過資訊清單設定來指定預設進程 DPI 感知。 雖然支援指定預設 via API，但不建議使用。

## <a name="setting-default-awareness-with-the-application-manifest"></a>使用應用程式資訊清單設定預設感知

有兩個資訊清單設定可讓您指定進程的預設 DPI 感知模式： \<dpiAwareness\> 和 \<dpiAware\> 。 \<dpiAware\> 是在 Windows Vista 中引進的，而且只會讓您的進程預設值設定為系統感知。 \<dpiAwareness\> 是在 Windows 10 1607 版中引進，可讓您指定進程預設 DPI 感知模式的已排序清單。 這可讓您設定備份 DPI 感知模式，如果您的應用程式是在某個版本的 Windows 上執行，而無法支援指定的第一個感知模式，則會使用此模式。 在較舊版本的 Windows 上，將會忽略較新的 \<dpiAwareness\> 標記。 這表示您可以同時使用這兩個資訊清單設定，以啟用您的進程預設值可能會對舊版 Windows 進行系統感知的情況，同時 Per-Monitor 高於 Windows 10 1607 版的版本。 在 Windows 10、版本1607和上， \<dpiAware\> 如果有元素，則會忽略此設定 \<dpiAwareness\> 。

下表說明如何使用兩個資訊清單設定來指定不同的進程預設 DPI 感知模式：

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>處理預設的 DPI 感知模式</th>
<th>&lt;DPIAware &gt; 設定</th>
<th>&lt;DPIAwareness &gt; 設定 (Windows 10，1607版和更新版本) </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>知道</td>
<td><p>N/A (資訊清單) 中沒有任何 DPIAware 設定</p>
<p>或</p>
<p>&lt;DPIAware &gt; false &lt; /DPIAware&gt;</p></td>
<td>&lt;DPIAwareness 不 &gt; 知道 &lt; /DPIAwareness&gt;</td>
</tr>
<tr class="even">
<td>系統感知</td>
<td>&lt;DPIAware &gt; true &lt; /DPIAware&gt;</td>
<td>&lt;DPIAwareness &gt; 系統 &lt; /DPIAwareness&gt;</td>
</tr>
<tr class="odd">
<td>每個監視器</td>
<td>&lt;DPIAware &gt; true/pm &lt; DPIAware&gt;</td>
<td>&lt;DPIAwareness &gt; PerMonitor &lt; /DPIAwareness&gt;</td>
</tr>
<tr class="even">
<td>每個監視器 V2</td>
<td>不支援</td>
<td>&lt;DPIAwareness &gt; PerMonitorV2 &lt; /DPIAwareness&gt;</td>
</tr>
</tbody>
</table>

 

下列範例顯示在相同的 \<dpiAwareness\> \<dpiAware\> 資訊清單檔中使用的和設定，以針對不同版本的 Windows 設定進程預設的 DPI 感知行為。

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
  <asmv3:application>
    <asmv3:windowsSettings>
      <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
      <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

## <a name="setting-default-awareness-programmatically"></a>以程式設計方式設定預設感知

雖然不建議這麼做，但您可以透過程式設計的方式設定預設的 DPI 感知。 在您的進程中建立了一個 (HWND) 的視窗之後，就不再支援變更 DPI 感知模式。 如果您要以程式設計方式設定進程預設的 DPI 感知模式，您必須在建立任何 Hwnd 之前呼叫對應的 API。

有多個 Api 可讓您指定進程的預設 DPI 感知。 目前建議的 API 是 [**SetProcessDpiAwarenessCoNtext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))，因為較舊的 api 提供較少的功能。

 

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>API</th>
<th>Windows 的最小版本</th>
<th>不知道 DPI</th>
<th>系統 DPI 感知</th>
<th>每台監視器 DPI 感知</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></td>
<td>Windows Vista</td>
<td>N/A</td>
<td>SetProcessDpiAware () </td>
<td>N/A</td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></td>
<td>Windows 8.1</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_UNAWARE) </td>
<td>SetProcessDpiAwareness (PROCESS_DPI_SYSTEM_DPI_AWARE) </td>
<td>SetProcessDpiAwareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE) </td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessCoNtext</strong></a></td>
<td>Windows 10 (版本 1607)</td>
<td>SetProcessDpiAwarenessCoNtext (DPI_AWARENESS_CONTEXT_UNAWARE) </td>
<td>SetProcessDpiAwarenessCoNtext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE) </td>
<td><p>SetProcessDpiAwarenessCoNtext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE) </p>
<p>SetProcessDpiAwarenessCoNtext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2) </p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a>進程-預設與執行緒預設值

本檔是指設定您的進程的預設 DPI 感知。 這是因為 Windows 10 在 Windows 10 之前引進了在單一進程中執行多個 DPI 感知模式的支援 (，整個程式必須符合單一的 DPI 感知模式) 。 支援在進程內執行多個 DPI 感知模式，稱為「混合模式 DPI 縮放比例」。 在您的進程中使用混合模式 DPI 縮放時，每個最上層視窗可以在 DPI 感知模式下執行，這可能會與處理常式預設值不同。 除非明確指定，否則每個執行緒會在建立時預設為處理常式預設值。 如需混合模式 DPI 縮放比例的詳細資訊，請參閱 [混合模式 Dpi 縮放比例](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) 文章。
