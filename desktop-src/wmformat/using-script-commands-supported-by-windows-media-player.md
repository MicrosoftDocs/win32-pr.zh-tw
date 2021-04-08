---
title: 使用 Windows Media Player 所支援的指令碼命令
description: 使用 Windows Media Player 所支援的指令碼命令
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows Media Format SDK，指令碼命令
- Windows Media Format SDK，Windows Media Player
- Advanced Systems Format (ASF) ，script 命令
- ASF (Advanced Systems Format) ，script 命令
- Advanced Systems Format (ASF) ，Windows Media Player
- ASF (Advanced Systems Format) ，Windows Media Player
- 腳本，命令
- 腳本，Windows Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021532"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a><span data-ttu-id="b2e05-112">使用 Windows Media Player 所支援的指令碼命令</span><span class="sxs-lookup"><span data-stu-id="b2e05-112">Using Script Commands Supported by Windows Media Player</span></span>

<span data-ttu-id="b2e05-113">Windows Media Format SDK 不提供剖析和回應指令碼命令的原生支援。</span><span class="sxs-lookup"><span data-stu-id="b2e05-113">The Windows Media Format SDK does not provide native support for parsing and responding to script commands.</span></span> <span data-ttu-id="b2e05-114">您必須在應用程式中包含與指令碼命令相關的任何邏輯。</span><span class="sxs-lookup"><span data-stu-id="b2e05-114">You must include any logic related to script commands in your application.</span></span> <span data-ttu-id="b2e05-115">您也必須在應用程式中定義您使用的腳本類型。</span><span class="sxs-lookup"><span data-stu-id="b2e05-115">The script types that you use must also be defined in your application.</span></span>

<span data-ttu-id="b2e05-116">您可以包含程式碼來處理 Windows Media Player 所支援的相同指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="b2e05-116">You can include code to handle the same script commands that are supported by Windows Media Player.</span></span> <span data-ttu-id="b2e05-117">維持與 Windows Media Player 的相容性，可讓您的檔案比內嵌自訂指令碼命令更通用。</span><span class="sxs-lookup"><span data-stu-id="b2e05-117">Maintaining compatibility with Windows Media Player makes your files more universal than if you embed custom script commands.</span></span>

<span data-ttu-id="b2e05-118">下表列出 Windows Media Player 所支援的腳本類型。</span><span class="sxs-lookup"><span data-stu-id="b2e05-118">The following table lists script types that are supported by Windows Media Player.</span></span>



| <span data-ttu-id="b2e05-119">指令碼類型</span><span class="sxs-lookup"><span data-stu-id="b2e05-119">Script type</span></span> | <span data-ttu-id="b2e05-120">描述</span><span class="sxs-lookup"><span data-stu-id="b2e05-120">Description</span></span>                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e05-121">URL</span><span class="sxs-lookup"><span data-stu-id="b2e05-121">URL</span></span>         | <span data-ttu-id="b2e05-122">播放程式會將指定的 URL 傳送給瀏覽器，以顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="b2e05-122">The player sends the specified URL to the browser for display to the user.</span></span> <span data-ttu-id="b2e05-123">如果使用內嵌播放機控制項，您可以使用 &&*framename* 語法，將特定的框架參考加入至 URL。</span><span class="sxs-lookup"><span data-stu-id="b2e05-123">If an embedded player control is being used, you can add a specific frame reference to the URL by using the &&*framename* syntax.</span></span>                                                                             |
| <span data-ttu-id="b2e05-124">檔案名</span><span class="sxs-lookup"><span data-stu-id="b2e05-124">FILENAME</span></span>    | <span data-ttu-id="b2e05-125">另一個要播放之媒體檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="b2e05-125">A URL to another media file to be played.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="b2e05-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="b2e05-126">CAPTION</span></span>     | <span data-ttu-id="b2e05-127">顯示在 Windows Media Player 的標題區域中的文字字串。</span><span class="sxs-lookup"><span data-stu-id="b2e05-127">A text string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="b2e05-128">此類型支援標準 HTML 格式，因此可以依您的需要將文字格式化。</span><span class="sxs-lookup"><span data-stu-id="b2e05-128">This type supports standard HTML formatting, so the text can be formatted as you wish.</span></span> <span data-ttu-id="b2e05-129">使用的範例有隱藏式輔助字幕。</span><span class="sxs-lookup"><span data-stu-id="b2e05-129">An example of use is closed captioning.</span></span>                                                                             |
| <span data-ttu-id="b2e05-130">事件</span><span class="sxs-lookup"><span data-stu-id="b2e05-130">EVENT</span></span>       | <span data-ttu-id="b2e05-131">要發生之事件的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e05-131">The name of an event that is to occur.</span></span> <span data-ttu-id="b2e05-132">事件種類支援自訂您自己的用途。</span><span class="sxs-lookup"><span data-stu-id="b2e05-132">The EVENT type supports customization for your own uses.</span></span> <span data-ttu-id="b2e05-133">您必須在資料流程的 Windows Media 中繼檔中定義指定事件的程式碼，播放程式才能執行指定的事件。</span><span class="sxs-lookup"><span data-stu-id="b2e05-133">The code for the specified event must be defined in the Windows Media metafile for the stream in order for the player to perform the specified event.</span></span> <span data-ttu-id="b2e05-134">使用的範例是 ad 插入。</span><span class="sxs-lookup"><span data-stu-id="b2e05-134">An example of use is ad insertion.</span></span> |
| <span data-ttu-id="b2e05-135">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="b2e05-135">OPENEVENT</span></span>   | <span data-ttu-id="b2e05-136">此腳本會在實際事件之前。</span><span class="sxs-lookup"><span data-stu-id="b2e05-136">This script precedes the actual EVENT.</span></span> <span data-ttu-id="b2e05-137">OPENEVENT 可讓播放程式預先緩衝處理內容，如此一來，當事件發生時，資料流程之間的切換就看起來很順暢。</span><span class="sxs-lookup"><span data-stu-id="b2e05-137">The OPENEVENT allows the player to pre-buffer the content so that when the EVENT occurs, the switch between streams appears to be seamless.</span></span>                                                                                                       |
| <span data-ttu-id="b2e05-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="b2e05-138">TEXT</span></span>        | <span data-ttu-id="b2e05-139">顯示在 Windows Media Player 的標題區域中的文字字串。</span><span class="sxs-lookup"><span data-stu-id="b2e05-139">A TEXT string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="b2e05-140">可以是純文字、薩米文或 HTML 格式的文字。</span><span class="sxs-lookup"><span data-stu-id="b2e05-140">Can be plain text, SAMI, or HTML formatted text.</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="b2e05-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2e05-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e05-142">**使用指令碼命令**</span><span class="sxs-lookup"><span data-stu-id="b2e05-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




