---
description: DirectShow SDK 和 Windows Media Format SDK
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: DirectShow SDK 和 Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321640"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a><span data-ttu-id="29765-103">DirectShow SDK 和 Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="29765-103">The DirectShow SDK and the Windows Media Format SDK</span></span>

<span data-ttu-id="29765-104">DirectShow 和 Windows Media Format SDK 提供互補的解決方案，可讓您撰寫可建立及播放 Windows Media 格式資料流程的應用程式。</span><span class="sxs-lookup"><span data-stu-id="29765-104">DirectShow and the Windows Media Format SDK offer complementary solutions for writing applications that create and play back Windows Media Format streams.</span></span> <span data-ttu-id="29765-105">如需詳細資訊，請參閱 MSDN Library 的「[音訊和影片](../audio-and-video.md)」一節。</span><span class="sxs-lookup"><span data-stu-id="29765-105">For more information, see the "[Audio and Video](../audio-and-video.md)" section of the MSDN Library.</span></span>

<span data-ttu-id="29765-106">ASF 寫入器篩選器會接受任意數量的輸入資料流程，並建立一個 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="29765-106">The ASF Writer filter accepts any number of input streams and creates an ASF file.</span></span> <span data-ttu-id="29765-107">此篩選器會使用 Windows Media Format SDK 將未壓縮的音訊或影片檔案轉換成 Windows Media 內容。</span><span class="sxs-lookup"><span data-stu-id="29765-107">The filter uses the Windows Media Format SDK to convert uncompressed audio or video files to Windows Media-based content.</span></span> <span data-ttu-id="29765-108">然後，壓縮的內容會以 ASF 容器格式儲存。</span><span class="sxs-lookup"><span data-stu-id="29765-108">The compressed content is then stored in the ASF container format.</span></span> <span data-ttu-id="29765-109">如果內容只是音訊，則會將檔案指定為 .wma 副檔名，而且稱為 Windows Media 音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="29765-109">If the content is audio only, then the file is given a .wma extension and is referred to as a Windows Media Audio file.</span></span> <span data-ttu-id="29765-110">如果內容只是影片或影片和音訊，則會將檔案指定為 .wmv 副檔名，並將其稱為 Windows Media 視訊檔案。</span><span class="sxs-lookup"><span data-stu-id="29765-110">If the content is video only or video and audio, then the file is given a .wmv extension and is referred to as a Windows Media Video file.</span></span> <span data-ttu-id="29765-111">這兩種檔案類型也可以包含中繼資料。</span><span class="sxs-lookup"><span data-stu-id="29765-111">Either type of file may also include metadata.</span></span>

<span data-ttu-id="29765-112">您可以在各種案例中使用 WM ASF 寫入器，包括數位視訊 (DV) 捕捉、音訊 recompression，以及 Audio-Video 交錯式 (AVI) 或 MPEG 多媒體檔案的轉換，以進行網路串流處理。</span><span class="sxs-lookup"><span data-stu-id="29765-112">You can use the WM ASF Writer in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG multimedia files for network streaming.</span></span> <span data-ttu-id="29765-113">此篩選器提供的唯一方法，是在 DirectShow Windows Media 視訊中建立 Microsoft® Windows Media™音訊 (WMA) 和 (WMV) 檔案。</span><span class="sxs-lookup"><span data-stu-id="29765-113">This filter provides the only way to create Microsoft® Windows Media™ Audio (WMA) and Windows Media Video (WMV) files in DirectShow®.</span></span> <span data-ttu-id="29765-114">篩選也可以建立受數位 Rights Management (DRM) 保護的檔案，也可以使用 Microsoft MPEG-2 編碼器建立 MPEG 4 內容。</span><span class="sxs-lookup"><span data-stu-id="29765-114">The filter can also create files that are secured by Digital Rights Management (DRM), and can also create MPEG-4 content using the Microsoft MPEG-4 Encoder.</span></span> <span data-ttu-id="29765-115">此內容會儲存為 ASF 容器格式。</span><span class="sxs-lookup"><span data-stu-id="29765-115">This content is stored in the ASF container format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29765-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="29765-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29765-117">在 DirectShow 中建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="29765-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
