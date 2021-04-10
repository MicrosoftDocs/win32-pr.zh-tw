---
description: COM + 交易概念
ms.assetid: e2198514-c403-4b31-8c8c-0b1c83c4f936
title: COM + 交易概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775537128aa0419d02ad3ab614a3ba2ec5eb5b2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111040"
---
# <a name="com-transactions-concepts"></a><span data-ttu-id="e34b2-103">COM + 交易概念</span><span class="sxs-lookup"><span data-stu-id="e34b2-103">COM+ Transactions Concepts</span></span>

<span data-ttu-id="e34b2-104">雖然 COM + 會處理許多與交易處理相關的繁瑣程式設計細節，但是當您需要在 COM + 中撰寫交易時，對交易理論具有概念瞭解相當實用。</span><span class="sxs-lookup"><span data-stu-id="e34b2-104">Although COM+ handles many of the tedious programming details associated with transaction processing, it is useful to have a conceptual understanding of transaction theory when you need to program transactions in COM+.</span></span>

<span data-ttu-id="e34b2-105">下表所述的主題將涵蓋適用于交易處理的概念。</span><span class="sxs-lookup"><span data-stu-id="e34b2-105">The topics described in the following table cover the concepts that apply to transaction processing.</span></span>



| <span data-ttu-id="e34b2-106">主題</span><span class="sxs-lookup"><span data-stu-id="e34b2-106">Topic</span></span>                                                                                                                     | <span data-ttu-id="e34b2-107">描述</span><span class="sxs-lookup"><span data-stu-id="e34b2-107">Description</span></span>                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e34b2-108">ACID 屬性</span><span class="sxs-lookup"><span data-stu-id="e34b2-108">ACID Properties</span></span>](acid-properties.md)<br/>                                                                         | <span data-ttu-id="e34b2-109">描述交易的不可部分完成、一致、隔離及持久屬性。</span><span class="sxs-lookup"><span data-stu-id="e34b2-109">Describes the atomic, consistent, isolated, and durable properties of transactions.</span></span><br/>                                                                                              |
| [<span data-ttu-id="e34b2-110">設定交易</span><span class="sxs-lookup"><span data-stu-id="e34b2-110">Configuring Transactions</span></span>](configuring-transactions.md)<br/>                                                       | <span data-ttu-id="e34b2-111">描述您可以指派給元件的交易屬性值，以判斷要強制執行的交易保護程度。</span><span class="sxs-lookup"><span data-stu-id="e34b2-111">Describes the transaction attribute values that you can assign to your components to determine the degree of transaction protection to be enforced.</span></span><br/>                              |
| [<span data-ttu-id="e34b2-112">設定交易隔離等級</span><span class="sxs-lookup"><span data-stu-id="e34b2-112">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)<br/>                       | <span data-ttu-id="e34b2-113">描述您可以指派給交易的隔離等級，可讓您根據效能和擴充性需求來增加或減少並行。</span><span class="sxs-lookup"><span data-stu-id="e34b2-113">Describes the isolation levels you can assign to your transactions, enabling you to increase or decrease concurrency depending on your performance and scalability requirements.</span></span><br/> |
| [<span data-ttu-id="e34b2-114">管理 COM + 中的自動交易</span><span class="sxs-lookup"><span data-stu-id="e34b2-114">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)<br/>                         | <span data-ttu-id="e34b2-115">COM + 支援的自動化交易程式總覽。</span><span class="sxs-lookup"><span data-stu-id="e34b2-115">Overview of the automated transaction process supported by COM+.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="e34b2-116">在交易中使用非交易式元件</span><span class="sxs-lookup"><span data-stu-id="e34b2-116">Using Non-Transactional Components in a Transaction</span></span>](using-non-transactional-components-in-a-transaction.md)<br/> | <span data-ttu-id="e34b2-117">描述如何在交易中使用非交易式元件，以及使用它們的時機。</span><span class="sxs-lookup"><span data-stu-id="e34b2-117">Describes how to use non-transactional components in a transaction and when you would use them.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e34b2-118">整合您自己的交易 (BYOT) </span><span class="sxs-lookup"><span data-stu-id="e34b2-118">Bring Your Own Transaction (BYOT)</span></span>](bring-your-own-transaction--byot-.md)<br/>                                     | <span data-ttu-id="e34b2-119">描述如何允許元件繼承外部交易。</span><span class="sxs-lookup"><span data-stu-id="e34b2-119">Describes how to allow a component inherit an external transaction.</span></span><br/>                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="e34b2-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="e34b2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e34b2-121">COM + 交易工作</span><span class="sxs-lookup"><span data-stu-id="e34b2-121">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)
</dt> </dl>

 

 




