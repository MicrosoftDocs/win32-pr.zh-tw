---
title: 事件處理常式
description: 事件處理常式
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Windows Media Player 的外觀、JScript 中的事件處理常式
- 在 JScript 中的事件處理常式的外觀
- 事件、JScript
- 適用于外觀的 JScript 檔案，事件處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec4413ae3a2358b01685cd0edfe66de92810a64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968205"
---
# <a name="event-handlers"></a><span data-ttu-id="a4f17-107">事件處理常式</span><span class="sxs-lookup"><span data-stu-id="a4f17-107">Event Handlers</span></span>

<span data-ttu-id="a4f17-108">Microsoft JScript 可用來處理面板定義檔中的事件。</span><span class="sxs-lookup"><span data-stu-id="a4f17-108">Microsoft JScript is used to process events in the skin definition file.</span></span> <span data-ttu-id="a4f17-109">如需事件處理常式的詳細資訊，請參閱 [處理事件](handling-events.md) 。</span><span class="sxs-lookup"><span data-stu-id="a4f17-109">See [Handling Events](handling-events.md) for more information about event handlers.</span></span>

<span data-ttu-id="a4f17-110">事件處理常式中可以有一行以上的程式碼，但必須小心不要超過 JScript 允許的行長度。</span><span class="sxs-lookup"><span data-stu-id="a4f17-110">You can have more than one line of code in an event handler, but care must be taken not to exceed the line length that JScript permits.</span></span> <span data-ttu-id="a4f17-111">以分號分隔程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="a4f17-111">Separate the lines by semicolons.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a><span data-ttu-id="a4f17-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4f17-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4f17-113">**使用 JScript**</span><span class="sxs-lookup"><span data-stu-id="a4f17-113">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




