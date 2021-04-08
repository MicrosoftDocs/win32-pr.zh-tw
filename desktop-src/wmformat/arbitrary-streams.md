---
title: 任意資料流程
description: 任意資料流程
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Media Format SDK，任意資料流程
- Advanced Systems Format (ASF) ，任意串流
- ASF (Advanced Systems Format) ，任意串流
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 任意資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671447"
---
# <a name="arbitrary-streams"></a><span data-ttu-id="6d0f5-110">任意資料流程</span><span class="sxs-lookup"><span data-stu-id="6d0f5-110">Arbitrary Streams</span></span>

<span data-ttu-id="6d0f5-111">除了音訊和影片串流和影像串流之外，ASF 檔案也可以容納包含各種資料的資料流程。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-111">In addition to audio and video streams and image streams, an ASF file can accommodate streams containing a variety of data.</span></span> <span data-ttu-id="6d0f5-112">Windows Media Format SDK 的物件提供腳本資料流程、檔案傳輸資料流程、Web 資料流程和任意資料流程的支援。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-112">The objects of the Windows Media Format SDK provide support for script streams, file transfer streams, Web streams, and arbitrary data streams.</span></span> <span data-ttu-id="6d0f5-113">這些資料流程類型全都是任意的，這表示讀取物件不會執行任何資料驗證。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-113">All of these stream types are arbitrary, meaning that no data validation is performed by the reading object.</span></span> <span data-ttu-id="6d0f5-114">當您在檔案中包含這些類型的資料流程時，請確定讀取應用程式會執行驗證或資料檢查，以確保您的內容未損毀或刻意遭到惡意的協力廠商損害。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-114">When you include streams of these types in your files, be sure that the reading application performs validation or data checking to ensure that your content has not been corrupted or intentionally mangled by a malicious third party.</span></span>

<span data-ttu-id="6d0f5-115">雖然此 SDK 的物件不會驗證或驗證任意資料流程中的資料，但原生支援數種類型的任意資料流程。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-115">Although the objects of this SDK do not verify or validate data in arbitrary streams, several types of arbitrary streams are natively supported.</span></span> <span data-ttu-id="6d0f5-116">下表列出預先定義的任意資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-116">The following table lists the predefined arbitrary stream types.</span></span> <span data-ttu-id="6d0f5-117">此外，也支援腳本資料流程，但在 [指令碼命令](script-commands.md) 區段中會另外討論。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-117">Script streams are also supported, but are discussed separately in the [Script Commands](script-commands.md) section.</span></span> <span data-ttu-id="6d0f5-118">如需建立自訂類型的詳細資訊，請參閱 [自訂任意資料流程](custom-arbitrary-data-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-118">For more information about creating custom types, see [Custom Arbitrary Data Streams](custom-arbitrary-data-streams.md).</span></span>



| <span data-ttu-id="6d0f5-119">任意類型</span><span class="sxs-lookup"><span data-stu-id="6d0f5-119">Arbitrary type</span></span>                   | <span data-ttu-id="6d0f5-120">Description</span><span class="sxs-lookup"><span data-stu-id="6d0f5-120">Description</span></span>                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="6d0f5-121">文字資料流</span><span class="sxs-lookup"><span data-stu-id="6d0f5-121">Text Streams</span></span>](text-streams.md) | <span data-ttu-id="6d0f5-122">包含文字字串。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-122">Contain text strings.</span></span>                                             |
| [<span data-ttu-id="6d0f5-123">檔案資料流程</span><span class="sxs-lookup"><span data-stu-id="6d0f5-123">File Streams</span></span>](file-streams.md) | <span data-ttu-id="6d0f5-124">包含一或多個資料檔案。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-124">Contain one or more data files.</span></span>                                   |
| [<span data-ttu-id="6d0f5-125">Web 串流</span><span class="sxs-lookup"><span data-stu-id="6d0f5-125">Web Streams</span></span>](web-streams.md)   | <span data-ttu-id="6d0f5-126">包含相當於網頁快取版本的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="6d0f5-126">Contain data files equivalent to the cached version of Web pages.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6d0f5-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d0f5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d0f5-128">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="6d0f5-128">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="6d0f5-129">**音訊和影片串流**</span><span class="sxs-lookup"><span data-stu-id="6d0f5-129">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="6d0f5-130">**設定任意資料流程類型**</span><span class="sxs-lookup"><span data-stu-id="6d0f5-130">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




