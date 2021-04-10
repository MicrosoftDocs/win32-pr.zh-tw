---
title: 使用非同步讀取器依時間進行搜尋
description: 使用非同步讀取器依時間進行搜尋
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Advanced Systems Format (ASF) ，依時間搜尋
- ASF (Advanced Systems Format) ，依時間搜尋
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- 非同步讀取器，依時間搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681425"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a><span data-ttu-id="e1864-108">使用非同步讀取器依時間進行搜尋</span><span class="sxs-lookup"><span data-stu-id="e1864-108">To Seek By Time Using the Asynchronous Reader</span></span>

<span data-ttu-id="e1864-109">如果您想要在 ASF 檔案中搜尋特定的呈現時間，必須正確設定檔案。</span><span class="sxs-lookup"><span data-stu-id="e1864-109">If you want to seek to a specific presentation time in an ASF file, the file must be properly configured.</span></span> <span data-ttu-id="e1864-110">根據預設，您只能搜尋音訊檔案，但必須先編制影片檔案的索引，才能進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="e1864-110">You can seek in audio only files by default, but video files need to be indexed before seeking.</span></span> <span data-ttu-id="e1864-111">如果您不確定如何建立檔案，您可以藉 \_ 由呼叫 [**IWMHeaderInfo：： GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)來檢查檔案標頭中的 g wszWMSeekable 屬性。</span><span class="sxs-lookup"><span data-stu-id="e1864-111">If you are not sure about how a file has been created, you can check the g\_wszWMSeekable attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="e1864-112">若要使用非同步讀取器以展示時間來搜尋 ASF 檔案中的資料，請呼叫 [**IWMReader：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start)，然後將您想要讀取之檔案部分的所需時間和持續時間，傳遞為 *cnsStart* 和 *cnsDuration* 。</span><span class="sxs-lookup"><span data-stu-id="e1864-112">To seek to data in an ASF file by presentation time using the asynchronous reader, call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passing the desired time and duration of the part of the file you want to read as *cnsStart* and *cnsDuration* respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1864-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1864-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1864-114">**IWMReader 介面**</span><span class="sxs-lookup"><span data-stu-id="e1864-114">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="e1864-115">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="e1864-115">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="e1864-116">**在播放時讀取中繼資料**</span><span class="sxs-lookup"><span data-stu-id="e1864-116">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="e1864-117">**使用索引**</span><span class="sxs-lookup"><span data-stu-id="e1864-117">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




