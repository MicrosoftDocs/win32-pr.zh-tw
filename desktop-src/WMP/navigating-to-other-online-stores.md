---
title: 流覽至其他線上商店
description: 流覽至其他線上商店
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player 線上商店，導覽
- 線上商店，導覽
- 輸入2個線上商店，導覽
- 流覽類型2線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300024"
---
# <a name="navigating-to-other-online-stores"></a><span data-ttu-id="61d3b-107">流覽至其他線上商店</span><span class="sxs-lookup"><span data-stu-id="61d3b-107">Navigating to Other Online Stores</span></span>

<span data-ttu-id="61d3b-108">您可以建立您所擁有之其他線上商店的連結，或與其他人所提供的線上商店連結。</span><span class="sxs-lookup"><span data-stu-id="61d3b-108">You can create links to other online stores you own or cross-link to online stores provided by others.</span></span> <span data-ttu-id="61d3b-109">若要這樣做，您需要知道您想要流覽的線上商店的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="61d3b-109">To do this, you need to know the key name for the online store to which you want to navigate.</span></span>

<span data-ttu-id="61d3b-110">下列範例程式碼顯示的 HTML 會建立一個連結，以從 Proseware online store 切換至 Southridge Video online store 的 "ServiceTask2" 功能：</span><span class="sxs-lookup"><span data-stu-id="61d3b-110">The following example code shows HTML that creates a link to switch from the Proseware online store to the "ServiceTask2" feature of the Southridge Video online store:</span></span>


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



<span data-ttu-id="61d3b-111">當使用者按一下連結時，Windows Media Player 會提示使用者切換至 Southridge 影片存放區。</span><span class="sxs-lookup"><span data-stu-id="61d3b-111">When the user clicks the link, Windows Media Player prompts the user to switch to the Southridge Video store.</span></span> <span data-ttu-id="61d3b-112">如果使用者允許，則玩家會切換儲存並流覽至指定的工作窗格，並附加查詢字串參數。</span><span class="sxs-lookup"><span data-stu-id="61d3b-112">If the user permits it, the Player then switches stores and navigates to the specified task pane, appending the query string parameters.</span></span> <span data-ttu-id="61d3b-113">上述範例中所示的查詢字串參數是自訂參數。</span><span class="sxs-lookup"><span data-stu-id="61d3b-113">The query string parameters shown in the preceding example are custom parameters.</span></span> <span data-ttu-id="61d3b-114">這表示您切換的線上商店必須預期這些值並加以處理。</span><span class="sxs-lookup"><span data-stu-id="61d3b-114">This means that the online store you switch to must expect these values and handle them.</span></span> <span data-ttu-id="61d3b-115">無論您選擇哪一種方式，您的線上商店 (以及切換至) 的任何存放區都可以使用查詢字串參數。</span><span class="sxs-lookup"><span data-stu-id="61d3b-115">Your online store (and any store you switch to) can use query string parameters any way you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61d3b-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="61d3b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61d3b-117">**在服務工作窗格之間流覽**</span><span class="sxs-lookup"><span data-stu-id="61d3b-117">**Navigating between Service Task Panes**</span></span>](navigating-between-service-task-panes.md)
</dt> <dt>

[<span data-ttu-id="61d3b-118">**類型2線上商店的流覽**</span><span class="sxs-lookup"><span data-stu-id="61d3b-118">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




