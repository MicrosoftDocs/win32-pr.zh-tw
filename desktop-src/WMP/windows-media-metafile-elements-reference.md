---
title: Windows Media 中繼檔元素參考
description: Windows Media 中繼檔元素參考
ms.assetid: 6f85e488-53f6-4fb0-ba48-55c3d7e59f1c
keywords:
- Windows Media 中繼檔，參考
- 中繼檔，參考
- Windows Media 中繼檔的參考
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20e024c97e9bf8d0f8877eb3f68002702cc1a76f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372343"
---
# <a name="windows-media-metafile-elements-reference"></a><span data-ttu-id="84fe7-106">Windows Media 中繼檔元素參考</span><span class="sxs-lookup"><span data-stu-id="84fe7-106">Windows Media Metafile Elements Reference</span></span>

<span data-ttu-id="84fe7-107">本節包含用戶端應用程式之所有 Windows Media 中繼檔元素的參考檔。</span><span class="sxs-lookup"><span data-stu-id="84fe7-107">This section contains reference documentation for all Windows Media metafile elements for client-side applications.</span></span> <span data-ttu-id="84fe7-108">參考專案包含元素的定義、其屬性和值，以及與每個專案相關的特殊條件。</span><span class="sxs-lookup"><span data-stu-id="84fe7-108">Reference entries include definitions of the elements, their attributes and values, and special conditions related to each element.</span></span>

<span data-ttu-id="84fe7-109">用戶端應用程式支援下列中繼檔元素。</span><span class="sxs-lookup"><span data-stu-id="84fe7-109">The following metafile elements are supported for client-side applications.</span></span>



