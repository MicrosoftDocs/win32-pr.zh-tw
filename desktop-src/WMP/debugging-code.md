---
title: 偵錯程式碼
description: 偵錯程式碼
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Windows Media Player 的面板，偵錯工具代碼
- 外觀，偵錯工具代碼
- 偵錯工具程式碼的程式碼
- Windows Media Player 的外觀、記錄
- 外觀，記錄
- 外觀中的記錄功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301895"
---
# <a name="debugging-code"></a><span data-ttu-id="9eaae-109">偵錯程式碼</span><span class="sxs-lookup"><span data-stu-id="9eaae-109">Debugging Code</span></span>

<span data-ttu-id="9eaae-110">您通常會想要查看面板中發生的情況。</span><span class="sxs-lookup"><span data-stu-id="9eaae-110">You often will want to see what is happening inside your skin.</span></span> <span data-ttu-id="9eaae-111">您可以透過文字控制項或記錄檔來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="9eaae-111">You can do this through a text control or through a log file.</span></span>

<span data-ttu-id="9eaae-112">您可以建立 **文字** 專案，並暫時將其放在面板的一部分上。</span><span class="sxs-lookup"><span data-stu-id="9eaae-112">You can create a **TEXT** element and place it on a part of your skin temporarily.</span></span> <span data-ttu-id="9eaae-113">例如，您可以使用下列程式碼來建立您的 **TEXT** 元素：</span><span class="sxs-lookup"><span data-stu-id="9eaae-113">For example, you could use the following code to create your **TEXT** element:</span></span>


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



<span data-ttu-id="9eaae-114">比方說，如果您想要查看 Windows Media Player 中數位媒體內容的目前位置，您可以使用類似下面的程式碼，在文字方塊中顯示目前的位置。</span><span class="sxs-lookup"><span data-stu-id="9eaae-114">Then, for example, if you want to see the current position of the digital media content in Windows Media Player, you could use code similar to the following to display the current position in the text box.</span></span>


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a><span data-ttu-id="9eaae-115">將調試資訊寫入記錄檔</span><span class="sxs-lookup"><span data-stu-id="9eaae-115">To Write Debugging Information to a Log File</span></span>

<span data-ttu-id="9eaae-116">若要啟用或停用偵錯工具，請變更下列登錄機碼的值：</span><span class="sxs-lookup"><span data-stu-id="9eaae-116">To enable or disable debugging, change the value of the following registry key:</span></span>

<span data-ttu-id="9eaae-117">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer 喜好設定 \\ \\ ScriptDebugging**</span><span class="sxs-lookup"><span data-stu-id="9eaae-117">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\MediaPlayer\\Preferences\\ScriptDebugging**</span></span>

<span data-ttu-id="9eaae-118">當您將值設定為1時，就會啟用記錄。</span><span class="sxs-lookup"><span data-stu-id="9eaae-118">When you set the value to 1, logging is enabled.</span></span> <span data-ttu-id="9eaae-119">當您將值設定為 0 (預設) 時，會停用記錄。</span><span class="sxs-lookup"><span data-stu-id="9eaae-119">When you set the value to 0 (the default), logging is disabled.</span></span>

<span data-ttu-id="9eaae-120">如果啟用記錄功能，檔案將會放在使用者的電腦上與面板相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="9eaae-120">If logging is enabled, a file will be placed on the user's computer in the same folder as the skin.</span></span> <span data-ttu-id="9eaae-121">檔案將命名為 "*filename* \_ 0 \_log.txt"，其中 *filename* 是面板檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eaae-121">The file will be named "*filename*\_0\_log.txt", where *filename* is the name of the skin file.</span></span> <span data-ttu-id="9eaae-122">您面板中的程式碼可以使用 *主題* 將文字寫入這個檔案。**logString** 方法。</span><span class="sxs-lookup"><span data-stu-id="9eaae-122">The code in your skin can write text to this file by using the *Theme*.**logString** method.</span></span> <span data-ttu-id="9eaae-123">如果您想要在程式碼執行時判斷在程式碼中發生的狀況，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="9eaae-123">This can be useful if you want to determine what is going on inside your code while it is running.</span></span> <span data-ttu-id="9eaae-124">請注意，文字檔是以 Unicode 字元編碼。</span><span class="sxs-lookup"><span data-stu-id="9eaae-124">Note that the text file is encoded with Unicode characters.</span></span>

<span data-ttu-id="9eaae-125">當啟用記錄功能，而且您已安裝提供偵錯工具的開發系統 (例如 Microsoft Visual Studio) 時，不是由腳本所處理的例外狀況會導致每個例外狀況的偵錯工具警告對話方塊開啟。</span><span class="sxs-lookup"><span data-stu-id="9eaae-125">When logging is enabled and you have installed a development system that provides debugging capabilities (such as Microsoft Visual Studio), exceptions that are not handled by your script code will cause a debugger warning dialog box to open for each exception.</span></span> <span data-ttu-id="9eaae-126">這是一項實用的功能，可協助您對腳本進行程式碼的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9eaae-126">This is a useful feature to help you debug your script code.</span></span> <span data-ttu-id="9eaae-127">此外，當啟用記錄功能時，您可以手動將 Windows Media Player 進程附加至偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9eaae-127">Also, you can manually attach the Windows Media Player process to your debugger when logging is enabled.</span></span>

<span data-ttu-id="9eaae-128">此 SDK 包含一個範例面板（稱為「記錄」），可示範面板中的記錄功能。</span><span class="sxs-lookup"><span data-stu-id="9eaae-128">This SDK includes a sample skin, called "logging", that demonstrates logging functionality in skins.</span></span> <span data-ttu-id="9eaae-129">若要深入瞭解如何使用範例，請參閱 [範例](samples.md)。</span><span class="sxs-lookup"><span data-stu-id="9eaae-129">To learn more about using the samples, see [Samples](samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9eaae-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="9eaae-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eaae-131">**關於外觀**</span><span class="sxs-lookup"><span data-stu-id="9eaae-131">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




