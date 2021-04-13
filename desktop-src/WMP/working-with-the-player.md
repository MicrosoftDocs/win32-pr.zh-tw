---
title: 使用播放玩家
description: 使用播放玩家
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player 的外觀、JScript 中的播放機屬性
- 在 JScript 中的外觀、播放機屬性
- 屬性、播放機
- player 屬性
- 適用于外觀的 JScript 檔案，player 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372638"
---
# <a name="working-with-the-player"></a><span data-ttu-id="f6bb7-108">使用播放玩家</span><span class="sxs-lookup"><span data-stu-id="f6bb7-108">Working with the Player</span></span>

<span data-ttu-id="f6bb7-109">使用 Microsoft JScript 存取 Windows Media Player 的方法和屬性時，您必須使用名稱 "Player" 作為控制項的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6bb7-109">When using Microsoft JScript to access methods and properties of Windows Media Player, you must use the name "player" for the name of the control.</span></span> <span data-ttu-id="f6bb7-110">例如，若要參考 Stop 方法，您必須輸入：</span><span class="sxs-lookup"><span data-stu-id="f6bb7-110">For example, to reference the Stop method, you must type:</span></span>


```C++
player.Controls.Stop()

```



<span data-ttu-id="f6bb7-111">**Player** global 屬性是透過外觀腳本存取 Windows Media Player 控制項的關鍵。</span><span class="sxs-lookup"><span data-stu-id="f6bb7-111">The **player** global attribute is the key to accessing the Windows Media Player control through skin scripting.</span></span> <span data-ttu-id="f6bb7-112">透過這個屬性，Windows Media Player 控制項的所有物件都會變成可透過其屬性和方法來進行執行時間修改的存取。</span><span class="sxs-lookup"><span data-stu-id="f6bb7-112">Through this attribute, all the objects of the Windows Media Player control become accessible for run-time modification through their properties and methods.</span></span> <span data-ttu-id="f6bb7-113">此外，還可以使用 **PLAYER** 元素，以便在設計階段指定事件處理常式和 **url** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f6bb7-113">Additionally, the **PLAYER** element is available so that you can specify event handlers and the **url** attribute at design time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6bb7-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6bb7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6bb7-115">**使用 JScript**</span><span class="sxs-lookup"><span data-stu-id="f6bb7-115">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




