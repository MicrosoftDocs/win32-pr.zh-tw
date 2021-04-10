---
title: 使用指令碼命令
description: 使用指令碼命令
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows Media Format SDK，指令碼命令
- Advanced Systems Format (ASF) ，script 命令
- ASF (Advanced Systems Format) ，script 命令
- 腳本，命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021531"
---
# <a name="using-script-commands"></a><span data-ttu-id="9ba26-107">使用指令碼命令</span><span class="sxs-lookup"><span data-stu-id="9ba26-107">Using Script Commands</span></span>

<span data-ttu-id="9ba26-108">Windows Media Format SDK 支援使用指令碼命令來通訊 ASF 檔案中的應用程式動作。</span><span class="sxs-lookup"><span data-stu-id="9ba26-108">The Windows Media Format SDK supports the use of script commands to communicate application actions in ASF files.</span></span> <span data-ttu-id="9ba26-109">每個指令碼命令都是由兩個字串所組成，第一個字串是命令的類型，第二個是命令資料。</span><span class="sxs-lookup"><span data-stu-id="9ba26-109">Each script command is made up of two strings, the first string is the type of command, the second is the command data.</span></span> <span data-ttu-id="9ba26-110">例如，您可以使用「URL」腳本類型，並傳遞有效的網際網路 URL 做為命令資料。</span><span class="sxs-lookup"><span data-stu-id="9ba26-110">For example, you can use the script type "URL" and pass a valid Internet URL as the command data.</span></span> <span data-ttu-id="9ba26-111">當支援型別為 "URL" 之指令碼命令的讀取應用程式收到此命令時，會在瀏覽器視窗中開啟指定的位址。</span><span class="sxs-lookup"><span data-stu-id="9ba26-111">When a reading application that supports script commands of type "URL" receives this command, it will open the specified address in a browser window.</span></span>

<span data-ttu-id="9ba26-112">Windows Media Format SDK 提供兩個選項，可讓您在 ASF 檔案中傳遞腳本。</span><span class="sxs-lookup"><span data-stu-id="9ba26-112">The Windows Media Format SDK provides two options for delivering script in ASF files.</span></span> <span data-ttu-id="9ba26-113">您可以建立腳本資料流程，也可以在檔案的標頭中包含指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="9ba26-113">You can create a script stream or you can include script commands in the header of the file.</span></span> <span data-ttu-id="9ba26-114">腳本資料流程很有用，因為指令碼命令會以展示時間順序傳遞。</span><span class="sxs-lookup"><span data-stu-id="9ba26-114">Script streams are useful because the script commands are delivered in presentation time order.</span></span> <span data-ttu-id="9ba26-115">如果您在檔案標頭中使用指令碼命令，則您的應用程式必須在開始播放之前，先取出所有的指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="9ba26-115">If you use script commands in the file header, your application will need to retrieve all of the script commands before starting playback.</span></span> <span data-ttu-id="9ba26-116">您必須追蹤指令碼命令的呈現時間，並在適當的時間進行回應。</span><span class="sxs-lookup"><span data-stu-id="9ba26-116">You must keep track of the presentation times of script commands and respond to them at the right time.</span></span>

<span data-ttu-id="9ba26-117">下列各節說明如何在 ASF 檔案中包含指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="9ba26-117">The following sections describe how to include script commands in an ASF file.</span></span>



| <span data-ttu-id="9ba26-118">區段</span><span class="sxs-lookup"><span data-stu-id="9ba26-118">Section</span></span>                                                                                                                | <span data-ttu-id="9ba26-119">描述</span><span class="sxs-lookup"><span data-stu-id="9ba26-119">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="9ba26-120">使用腳本資料流程</span><span class="sxs-lookup"><span data-stu-id="9ba26-120">To Use a Script Stream</span></span>](to-use-a-script-stream.md)                                                                   | <span data-ttu-id="9ba26-121">描述如何在腳本資料流程中包含指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="9ba26-121">Describes how to include script commands in a script stream.</span></span> |
| [<span data-ttu-id="9ba26-122">將腳本資料新增至標頭</span><span class="sxs-lookup"><span data-stu-id="9ba26-122">To Add Script Data to the Header</span></span>](to-add-script-data-to-the-header.md)                                               | <span data-ttu-id="9ba26-123">描述如何在檔案標頭中包含指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="9ba26-123">Describes how to include script commands in the file header.</span></span> |
| [<span data-ttu-id="9ba26-124">使用 Windows Media Player 所支援的指令碼命令</span><span class="sxs-lookup"><span data-stu-id="9ba26-124">Using Script Commands Supported by Windows Media Player</span></span>](using-script-commands-supported-by-windows-media-player.md) | <span data-ttu-id="9ba26-125">描述 Windows Media Player 所使用的指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="9ba26-125">Describes the script commands used by Windows Media Player.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="9ba26-126">在舊版的 Windows Media Format SDK 中，腳本串流是用來開啟對應至 ASF 檔案內容的 Web 位址。</span><span class="sxs-lookup"><span data-stu-id="9ba26-126">In previous versions of the Windows Media Format SDK, script streams were used to open Web addresses corresponding to the content of an ASF file.</span></span> <span data-ttu-id="9ba26-127">您現在可以使用 Web 資料流程來處理已同步處理的網頁。</span><span class="sxs-lookup"><span data-stu-id="9ba26-127">You can now use Web streams to work with synchronized Web pages.</span></span> <span data-ttu-id="9ba26-128">如需詳細資訊，</span><span class="sxs-lookup"><span data-stu-id="9ba26-128">For more information.</span></span> <span data-ttu-id="9ba26-129">請參閱 [Web 串流](web-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="9ba26-129">see [Web Streams](web-streams.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9ba26-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ba26-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ba26-131">**指令碼命令**</span><span class="sxs-lookup"><span data-stu-id="9ba26-131">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="9ba26-132">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="9ba26-132">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




