---
title: 新增 BUTTONGROUP
description: 新增 BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- 建立外觀，BUTTONGROUP 元素
- Windows Media Player 的 BUTTONGROUP 元素
- 外觀，BUTTONGROUP 元素
- 外觀定義檔，BUTTONGROUP 元素
- BUTTONGROUP 元素
- 元素，BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300419"
---
# <a name="adding-buttongroup"></a><span data-ttu-id="d71ce-109">新增 BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="d71ce-109">Adding BUTTONGROUP</span></span>

<span data-ttu-id="d71ce-110">這個範例會使用 **BUTTONGROUP** 專案來進行面板定義檔中的程式碼撰寫。</span><span class="sxs-lookup"><span data-stu-id="d71ce-110">This example uses the **BUTTONGROUP** element for the coding in the skin definition file.</span></span> <span data-ttu-id="d71ce-111">**BUTTONGROUP** 會建立一個簡單的方法來處理滑鼠事件，而不需要計算畫面上的確切位置，而是使用色彩，而不是 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="d71ce-111">**BUTTONGROUP** creates an easy way to process mouse events without having to calculate exact locations on the screen and uses color instead of x and y-coordinates.</span></span>

<span data-ttu-id="d71ce-112">首先，您必須將 **BUTTONGROUP** 標記新增至您建立的面板定義檔。</span><span class="sxs-lookup"><span data-stu-id="d71ce-112">First you must add the **BUTTONGROUP** tags to the skin definition file you created.</span></span> <span data-ttu-id="d71ce-113">將它們放在 **主題** 標記屬性之後。</span><span class="sxs-lookup"><span data-stu-id="d71ce-113">Put them after the **THEME** tag attributes.</span></span>


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



<span data-ttu-id="d71ce-114">針對您接下來要新增的按鈕，在結尾 **BUTTONGROUP** 標籤上方留下幾行空白行。</span><span class="sxs-lookup"><span data-stu-id="d71ce-114">Leave a few blank lines above the closing **BUTTONGROUP** tag for the buttons you will add next.</span></span>

<span data-ttu-id="d71ce-115">下列屬性是用來定義 **BUTTONGROUP**：</span><span class="sxs-lookup"><span data-stu-id="d71ce-115">The following attributes are used to define **BUTTONGROUP**:</span></span>

<span data-ttu-id="d71ce-116">**mappingImage**</span><span class="sxs-lookup"><span data-stu-id="d71ce-116">**mappingImage**</span></span>

<span data-ttu-id="d71ce-117">這是您先前建立之地圖美工檔案的檔案名，也就是具有紅色和綠色圓形的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d71ce-117">This is the file name of the mapping art file you created before, the one with the red and green circles.</span></span> <span data-ttu-id="d71ce-118">任何 **BUTTONGROUP** 都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d71ce-118">This attribute is required for any **BUTTONGROUP**.</span></span>

<span data-ttu-id="d71ce-119">**hoverImage**</span><span class="sxs-lookup"><span data-stu-id="d71ce-119">**hoverImage**</span></span>

<span data-ttu-id="d71ce-120">這是您先前建立之暫止的美工圖案檔案的檔案名，其中有兩個黃色按鈕，其會讀取「播放」和「關閉」。</span><span class="sxs-lookup"><span data-stu-id="d71ce-120">This is the file name of the hover art file you created before, the one with the two yellow buttons that read "Play" and "Close".</span></span> <span data-ttu-id="d71ce-121">這並不是必要的，但暫留影像有助於將意見反應提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="d71ce-121">This is not required, but a hover image helps to provide feedback to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d71ce-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="d71ce-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d71ce-123">**建立外觀定義檔**</span><span class="sxs-lookup"><span data-stu-id="d71ce-123">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




