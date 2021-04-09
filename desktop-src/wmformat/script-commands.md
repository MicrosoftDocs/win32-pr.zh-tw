---
title: 指令碼命令
description: 指令碼命令
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows Media Format SDK，指令碼命令
- Advanced Systems Format (ASF) ，script 命令
- ASF (Advanced Systems Format) ，script 命令
- Windows Media Format SDK，腳本資料流程
- Advanced Systems Format (ASF) 、腳本資料流程
- ASF (Advanced 系統格式) 、腳本資料流程
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 腳本，命令
- 腳本，資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024298"
---
# <a name="script-commands"></a><span data-ttu-id="c126c-114">指令碼命令</span><span class="sxs-lookup"><span data-stu-id="c126c-114">Script Commands</span></span>

<span data-ttu-id="c126c-115">Windows Media 格式 SDK 所支援的指令碼命令為簡單名稱和值字串組。</span><span class="sxs-lookup"><span data-stu-id="c126c-115">The script commands supported by the Windows Media Format SDK are simple name and value string pairs.</span></span> <span data-ttu-id="c126c-116">例如，一般的指令碼命令為 "URL"，Windows Media Player 和其他播放應用程式用來開啟網頁。</span><span class="sxs-lookup"><span data-stu-id="c126c-116">For example, a common script command is "URL", which is used by Windows Media Player and other playing applications to open Web pages.</span></span> <span data-ttu-id="c126c-117">"URL" 命令的腳本配對的另一半包含有效的統一資源定位器 (URL) ，例如 `https://www.adatum.com` 。</span><span class="sxs-lookup"><span data-stu-id="c126c-117">The other half of the script pair for "URL" command contains a valid uniform resource locator (URL), such as `https://www.adatum.com`.</span></span> <span data-ttu-id="c126c-118">此 SDK 的物件不提供任何特定命令的支援;您的應用程式必須包含邏輯，才能處理您使用的任何命令。</span><span class="sxs-lookup"><span data-stu-id="c126c-118">No support is provided by the objects of this SDK for any specific commands; your application must include logic to handle whatever commands you use.</span></span> <span data-ttu-id="c126c-119">您可以使用 Windows Media Player 所支援的命令來維持與大部分播放程式的相容性。</span><span class="sxs-lookup"><span data-stu-id="c126c-119">You can use the commands supported by Windows Media Player to maintain compatibility with most players.</span></span>

<span data-ttu-id="c126c-120">您可以使用下列兩種方式之一來傳遞指令碼命令：在腳本資料流程或檔案標頭中。</span><span class="sxs-lookup"><span data-stu-id="c126c-120">Script commands can be delivered in one of two ways: in a script stream or in the file header.</span></span>

## <a name="script-streams"></a><span data-ttu-id="c126c-121">腳本資料流程</span><span class="sxs-lookup"><span data-stu-id="c126c-121">Script Streams</span></span>

<span data-ttu-id="c126c-122">您可以在 ASF 檔案的資料流程中傳遞指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="c126c-122">You can deliver script commands in their own stream in an ASF file.</span></span> <span data-ttu-id="c126c-123">腳本資料流程中的每個範例都包含名稱/值組的兩個字串。</span><span class="sxs-lookup"><span data-stu-id="c126c-123">Each sample in a script stream contains the two strings of the name/value pair.</span></span> <span data-ttu-id="c126c-124">使用腳本資料流程的優點是，命令會以正確的呈現時間傳遞。</span><span class="sxs-lookup"><span data-stu-id="c126c-124">The advantage of using a script stream is that the commands will be delivered at the correct presentation time.</span></span>

## <a name="script-commands-in-the-file-header"></a><span data-ttu-id="c126c-125">檔案標頭中的指令碼命令</span><span class="sxs-lookup"><span data-stu-id="c126c-125">Script Commands in the File Header</span></span>

<span data-ttu-id="c126c-126">指令碼命令可包含在檔案標頭中，以在播放時進行抓取。</span><span class="sxs-lookup"><span data-stu-id="c126c-126">Script commands can be included in the file header for retrieval at the time of playback.</span></span> <span data-ttu-id="c126c-127">播放應用程式會負責在適當的時間執行指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="c126c-127">The playing application is responsible for executing the script commands at the proper time.</span></span> <span data-ttu-id="c126c-128">在檔案標頭中使用指令碼命令的優點是，所有的指令碼命令都可供使用，然後才開始接收範例。</span><span class="sxs-lookup"><span data-stu-id="c126c-128">The advantage of using script commands in the file header is that all of the script commands are available before beginning to receive samples.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c126c-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="c126c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c126c-130">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="c126c-130">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="c126c-131">**使用指令碼命令**</span><span class="sxs-lookup"><span data-stu-id="c126c-131">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




