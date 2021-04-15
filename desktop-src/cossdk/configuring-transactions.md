---
description: 交易屬性是一種宣告式屬性，會自動管理元件開發人員的交易。 藉由設定這個屬性，您就不必在您的元件中使用明確的交易控制項。
ms.assetid: ea0e4d7e-2598-4a42-993c-58815f2fa138
title: 設定交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57f27d47836193dc5d23c44e3344cb2a81d5984
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104569469"
---
# <a name="configuring-transactions"></a><span data-ttu-id="80978-104">設定交易</span><span class="sxs-lookup"><span data-stu-id="80978-104">Configuring Transactions</span></span>

<span data-ttu-id="80978-105">*交易屬性* 是一種宣告式屬性，會自動管理元件開發人員的交易。</span><span class="sxs-lookup"><span data-stu-id="80978-105">The *transaction attribute* is a declarative property that automatically manages transactions for the component developer.</span></span> <span data-ttu-id="80978-106">藉由設定這個屬性，您就不必在您的元件中使用明確的交易控制項。</span><span class="sxs-lookup"><span data-stu-id="80978-106">By setting this attribute, you eliminate the need to use explicit transaction controls in your component.</span></span>

<span data-ttu-id="80978-107">COM + 會使用元件的交易屬性，判斷其啟動的每一個物件所需的交易保護類型。</span><span class="sxs-lookup"><span data-stu-id="80978-107">COM+ uses the component's transaction attribute to determine the type of transaction protection required for each object it activates.</span></span> <span data-ttu-id="80978-108">根據其需求，物件可以共用其呼叫端的交易、需要新的交易，或在沒有交易保護的情況下運作。</span><span class="sxs-lookup"><span data-stu-id="80978-108">Depending on its requirement, an object can share its caller's transaction, require a new transaction, or operate without transaction protection.</span></span>

<span data-ttu-id="80978-109">COM + 提供下列交易屬性值：</span><span class="sxs-lookup"><span data-stu-id="80978-109">COM+ provides the following transaction attribute values:</span></span>

<dl> <dt>

<span data-ttu-id="80978-110"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>禁用</span><span class="sxs-lookup"><span data-stu-id="80978-110"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>Disabled</span></span>
</dt> <dd>

<span data-ttu-id="80978-111">一般來說，只有當您確定元件永遠不會存取 resource manager 時，才應該設定此屬性值。</span><span class="sxs-lookup"><span data-stu-id="80978-111">In general, you should set this attribute value only when you are sure that the component never accesses a resource manager.</span></span> <span data-ttu-id="80978-112">當您停用交易屬性時，COM + 會在判斷物件的內容位置時，忽略元件的交易需求。</span><span class="sxs-lookup"><span data-stu-id="80978-112">When you disable the transaction attribute, COM+ ignores the transactional requirements of the component in determining context placement of the object.</span></span> <span data-ttu-id="80978-113">因此，物件可以共用其呼叫端的內容 (和交易) 。</span><span class="sxs-lookup"><span data-stu-id="80978-113">As a result, the object can share its caller's context (and transaction).</span></span> <span data-ttu-id="80978-114">將 COM 元件遷移至 COM + 時，您必須停用交易屬性，以維護與未設定的 COM 元件相同的交易行為。</span><span class="sxs-lookup"><span data-stu-id="80978-114">When migrating a COM component to COM+, you must disable the transaction attribute to maintain the same transactional behavior as the unconfigured COM component.</span></span>

> [!Note]  
> <span data-ttu-id="80978-115">未設定的 *元件* 是未安裝在 com + 應用程式中的 com 元件。</span><span class="sxs-lookup"><span data-stu-id="80978-115">An *unconfigured component* is a COM component that has not been installed in a COM+ application.</span></span>

 

</dd> <dt>

<span data-ttu-id="80978-116"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>不支援</span><span class="sxs-lookup"><span data-stu-id="80978-116"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>Not Supported</span></span>
</dt> <dd>

