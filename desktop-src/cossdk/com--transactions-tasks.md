---
description: COM + 交易工作
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: COM + 交易工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111037"
---
# <a name="com-transactions-tasks"></a><span data-ttu-id="f5f36-103">COM + 交易工作</span><span class="sxs-lookup"><span data-stu-id="f5f36-103">COM+ Transactions Tasks</span></span>

<span data-ttu-id="f5f36-104">雖然 COM + 中的自動交易處理可讓您在建立及設定想要參與自動交易的物件時，花更高生產力的開發時間，但您可以執行一些程式設計工作，以針對您的應用程式需求量身打造交易行為。</span><span class="sxs-lookup"><span data-stu-id="f5f36-104">While automatic transaction processing in COM+ allows you to spend more productive development time in creating and configuring objects that you want to participate in automatic transactions, there are some programming tasks you can perform to tailor transaction behavior to your application requirements.</span></span>

<span data-ttu-id="f5f36-105">下列主題討論與交易處理相關的特定程式設計選項。</span><span class="sxs-lookup"><span data-stu-id="f5f36-105">The following topics discuss specific programming options related to transaction processing.</span></span>



| <span data-ttu-id="f5f36-106">主題</span><span class="sxs-lookup"><span data-stu-id="f5f36-106">Topic</span></span>                                                                                             | <span data-ttu-id="f5f36-107">描述</span><span class="sxs-lookup"><span data-stu-id="f5f36-107">Description</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5f36-108">設定交易屬性</span><span class="sxs-lookup"><span data-stu-id="f5f36-108">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)<br/>             | <span data-ttu-id="f5f36-109">描述如何設定交易對象的交易屬性值。</span><span class="sxs-lookup"><span data-stu-id="f5f36-109">Describes how to set transaction attribute values for your transaction objects.</span></span><br/>         |
| [<span data-ttu-id="f5f36-110">設定交易隔離等級</span><span class="sxs-lookup"><span data-stu-id="f5f36-110">Setting the Transaction Isolation Level</span></span>](setting-the-transaction-isolation-level.md)<br/> | <span data-ttu-id="f5f36-111">描述如何設定交易對象的交易隔離等級。</span><span class="sxs-lookup"><span data-stu-id="f5f36-111">Describes how to set the transaction isolation levels for your transaction objects.</span></span><br/>     |
| [<span data-ttu-id="f5f36-112">設定交易超時</span><span class="sxs-lookup"><span data-stu-id="f5f36-112">Setting the Transaction Time-Out</span></span>](setting-the-transaction-time-out.md)<br/>               | <span data-ttu-id="f5f36-113">說明如何設定交易的逾時間隔。</span><span class="sxs-lookup"><span data-stu-id="f5f36-113">Describes how to set time-out intervals for your transactions.</span></span><br/>                          |
| [<span data-ttu-id="f5f36-114">設定一致且完成的旗標</span><span class="sxs-lookup"><span data-stu-id="f5f36-114">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)<br/>     | <span data-ttu-id="f5f36-115">顯示如何使用「一致」和「完成」旗標來控制交易的結果。</span><span class="sxs-lookup"><span data-stu-id="f5f36-115">Shows how to use the consistent and done flags to control the outcome of a transaction.</span></span><br/> |
| [<span data-ttu-id="f5f36-116">建立 BYOT 物件</span><span class="sxs-lookup"><span data-stu-id="f5f36-116">Creating BYOT Objects</span></span>](creating-byot-objects.md)<br/>                                     | <span data-ttu-id="f5f36-117">描述如何建立物件，讓您可以將自己的交易 (BYOT) 。</span><span class="sxs-lookup"><span data-stu-id="f5f36-117">Describes how to create objects so you can Bring Your Own Transaction (BYOT).</span></span><br/>           |



 

> [!Note]  
> <span data-ttu-id="f5f36-118">一般來說，任何更新持續狀態的元件都應該支援交易。</span><span class="sxs-lookup"><span data-stu-id="f5f36-118">As a general rule, any component that updates persistent state should support transactions.</span></span> <span data-ttu-id="f5f36-119">將兩個或多個物件的作業結合成單一工作的元件，應該使用交易來簡化錯誤復原。</span><span class="sxs-lookup"><span data-stu-id="f5f36-119">Components that combine the operations of two or more objects into a single task should use transactions to simplify error recovery.</span></span> <span data-ttu-id="f5f36-120">此外，若要釋放資源（例如資料庫連接），COM + 中的交易應該盡可能簡短。</span><span class="sxs-lookup"><span data-stu-id="f5f36-120">Also, to release resources, such as database connections, transactions in COM+ should be as short as you can make them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f5f36-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5f36-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5f36-122">COM + 交易概念</span><span class="sxs-lookup"><span data-stu-id="f5f36-122">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)
</dt> </dl>

 

 




