---
description: 因為自訂動作可在 UI 和執行順序資料表中排程，而且可以在服務或用戶端進程中執行，所以自訂動作可能會執行多次。
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: 自訂動作執行排程選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986981"
---
# <a name="custom-action-execution-scheduling-options"></a><span data-ttu-id="48554-103">自訂動作執行排程選項</span><span class="sxs-lookup"><span data-stu-id="48554-103">Custom Action Execution Scheduling Options</span></span>

<span data-ttu-id="48554-104">因為自訂動作可在 UI 和執行順序資料表中排程，而且可以在服務或用戶端進程中執行，所以自訂動作可能會執行多次。</span><span class="sxs-lookup"><span data-stu-id="48554-104">Because a custom action can be scheduled in both the UI and execute sequence tables, and can be executed either in the service or client process, a custom action can potentially execute multiple times.</span></span>

<span data-ttu-id="48554-105">請注意，安裝程式：</span><span class="sxs-lookup"><span data-stu-id="48554-105">Note that the installer:</span></span>

-   <span data-ttu-id="48554-106">預設會立即在順序資料表中執行動作。</span><span class="sxs-lookup"><span data-stu-id="48554-106">Executes actions in a sequence table immediately by default.</span></span>
-   <span data-ttu-id="48554-107">如果 sequence 資料表的條件運算式欄位評估為 False，則不會執行動作。</span><span class="sxs-lookup"><span data-stu-id="48554-107">Does not execute an action if the conditional expression field of the sequence table evaluates to False.</span></span>
-   <span data-ttu-id="48554-108">如果內部使用者的介面層級設定為完整的 UI 模式，則處理用戶端進程中的 UI 順序資料表 (如需) 的 UI 層級描述，請參閱 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) 。</span><span class="sxs-lookup"><span data-stu-id="48554-108">Processes the UI sequence table in the client process if the internal user's interface level is set to the full UI mode (see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) for a description of UI levels).</span></span>
-   <span data-ttu-id="48554-109">是使用 Windows 2000 時預設註冊的服務，在此情況下，會在安裝程式服務中處理執行順序資料表。</span><span class="sxs-lookup"><span data-stu-id="48554-109">Is a service registered by default when using Windows 2000 and, in this case, the execute sequence table is processed in the installer service.</span></span>

<span data-ttu-id="48554-110">您可以使用下列選項旗標來控制多個立即執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="48554-110">You can use the following option flags to control multiple immediate execution of custom actions.</span></span> <span data-ttu-id="48554-111">若要設定選項，請將此資料表中的值加入至 [CustomAction 資料表](customaction-table.md)之 [類型] 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="48554-111">To set an option, add the value in this table to the value in the Type field of the [CustomAction table](customaction-table.md).</span></span> <span data-ttu-id="48554-112">下列旗標都不應搭配延後 [執行自訂動作](deferred-execution-custom-actions.md)使用。</span><span class="sxs-lookup"><span data-stu-id="48554-112">None of the following flags should be used with [deferred execution custom actions](deferred-execution-custom-actions.md).</span></span>

<dl> <dt>

<span data-ttu-id="48554-113"><span id="_default_"></span><span id="_DEFAULT_"></span> (預設) </span><span class="sxs-lookup"><span data-stu-id="48554-113"><span id="_default_"></span><span id="_DEFAULT_"></span>(default)</span></span>
</dt> <dd>

<span data-ttu-id="48554-114">十六進位：0x00000000</span><span class="sxs-lookup"><span data-stu-id="48554-114">Hexadecimal: 0x00000000</span></span>

<span data-ttu-id="48554-115">Decimal：0</span><span class="sxs-lookup"><span data-stu-id="48554-115">Decimal: 0</span></span>

<span data-ttu-id="48554-116">一律執行。</span><span class="sxs-lookup"><span data-stu-id="48554-116">Always execute.</span></span> <span data-ttu-id="48554-117">如果兩個順序資料表中都有動作，動作可能會執行兩次。</span><span class="sxs-lookup"><span data-stu-id="48554-117">Action may run twice if present in both sequence tables.</span></span>

</dd> <dt>

<span data-ttu-id="48554-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span><span class="sxs-lookup"><span data-stu-id="48554-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span></span> 
</dt> <dd>

<span data-ttu-id="48554-119">十六進位：0x00000100</span><span class="sxs-lookup"><span data-stu-id="48554-119">Hexadecimal: 0x00000100</span></span>

<span data-ttu-id="48554-120">Decimal：256</span><span class="sxs-lookup"><span data-stu-id="48554-120">Decimal: 256</span></span>