<span data-ttu-id="80978-117">當您設定這個屬性值時，COM + 會確保從元件建立的任何物件都不會參與交易，不論其呼叫端的交易式狀態為何。</span><span class="sxs-lookup"><span data-stu-id="80978-117">When you set this attribute value, COM+ ensures that any object created from the component never participates in a transaction, regardless of the transactional status of its caller.</span></span> <span data-ttu-id="80978-118">藉由宣告此值，您可以確定物件不會在其呼叫端的交易中進行投票，也無法開始本身的交易。</span><span class="sxs-lookup"><span data-stu-id="80978-118">By declaring this value, you ensure that an object does not vote in its caller's transaction nor can it begin a transaction of its own.</span></span> <span data-ttu-id="80978-119">[不支援] 是所有元件的預設值。</span><span class="sxs-lookup"><span data-stu-id="80978-119">Not Supported is the default value for all components.</span></span>

</dd> <dt>

<span data-ttu-id="80978-120"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>支援</span><span class="sxs-lookup"><span data-stu-id="80978-120"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>Supported</span></span>
</dt> <dd>

<span data-ttu-id="80978-121">當您設定這個屬性值時，COM + 會確保從元件建立的任何物件都參與交易（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="80978-121">When you set this attribute value, COM+ ensures that any object created from the component participates in a transaction if one exists.</span></span> <span data-ttu-id="80978-122">當您想要讓物件在其呼叫端的交易中共用，而不需要自己的交易時，您可以宣告此值。</span><span class="sxs-lookup"><span data-stu-id="80978-122">You declare this value when you want an object to share in its caller's transaction without requiring a transaction of its own.</span></span>

</dd> <dt>

<span data-ttu-id="80978-123"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>必填</span><span class="sxs-lookup"><span data-stu-id="80978-123"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>Required</span></span>
</dt> <dd>

<span data-ttu-id="80978-124">當您設定這個屬性值時，COM + 會確保從元件建立的任何物件都是交易式的。</span><span class="sxs-lookup"><span data-stu-id="80978-124">When you set this attribute value, COM+ ensures that any object created from the component is transactional.</span></span> <span data-ttu-id="80978-125">當 COM + 以必要的設定啟始物件時，它會查看其呼叫端的交易狀態。</span><span class="sxs-lookup"><span data-stu-id="80978-125">When COM+ activates an object with the Required setting, it looks at the transactional status of its caller.</span></span> <span data-ttu-id="80978-126">如果呼叫端有交易，新的物件就會包含在目前的交易中。</span><span class="sxs-lookup"><span data-stu-id="80978-126">If the caller has a transaction, the new object is included in the current transaction.</span></span> <span data-ttu-id="80978-127">否則，COM + 會開始交易，讓新的物件成為交易的根。</span><span class="sxs-lookup"><span data-stu-id="80978-127">Otherwise, COM+ begins a transaction, making the new object the root of the transaction.</span></span> <span data-ttu-id="80978-128">這是執行資源活動之元件的慣用設定，因為它有助於提供這些活動的交易保護。</span><span class="sxs-lookup"><span data-stu-id="80978-128">This is the preferred setting for a component that performs resource activities because it helps provide transaction protection for those activities.</span></span>

</dd> <dt>

<span data-ttu-id="80978-129"><span id="Requires_New"></span><span id="requires_new"></span><span id="REQUIRES_NEW"></span>需要新的</span><span class="sxs-lookup"><span data-stu-id="80978-129"><span id="Requires_New"></span><span id="requires_new"></span><span id="REQUIRES_NEW"></span>Requires New</span></span>
</dt> <dd>

<span data-ttu-id="80978-130">當您設定這個屬性值時，COM + 會確保從元件建立的任何物件都必須參與新交易做為交易的根，不論呼叫端的交易式狀態為何。</span><span class="sxs-lookup"><span data-stu-id="80978-130">When you set this attribute value, COM+ ensures that any objects created from the component must participate in a new transaction as the root of the transaction, regardless of the transactional status of the caller.</span></span> <span data-ttu-id="80978-131">COM + 會自動起始與呼叫端交易不同的新交易。</span><span class="sxs-lookup"><span data-stu-id="80978-131">COM+ automatically initiates a new transaction that is distinct from the caller's transaction.</span></span>

