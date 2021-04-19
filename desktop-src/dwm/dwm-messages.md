---
title: DWM 訊息
description: 本節包含桌面視窗管理員 (DWM) 訊息的相關資訊。
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- 桌面視窗管理員 (DWM) ，參考
- DWM (桌面視窗管理員) ，參考
- 桌面視窗管理員 (DWM) 、訊息
- DWM (桌面視窗管理員) 、訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "106969503"
---
# <a name="dwm-messages"></a><span data-ttu-id="9cdd3-107">DWM 訊息</span><span class="sxs-lookup"><span data-stu-id="9cdd3-107">DWM Messages</span></span>

<span data-ttu-id="9cdd3-108">本節包含桌面視窗管理員 (DWM) 訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-108">This section contains information about the Desktop Window Manager (DWM) messages.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9cdd3-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="9cdd3-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9cdd3-110">主題</span><span class="sxs-lookup"><span data-stu-id="9cdd3-110">Topic</span></span></th>
<th><span data-ttu-id="9cdd3-111">描述</span><span class="sxs-lookup"><span data-stu-id="9cdd3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cdd3-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cdd3-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="9cdd3-113">通知所有最上層視窗的顏色標示色彩已變更。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-113">Informs all top-level windows that the colorization color has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cdd3-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cdd3-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="9cdd3-115">通知所有最上層視窗的 DWM 組合已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-115">Informs all top-level windows that DWM composition has been enabled or disabled.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9cdd3-116">從 Windows 8，一律會啟用 DWM 組合，因此不論影片模式變更為何，都不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-116">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cdd3-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cdd3-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="9cdd3-118">當非工作區轉譯原則變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-118">Sent when the non-client area rendering policy has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cdd3-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cdd3-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span></span><br/></td>
<td><span data-ttu-id="9cdd3-120">指示視窗提供靜態點陣圖作為 <em>即時預覽</em> (也稱為該視窗的 <em>查看預覽</em>) 。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-120">Instructs a window to provide a static bitmap to use as a <em>live preview</em> (also known as a <em>Peek preview</em>) of that window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cdd3-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cdd3-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span></span><br/></td>
<td><span data-ttu-id="9cdd3-122">指示視窗提供靜態點陣圖，以用來做為該視窗的縮圖標記法。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-122">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cdd3-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9cdd3-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="9cdd3-124">當 DWM 組成的視窗最大化時傳送。</span><span class="sxs-lookup"><span data-stu-id="9cdd3-124">Sent when a DWM composed window is maximized.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





