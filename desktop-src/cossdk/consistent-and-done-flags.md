---
description: 一致且完成的旗標
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: 一致且完成的旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510754"
---
# <a name="consistent-and-done-flags"></a><span data-ttu-id="0a21c-103">一致且完成的旗標</span><span class="sxs-lookup"><span data-stu-id="0a21c-103">Consistent and Done Flags</span></span>

<span data-ttu-id="0a21c-104">在啟動交易對象之前，COM + 一律會建立內容物件。</span><span class="sxs-lookup"><span data-stu-id="0a21c-104">COM+ always creates a context object before activating a transactional object.</span></span> <span data-ttu-id="0a21c-105">內容物件會保存物件相關資訊，例如其建立者及其交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a21c-105">The context object holds object-related information, such as its creator and its transaction identifier.</span></span> <span data-ttu-id="0a21c-106">每個內容物件也包含 *一致的旗* 標和 *完成的旗* 標。</span><span class="sxs-lookup"><span data-stu-id="0a21c-106">Each context object also contains a *consistent flag* and a *done flag*.</span></span> <span data-ttu-id="0a21c-107">這些旗標一起決定交易對象的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a21c-107">Together these flags determine the status of the transactional object.</span></span>

<span data-ttu-id="0a21c-108">一致性旗標表示交易對象為一致或不一致。</span><span class="sxs-lookup"><span data-stu-id="0a21c-108">The consistent flag indicates that the transactional object is either consistent or inconsistent.</span></span> <span data-ttu-id="0a21c-109">讓物件的狀態保持一致的特定詳細資料，取決於程式設計人員。</span><span class="sxs-lookup"><span data-stu-id="0a21c-109">The specific details of what makes an object's state consistent is up to the programmer.</span></span> <span data-ttu-id="0a21c-110">當方法呼叫將此旗標設為 True 時，表示物件是一致的。</span><span class="sxs-lookup"><span data-stu-id="0a21c-110">When a method call sets this flag to True, the object is consistent.</span></span> <span data-ttu-id="0a21c-111">False 表示物件不一致。</span><span class="sxs-lookup"><span data-stu-id="0a21c-111">False indicates that the object is inconsistent.</span></span> <span data-ttu-id="0a21c-112">COM + 會在建立物件實例時將旗標設定為 True。</span><span class="sxs-lookup"><span data-stu-id="0a21c-112">COM+ sets the flag to True when it creates an object instance.</span></span> <span data-ttu-id="0a21c-113">一致的物件已準備好繼續進行交易。</span><span class="sxs-lookup"><span data-stu-id="0a21c-113">A consistent object is ready to proceed with the transaction.</span></span> <span data-ttu-id="0a21c-114">當物件維持使用中狀態時，後續的方法呼叫可以重複地將一致旗標從 True 切換為 False，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="0a21c-114">While an object remains active, subsequent method calls can repeatedly switch the consistent flag from True to False and vice versa.</span></span>

<span data-ttu-id="0a21c-115">完成旗標會決定交易的持續時間。</span><span class="sxs-lookup"><span data-stu-id="0a21c-115">The done flag determines the duration of a transaction.</span></span> <span data-ttu-id="0a21c-116">當方法呼叫傳回時，COM + 會檢查完成的旗標。</span><span class="sxs-lookup"><span data-stu-id="0a21c-116">When a method call returns, COM+ inspects the done flag.</span></span> <span data-ttu-id="0a21c-117">如果方法將此旗標設定為 True，COM + 就會停用該物件，並記下一致的旗標。</span><span class="sxs-lookup"><span data-stu-id="0a21c-117">If the method sets this flag to True, COM+ deactivates the object and notes the consistent flag.</span></span> <span data-ttu-id="0a21c-118">當 done 旗標為 False 時，COM + 都不會停用物件，也不會記下一致的旗標。</span><span class="sxs-lookup"><span data-stu-id="0a21c-118">When the done flag is False, COM+ neither deactivates the object nor notes the consistent flag.</span></span> <span data-ttu-id="0a21c-119">當 COM + 建立物件實例時，會將完成的旗標設定為 False。</span><span class="sxs-lookup"><span data-stu-id="0a21c-119">COM+ sets the done flag to False when it creates an object instance.</span></span>

<span data-ttu-id="0a21c-120">「一致」旗標會將投票轉換成認可或中止執行的交易，而「完成」旗標會完成投票。</span><span class="sxs-lookup"><span data-stu-id="0a21c-120">The consistent flag casts a vote to commit or abort the transaction in which it executes, and the done flag finalizes the vote.</span></span> <span data-ttu-id="0a21c-121">當方法呼叫傳回上的 [完成] 旗標設為 True 或物件停用時，COM + 會檢查一致的旗標。</span><span class="sxs-lookup"><span data-stu-id="0a21c-121">COM+ inspects the consistent flag when the done flag is set to True on a method call return or when the object deactivates.</span></span> <span data-ttu-id="0a21c-122">雖然物件的一致旗標可能會在每個方法呼叫中重複變更，但只有最後一個變更計數。</span><span class="sxs-lookup"><span data-stu-id="0a21c-122">Although an object's consistent flag can change repeatedly within each method call, only the last change counts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a21c-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a21c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a21c-124">管理 COM + 中的自動交易</span><span class="sxs-lookup"><span data-stu-id="0a21c-124">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[<span data-ttu-id="0a21c-125">設定一致且完成的旗標</span><span class="sxs-lookup"><span data-stu-id="0a21c-125">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