> [!Note]  
> <span data-ttu-id="80978-132">COM + 不支援嵌套交易。</span><span class="sxs-lookup"><span data-stu-id="80978-132">COM+ does not support nested transactions.</span></span> <span data-ttu-id="80978-133">當一個交易對象呼叫另一個標記為「需要新」的元件時，COM + 會為新啟用的物件建立獨立的交易式界限。</span><span class="sxs-lookup"><span data-stu-id="80978-133">When one transactional object calls another component marked as Requires New, COM+ creates an independent transactional boundary for the newly activated object.</span></span> <span data-ttu-id="80978-134">第二筆交易不會影響第一個交易，除非第一個交易明確注明第二筆交易的結果，並根據這些結果修改其投票。</span><span class="sxs-lookup"><span data-stu-id="80978-134">The second transaction cannot affect the first transaction unless the first transaction explicitly notes the results of the second transaction and modifies its vote based on those results.</span></span>

 

</dd> </dl>

## <a name="transaction-attribute-dependencies"></a><span data-ttu-id="80978-135">交易屬性相依性</span><span class="sxs-lookup"><span data-stu-id="80978-135">Transaction Attribute Dependencies</span></span>

<span data-ttu-id="80978-136">下表顯示每個 COM + 交易屬性值的特性，包括值對交易特性的影響。</span><span class="sxs-lookup"><span data-stu-id="80978-136">The following table shows the characteristics of each COM+ transaction attribute value, including the value's effect on transaction characteristics.</span></span> <span data-ttu-id="80978-137">COM + 會強制執行所有交易元件的 [JIT 啟用](com--just-in-time-activation.md) 和 [同步](com--synchronization.md) 處理。</span><span class="sxs-lookup"><span data-stu-id="80978-137">COM+ enforces [JIT activation](com--just-in-time-activation.md) and [Synchronization](com--synchronization.md) for all transaction components.</span></span>