<span data-ttu-id="48554-121">如果同時存在於兩個順序資料表中，則不會執行一次以上。</span><span class="sxs-lookup"><span data-stu-id="48554-121">Execute no more than once if present in both sequence tables.</span></span> <span data-ttu-id="48554-122">如果 UI 順序已執行，一律會略過執行順序中的動作。</span><span class="sxs-lookup"><span data-stu-id="48554-122">Always skips action in execute sequence if UI sequence has run.</span></span> <span data-ttu-id="48554-123">UI 順序中沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="48554-123">No effect in UI sequence.</span></span> <span data-ttu-id="48554-124">動作不一定要存在，也不能在 UI 順序中執行，以在執行順序中略過。</span><span class="sxs-lookup"><span data-stu-id="48554-124">The action is not required to be present or run in the UI sequence to be skipped in the execute sequence.</span></span> <span data-ttu-id="48554-125">不受安裝服務註冊的影響。</span><span class="sxs-lookup"><span data-stu-id="48554-125">Not affected by install service registration.</span></span>

</dd> <dt>

<span data-ttu-id="48554-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span><span class="sxs-lookup"><span data-stu-id="48554-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span></span>
</dt> <dd>

<span data-ttu-id="48554-127">十六進位：0x00000200</span><span class="sxs-lookup"><span data-stu-id="48554-127">Hexadecimal: 0x00000200</span></span>

<span data-ttu-id="48554-128">Decimal：512</span><span class="sxs-lookup"><span data-stu-id="48554-128">Decimal: 512</span></span>

<span data-ttu-id="48554-129">如果在這兩個順序資料表中，每個進程執行一次。</span><span class="sxs-lookup"><span data-stu-id="48554-129">Execute once per process if in both sequence tables.</span></span> <span data-ttu-id="48554-130">如果 UI 序列已在相同的進程中執行，例如在用戶端進程中執行，則會略過執行序列中的動作。</span><span class="sxs-lookup"><span data-stu-id="48554-130">Skips action in execute sequence if UI sequence has been run in same process, for example both run in the client process.</span></span> <span data-ttu-id="48554-131">用來防止修改會話狀態的動作，例如屬性和資料庫資料，而不是執行兩次。</span><span class="sxs-lookup"><span data-stu-id="48554-131">Used to prevent actions that modify the session state, such as property and database data, from running twice.</span></span>

</dd> <dt>

<span data-ttu-id="48554-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span><span class="sxs-lookup"><span data-stu-id="48554-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span></span>
</dt> <dd>

<span data-ttu-id="48554-133">十六進位：0x00000300</span><span class="sxs-lookup"><span data-stu-id="48554-133">Hexadecimal: 0x00000300</span></span>

<span data-ttu-id="48554-134">Decimal：768</span><span class="sxs-lookup"><span data-stu-id="48554-134">Decimal: 768</span></span>

<span data-ttu-id="48554-135">只有在 UI 循序執行後於用戶端上執行時才執行。</span><span class="sxs-lookup"><span data-stu-id="48554-135">Execute only if running on client after UI sequence has run.</span></span> <span data-ttu-id="48554-136">只有當執行順序是在用戶端上執行的執行順序之後，才會執行動作。</span><span class="sxs-lookup"><span data-stu-id="48554-136">The action runs only if the execute sequence is run on the client following UI sequence.</span></span> <span data-ttu-id="48554-137">可以用來提供或邏輯，或隱藏 UI 相關的處理（如果用戶端會話已完成）。</span><span class="sxs-lookup"><span data-stu-id="48554-137">May be used to provide either/or logic, or to suppress the UI-related processing if already done for the client session.</span></span>

</dd> </dl>

<span data-ttu-id="48554-138">請注意，若要在兩個不同的執行模式中執行自訂動作，請在 [CustomAction 資料表](customaction-table.md) 中撰寫兩個專案。</span><span class="sxs-lookup"><span data-stu-id="48554-138">Note that to run a custom action during two different run modes, author two entries into the [CustomAction table](customaction-table.md) .</span></span> <span data-ttu-id="48554-139">例如，若要讓自訂動作呼叫 C/c + + 動態連結程式庫 (DLL)  ( [自訂動作類型 1](custom-action-type-1.md)) 當模式 MSIRUNMODE \_ 排程和 MSIRUNMODE 回復時 \_ ，請將兩個專案放在呼叫相同 DLL 但具有不同數數值型別的 CustomAction 資料表中。</span><span class="sxs-lookup"><span data-stu-id="48554-139">For example, to have a custom action that calls a C/C++ dynamic link library (DLL) ( [Custom Action Type 1](custom-action-type-1.md)) both when the mode is MSIRUNMODE\_SCHEDULED and MSIRUNMODE\_ROLLBACK, put two entries in the CustomAction table that call the same DLL but that have different numeric types.</span></span> <span data-ttu-id="48554-140">包含呼叫 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 的程式碼，以判斷何時要執行哪個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="48554-140">Include code that calls [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) to determine when to run which custom action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48554-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="48554-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48554-142">自訂動作參考</span><span class="sxs-lookup"><span data-stu-id="48554-142">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="48554-143">關於自訂動作</span><span class="sxs-lookup"><span data-stu-id="48554-143">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="48554-144">使用自訂動作</span><span class="sxs-lookup"><span data-stu-id="48554-144">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