| <span data-ttu-id="84fe7-110">元素</span><span class="sxs-lookup"><span data-stu-id="84fe7-110">Element</span></span>                                           | <span data-ttu-id="84fe7-111">描述</span><span class="sxs-lookup"><span data-stu-id="84fe7-111">Description</span></span>                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84fe7-112">抽象</span><span class="sxs-lookup"><span data-stu-id="84fe7-112">ABSTRACT</span></span>](abstract-element.md)                  | <span data-ttu-id="84fe7-113">包含描述相關聯的 **ASX**、 **橫幅** 或 **ENTRY** 元素的文字。</span><span class="sxs-lookup"><span data-stu-id="84fe7-113">Contains text that describes the associated **ASX**, **BANNER**, or **ENTRY** element.</span></span>                                 |
| [<span data-ttu-id="84fe7-114">.ASX</span><span class="sxs-lookup"><span data-stu-id="84fe7-114">ASX</span></span>](asx-element.md)                            | <span data-ttu-id="84fe7-115">將檔案定義為 Windows Media 中繼檔。</span><span class="sxs-lookup"><span data-stu-id="84fe7-115">Defines a file as a Windows Media metafile.</span></span>                                                                            |
| [<span data-ttu-id="84fe7-116">作者</span><span class="sxs-lookup"><span data-stu-id="84fe7-116">AUTHOR</span></span>](author-element.md)                      | <span data-ttu-id="84fe7-117">包含媒體剪輯或 Windows Media 中繼檔的作者名稱。</span><span class="sxs-lookup"><span data-stu-id="84fe7-117">Contains the name of the author of a media clip or a Windows Media metafile.</span></span>                                           |
| [<span data-ttu-id="84fe7-118">旗幟</span><span class="sxs-lookup"><span data-stu-id="84fe7-118">BANNER</span></span>](banner-element.md)                      | <span data-ttu-id="84fe7-119">指定出現在 Windows Media Player 顯示面板中之圖形的 URL。</span><span class="sxs-lookup"><span data-stu-id="84fe7-119">Specifies a URL for a graphic that appears in the display panel of Windows Media Player.</span></span>                               |
| [<span data-ttu-id="84fe7-120">基地</span><span class="sxs-lookup"><span data-stu-id="84fe7-120">BASE</span></span>](base-element.md)                          | <span data-ttu-id="84fe7-121">指定附加至傳送給 Windows Media Player 之 Url 前面的字串。</span><span class="sxs-lookup"><span data-stu-id="84fe7-121">Specifies a string that is appended to the front of URLs sent to Windows Media Player.</span></span>                                 |
| [<span data-ttu-id="84fe7-122">註解</span><span class="sxs-lookup"><span data-stu-id="84fe7-122">Comments</span></span>](comments.md)                          | <span data-ttu-id="84fe7-123">指定批註的 XML 語法 (</span><span class="sxs-lookup"><span data-stu-id="84fe7-123">Specifies the XML syntax for comments (</span></span> <!--...--> <span data-ttu-id="84fe7-124">).</span><span class="sxs-lookup"><span data-stu-id="84fe7-124">).</span></span>                                                            |
| [<span data-ttu-id="84fe7-125">版權</span><span class="sxs-lookup"><span data-stu-id="84fe7-125">COPYRIGHT</span></span>](copyright-element.md)                | <span data-ttu-id="84fe7-126">包含 **ASX** 或 **ENTRY** 元素的著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="84fe7-126">Contains the copyright information for an **ASX** or **ENTRY** element.</span></span>                                                |
| [<span data-ttu-id="84fe7-127">DURATION</span><span class="sxs-lookup"><span data-stu-id="84fe7-127">DURATION</span></span>](duration-element.md)                  | <span data-ttu-id="84fe7-128">指定 Windows Media Player 呈現資料流程的時間長度。</span><span class="sxs-lookup"><span data-stu-id="84fe7-128">Specifies the length of time Windows Media Player renders a stream.</span></span>                                                    |
| [<span data-ttu-id="84fe7-129">ENDMARKER</span><span class="sxs-lookup"><span data-stu-id="84fe7-129">ENDMARKER</span></span>](endmarker-element.md)                | <span data-ttu-id="84fe7-130">指定 Windows Media Player 停止呈現資料流程的標記。</span><span class="sxs-lookup"><span data-stu-id="84fe7-130">Specifies a marker at which Windows Media Player stops rendering the stream.</span></span>                                           |
| [<span data-ttu-id="84fe7-131">進入</span><span class="sxs-lookup"><span data-stu-id="84fe7-131">ENTRY</span></span>](entry-element.md)                        | <span data-ttu-id="84fe7-132">指定媒體剪輯的路徑。</span><span class="sxs-lookup"><span data-stu-id="84fe7-132">Specifies the path for a media clip.</span></span>                                                                                   |
| [<span data-ttu-id="84fe7-133">ENTRYREF</span><span class="sxs-lookup"><span data-stu-id="84fe7-133">ENTRYREF</span></span>](entryref-element.md)                  | <span data-ttu-id="84fe7-134">連結至外部 Windows Media 中繼檔中具有 .asx、. 地板蠟、. 300k.wvx 或 wmx 副檔名的 **專案專案** 。</span><span class="sxs-lookup"><span data-stu-id="84fe7-134">Links to the **ENTRY** elements in an external Windows Media metafile that has an .asx, .wax, .wvx, or .wmx extension.</span></span> |
| [<span data-ttu-id="84fe7-135">事件</span><span class="sxs-lookup"><span data-stu-id="84fe7-135">EVENT</span></span>](event-element.md)                        | <span data-ttu-id="84fe7-136">定義在收到標記為事件的指令碼命令時，Windows Media Player 所採取的行為或動作。</span><span class="sxs-lookup"><span data-stu-id="84fe7-136">Defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span>      |
| [<span data-ttu-id="84fe7-137">LOGURL</span><span class="sxs-lookup"><span data-stu-id="84fe7-137">LOGURL</span></span>](logurl-element.md)                      | <span data-ttu-id="84fe7-138">指示 Windows Media Player 將任何記錄資料提交至指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="84fe7-138">Instructs Windows Media Player to submit any log data to the specified URL.</span></span>                                            |
| [<span data-ttu-id="84fe7-139">MOREINFO</span><span class="sxs-lookup"><span data-stu-id="84fe7-139">MOREINFO</span></span>](moreinfo-element.md)                  | <span data-ttu-id="84fe7-140">指定與顯示、剪輯或橫幅相關聯之網站、電子郵件地址或指令碼命令的 URL。</span><span class="sxs-lookup"><span data-stu-id="84fe7-140">Specifies a URL for a website, email address, or script command associated with a show, clip, or banner.</span></span>               |
| [<span data-ttu-id="84fe7-141">參數</span><span class="sxs-lookup"><span data-stu-id="84fe7-141">PARAM</span></span>](param-element.md)                        | <span data-ttu-id="84fe7-142">指定與播放清單或播放清單元素相關聯之自訂參數的值。</span><span class="sxs-lookup"><span data-stu-id="84fe7-142">Specifies the value of a custom parameter associated with a playlist or an element of a playlist.</span></span>                      |
| [<span data-ttu-id="84fe7-143">PREVIEWDURATION</span><span class="sxs-lookup"><span data-stu-id="84fe7-143">PREVIEWDURATION</span></span>](previewduration-element.md)    | <span data-ttu-id="84fe7-144">指定在預覽模式下播放剪輯的時間長度。</span><span class="sxs-lookup"><span data-stu-id="84fe7-144">Specifies the length of time a clip is played in preview mode.</span></span>                                                         |
| [<span data-ttu-id="84fe7-145">裁判</span><span class="sxs-lookup"><span data-stu-id="84fe7-145">REF</span></span>](ref-element.md)                            | <span data-ttu-id="84fe7-146">指定一段數位媒體內容的 URL。</span><span class="sxs-lookup"><span data-stu-id="84fe7-146">Specifies a URL for a piece of digital media content.</span></span>                                                                  |
| [<span data-ttu-id="84fe7-147">重複</span><span class="sxs-lookup"><span data-stu-id="84fe7-147">REPEAT</span></span>](repeat-element.md)                      | <span data-ttu-id="84fe7-148">指定 Windows Media Player 重複一或多個 **ENTRY** 或 **ENTRYREF** 元素的次數。</span><span class="sxs-lookup"><span data-stu-id="84fe7-148">Specifies the number of times Windows Media Player repeats one or more **ENTRY** or **ENTRYREF** elements.</span></span>             |
| [<span data-ttu-id="84fe7-149">面板 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="84fe7-149">SKIN (deprecated)</span></span>](skin-element--deprecated.md) | <span data-ttu-id="84fe7-150">指定內嵌面板的 URL。</span><span class="sxs-lookup"><span data-stu-id="84fe7-150">Specifies a URL to an embedded skin.</span></span>                                                                                   |
| [<span data-ttu-id="84fe7-151">STARTMARKER</span><span class="sxs-lookup"><span data-stu-id="84fe7-151">STARTMARKER</span></span>](startmarker-element.md)            | <span data-ttu-id="84fe7-152">指定 Windows Media Player 開始呈現資料流程的標記。</span><span class="sxs-lookup"><span data-stu-id="84fe7-152">Specifies a marker at which Windows Media Player starts rendering the stream.</span></span>                                          |
| [<span data-ttu-id="84fe7-153">STARTTIME</span><span class="sxs-lookup"><span data-stu-id="84fe7-153">STARTTIME</span></span>](starttime-element.md)                | <span data-ttu-id="84fe7-154">指定 Windows Media Player 將開始呈現資料流程的時間。</span><span class="sxs-lookup"><span data-stu-id="84fe7-154">Specifies a time at which Windows Media Player will start rendering the stream.</span></span>                                        |
| [<span data-ttu-id="84fe7-155">標題</span><span class="sxs-lookup"><span data-stu-id="84fe7-155">TITLE</span></span>](title-element--metafile.md)              | <span data-ttu-id="84fe7-156">包含 **ASX** 或 **ENTRY** 元素的標題。</span><span class="sxs-lookup"><span data-stu-id="84fe7-156">Contains the title of an **ASX** or **ENTRY** element.</span></span>                                                                 |



 

 

 




