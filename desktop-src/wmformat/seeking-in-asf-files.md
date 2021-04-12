---
title: '在 ASF 檔案中搜尋 (Windows Media Format 11 SDK) '
description: 在 ASF 檔案中搜尋
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK，在 ASF 檔案中搜尋
- Windows Media Format SDK、DirectShow
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) ，搜尋
- ASF (Advanced Systems Format) ，搜尋
- DirectShow，在 ASF 檔案中搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18389ded80f0202564cba0ce6384b5ff02d26fdd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024421"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="bd5e9-110">在 ASF 檔案中搜尋 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="bd5e9-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="bd5e9-111">透過其 **IMediaSeeking** 介面的 [WM ASF 讀取器](wm-asf-reader-filter.md)，可以在具有時態性索引的 Windows Media 內容上執行非常精確的時態搜尋。</span><span class="sxs-lookup"><span data-stu-id="bd5e9-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="bd5e9-112"> (所有框架索引的內容也包含時態性索引 ) 。在 WM ASF 讀取器中，不直接支援以框架精確的搜尋，但如果您需要這項功能，有方法可以這麼做。</span><span class="sxs-lookup"><span data-stu-id="bd5e9-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="bd5e9-113">首先，使用 Windows Media Format SDK 來建立同步讀取器物件的實例、開啟檔案、取得與指定框架相關聯的時間戳記，然後使用 DirectShow **IMediaSeeking** 介面來搜尋該時間。</span><span class="sxs-lookup"><span data-stu-id="bd5e9-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="bd5e9-114">DirectShow **IVideoFrameStep** 介面不支援以畫面格精確的形式搜尋以 Windows Media 為基礎的內容。</span><span class="sxs-lookup"><span data-stu-id="bd5e9-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="bd5e9-115">Windows Media 格式 SDK 中的 DSSeekFm 範例會示範如何使用 WM ASF 讀取器執行框架精確的搜尋。</span><span class="sxs-lookup"><span data-stu-id="bd5e9-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd5e9-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd5e9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd5e9-117">**WM ASF 讀取器篩選器**</span><span class="sxs-lookup"><span data-stu-id="bd5e9-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