| <span data-ttu-id="80978-138">屬性值</span><span class="sxs-lookup"><span data-stu-id="80978-138">Attribute Value</span></span>          | <span data-ttu-id="80978-139">新增交易</span><span class="sxs-lookup"><span data-stu-id="80978-139">New Transaction</span></span>   | <span data-ttu-id="80978-140">用戶端的交易</span><span class="sxs-lookup"><span data-stu-id="80978-140">Client's Transaction</span></span>                 | <span data-ttu-id="80978-141">交易根目錄</span><span class="sxs-lookup"><span data-stu-id="80978-141">Transaction Root</span></span>                        | <span data-ttu-id="80978-142">JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="80978-142">JIT Activation</span></span>      | <span data-ttu-id="80978-143">同步處理</span><span class="sxs-lookup"><span data-stu-id="80978-143">Synchronization</span></span>     |
|--------------------------|-------------------|--------------------------------------|-----------------------------------------|---------------------|---------------------|
| <span data-ttu-id="80978-144">Disabled</span><span class="sxs-lookup"><span data-stu-id="80978-144">Disabled</span></span><br/>      | <span data-ttu-id="80978-145">永不</span><span class="sxs-lookup"><span data-stu-id="80978-145">Never</span></span><br/>  | <span data-ttu-id="80978-146">可能</span><span class="sxs-lookup"><span data-stu-id="80978-146">Maybe</span></span><br/>                     | <span data-ttu-id="80978-147">永不</span><span class="sxs-lookup"><span data-stu-id="80978-147">Never</span></span><br/>                        | <span data-ttu-id="80978-148">選用</span><span class="sxs-lookup"><span data-stu-id="80978-148">Optional</span></span><br/> | <span data-ttu-id="80978-149">選用</span><span class="sxs-lookup"><span data-stu-id="80978-149">Optional</span></span><br/> |
| <span data-ttu-id="80978-150">不支援</span><span class="sxs-lookup"><span data-stu-id="80978-150">Not Supported</span></span><br/> | <span data-ttu-id="80978-151">永不</span><span class="sxs-lookup"><span data-stu-id="80978-151">Never</span></span><br/>  | <span data-ttu-id="80978-152">永不</span><span class="sxs-lookup"><span data-stu-id="80978-152">Never</span></span><br/>                     | <span data-ttu-id="80978-153">永不</span><span class="sxs-lookup"><span data-stu-id="80978-153">Never</span></span><br/>                        | <span data-ttu-id="80978-154">選用</span><span class="sxs-lookup"><span data-stu-id="80978-154">Optional</span></span><br/> | <span data-ttu-id="80978-155">選用</span><span class="sxs-lookup"><span data-stu-id="80978-155">Optional</span></span><br/> |
| <span data-ttu-id="80978-156">支援</span><span class="sxs-lookup"><span data-stu-id="80978-156">Supported</span></span><br/>     | <span data-ttu-id="80978-157">永不</span><span class="sxs-lookup"><span data-stu-id="80978-157">Never</span></span><br/>  | <span data-ttu-id="80978-158">如果用戶端有交易</span><span class="sxs-lookup"><span data-stu-id="80978-158">If client has transaction</span></span><br/> | <span data-ttu-id="80978-159">永不</span><span class="sxs-lookup"><span data-stu-id="80978-159">Never</span></span><br/>                        | <span data-ttu-id="80978-160">必要</span><span class="sxs-lookup"><span data-stu-id="80978-160">Required</span></span><br/> | <span data-ttu-id="80978-161">必要</span><span class="sxs-lookup"><span data-stu-id="80978-161">Required</span></span><br/> |
| <span data-ttu-id="80978-162">必要</span><span class="sxs-lookup"><span data-stu-id="80978-162">Required</span></span><br/>      | <span data-ttu-id="80978-163">可能</span><span class="sxs-lookup"><span data-stu-id="80978-163">Maybe</span></span><br/>  | <span data-ttu-id="80978-164">如果用戶端有交易</span><span class="sxs-lookup"><span data-stu-id="80978-164">If client has transaction</span></span><br/> | <span data-ttu-id="80978-165">如果用戶端沒有交易</span><span class="sxs-lookup"><span data-stu-id="80978-165">If client has no transaction</span></span><br/> | <span data-ttu-id="80978-166">必要</span><span class="sxs-lookup"><span data-stu-id="80978-166">Required</span></span><br/> | <span data-ttu-id="80978-167">必要</span><span class="sxs-lookup"><span data-stu-id="80978-167">Required</span></span><br/> |
| <span data-ttu-id="80978-168">必須是新交易</span><span class="sxs-lookup"><span data-stu-id="80978-168">Requires New</span></span><br/>  | <span data-ttu-id="80978-169">一律</span><span class="sxs-lookup"><span data-stu-id="80978-169">Always</span></span><br/> | <span data-ttu-id="80978-170">永不</span><span class="sxs-lookup"><span data-stu-id="80978-170">Never</span></span><br/>                     | <span data-ttu-id="80978-171">一律</span><span class="sxs-lookup"><span data-stu-id="80978-171">Always</span></span><br/>                       | <span data-ttu-id="80978-172">必要</span><span class="sxs-lookup"><span data-stu-id="80978-172">Required</span></span><br/> | <span data-ttu-id="80978-173">必要</span><span class="sxs-lookup"><span data-stu-id="80978-173">Required</span></span><br/> |



 

## <a name="transaction-boundaries"></a><span data-ttu-id="80978-174">交易界限</span><span class="sxs-lookup"><span data-stu-id="80978-174">Transaction Boundaries</span></span>

<span data-ttu-id="80978-175">交易具有開頭、結尾，而且只會發生一次。</span><span class="sxs-lookup"><span data-stu-id="80978-175">A transaction has a beginning, an end, and occurs exactly once.</span></span> <span data-ttu-id="80978-176">在其執行期間，交易可能會對資源（例如資料庫或佇列）進行呼叫，以完成一或多個工作。</span><span class="sxs-lookup"><span data-stu-id="80978-176">During its execution, a transaction may call on a resource, such as a database or queue, to accomplish one or more tasks.</span></span> <span data-ttu-id="80978-177">每個資源都落在 *交易界限* 內。</span><span class="sxs-lookup"><span data-stu-id="80978-177">Each resource falls within the *transaction boundary*.</span></span> <span data-ttu-id="80978-178">交易界限內的所有資源（可以跨多個進程和電腦界限）共用單一交易。</span><span class="sxs-lookup"><span data-stu-id="80978-178">All resources within a transaction boundary, which can span multiple process and computer boundaries, share a single transaction.</span></span> <span data-ttu-id="80978-179">管理這些程式和電腦界限之間的一致性相當重要。</span><span class="sxs-lookup"><span data-stu-id="80978-179">Managing consistency across these process and computer boundaries is important.</span></span>

