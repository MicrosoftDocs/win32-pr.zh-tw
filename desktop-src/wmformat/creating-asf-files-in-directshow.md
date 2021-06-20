---
title: '在 DirectShow 中建立 ASF 檔案 (Windows Media Format 11 SDK) '
description: 瞭解如何使用 Windows Media Format 11 SDK 在 DirectShow 中建立 ASF 檔案。 ASF 是一種容器格式，可包含任何類型的資料。
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK，在 DirectShow 中建立 ASF 檔案
- Windows Media Format SDK、DirectShow
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) ，在 DirectShow 中建立
- ASF (Advanced Systems Format) ，在 DirectShow 中建立
- DirectShow，建立 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e06b6deb6dc9f07115f8143309d32dcf4a58a0f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406181"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="90f44-111">在 DirectShow 中建立 ASF 檔案 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="90f44-111">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="90f44-112">您可以使用 DirectShow 直接從捕捉來源（例如 DV 攝影機）建立 ASF 檔案，或將其他檔案轉碼成 Windows Media 格式。</span><span class="sxs-lookup"><span data-stu-id="90f44-112">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="90f44-113">在任一案例中，應用程式會建立包含 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器作為轉譯器的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="90f44-113">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="90f44-114">WM ASF 寫入器提供 Windows Media 格式 SDK 的部分包裝函式。</span><span class="sxs-lookup"><span data-stu-id="90f44-114">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="90f44-115">應用程式可以使用篩選器的 [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) 介面，將系統設定檔傳入 (4、7或 8) 的系統設定檔，或直接使用 Windows MEDIA 格式 SDK 來建立自訂設定檔，以傳遞至篩選準則。</span><span class="sxs-lookup"><span data-stu-id="90f44-115">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="90f44-116">若要加入中繼資料和其他標頭資訊，應用程式會使用 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面（可從篩選中取得）。</span><span class="sxs-lookup"><span data-stu-id="90f44-116">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="90f44-117">設定設定檔和中繼資料之後，應用程式就可以直接執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="90f44-117">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="90f44-118">就內部而言，此篩選器會使用 Windows Media Format SDK 來寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="90f44-118">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="90f44-119">此篩選器會處理所有音訊影片的同步處理詳細資料，而這也是應用程式的責任。</span><span class="sxs-lookup"><span data-stu-id="90f44-119">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="90f44-120">下列各節將更詳細地說明此程式。</span><span class="sxs-lookup"><span data-stu-id="90f44-120">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="90f44-121">區段</span><span class="sxs-lookup"><span data-stu-id="90f44-121">Section</span></span>                                                                                                           | <span data-ttu-id="90f44-122">描述</span><span class="sxs-lookup"><span data-stu-id="90f44-122">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="90f44-123">設定 WM ASF 寫入器 (QASF) </span><span class="sxs-lookup"><span data-stu-id="90f44-123">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="90f44-124">說明如何設定 WM ASF 寫入器篩選器。</span><span class="sxs-lookup"><span data-stu-id="90f44-124">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="90f44-125">建立篩選圖形來將 ASF 檔案寫入 (QASF) </span><span class="sxs-lookup"><span data-stu-id="90f44-125">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="90f44-126">描述如何建立檔轉碼和捕獲圖形。</span><span class="sxs-lookup"><span data-stu-id="90f44-126">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="90f44-127"> (QASF) 設定設定檔和其他檔案屬性 </span><span class="sxs-lookup"><span data-stu-id="90f44-127">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="90f44-128">說明如何使用 WM ASF 寫入器執行各種 ASF 檔案設定工作。</span><span class="sxs-lookup"><span data-stu-id="90f44-128">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
