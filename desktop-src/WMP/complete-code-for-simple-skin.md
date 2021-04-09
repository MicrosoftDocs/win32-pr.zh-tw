---
title: 簡單面板的完整程式碼
description: 簡單面板的完整程式碼
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- 建立外觀，程式碼範例
- Windows Media Player 的外觀，程式碼範例
- 外觀，程式碼範例
- 外觀定義檔，程式碼範例
- 建立外觀、範例
- Windows Media Player 的外觀範例
- 外觀，範例
- 外觀定義檔，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840327"
---
# <a name="complete-code-for-simple-skin"></a><span data-ttu-id="46fdd-111">簡單面板的完整程式碼</span><span class="sxs-lookup"><span data-stu-id="46fdd-111">Complete Code for Simple Skin</span></span>

<span data-ttu-id="46fdd-112">以下是第一個範例面板的完整程式碼：</span><span class="sxs-lookup"><span data-stu-id="46fdd-112">Here is the complete code for the first sample skin:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



<span data-ttu-id="46fdd-113">現在您已將所有的元件放在一起。</span><span class="sxs-lookup"><span data-stu-id="46fdd-113">Now you have all the pieces put together.</span></span>

<span data-ttu-id="46fdd-114">建立副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="46fdd-114">Create a compressed file with a .zip file name extension.</span></span> <span data-ttu-id="46fdd-115">此壓縮檔案包含您要包含的面板定義檔、點陣圖和任何數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="46fdd-115">This compressed file contains your skin definition file, bitmaps, and any digital media files you want to include.</span></span> <span data-ttu-id="46fdd-116">將檔案重新命名，使其副檔名為 wmz。</span><span class="sxs-lookup"><span data-stu-id="46fdd-116">Rename the file so that it has a .wmz file name extension.</span></span> <span data-ttu-id="46fdd-117">然後按兩下您的壓縮面板將會開始播放。</span><span class="sxs-lookup"><span data-stu-id="46fdd-117">Then double-clicking your compressed skin will start it playing.</span></span>

<span data-ttu-id="46fdd-118">您可以在 SDK 的 [範例] 區段中看到類似的工作簡單外觀。</span><span class="sxs-lookup"><span data-stu-id="46fdd-118">You can see a similar working simple skin in the samples section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46fdd-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="46fdd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46fdd-120">**建立外觀定義檔**</span><span class="sxs-lookup"><span data-stu-id="46fdd-120">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