<span data-ttu-id="80978-180">COM + 會根據您為每個元件設定的交易屬性值，自動管理交易界限以確保一致性。</span><span class="sxs-lookup"><span data-stu-id="80978-180">COM+ ensures consistency by managing transaction boundaries automatically, based on the value of the transaction attribute that you set for each component.</span></span> <span data-ttu-id="80978-181">COM + 交易會自動流向已指示參與交易的物件，並略過在交易外指示執行的物件。</span><span class="sxs-lookup"><span data-stu-id="80978-181">A COM+ transaction automatically flows to objects instructed to participate in a transaction and bypasses objects instructed to execute outside a transaction.</span></span> <span data-ttu-id="80978-182">COM + 不支援嵌套交易。</span><span class="sxs-lookup"><span data-stu-id="80978-182">COM+ does not support nested transactions.</span></span> <span data-ttu-id="80978-183">相反地，COM + 交易是不同的，而且存留期很短。</span><span class="sxs-lookup"><span data-stu-id="80978-183">Instead, COM+ transactions are distinct and short-lived.</span></span>

<span data-ttu-id="80978-184">交易界限中的第一個物件是交易的特殊物件，稱為交易的 *根物件* 。</span><span class="sxs-lookup"><span data-stu-id="80978-184">The first object in a transaction boundary is special to the transaction and is called the *root object* of the transaction.</span></span> <span data-ttu-id="80978-185">交易中只能有一個根物件。</span><span class="sxs-lookup"><span data-stu-id="80978-185">There can be only one root object in a transaction.</span></span> <span data-ttu-id="80978-186">在根物件下，交易式階層中的所有其他物件都稱為 *內建物件*。</span><span class="sxs-lookup"><span data-stu-id="80978-186">All other objects in the transactional hierarchy under the root object are called *interior objects*.</span></span>

## <a name="mapping-transactions"></a><span data-ttu-id="80978-187">對應交易</span><span class="sxs-lookup"><span data-stu-id="80978-187">Mapping Transactions</span></span>

<span data-ttu-id="80978-188">有一種方法可確保物件包含在正確的交易界限內，就是在開始撰寫元件之前，先對應您的交易。</span><span class="sxs-lookup"><span data-stu-id="80978-188">One way to ensure that an object is included in the correct transaction boundary is to map your transactions before you start writing your components.</span></span> <span data-ttu-id="80978-189">您可以藉由對應交易，判斷每個所撰寫元件的最佳設定。</span><span class="sxs-lookup"><span data-stu-id="80978-189">By mapping transactions, you can determine the best setting for each component you write.</span></span> <span data-ttu-id="80978-190">您可以更清楚地瞭解如何使用元件，選取正確的交易屬性值就越容易。</span><span class="sxs-lookup"><span data-stu-id="80978-190">The more certain you are about how your components are to be used, the easier it is to select the correct transaction attribute value.</span></span>

<span data-ttu-id="80978-191">在執行時間，COM + 會查看交易屬性，以判斷物件是否應為新交易的根、在現有交易中建立，或建立為非交易式物件。</span><span class="sxs-lookup"><span data-stu-id="80978-191">At run time, COM+ looks at the transaction attribute to determine whether an object should be the root of a new transaction, be created in an existing transaction, or be created as a non-transactional object.</span></span>

