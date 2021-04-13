---
description: 在 ASF 檔案中搜尋
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: '在 ASF 檔案中搜尋 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e957fbdf7ed7df1a9cb38b14e39d384b15ab25b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509983"
---
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="008b2-103">在 ASF 檔案中搜尋 (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="008b2-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="008b2-104">透過其 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)介面的 [WM ASF 讀取器](wm-asf-reader-filter.md)，可以在具有時態性索引的 Windows Media 內容上執行非常精確的時態搜尋。</span><span class="sxs-lookup"><span data-stu-id="008b2-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="008b2-105"> (所有框架索引的內容也包含時態性索引 ) 。在 WM ASF 讀取器中，不直接支援以框架精確的搜尋，但如果您需要這項功能，有方法可以這麼做。</span><span class="sxs-lookup"><span data-stu-id="008b2-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="008b2-106">首先，使用 Windows Media Format SDK 來建立同步讀取器物件的實例、開啟檔案、取得與指定框架相關聯的時間戳記，然後使用 DirectShow **IMediaSeeking** 介面來搜尋該時間。</span><span class="sxs-lookup"><span data-stu-id="008b2-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="008b2-107">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)介面不支援以畫面格精確的形式搜尋 Windows Media 內容。</span><span class="sxs-lookup"><span data-stu-id="008b2-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="008b2-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="008b2-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="008b2-109">在 DirectShow 中讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="008b2-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



