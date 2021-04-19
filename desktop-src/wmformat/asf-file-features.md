---
title: ASF 檔案功能
description: ASF 檔案功能
ms.assetid: 6e180f27-69ef-4fe0-b06c-b2ead7be8a05
keywords:
- Windows Media Format SDK，ASF 檔案功能
- Windows Media Format SDK，功能
- Advanced Systems Format (ASF) ，檔案功能
- ASF (Advanced Systems Format) ，檔案功能
- Advanced Systems Format (ASF) ，功能
- ASF (Advanced Systems Format) ，功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871d2986ad85716fe198b9a16e1a3772d1cca5f8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106967504"
---
# <a name="asf-file-features"></a><span data-ttu-id="4569d-109">ASF 檔案功能</span><span class="sxs-lookup"><span data-stu-id="4569d-109">ASF File Features</span></span>

<span data-ttu-id="4569d-110">Windows Media Format SDK 的主要目的是要支援以 Advanced Systems 格式封裝數位媒體資料 (ASF) 檔，並將媒體傳遞至用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="4569d-110">The primary purpose of the Windows Media Format SDK is to provide support for encapsulating digital media data in Advanced Systems Format (ASF) files and delivering the media to a client application.</span></span> <span data-ttu-id="4569d-111">傳遞案例可能會在應用程式和應用程式之間有很大的差異，但全都在撰寫和傳遞之間使用 ASF 檔案結構。</span><span class="sxs-lookup"><span data-stu-id="4569d-111">Delivery scenarios can vary widely from application to application, but all use the ASF file structure between authoring and delivery.</span></span> <span data-ttu-id="4569d-112">ASF 檔案符合定義完善但非常有彈性的結構。</span><span class="sxs-lookup"><span data-stu-id="4569d-112">ASF files conform to a well defined but very flexible structure.</span></span> <span data-ttu-id="4569d-113">如需有關 ASF 檔案結構的詳細資訊，請參閱 [Asf 格式的總覽](overview-of-the-asf-format.md)。</span><span class="sxs-lookup"><span data-stu-id="4569d-113">For more information about the ASF file structure, see [Overview of the ASF Format](overview-of-the-asf-format.md).</span></span>

<span data-ttu-id="4569d-114">您可以從 [Microsoft 網站](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)下載的 asf 規格中提供有關 asf 檔案中資料的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4569d-114">Detailed information about the data in an ASF file is provided in the ASF specification, which you can download from the [Microsoft Web site](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span></span>

<span data-ttu-id="4569d-115">Windows Media Format SDK 提供最廣泛透過用來建立檔案之設定檔的 ASF 規格功能的支援。</span><span class="sxs-lookup"><span data-stu-id="4569d-115">The Windows Media Format SDK provides support for the features of the ASF specification mostly through the profile that is used to create a file.</span></span> <span data-ttu-id="4569d-116">如需設定檔的詳細資訊，請參閱 [設定檔](profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="4569d-116">For more information about profiles, see [Profiles](profiles.md).</span></span>

<span data-ttu-id="4569d-117">本節將討論下列功能。</span><span class="sxs-lookup"><span data-stu-id="4569d-117">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="4569d-118">音訊和影片串流</span><span class="sxs-lookup"><span data-stu-id="4569d-118">Audio and Video Streams</span></span>](audio-and-video-streams.md)
-   [<span data-ttu-id="4569d-119">影像串流</span><span class="sxs-lookup"><span data-stu-id="4569d-119">Image Streams</span></span>](image-streams.md)
-   [<span data-ttu-id="4569d-120">任意資料流程</span><span class="sxs-lookup"><span data-stu-id="4569d-120">Arbitrary Streams</span></span>](arbitrary-streams.md)
-   [<span data-ttu-id="4569d-121">指令碼命令</span><span class="sxs-lookup"><span data-stu-id="4569d-121">Script Commands</span></span>](script-commands.md)
-   [<span data-ttu-id="4569d-122">資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="4569d-122">Data Unit Extensions</span></span>](data-unit-extensions.md)
-   [<span data-ttu-id="4569d-123">SMPTE 時間代碼支援</span><span class="sxs-lookup"><span data-stu-id="4569d-123">SMPTE Time Code Support</span></span>](smpte-time-code-support.md)
-   [<span data-ttu-id="4569d-124">互斥</span><span class="sxs-lookup"><span data-stu-id="4569d-124">Mutual Exclusion</span></span>](mutual-exclusion.md)
-   [<span data-ttu-id="4569d-125">資料流程優先順序</span><span class="sxs-lookup"><span data-stu-id="4569d-125">Stream Prioritization</span></span>](stream-prioritization.md)
-   [<span data-ttu-id="4569d-126">頻寬共用</span><span class="sxs-lookup"><span data-stu-id="4569d-126">Bandwidth Sharing</span></span>](bandwidth-sharing.md)
-   [<span data-ttu-id="4569d-127">索引數</span><span class="sxs-lookup"><span data-stu-id="4569d-127">Indexes</span></span>](indexes.md)
-   [<span data-ttu-id="4569d-128">標記</span><span class="sxs-lookup"><span data-stu-id="4569d-128">Markers</span></span>](markers.md)
-   [<span data-ttu-id="4569d-129">ASF 功能的讀取器回應</span><span class="sxs-lookup"><span data-stu-id="4569d-129">Reader Response to ASF Features</span></span>](reader-response-to-asf-features.md)

## <a name="related-topics"></a><span data-ttu-id="4569d-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="4569d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4569d-131">**特性**</span><span class="sxs-lookup"><span data-stu-id="4569d-131">**Features**</span></span>](features.md)
</dt> </dl>

 

 




