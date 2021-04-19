---
description: 如果您在 ICE 參考中所列的現有 ICE 自訂動作之間找不到您需要的內部一致性評估工具，您將需要準備自己的 ICE 來驗證您的套件。
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: 打造冰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981536"
---
# <a name="building-an-ice"></a><span data-ttu-id="44056-103">打造冰</span><span class="sxs-lookup"><span data-stu-id="44056-103">Building An ICE</span></span>

<span data-ttu-id="44056-104">如果您在[Ice 參考](ice-reference.md)中所列的現有 ICE 自訂動作之間找不到您需要的[內部一致性評估](internal-consistency-evaluators-ices.md)工具，您將需要準備自己的 ice 來驗證您的套件。</span><span class="sxs-lookup"><span data-stu-id="44056-104">If you are unable to find the [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) you need among the existing ICE custom actions listed in the [ICE Reference](ice-reference.md), you will need to prepare your own ICE to validate your package.</span></span>

<span data-ttu-id="44056-105">撰寫 ICE 自訂動作時，您應該執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="44056-105">When authoring ICE custom actions you should do the following:</span></span>

-   <span data-ttu-id="44056-106">只以顯示的表格中所列的自訂動作為依據。</span><span class="sxs-lookup"><span data-stu-id="44056-106">Base the ICEs only on custom actions of types listed in the table shown.</span></span>
-   <span data-ttu-id="44056-107">呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 並張貼 INSTALLMESSAGE \_ 使用者類型的訊息。</span><span class="sxs-lookup"><span data-stu-id="44056-107">Call [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and post an INSTALLMESSAGE\_USER type of message.</span></span> <span data-ttu-id="44056-108">撰寫 ICE 訊息時，請遵循 [ICE 訊息指導方針](ice-message-guidelines.md)中的訊息格式。</span><span class="sxs-lookup"><span data-stu-id="44056-108">When authoring your ICE messages follow the message format in the [ICE Message Guidelines](ice-message-guidelines.md).</span></span>
-   <span data-ttu-id="44056-109">撰寫您的 ICE，讓它能捕捉任何 API 錯誤，而且一律會傳回錯誤 \_ 成功。</span><span class="sxs-lookup"><span data-stu-id="44056-109">Write your ICE such that it captures any API errors and always returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="44056-110">這是必要的，以允許後續自訂動作在 ICE 失敗後執行。</span><span class="sxs-lookup"><span data-stu-id="44056-110">This is necessary to allow subsequent custom actions to run following the failure of an ICE.</span></span>

<span data-ttu-id="44056-111">ICE 自訂動作僅限於下列自訂動作類型。</span><span class="sxs-lookup"><span data-stu-id="44056-111">ICE custom actions are limited to the following custom action types.</span></span>



| <span data-ttu-id="44056-112">自訂動作類型</span><span class="sxs-lookup"><span data-stu-id="44056-112">Custom action type</span></span>                                 | <span data-ttu-id="44056-113">Description</span><span class="sxs-lookup"><span data-stu-id="44056-113">Description</span></span>               |
|----------------------------------------------------|---------------------------|
| [<span data-ttu-id="44056-114">自訂動作類型1</span><span class="sxs-lookup"><span data-stu-id="44056-114">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="44056-115">二進位資料流程中的 DLL</span><span class="sxs-lookup"><span data-stu-id="44056-115">DLL in binary stream</span></span>      |
| [<span data-ttu-id="44056-116">自訂動作類型2</span><span class="sxs-lookup"><span data-stu-id="44056-116">Custom Action Type 2</span></span>](custom-action-type-2.md)   | <span data-ttu-id="44056-117">二進位資料流程中的 EXE</span><span class="sxs-lookup"><span data-stu-id="44056-117">EXE in binary stream</span></span>      |
| [<span data-ttu-id="44056-118">自訂動作類型5</span><span class="sxs-lookup"><span data-stu-id="44056-118">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="44056-119">二進位資料流程中的 JScript</span><span class="sxs-lookup"><span data-stu-id="44056-119">JScript in binary stream</span></span>  |
| [<span data-ttu-id="44056-120">自訂動作類型6</span><span class="sxs-lookup"><span data-stu-id="44056-120">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="44056-121">二進位資料流程中的 VBScript</span><span class="sxs-lookup"><span data-stu-id="44056-121">VBScript in binary stream</span></span> |
| [<span data-ttu-id="44056-122">自訂動作類型37</span><span class="sxs-lookup"><span data-stu-id="44056-122">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="44056-123">字串形式的 JScript 程式碼</span><span class="sxs-lookup"><span data-stu-id="44056-123">JScript code as string</span></span>    |
| [<span data-ttu-id="44056-124">自訂動作類型38</span><span class="sxs-lookup"><span data-stu-id="44056-124">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="44056-125">VBScript 程式碼字串</span><span class="sxs-lookup"><span data-stu-id="44056-125">VBScript code as string</span></span>   |



 

<span data-ttu-id="44056-126">撰寫 ICE 自訂動作時，請勿執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="44056-126">When authoring an ICE custom action, do not do the following:</span></span>

-   <span data-ttu-id="44056-127">請勿假設 ICE 所接收引擎的控制碼是安裝程式資料庫的安裝實例。</span><span class="sxs-lookup"><span data-stu-id="44056-127">Do not assume that the handle to the engine that the ICE receives is an installation instance of the installer database.</span></span> <span data-ttu-id="44056-128">如果不是安裝實例，就不會定義某些屬性、不會解析來源和目標目錄，也不會定義目前的功能狀態。</span><span class="sxs-lookup"><span data-stu-id="44056-128">If it is not a installation instance, certain properties are not defined, the source and target directories are not resolved, and current feature states are not defined.</span></span>
-   <span data-ttu-id="44056-129">請勿依賴任何安裝程式動作、自訂動作或其他 ICE 的先前執行或非執行。</span><span class="sxs-lookup"><span data-stu-id="44056-129">Do not rely on the prior execution, or non-execution, of any installer action, custom action, or another ICE.</span></span> <span data-ttu-id="44056-130">因為先前的 ICE 可能已在任何資料表中建立暫存資料行，所以作者應該盡可能依名稱參考資料行。</span><span class="sxs-lookup"><span data-stu-id="44056-130">Because a prior ICE may have created temporary columns in any table, authors should reference columns by name whenever possible.</span></span> <span data-ttu-id="44056-131">在結束之前，請先清除任何暫時的資料行或資料表。</span><span class="sxs-lookup"><span data-stu-id="44056-131">ICEs should cleanup any temporary columns or tables before they exit.</span></span>
-   <span data-ttu-id="44056-132">請勿假設作者可以存取資料庫來原始目錄的影像。</span><span class="sxs-lookup"><span data-stu-id="44056-132">Do not assume that authors have access to an image of the source directory of the database.</span></span>
-   <span data-ttu-id="44056-133">請勿假設對資料庫所做的變更不會保存。</span><span class="sxs-lookup"><span data-stu-id="44056-133">Do not assume that changes made to the database do not persist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44056-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="44056-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44056-135">C + + 中的範例 ICE</span><span class="sxs-lookup"><span data-stu-id="44056-135">Sample ICE in C++</span></span>](sample-ice-in-c-.md)
</dt> <dt>

[<span data-ttu-id="44056-136">VBScript 中的範例 ICE</span><span class="sxs-lookup"><span data-stu-id="44056-136">Sample ICE in VBScript</span></span>](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



