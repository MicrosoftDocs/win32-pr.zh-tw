---
title: 執行範例專案
description: 執行範例專案
ms.assetid: d0c32a75-4d30-408b-8da8-3917f6fd6ea4
keywords:
- Windows Media Player 線上商店，執行範例專案
- 線上商店，執行範例專案
- 類型2線上商店，執行範例專案
- Windows Media Player 線上商店、範例專案
- 線上商店、範例專案
- 類型2線上商店、範例專案
- 正在執行範例專案
- 範例，請輸入2個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8f42829add3ffbe5cc026f7dc2451513701fd2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372388"
---
# <a name="running-the-sample-project"></a><span data-ttu-id="23b78-111">執行範例專案</span><span class="sxs-lookup"><span data-stu-id="23b78-111">Running the Sample Project</span></span>

<span data-ttu-id="23b78-112">範例 COM 元件會示範 **IWMPSubscriptionServices** 方法所提供的功能，方法是在每次 Windows Media Player 呼叫其中一個方法時顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="23b78-112">The sample COM component demonstrates the functionality provided by the methods of **IWMPSubscriptionServices** by displaying a dialog box whenever Windows Media Player calls one of the methods.</span></span> <span data-ttu-id="23b78-113">若要查看此情況，您必須先將某些內容新增至程式庫，其中包含符合您服務的 **ContentDistributor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="23b78-113">To see this happen, you must first add some content to the library that contains a **ContentDistributor** attribute that matches your service.</span></span> <span data-ttu-id="23b78-114">請參閱 [新增 ContentDistributor 屬性](adding-the-contentdistributor-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="23b78-114">See [Adding the ContentDistributor Attribute](adding-the-contentdistributor-attribute.md).</span></span> <span data-ttu-id="23b78-115">然後，使用 Windows Media Player 10 或更新版本來開啟您的線上商店、播放 premium 內容，並將您的 premium 內容複寫到裝置。</span><span class="sxs-lookup"><span data-stu-id="23b78-115">Then, use Windows Media Player 10 or later to open your online store, play your premium content, and copy your premium content to a device.</span></span> <span data-ttu-id="23b78-116">Windows Media Player 會將範例 COM 元件具現化，並在適當時呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="23b78-116">Windows Media Player will instantiate the sample COM component and call methods when appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23b78-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="23b78-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23b78-118">**建立 Type 2 線上商店的外掛程式**</span><span class="sxs-lookup"><span data-stu-id="23b78-118">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




