---
title: 檔案名延伸指導方針
description: 檔案名延伸指導方針
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Media Format SDK，副檔名
- Advanced Systems Format (ASF) 、副檔名
- ASF (Advanced 系統格式) 、副檔名
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932168"
---
# <a name="file-name-extension-guidelines"></a><span data-ttu-id="55452-106">檔案名延伸指導方針</span><span class="sxs-lookup"><span data-stu-id="55452-106">File Name Extension Guidelines</span></span>

<span data-ttu-id="55452-107">副檔名會提供獨立軟體廠商，包含使用該特定延伸的應用程式呈現需求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="55452-107">A file name extension provides an independent software vendor with information about the rendering requirements of an application that uses that particular extension.</span></span>

<span data-ttu-id="55452-108">您必須用於以 Windows Media Format SDK 為基礎之應用程式所建立之檔案的副檔名，取決於檔案中的內容類型。</span><span class="sxs-lookup"><span data-stu-id="55452-108">The file name extension you must use for a file created by an application based on the Windows Media Format SDK is determined by the type of content in the file.</span></span> <span data-ttu-id="55452-109">使用下列邏輯來決定您必須使用的副檔名。</span><span class="sxs-lookup"><span data-stu-id="55452-109">Use the following logic to determine the file name extension you must use.</span></span>

<span data-ttu-id="55452-110">如果檔案包含任何使用協力廠商編解碼器編碼的資料流程或任何不支援的未壓縮資料 (包括任意資料) ，則檔案必須使用 .asf 副檔名。</span><span class="sxs-lookup"><span data-stu-id="55452-110">If the file contains any streams encoded with third-party codecs or any unsupported uncompressed data (including arbitrary data), the file must use the .asf extension.</span></span>

<span data-ttu-id="55452-111">如果檔案未包含不支援的資料流程，並包含一或多個未壓縮或使用任何 Windows Media video 編解碼器編碼的影片串流，則檔案必須使用 .wmv 副檔名。</span><span class="sxs-lookup"><span data-stu-id="55452-111">If the file contains no unsupported streams and contains one or more video streams either uncompressed or encoded with any Windows Media video codec, the file must use the .wmv extension.</span></span> <span data-ttu-id="55452-112">這些檔案也可能包含 PCM 音訊串流、以任何 Windows Media 音訊編解碼器編碼的音訊串流、腳本資料流程和 Web 串流。</span><span class="sxs-lookup"><span data-stu-id="55452-112">These files may also include PCM audio streams, audio streams encoded with any Windows Media audio codec, script streams, and Web streams.</span></span>

<span data-ttu-id="55452-113">如果檔案未包含不支援的資料流程且沒有支援的視頻串流，且包含一或多個音訊串流未壓縮的 PCM 或使用任何 Windows Media 音訊編解碼器進行編碼，則檔案必須使用 .wma 副檔名。</span><span class="sxs-lookup"><span data-stu-id="55452-113">If the file contains no unsupported streams and no supported video streams, and contains one or more audio streams either uncompressed PCM or encoded with any Windows Media audio codec, the file must use the .wma extension.</span></span> <span data-ttu-id="55452-114">這些檔案也可以包含腳本資料流程和 Web 資料流程。</span><span class="sxs-lookup"><span data-stu-id="55452-114">These files may also contain script streams, and Web streams.</span></span>

<span data-ttu-id="55452-115">如果檔案只包含非音訊或影片的資料流程，則必須使用 .asf 副檔名。</span><span class="sxs-lookup"><span data-stu-id="55452-115">If the file contains only streams that are neither audio nor video, it must use the .asf extension.</span></span>

<span data-ttu-id="55452-116">支援的未壓縮影片類型包括 RGB8、RGB565、RGB555、RGB24、RGB32、I420、IYUV、YV12、YUY2、UYVY、YVYU 和 YVU9。</span><span class="sxs-lookup"><span data-stu-id="55452-116">Supported uncompressed video types include RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU, and YVU9.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55452-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="55452-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55452-118">**專案考慮**</span><span class="sxs-lookup"><span data-stu-id="55452-118">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




