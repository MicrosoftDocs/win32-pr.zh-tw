---
title: DirectShow 和 Windows Media
description: DirectShow 和 Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK、DirectShow
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- DirectShow，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675676"
---
# <a name="directshow-and-windows-media"></a><span data-ttu-id="b3ee6-107">DirectShow 和 Windows Media</span><span class="sxs-lookup"><span data-stu-id="b3ee6-107">DirectShow and Windows Media</span></span>

<span data-ttu-id="b3ee6-108">除了單獨使用 Windows Media 格式 SDK 之外，應用程式也可以使用 Microsoft® DirectShow®串流架構來讀取和寫入 Windows Media 內容，如下列各節所述。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-108">As an alternative to using the Windows Media Format SDK exclusively, applications can also read and write Windows Media-based content by using the Microsoft® DirectShow® streaming architecture, as described in the following sections.</span></span>



| <span data-ttu-id="b3ee6-109">區段</span><span class="sxs-lookup"><span data-stu-id="b3ee6-109">Section</span></span>                                                                                   | <span data-ttu-id="b3ee6-110">描述</span><span class="sxs-lookup"><span data-stu-id="b3ee6-110">Description</span></span>                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3ee6-111">關於 DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3ee6-111">About DirectShow</span></span>](about-directshow.md)                                                  | <span data-ttu-id="b3ee6-112">描述 DirectShow 的一般術語，並告訴您要在哪裡取得更多相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-112">Describes DirectShow in general terms and tells where to get more information about it.</span></span>                                                     |
| [<span data-ttu-id="b3ee6-113">為何要使用 DirectShow？</span><span class="sxs-lookup"><span data-stu-id="b3ee6-113">Why Use DirectShow?</span></span>](why-use-directshow.md)                                             | <span data-ttu-id="b3ee6-114">描述 DirectShow 如何簡化建立和播放 Windows Media 內容的特定工作。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-114">Describes how DirectShow simplifies certain tasks in the creation and playback of Windows Media–based content.</span></span>                              |
| [<span data-ttu-id="b3ee6-115">在 DirectShow 中讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="b3ee6-115">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)                    | <span data-ttu-id="b3ee6-116">說明如何使用 DirectShow 播放 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-116">Describes how to play ASF files using DirectShow.</span></span>                                                                                           |
| [<span data-ttu-id="b3ee6-117">在 DirectShow 中建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="b3ee6-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)                  | <span data-ttu-id="b3ee6-118">說明如何使用 DirectShow 建立 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-118">Describes how to create ASF files using DirectShow.</span></span>                                                                                         |
| [<span data-ttu-id="b3ee6-119">\_DirectShow 中的 WMT 狀態事件通知</span><span class="sxs-lookup"><span data-stu-id="b3ee6-119">WMT\_STATUS Event Notification in DirectShow</span></span>](wmt-status-notification-in-directshow.md) | <span data-ttu-id="b3ee6-120">描述 ASF 讀取器和 ASF 寫入器篩選器會處理哪些 **WMT \_ 狀態** 事件，以及應用程式如何接收這些事件。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-120">Describes which **WMT\_STATUS** events are handled by the ASF Reader and ASF Writer filters, and how applications can receive those events.</span></span> |
| [<span data-ttu-id="b3ee6-121">DirectShow 中的 DRM 支援</span><span class="sxs-lookup"><span data-stu-id="b3ee6-121">DRM Support in DirectShow</span></span>](drm-support-in-directshow.md)                                | <span data-ttu-id="b3ee6-122">說明如何透過 DirectShow 讀取和寫入受 DRM 保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-122">Describes how to read and write DRM-protected files through DirectShow.</span></span>                                                                     |
| [<span data-ttu-id="b3ee6-123">DirectShow QASF 參考</span><span class="sxs-lookup"><span data-stu-id="b3ee6-123">DirectShow QASF Reference</span></span>](directshow-qasf-reference.md)                                | <span data-ttu-id="b3ee6-124">包含支援 Windows Media 之 DirectShow 元件的參考檔。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-124">Contains the reference documentation for the DirectShow components that support Windows Media.</span></span>                                              |



 

<span data-ttu-id="b3ee6-125">SDK 中的三個範例應用程式說明如何使用 DirectShow： DSCopy、DSPlay 和 DSSeekFM。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-125">Three sample applications in the SDK illustrate the use of DirectShow: DSCopy, DSPlay, and DSSeekFM.</span></span> <span data-ttu-id="b3ee6-126">如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-126">For more information, see [Sample Applications](sample-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="b3ee6-127">使用此 SDK 所含 QASF 元件的應用程式需要在 Windows®2000、Windows 98 和 Windows 95 系統上安裝 Microsoft DirectX®8.1 或更新版本的 SDK 執行時間。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-127">Applications that use the QASF components included in this SDK require the Microsoft DirectX® 8.1 or later SDK runtime to be installed on Windows® 2000, Windows 98, and Windows 95 systems.</span></span> <span data-ttu-id="b3ee6-128">具體而言，在 DirectShow 篩選圖形中裝載 Windows Media 編解碼器的 SQL-DMO 包裝函式篩選器需要此執行時間。</span><span class="sxs-lookup"><span data-stu-id="b3ee6-128">Specifically, this runtime is required by the DMO Wrapper filter which hosts the Windows Media codecs in a DirectShow filter graph.</span></span>

 

 

 