<span data-ttu-id="80978-192">下圖顯示可能的交易對應。</span><span class="sxs-lookup"><span data-stu-id="80978-192">The following illustration shows a possible transaction mapping.</span></span> <span data-ttu-id="80978-193">在圖例中，用戶端會建立需要交易的物件1。</span><span class="sxs-lookup"><span data-stu-id="80978-193">In the illustration, the client creates Object  1, which requires a transaction.</span></span> <span data-ttu-id="80978-194">因為不存在交易，COM + 會建立交易1，並將物件1放在其中做為根物件。</span><span class="sxs-lookup"><span data-stu-id="80978-194">Because no transaction exists, COM+ creates Transaction 1 and places Object 1 in it as the root object.</span></span> <span data-ttu-id="80978-195">物件1會建立支援交易的物件2，因此會放置在交易1中。</span><span class="sxs-lookup"><span data-stu-id="80978-195">Object 1 creates Object 2, which supports transactions and is therefore placed in Transaction 1.</span></span> <span data-ttu-id="80978-196">物件2會建立不支援交易的物件3，因此會放置在所有交易之外。</span><span class="sxs-lookup"><span data-stu-id="80978-196">Object 2 creates Object 3, which does not support transactions and therefore is placed outside all transactions.</span></span> <span data-ttu-id="80978-197">物件2也會建立需要交易的物件4，因此會放置在交易1中。</span><span class="sxs-lookup"><span data-stu-id="80978-197">Object 2 also creates Object 4, which requires a transaction and is therefore placed in Transaction  1.</span></span> <span data-ttu-id="80978-198">物件3會建立可支援交易的物件5。</span><span class="sxs-lookup"><span data-stu-id="80978-198">Object 3 creates Object 5, which supports transactions.</span></span> <span data-ttu-id="80978-199">不過，由於物件5是由交易內不存在的物件所建立，因此它也會置於所有交易之外。</span><span class="sxs-lookup"><span data-stu-id="80978-199">However, because Object 5 is created by an object that does not exist within a transaction, it also is placed outside all transactions.</span></span> <span data-ttu-id="80978-200">物件4會建立需要新交易的物件6，因此 COM + 會建立交易2，並將物件6放在其中做為根物件。</span><span class="sxs-lookup"><span data-stu-id="80978-200">Object 4 creates Object 6, which requires a new transaction, so COM+ creates Transaction 2 and places Object 6 in it as the root object.</span></span> <span data-ttu-id="80978-201">物件6會建立支援交易的物件7，因此會放置在交易2中。</span><span class="sxs-lookup"><span data-stu-id="80978-201">Object 6 creates Object 7, which supports transactions and is therefore placed in Transaction 2.</span></span>

![顯示與交易1和交易2的用戶端互動的圖表。](images/fc7e2d03-94c2-40d9-a79b-1e05ca31dd80.png)

<span data-ttu-id="80978-203">上圖顯示兩個潛在的問題區域。</span><span class="sxs-lookup"><span data-stu-id="80978-203">The preceding illustration shows two potential problem areas.</span></span> <span data-ttu-id="80978-204">首先，大部分的工作都是在兩個不同的交易之間分割。</span><span class="sxs-lookup"><span data-stu-id="80978-204">First, the majority of work is split between two distinct transactions.</span></span> <span data-ttu-id="80978-205">如果在物件4建立物件6之後，交易1失敗，則交易2的執行不會受到交易1的結果影響。</span><span class="sxs-lookup"><span data-stu-id="80978-205">If Transaction 1 fails after Object 4 creates Object 6, Transaction 2 runs unaffected by the outcome of Transaction 1.</span></span> <span data-ttu-id="80978-206">如果這不是預期的結果，您可能會想要將這兩筆交易的作業折迭成單一交易，您可以將物件6的交易屬性變更為 Required 來完成這項交易。</span><span class="sxs-lookup"><span data-stu-id="80978-206">If this outcome is unintended, you might prefer to fold the operations of both transactions into a single transaction, which you can accomplish by changing the transaction attribute of Object  6 to Required.</span></span>

<span data-ttu-id="80978-207">對應圖也會顯示物件3和物件5為非交易式，並在交易1和2的範圍內完全執行。</span><span class="sxs-lookup"><span data-stu-id="80978-207">The mapping illustration also shows that Object 3 and Object 5 are non-transactional, running completely outside the scope of Transactions 1 and 2.</span></span> <span data-ttu-id="80978-208">如果物件5更新持續性資料，您可能會想要重新考慮其非交易狀態。</span><span class="sxs-lookup"><span data-stu-id="80978-208">If Object 5 updates persistent data, you might want to reconsider its non-transactional status.</span></span> <span data-ttu-id="80978-209">您可以藉由將物件5的交易屬性變更為 [必要]，將物件5置於交易內。</span><span class="sxs-lookup"><span data-stu-id="80978-209">Object 5 can be placed within a transaction by changing its transaction attribute to Required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80978-210">相關主題</span><span class="sxs-lookup"><span data-stu-id="80978-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80978-211">設定交易屬性</span><span class="sxs-lookup"><span data-stu-id="80978-211">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)
</dt> </dl>

 

 




