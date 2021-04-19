---
description: 設定完成位
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: 設定完成位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992394"
---
# <a name="setting-the-done-bit"></a><span data-ttu-id="c6fba-103">設定完成位</span><span class="sxs-lookup"><span data-stu-id="c6fba-103">Setting the Done Bit</span></span>

<span data-ttu-id="c6fba-104">COM + 會根據內容屬性的狀態（完成位）停用 JIT 啟動的物件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c6fba-104">COM+ will deactivate a JIT-activated object based on the status of a context property, the done bit, as follows:</span></span>

-   <span data-ttu-id="c6fba-105">當完成位設定為 True 時，COM + 會在目前的方法呼叫傳回時停用物件。</span><span class="sxs-lookup"><span data-stu-id="c6fba-105">When the done bit is set to True, COM+ deactivates the object when the current method call returns.</span></span>
-   <span data-ttu-id="c6fba-106">當完成位設定為 False 時，當目前的方法呼叫傳回時，物件會保持作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="c6fba-106">When the done bit is set to False, the object remains active when the current method call returns.</span></span>

<span data-ttu-id="c6fba-107">根據預設，當建立物件並初始化其內容時，完成位會設為 False。</span><span class="sxs-lookup"><span data-stu-id="c6fba-107">By default, the done bit is set to False when an object is created and its context initialized.</span></span> <span data-ttu-id="c6fba-108"> (任何 JIT 啟動的物件都是在它自己的內容中建立的，因此它會有自己的完成位來設定 ) 。不過，您可以使用自動完成屬性，以每個方法為基礎變更此預設設定。</span><span class="sxs-lookup"><span data-stu-id="c6fba-108">(Any JIT-activated object is created in its own context so that it has its own done bit to set.) However, you can change this default setting on a per-method basis by using the auto-done property.</span></span> <span data-ttu-id="c6fba-109">您可以透過下列方式設定完成位：</span><span class="sxs-lookup"><span data-stu-id="c6fba-109">You can set the done bit in the following ways:</span></span>

-   <span data-ttu-id="c6fba-110">使用 [ **ICoNtextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="c6fba-110">Using [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span></span>
-   <span data-ttu-id="c6fba-111">使用 [ **IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="c6fba-111">Using [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span></span>
-   <span data-ttu-id="c6fba-112">使用自動完成屬性</span><span class="sxs-lookup"><span data-stu-id="c6fba-112">Using the auto-done property</span></span>

## <a name="using-icontextstate"></a><span data-ttu-id="c6fba-113">使用 ICoNtextState</span><span class="sxs-lookup"><span data-stu-id="c6fba-113">Using IContextState</span></span>

<span data-ttu-id="c6fba-114">您可以使用 [**ICoNtextState：： SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) 將完成位設定為 True 或 False。</span><span class="sxs-lookup"><span data-stu-id="c6fba-114">You can use [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) to set the done bit to True or False.</span></span>

<span data-ttu-id="c6fba-115">您可以使用 [**ICoNtextState：： GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) 從物件內容取得完成位的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c6fba-115">You can use [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) to get the current status of the done bit from the object context.</span></span>

## <a name="using-iobjectcontext"></a><span data-ttu-id="c6fba-116">使用 IObjectCoNtext</span><span class="sxs-lookup"><span data-stu-id="c6fba-116">Using IObjectContext</span></span>

<span data-ttu-id="c6fba-117">您可以在 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 上使用下列方法來設定完成位，同時設定在交易中用來投票的一致位：</span><span class="sxs-lookup"><span data-stu-id="c6fba-117">You can use the following methods on [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) to set the done bit while simultaneously setting the consistent bit used for voting in transactions:</span></span>

-   <span data-ttu-id="c6fba-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 會通知您已完成，而且您會投票以認可目前的交易。</span><span class="sxs-lookup"><span data-stu-id="c6fba-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signals both that you are done and that you vote to commit the current transaction.</span></span> <span data-ttu-id="c6fba-119">它會將完成位和一致的位設定為 True。</span><span class="sxs-lookup"><span data-stu-id="c6fba-119">It sets both the done bit and the consistent bit to True.</span></span>
-   <span data-ttu-id="c6fba-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) 表示您已完成，並 dooms 目前的交易。</span><span class="sxs-lookup"><span data-stu-id="c6fba-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signals that you are done and dooms the current transaction.</span></span> <span data-ttu-id="c6fba-121">它會將完成的位設定為 True，並將一致的位設定為 False。</span><span class="sxs-lookup"><span data-stu-id="c6fba-121">It sets the done bit to True and the consistent bit to False.</span></span>
-   <span data-ttu-id="c6fba-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) 表示您未完成，但您已投票認可交易。</span><span class="sxs-lookup"><span data-stu-id="c6fba-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signals that you are not done but that you vote to commit the transaction.</span></span> <span data-ttu-id="c6fba-123">它會將完成的位設定為 False，並將一致的位設定為 True。</span><span class="sxs-lookup"><span data-stu-id="c6fba-123">It sets the done bit to False and the consistent bit to True.</span></span>
-   <span data-ttu-id="c6fba-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) 信號表示您未完成，而且您目前未對交易進行投票，通常是因為狀態不一致。</span><span class="sxs-lookup"><span data-stu-id="c6fba-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signals that you are not done and that you vote not to commit the transaction at this time, usually because the state is inconsistent.</span></span> <span data-ttu-id="c6fba-125">它會將完成位和一致的位設定為 False。</span><span class="sxs-lookup"><span data-stu-id="c6fba-125">It sets both the done bit and the consistent bit to False.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6fba-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6fba-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6fba-127">COM + 即時啟用概念</span><span class="sxs-lookup"><span data-stu-id="c6fba-127">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="c6fba-128">啟用元件的 JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="c6fba-128">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="c6fba-129">物件共用和 COM + JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="c6fba-129">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[<span data-ttu-id="c6fba-130">交易和 COM + JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="c6fba-130">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



