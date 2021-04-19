---
description: 您可以針對啟用 COM + JIT 啟用的元件所公開的任何方法，啟用自動完成功能。 如果已停用 JIT 啟用，則無法使用自動完成。
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: 為方法啟用自動完成
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986266"
---
# <a name="enabling-auto-done-for-a-method"></a><span data-ttu-id="a5f91-104">為方法啟用自動完成</span><span class="sxs-lookup"><span data-stu-id="a5f91-104">Enabling Auto-Done for a Method</span></span>

<span data-ttu-id="a5f91-105">您可以針對啟用 COM + JIT 啟用的元件所公開的任何方法，啟用自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="a5f91-105">You can enable the auto-done feature for any method exposed by a component for which COM+ JIT activation is enabled.</span></span> <span data-ttu-id="a5f91-106">如果已停用 JIT 啟用，則無法使用自動完成。</span><span class="sxs-lookup"><span data-stu-id="a5f91-106">If JIT activation is disabled, auto-done is unavailable.</span></span>

<span data-ttu-id="a5f91-107">您應該只針對刻意撰寫的方法啟用自動完成，以利用它，因為這項功能可能會變更方法的預期行為。</span><span class="sxs-lookup"><span data-stu-id="a5f91-107">You should enable auto-done only for a method that has intentionally been written to take advantage of it because this feature can potentially change the expected behavior of the method.</span></span>

<span data-ttu-id="a5f91-108">當您啟用自動完成時，會變更該方法的 JIT 啟用和自動交易的預設行為。</span><span class="sxs-lookup"><span data-stu-id="a5f91-108">When you enable auto-done, you are changing the default behavior of both JIT activation and automatic transactions for that method.</span></span> <span data-ttu-id="a5f91-109">您可能會想要使用這項功能，因為它可以移除明確宣告一致性和 doneness 的必要項。</span><span class="sxs-lookup"><span data-stu-id="a5f91-109">You may want to use this feature because it can remove the necessity to explicitly declare consistency and doneness.</span></span> <span data-ttu-id="a5f91-110">這可以改為在啟用自動完成時直接傳回 HRESULT 來完成。</span><span class="sxs-lookup"><span data-stu-id="a5f91-110">This can instead be done by simply returning an HRESULT when auto-done is enabled.</span></span> <span data-ttu-id="a5f91-111">基本上，當您啟用自動完成時，會指示 COM + 執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="a5f91-111">Essentially, when you enable auto-done, you are instructing COM+ to do the following:</span></span>

-   <span data-ttu-id="a5f91-112">在每次呼叫這個方法時，會在執行物件的內容上，將完成的位設定為 True。</span><span class="sxs-lookup"><span data-stu-id="a5f91-112">Set the done bit to True by default on the context in which the object runs whenever this method is called.</span></span>
-   <span data-ttu-id="a5f91-113">檢查方法傳回的 HRESULT;如果它指出成功或失敗，請適當地設定一致性位。</span><span class="sxs-lookup"><span data-stu-id="a5f91-113">Inspect the HRESULT returned by the method; if it indicates SUCCESS or FAILURE, set the consistency bit accordingly.</span></span> <span data-ttu-id="a5f91-114">這可能會導致自動呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 或 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)，這取決於方法在內部的運作方式。</span><span class="sxs-lookup"><span data-stu-id="a5f91-114">This can result in an automatic call to [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) or [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), depending also on what the method does internally.</span></span>

<span data-ttu-id="a5f91-115">**若要為方法啟用自動完成**</span><span class="sxs-lookup"><span data-stu-id="a5f91-115">**To enable auto-done for a method**</span></span>

1.  <span data-ttu-id="a5f91-116">在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠 **按右鍵您** 要設定的方法，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="a5f91-116">In the details pane of the Component Services administrative tool, right-click the method that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="a5f91-117">在 [方法屬性] 對話方塊中，按一下 [ **一般** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="a5f91-117">In the method properties dialog box, click the **General** tab.</span></span>

3.  <span data-ttu-id="a5f91-118">若要啟用自動完成，請選取 [ **當此方法傳回時自動停用此物件** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="a5f91-118">To enable auto-done, select the **Automatically deactivate this object when this method returns** check box.</span></span> <span data-ttu-id="a5f91-119">如果核取方塊無法使用，您必須先啟用元件的 JIT 啟用。</span><span class="sxs-lookup"><span data-stu-id="a5f91-119">If the check box is unavailable, you must first enable JIT Activation for the component.</span></span> <span data-ttu-id="a5f91-120">如需詳細指示，請參閱[啟用元件的 JIT 啟用](enabling-jit-activation-for-a-component.md) (。 ) </span><span class="sxs-lookup"><span data-stu-id="a5f91-120">(See[Enabling JIT Activation for a Component](enabling-jit-activation-for-a-component.md) for detailed instructions.)</span></span>

4.  <span data-ttu-id="a5f91-121">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="a5f91-121">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5f91-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5f91-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5f91-123">COM + 即時啟用概念</span><span class="sxs-lookup"><span data-stu-id="a5f91-123">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="a5f91-124">啟用元件的 JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="a5f91-124">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="a5f91-125">設定完成位</span><span class="sxs-lookup"><span data-stu-id="a5f91-125">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



