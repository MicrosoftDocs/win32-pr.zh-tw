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
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="003cd-103">設定進程的預設 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="003cd-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="003cd-104">Windows 上的桌面應用程式可以在不同的 DPI 感知模式下執行。</span><span class="sxs-lookup"><span data-stu-id="003cd-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="003cd-105">這些模式會啟用不同的 DPI 縮放比例行為，而且可以使用不同的座標空間。</span><span class="sxs-lookup"><span data-stu-id="003cd-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="003cd-106">如需 DPI 感知的詳細資訊，請參閱 [Windows 上的高 DPI 桌面應用程式開發。](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="003cd-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="003cd-107">請務必明確地設定流程的預設 DPI 感知模式，以避免非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="003cd-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="003cd-108">有兩個主要方法可指定進程的預設 DPI 感知：</span><span class="sxs-lookup"><span data-stu-id="003cd-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="003cd-109">1 \) 透過應用程式資訊清單設定</span><span class="sxs-lookup"><span data-stu-id="003cd-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="003cd-110">\)透過 API 呼叫以程式設計方式2</span><span class="sxs-lookup"><span data-stu-id="003cd-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="003cd-111">我們建議您透過資訊清單設定來指定預設進程 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="003cd-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="003cd-112">雖然支援指定預設 via API，但不建議使用。</span><span class="sxs-lookup"><span data-stu-id="003cd-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="003cd-113">使用應用程式資訊清單設定預設感知</span><span class="sxs-lookup"><span data-stu-id="003cd-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="003cd-114">有兩個資訊清單設定可讓您指定進程的預設 DPI 感知模式： \<dpiAwareness\> 和 \<dpiAware\> 。</span><span class="sxs-lookup"><span data-stu-id="003cd-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="003cd-115">\<dpiAware\> 是在 Windows Vista 中引進的，而且只會讓您的進程預設值設定為系統感知。</span><span class="sxs-lookup"><span data-stu-id="003cd-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="003cd-116">\<dpiAwareness\> 是在 Windows 10 1607 版中引進，可讓您指定進程預設 DPI 感知模式的已排序清單。</span><span class="sxs-lookup"><span data-stu-id="003cd-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="003cd-117">這可讓您設定備份 DPI 感知模式，如果您的應用程式是在某個版本的 Windows 上執行，而無法支援指定的第一個感知模式，則會使用此模式。</span><span class="sxs-lookup"><span data-stu-id="003cd-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="003cd-118">在較舊版本的 Windows 上，將會忽略較新的 \<dpiAwareness\> 標記。</span><span class="sxs-lookup"><span data-stu-id="003cd-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="003cd-119">這表示您可以同時使用這兩個資訊清單設定，以啟用您的進程預設值可能會對舊版 Windows 進行系統感知的情況，同時 Per-Monitor 高於 Windows 10 1607 版的版本。</span><span class="sxs-lookup"><span data-stu-id="003cd-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="003cd-120">在 Windows 10、版本1607和上， \<dpiAware\> 如果有元素，則會忽略此設定 \<dpiAwareness\> 。</span><span class="sxs-lookup"><span data-stu-id="003cd-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="003cd-121">下表說明如何使用兩個資訊清單設定來指定不同的進程預設 DPI 感知模式：</span><span class="sxs-lookup"><span data-stu-id="003cd-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="003cd-122">處理預設的 DPI 感知模式</span><span class="sxs-lookup"><span data-stu-id="003cd-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="003cd-123">&lt;DPIAware &gt; 設定</span><span class="sxs-lookup"><span data-stu-id="003cd-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="003cd-124">&lt;DPIAwareness &gt; 設定 (Windows 10，1607版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="003cd-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="003cd-125">知道</span><span class="sxs-lookup"><span data-stu-id="003cd-125">unaware</span></span></td>
<td><p><span data-ttu-id="003cd-126">N/A (資訊清單) 中沒有任何 DPIAware 設定</span><span class="sxs-lookup"><span data-stu-id="003cd-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="003cd-127">或</span><span class="sxs-lookup"><span data-stu-id="003cd-127">or</span></span></p>
<p><span data-ttu-id="003cd-128">&lt;DPIAware &gt; false &lt; /DPIAware&gt;</span><span class="sxs-lookup"><span data-stu-id="003cd-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="003cd-129">&lt;DPIAwareness 不 &gt; 知道 &lt; /DPIAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="003cd-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003cd-130">系統感知</span><span class="sxs-lookup"><span data-stu-id="003cd-130">System aware</span></span></td>
<td><span data-ttu-id="003cd-131">&lt;DPIAware &gt; true &lt; /DPIAware&gt;</span><span class="sxs-lookup"><span data-stu-id="003cd-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="003cd-132">&lt;DPIAwareness &gt; 系統 &lt; /DPIAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="003cd-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="003cd-133">每個監視器</span><span class="sxs-lookup"><span data-stu-id="003cd-133">Per Monitor</span></span></td>
<td><span data-ttu-id="003cd-134">&lt;DPIAware &gt; true/pm &lt; DPIAware&gt;</span><span class="sxs-lookup"><span data-stu-id="003cd-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="003cd-135">&lt;DPIAwareness &gt; PerMonitor &lt; /DPIAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="003cd-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003cd-136">每個監視器 V2</span><span class="sxs-lookup"><span data-stu-id="003cd-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="003cd-137">不支援</span><span class="sxs-lookup"><span data-stu-id="003cd-137">Not supported</span></span></td>
<td><span data-ttu-id="003cd-138">&lt;DPIAwareness &gt; PerMonitorV2 &lt; /DPIAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="003cd-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="003cd-139">下列範例顯示在相同的 \<dpiAwareness\> \<dpiAware\> 資訊清單檔中使用的和設定，以針對不同版本的 Windows 設定進程預設的 DPI 感知行為。</span><span class="sxs-lookup"><span data-stu-id="003cd-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

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

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="003cd-140">以程式設計方式設定預設感知</span><span class="sxs-lookup"><span data-stu-id="003cd-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="003cd-141">雖然不建議這麼做，但您可以透過程式設計的方式設定預設的 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="003cd-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="003cd-142">在您的進程中建立了一個 (HWND) 的視窗之後，就不再支援變更 DPI 感知模式。</span><span class="sxs-lookup"><span data-stu-id="003cd-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="003cd-143">如果您要以程式設計方式設定進程預設的 DPI 感知模式，您必須在建立任何 Hwnd 之前呼叫對應的 API。</span><span class="sxs-lookup"><span data-stu-id="003cd-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="003cd-144">有多個 Api 可讓您指定進程的預設 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="003cd-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="003cd-145">目前建議的 API 是 [**SetProcessDpiAwarenessCoNtext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))，因為較舊的 api 提供較少的功能。</span><span class="sxs-lookup"><span data-stu-id="003cd-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

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
<th><span data-ttu-id="003cd-146">API</span><span class="sxs-lookup"><span data-stu-id="003cd-146">API</span></span></th>
<th><span data-ttu-id="003cd-147">Windows 的最小版本</span><span class="sxs-lookup"><span data-stu-id="003cd-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="003cd-148">不知道 DPI</span><span class="sxs-lookup"><span data-stu-id="003cd-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="003cd-149">系統 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="003cd-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="003cd-150">每台監視器 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="003cd-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="003cd-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span><span class="sxs-lookup"><span data-stu-id="003cd-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span></span></td>
<td><span data-ttu-id="003cd-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="003cd-152">Windows Vista</span></span></td>
<td><span data-ttu-id="003cd-153">N/A</span><span class="sxs-lookup"><span data-stu-id="003cd-153">N/A</span></span></td>
<td><span data-ttu-id="003cd-154">SetProcessDpiAware () </span><span class="sxs-lookup"><span data-stu-id="003cd-154">SetProcessDpiAware()</span></span></td>
<td><span data-ttu-id="003cd-155">N/A</span><span class="sxs-lookup"><span data-stu-id="003cd-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003cd-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span><span class="sxs-lookup"><span data-stu-id="003cd-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="003cd-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="003cd-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="003cd-158">SetProcessDpiAwareness (PROCESS_DPI_UNAWARE) </span><span class="sxs-lookup"><span data-stu-id="003cd-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="003cd-159">SetProcessDpiAwareness (PROCESS_DPI_SYSTEM_DPI_AWARE) </span><span class="sxs-lookup"><span data-stu-id="003cd-159">SetProcessDpiAwareness(PROCESS_DPI_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="003cd-160">SetProcessDpiAwareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE) </span><span class="sxs-lookup"><span data-stu-id="003cd-160">SetProcessDpiAwareness(PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="003cd-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessCoNtext</strong></a></span><span class="sxs-lookup"><span data-stu-id="003cd-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="003cd-162">Windows 10 (版本 1607)</span><span class="sxs-lookup"><span data-stu-id="003cd-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="003cd-163">SetProcessDpiAwarenessCoNtext (DPI_AWARENESS_CONTEXT_UNAWARE) </span><span class="sxs-lookup"><span data-stu-id="003cd-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="003cd-164">SetProcessDpiAwarenessCoNtext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE) </span><span class="sxs-lookup"><span data-stu-id="003cd-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="003cd-165">SetProcessDpiAwarenessCoNtext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE) </span><span class="sxs-lookup"><span data-stu-id="003cd-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="003cd-166">SetProcessDpiAwarenessCoNtext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2) </span><span class="sxs-lookup"><span data-stu-id="003cd-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="003cd-167">進程-預設與執行緒預設值</span><span class="sxs-lookup"><span data-stu-id="003cd-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="003cd-168">本檔是指設定您的進程的預設 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="003cd-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="003cd-169">這是因為 Windows 10 在 Windows 10 之前引進了在單一進程中執行多個 DPI 感知模式的支援 (，整個程式必須符合單一的 DPI 感知模式) 。</span><span class="sxs-lookup"><span data-stu-id="003cd-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="003cd-170">支援在進程內執行多個 DPI 感知模式，稱為「混合模式 DPI 縮放比例」。</span><span class="sxs-lookup"><span data-stu-id="003cd-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="003cd-171">在您的進程中使用混合模式 DPI 縮放時，每個最上層視窗可以在 DPI 感知模式下執行，這可能會與處理常式預設值不同。</span><span class="sxs-lookup"><span data-stu-id="003cd-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="003cd-172">除非明確指定，否則每個執行緒會在建立時預設為處理常式預設值。</span><span class="sxs-lookup"><span data-stu-id="003cd-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="003cd-173">如需混合模式 DPI 縮放比例的詳細資訊，請參閱 [混合模式 Dpi 縮放比例](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) 文章。</span><span class="sxs-lookup"><span data-stu-id="003cd-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>
