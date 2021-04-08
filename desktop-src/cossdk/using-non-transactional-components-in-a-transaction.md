---
description: 在交易中使用非交易式元件
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: 在交易中使用非交易式元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75cd8ebc756971a56413e371cf23de2144e5816
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689172"
---
# <a name="using-non-transactional-components-in-a-transaction"></a><span data-ttu-id="c5394-103">在交易中使用非交易式元件</span><span class="sxs-lookup"><span data-stu-id="c5394-103">Using Non-Transactional Components in a Transaction</span></span>

<span data-ttu-id="c5394-104">將非交易式元件放置在交易中，以利用交易的 [ACID 屬性](acid-properties.md) 通常很有用。</span><span class="sxs-lookup"><span data-stu-id="c5394-104">It is often useful to place non-transactional components into a transaction to take advantage of the [ACID properties](acid-properties.md) of transactions.</span></span> <span data-ttu-id="c5394-105">例如，如果您使用非交易式舊版元件來更新網路上的密碼，您可以將這些元件放在交易中，以確保網路上的密碼更新是一致的。</span><span class="sxs-lookup"><span data-stu-id="c5394-105">For example, if you have non-transactional legacy components that you use to update passwords on a network, you can place those components in a transaction to ensure that password updates are consistent across the network.</span></span>

<span data-ttu-id="c5394-106">*交易內容物件* 是泛型物件，可讓非交易式用戶端將多個 COM 物件的工作結合成單一交易，而不需要您特別針對該目的開發新元件。</span><span class="sxs-lookup"><span data-stu-id="c5394-106">The *transaction context object* is a generic object that allows non-transactional clients to combine the work of multiple COM objects into a single transaction, without requiring you to develop a new component specifically for that purpose.</span></span> <span data-ttu-id="c5394-107">相對於自動交易，交易內容物件需要其用戶端明確地認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="c5394-107">In contrast to an automatic transaction, the transaction context object requires its client to explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="c5394-108">依預設，交易內容物件的交易屬性值會設定為 [必要]。</span><span class="sxs-lookup"><span data-stu-id="c5394-108">By default, the transaction attribute value of the transaction context object is set to Required.</span></span> <span data-ttu-id="c5394-109">如果用戶端在沒有明確發出認可或中止呼叫的情況下釋放交易內容物件，COM + 就會中止交易。</span><span class="sxs-lookup"><span data-stu-id="c5394-109">COM+ aborts the transaction if the client releases the transaction context object without explicitly issuing a commit or abort call.</span></span>

<span data-ttu-id="c5394-110">下列 Visual Basic 範例顯示非交易式用戶端如何將一個以上的物件所完成的工作組成單一交易：</span><span class="sxs-lookup"><span data-stu-id="c5394-110">The following Visual Basic example shows how a non-transactional client can compose the work done by more than one object into a single transaction:</span></span>


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a><span data-ttu-id="c5394-111">交易內容物件的限制</span><span class="sxs-lookup"><span data-stu-id="c5394-111">Limitations of the Transaction Context Object</span></span>

<span data-ttu-id="c5394-112">以下是交易內容物件的一些重要限制：</span><span class="sxs-lookup"><span data-stu-id="c5394-112">Following are some important limitations of the transaction context object:</span></span>

-   <span data-ttu-id="c5394-113">使用交易內容物件時，將多個物件的工作結合成單一交易的應用程式邏輯會系結至特定的非交易式用戶端執行，而且會遺失使用 COM 元件的一些優點。</span><span class="sxs-lookup"><span data-stu-id="c5394-113">When using a transaction context object, the application logic that combines the work of multiple objects into a single transaction is tied to a specific non-transactional client implementation and some advantages of using COM components are lost.</span></span> <span data-ttu-id="c5394-114">這些遺失的優點包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="c5394-114">These lost advantages include the following:</span></span>
    -   <span data-ttu-id="c5394-115">在更大的交易中重複使用應用程式邏輯的能力</span><span class="sxs-lookup"><span data-stu-id="c5394-115">Ability to reuse the application logic as part of an even larger transaction</span></span>
    -   <span data-ttu-id="c5394-116">宣告式安全性的拼版</span><span class="sxs-lookup"><span data-stu-id="c5394-116">Imposition of declarative security</span></span>
    -   <span data-ttu-id="c5394-117">從用戶端遠端執行邏輯的彈性</span><span class="sxs-lookup"><span data-stu-id="c5394-117">Flexibility to run the logic remotely from the client</span></span>
-   <span data-ttu-id="c5394-118">交易內容物件會與非交易式用戶端一起執行，這表示 COM + 必須可在非交易式用戶端電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="c5394-118">The transaction context object runs in-process with the non-transactional client, which means that COM+ must be available on the non-transactional client computer.</span></span> <span data-ttu-id="c5394-119">這可能不是問題，例如，從使用中的伺服器頁（在與 COM + 相同伺服器上執行的 (ASP) 頁面）使用交易內容物件時。</span><span class="sxs-lookup"><span data-stu-id="c5394-119">This might not be a problem, for example, when the transaction context object is used from an Active Server Pages (ASP) page that is running on the same server as COM+.</span></span>
-   <span data-ttu-id="c5394-120">當您建立交易內容物件時，不會取得非交易式用戶端的內容。</span><span class="sxs-lookup"><span data-stu-id="c5394-120">You do not get a context for the non-transactional client when you create a transaction context object.</span></span> <span data-ttu-id="c5394-121">交易式工作只能透過使用交易內容物件所建立的 COM 物件來間接完成。</span><span class="sxs-lookup"><span data-stu-id="c5394-121">Transactional work can only be done indirectly, through COM objects created by using the transaction context object.</span></span> <span data-ttu-id="c5394-122">尤其是，非交易式用戶端無法使用 COM + 資源機 (例如 ODBC) ，並將工作包含在交易中。</span><span class="sxs-lookup"><span data-stu-id="c5394-122">In particular, the non-transactional client cannot use COM+ resource dispensers (such as ODBC) and have the work included in the transaction.</span></span> <span data-ttu-id="c5394-123">例如，開發人員可能會熟悉下列在關係資料庫系統上執行交易式工作的語法：</span><span class="sxs-lookup"><span data-stu-id="c5394-123">For example, developers may be familiar with the following syntax for doing transactional work on relational database systems:</span></span>

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    <span data-ttu-id="c5394-124">以類似的方式使用交易內容物件不會產生所需的結果：</span><span class="sxs-lookup"><span data-stu-id="c5394-124">Using the transaction context object in a similar way does not yield the desired result:</span></span>

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    <span data-ttu-id="c5394-125">在此範例中，呼叫 DoWork 不會在交易中登記。</span><span class="sxs-lookup"><span data-stu-id="c5394-125">The call to DoWork in this example is not enlisted in a transaction.</span></span> <span data-ttu-id="c5394-126">相反地，您必須建立會呼叫 DoWork 的 COM 元件、使用交易內容物件來建立該元件的物件實例，然後從非交易式用戶端呼叫該物件，讓工作成為用戶端控制交易的一部分。</span><span class="sxs-lookup"><span data-stu-id="c5394-126">Instead, you must build a COM component that calls DoWork, create an object instance of that component using the transaction context object, and then call that object from the non-transactional client for the work to be part of the client-controlled transaction.</span></span>

 

 



