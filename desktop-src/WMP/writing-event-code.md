---
title: 撰寫事件程式碼
description: 撰寫事件程式碼
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Windows Media Player 的面板，撰寫程式碼
- 外觀，撰寫程式碼
- 事件，撰寫程式碼
- 撰寫適用于面板的程式碼，關於
- Windows Media Player 的外觀、事件
- 外觀，事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022055"
---
# <a name="writing-event-code"></a><span data-ttu-id="35736-109">撰寫事件程式碼</span><span class="sxs-lookup"><span data-stu-id="35736-109">Writing Event Code</span></span>

<span data-ttu-id="35736-110">事件的處理方式類似于屬性。</span><span class="sxs-lookup"><span data-stu-id="35736-110">Events are treated similarly to attributes.</span></span> <span data-ttu-id="35736-111">您必須為事件提供值，而值則是您想要在事件發生時執行的程式碼。</span><span class="sxs-lookup"><span data-stu-id="35736-111">You must give the event a value, and the value is the code you want to run when the event happens.</span></span> <span data-ttu-id="35736-112">"On" 這個字會新增至事件名稱的前方;例如，click 事件將會變成 **onclick**。</span><span class="sxs-lookup"><span data-stu-id="35736-112">The word "on" is added to the front of the event name; for example, the click event will become **onclick**.</span></span>

<span data-ttu-id="35736-113">事件值是以雙引號括住，並以後面接著冒號的單字 JScript 開頭。</span><span class="sxs-lookup"><span data-stu-id="35736-113">The event value is in double quotes and starts with the word JScript followed by a colon.</span></span> <span data-ttu-id="35736-114">接下來是您想要執行的程式碼，後面接著分號和結尾雙引號。</span><span class="sxs-lookup"><span data-stu-id="35736-114">The code you want to run comes next, followed by a semicolon and the closing double quotes.</span></span> <span data-ttu-id="35736-115">例如，若要在使用者按一下按鈕時停止播放，請在 **按鈕** 元素程式碼中輸入下列內容做為屬性：</span><span class="sxs-lookup"><span data-stu-id="35736-115">For example, to stop playing when the user clicks on a button, type the following as an attribute in your **BUTTON** element code:</span></span>


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



<span data-ttu-id="35736-116">如果您的程式碼需要用引號括住，請使用單引號。</span><span class="sxs-lookup"><span data-stu-id="35736-116">If you have a code that requires quotes, use single quotes.</span></span> <span data-ttu-id="35736-117">使用引號時必須特別小心，如此才能適當地平衡。</span><span class="sxs-lookup"><span data-stu-id="35736-117">Care must be taken when using quotation marks so that they are balanced properly.</span></span> <span data-ttu-id="35736-118">以下是使用這兩種類型的範例：</span><span class="sxs-lookup"><span data-stu-id="35736-118">Here is an example of using both types:</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



<span data-ttu-id="35736-119">您也可以在處理外來事件時變更面板的屬性。</span><span class="sxs-lookup"><span data-stu-id="35736-119">You can also change attributes of your skin when handling an external event.</span></span> <span data-ttu-id="35736-120">例如，若要關閉名為 myView 的視圖，您可以輸入：</span><span class="sxs-lookup"><span data-stu-id="35736-120">For example, to close a view named myView, you could type:</span></span>


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a><span data-ttu-id="35736-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="35736-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35736-122">**處理事件**</span><span class="sxs-lookup"><span data-stu-id="35736-122">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




