---
description: 啟用元件的 JIT 啟用
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: 啟用元件的 JIT 啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972138"
---
# <a name="enabling-jit-activation-for-a-component"></a><span data-ttu-id="5474f-103">啟用元件的 JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="5474f-103">Enabling JIT Activation for a Component</span></span>

<span data-ttu-id="5474f-104">您應該將元件設定為只在正確撰寫時才啟用 JIT，以支援 COM + 即時 (JIT) 啟用服務。</span><span class="sxs-lookup"><span data-stu-id="5474f-104">You should configure a component to be JIT activated only when it is correctly written to support the COM+ Just-in-Time (JIT) Activation service.</span></span> <span data-ttu-id="5474f-105">如果在方法呼叫之間停用元件，則會遺失任何相關聯的狀態。</span><span class="sxs-lookup"><span data-stu-id="5474f-105">If a component is deactivated between method calls, it will lose any associated state.</span></span> <span data-ttu-id="5474f-106">由於 JIT 啟用的預設行為，不太可能發生這種情況，但在變更其設定以及將呼叫元件的用戶端期望之前，您應該先留意元件的需求。</span><span class="sxs-lookup"><span data-stu-id="5474f-106">Given the default behavior of JIT Activation, this is unlikely to occur when you don't expect it to, but you should be aware of a component's requirements prior to changing its configuration and of the expectations of clients that will be calling the component.</span></span>

> [!Note]  
> <span data-ttu-id="5474f-107">如果元件已設定為需要交易，則會自動啟用 COM + JIT 啟用服務。</span><span class="sxs-lookup"><span data-stu-id="5474f-107">If a component is configured to require transactions, the COM+ JIT Activation service is enabled automatically.</span></span> <span data-ttu-id="5474f-108">在此情況下，您不能停用它。</span><span class="sxs-lookup"><span data-stu-id="5474f-108">You cannot disable it in this case.</span></span> <span data-ttu-id="5474f-109">如需詳細資訊，請參閱設定 [交易](configuring-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="5474f-109">For more detail, see [Configuring Transactions](configuring-transactions.md).</span></span>

 

<span data-ttu-id="5474f-110">當您啟用元件的 JIT 啟用時，其同步處理屬性會設定為該元件的 [必要]。</span><span class="sxs-lookup"><span data-stu-id="5474f-110">When you enable JIT Activation for a component, its synchronization attribute is set to required for that component.</span></span> <span data-ttu-id="5474f-111">在此情況下，您無法變更同步處理設定。</span><span class="sxs-lookup"><span data-stu-id="5474f-111">You cannot change the synchronization setting in this case.</span></span> <span data-ttu-id="5474f-112">如需詳細資訊，請參閱 [同步](synchronization-dependencies.md)處理相依性。</span><span class="sxs-lookup"><span data-stu-id="5474f-112">For more detail, see [Synchronization Dependencies](synchronization-dependencies.md).</span></span>

<span data-ttu-id="5474f-113">**若要啟用 JIT 啟用**</span><span class="sxs-lookup"><span data-stu-id="5474f-113">**To enable JIT Activation**</span></span>

1.  <span data-ttu-id="5474f-114">在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="5474f-114">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="5474f-115">在 [元件屬性] 對話方塊中，按一下 [ **啟用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5474f-115">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="5474f-116">若要啟用元件的 JIT 啟用，請選取 [ **啟用即時啟用** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="5474f-116">To enable JIT activation for the component, select the **Enable Just In Time Activation** check box.</span></span>

4.  <span data-ttu-id="5474f-117">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="5474f-117">Click **OK**.</span></span>

<span data-ttu-id="5474f-118">當您啟用元件的 JIT 啟用時，可以選擇針對該元件所公開的任何方法啟用自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="5474f-118">When you have enabled JIT Activation for a component, you have the option of enabling the auto-done feature for any method exposed by that component.</span></span> <span data-ttu-id="5474f-119">如需詳細資訊，請參閱為 [方法啟用自動完成](enabling-auto-done-for-a-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="5474f-119">See [Enabling Auto-Done for a Method](enabling-auto-done-for-a-method.md) for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5474f-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="5474f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5474f-121">為方法啟用自動完成</span><span class="sxs-lookup"><span data-stu-id="5474f-121">Enabling Auto-Done for a Method</span></span>](enabling-auto-done-for-a-method.md)
</dt> <dt>

[<span data-ttu-id="5474f-122">設定完成位</span><span class="sxs-lookup"><span data-stu-id="5474f-122">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



