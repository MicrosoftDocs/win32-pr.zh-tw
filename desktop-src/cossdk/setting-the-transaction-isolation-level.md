---
description: 您可以使用 [元件服務] 系統管理工具手動設定元件的交易隔離等級，也可以使用 COM + 系統管理介面，以程式設計的方式設定元件的交易隔離等級。
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: 設定交易隔離等級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689099"
---
# <a name="setting-the-transaction-isolation-level"></a><span data-ttu-id="2ef72-103">設定交易隔離等級</span><span class="sxs-lookup"><span data-stu-id="2ef72-103">Setting the Transaction Isolation Level</span></span>

<span data-ttu-id="2ef72-104">您可以使用 [元件服務] 系統管理工具手動設定元件的交易隔離等級，也可以使用 [Com + 系統管理介面](com--administration-interfaces.md)，以程式設計的方式設定元件的交易隔離等級。</span><span class="sxs-lookup"><span data-stu-id="2ef72-104">You can manually set the transaction isolation level of components by using the Component Services administrative tool, or you can programmatically configure the transaction isolation level for a component by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span>

<span data-ttu-id="2ef72-105">如需交易隔離等級的詳細資訊，請參閱設定 [交易隔離等級](configuring-transaction-isolation-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="2ef72-105">For more on transaction isolation levels, see [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md).</span></span>

<span data-ttu-id="2ef72-106">**使用元件服務系統管理工具設定交易隔離等級**</span><span class="sxs-lookup"><span data-stu-id="2ef72-106">**To set the transaction isolation level by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="2ef72-107">在主控台樹中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="2ef72-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="2ef72-108">在 [元件屬性] 對話方塊中，按一下 [ **交易** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2ef72-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="2ef72-109">在 [ **交易隔離等級**] 下，從下拉式方塊中選取您想要的值。</span><span class="sxs-lookup"><span data-stu-id="2ef72-109">Under **Transaction Isolation Level**, select the value you want from the drop-down box.</span></span> <span data-ttu-id="2ef72-110">所有元件的預設值都已 **序列化**。</span><span class="sxs-lookup"><span data-stu-id="2ef72-110">The default value for all components is **Serialized**.</span></span>

    > [!Note]  
    > <span data-ttu-id="2ef72-111">如果選取 [**交易支援**] 下的 [**停用**] 或 [**不支援**]，您就無法設定交易隔離等級。</span><span class="sxs-lookup"><span data-stu-id="2ef72-111">If either **Disabled** or **Not Supported** is selected under **Transaction support**, you cannot set the transaction isolation level.</span></span>

     

4.  <span data-ttu-id="2ef72-112">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="2ef72-112">Click **OK**.</span></span>

<span data-ttu-id="2ef72-113">您必須為每個元件重複此程式。</span><span class="sxs-lookup"><span data-stu-id="2ef72-113">You must repeat this procedure for each component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ef72-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ef72-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ef72-115">設定交易隔離等級</span><span class="sxs-lookup"><span data-stu-id="2ef72-115">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



