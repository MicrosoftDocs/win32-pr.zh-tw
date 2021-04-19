---
description: RemoveEnvironmentStrings 動作會修改環境變數的值。
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: RemoveEnvironmentStrings 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c958f2095d2b8562bbd7518ef691634186a9128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988502"
---
# <a name="removeenvironmentstrings-action"></a><span data-ttu-id="37488-103">RemoveEnvironmentStrings 動作</span><span class="sxs-lookup"><span data-stu-id="37488-103">RemoveEnvironmentStrings Action</span></span>

<span data-ttu-id="37488-104">RemoveEnvironmentStrings 動作會修改環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="37488-104">The RemoveEnvironmentStrings action modifies the values of environment variables.</span></span>

<span data-ttu-id="37488-105">請注意，執行 [WriteEnvironmentStrings 動作](writeenvironmentstrings-action.md) 或 RemoveEnvironmentStrings 動作時，環境變數不會變更進行中的安裝。</span><span class="sxs-lookup"><span data-stu-id="37488-105">Note that environment variables do not change for the installation in progress when either the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) or RemoveEnvironmentStrings action are run.</span></span> <span data-ttu-id="37488-106">在 Windows 2000 上，這項資訊會儲存在登錄中，並傳送一則訊息，通知系統在安裝完成時的變更。</span><span class="sxs-lookup"><span data-stu-id="37488-106">On Windows 2000, this information is stored in the registry and a message is sent to notify the system of changes when the installation completes.</span></span> <span data-ttu-id="37488-107">新的進程或另一個檢查這些訊息的程式，將會使用新的環境變數。</span><span class="sxs-lookup"><span data-stu-id="37488-107">A new process, or another process that checks for these messages, will use the new environment variables.</span></span>

<span data-ttu-id="37488-108">安裝程式只會在安裝或重新安裝元件期間執行 [WriteEnvironmentStrings 動作](writeenvironmentstrings-action.md) ，而且只會在移除元件期間執行 RemoveEnvironmentStrings 動作。</span><span class="sxs-lookup"><span data-stu-id="37488-108">The installer runs the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) only during the installation or reinstallation of a component, and runs the RemoveEnvironmentStrings action only during the removal of a component.</span></span>

<span data-ttu-id="37488-109">系統會根據選取的主要動作和修飾詞來寫入或移除值。</span><span class="sxs-lookup"><span data-stu-id="37488-109">Values are written or removed based on the selection of primary actions and modifiers.</span></span> <span data-ttu-id="37488-110">下列 ActionData 訊息章節將說明這些情況。</span><span class="sxs-lookup"><span data-stu-id="37488-110">These are described in the following ActionData Messages section.</span></span> <span data-ttu-id="37488-111">請注意，根據指定的動作而定，WriteEnvironmentStrings 可能會移除變數，而 RemoveEnvironmentStrings 可以根據 [環境資料表](environment-table.md)的編寫來加入這些變數。</span><span class="sxs-lookup"><span data-stu-id="37488-111">Note that depending upon the action specified, WriteEnvironmentStrings may remove variables, and RemoveEnvironmentStrings may add them based on the authoring of the [Environment table](environment-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="37488-112">順序限制</span><span class="sxs-lookup"><span data-stu-id="37488-112">Sequence Restrictions</span></span>

<span data-ttu-id="37488-113">[InstallValidate 動作](installvalidate-action.md)必須在 RemoveEnvironmentStrings 動作之前執行。</span><span class="sxs-lookup"><span data-stu-id="37488-113">The [InstallValidate action](installvalidate-action.md) must be executed before the RemoveEnvironmentStrings action.</span></span> <span data-ttu-id="37488-114">因為 WriteEnvironmentStrings 動作和 RemoveEnvironmentStrings 動作絕不會在安裝或移除元件期間套用，所以不會限制它們的相對順序。</span><span class="sxs-lookup"><span data-stu-id="37488-114">Because the WriteEnvironmentStrings action and RemoveEnvironmentStrings action are never both applied during the installation or removal of a component, their relative sequence is not restricted.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="37488-115">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="37488-115">ActionData Messages</span></span>



| <span data-ttu-id="37488-116">欄位</span><span class="sxs-lookup"><span data-stu-id="37488-116">Field</span></span> | <span data-ttu-id="37488-117">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="37488-117">Description of action data</span></span>                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37488-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="37488-118">\[1\]</span></span> | <span data-ttu-id="37488-119">要修改的環境變數名稱。</span><span class="sxs-lookup"><span data-stu-id="37488-119">Name of the environment variable to modify.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="37488-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="37488-120">\[2\]</span></span> | <span data-ttu-id="37488-121">環境變數值。</span><span class="sxs-lookup"><span data-stu-id="37488-121">The environment variable value.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="37488-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="37488-122">\[3\]</span></span> | <span data-ttu-id="37488-123">這是位旗標的欄位，可指定要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="37488-123">This is a field of bit flags that specify the action to be performed.</span></span> <span data-ttu-id="37488-124">主要動作只包含一個位。</span><span class="sxs-lookup"><span data-stu-id="37488-124">Include only one bit for a primary action.</span></span> <span data-ttu-id="37488-125">此欄位中可能包含一個以上的修飾詞位。</span><span class="sxs-lookup"><span data-stu-id="37488-125">There may be more than one modifier bit included in this field.</span></span> <span data-ttu-id="37488-126">請參閱下列位旗標描述。</span><span class="sxs-lookup"><span data-stu-id="37488-126">See the following bit flag descriptions.</span></span> |



 



| <span data-ttu-id="37488-127">位元值</span><span class="sxs-lookup"><span data-stu-id="37488-127">Bit value</span></span> | <span data-ttu-id="37488-128">主要動作的描述</span><span class="sxs-lookup"><span data-stu-id="37488-128">Description of primary actions</span></span>                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37488-129">0x1</span><span class="sxs-lookup"><span data-stu-id="37488-129">0x1</span></span>       | <span data-ttu-id="37488-130">設定。</span><span class="sxs-lookup"><span data-stu-id="37488-130">Set.</span></span> <span data-ttu-id="37488-131">在所有情況下設定環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="37488-131">Sets the value of the environment variable in all cases.</span></span><br/> <span data-ttu-id="37488-132">如果這個位結合了附加或前置詞修飾詞位，此動作會將值加入至變數中的任何現有值。</span><span class="sxs-lookup"><span data-stu-id="37488-132">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/> |
| <span data-ttu-id="37488-133">0x2</span><span class="sxs-lookup"><span data-stu-id="37488-133">0x2</span></span>       | <span data-ttu-id="37488-134">設定。</span><span class="sxs-lookup"><span data-stu-id="37488-134">Set.</span></span> <span data-ttu-id="37488-135">如果變數不存在，則設定該值。</span><span class="sxs-lookup"><span data-stu-id="37488-135">Sets the value if the variable is absent.</span></span><br/> <span data-ttu-id="37488-136">如果這個位結合了附加或前置詞修飾詞位，此動作會將值加入至變數中的任何現有值。</span><span class="sxs-lookup"><span data-stu-id="37488-136">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/>                |
| <span data-ttu-id="37488-137">0x4</span><span class="sxs-lookup"><span data-stu-id="37488-137">0x4</span></span>       | <span data-ttu-id="37488-138">移除。</span><span class="sxs-lookup"><span data-stu-id="37488-138">Remove.</span></span> <span data-ttu-id="37488-139">從變數中移除值。</span><span class="sxs-lookup"><span data-stu-id="37488-139">Removes the value from the variable.</span></span><br/> <span data-ttu-id="37488-140">如果這個位結合了附加或前置詞修飾詞，則會從現有字串中移除值（如果值存在的話）。</span><span class="sxs-lookup"><span data-stu-id="37488-140">If this bit is combined with an Append or Prefix modifier bit, the value is removed from the existing string, if the value exists.</span></span><br/>               |



 



| <span data-ttu-id="37488-141">位元值</span><span class="sxs-lookup"><span data-stu-id="37488-141">Bit value</span></span>  | <span data-ttu-id="37488-142">修飾詞的描述</span><span class="sxs-lookup"><span data-stu-id="37488-142">Description of modifier</span></span>                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37488-143">0x20000000</span><span class="sxs-lookup"><span data-stu-id="37488-143">0x20000000</span></span> | <span data-ttu-id="37488-144">如果設定此位，則會將動作套用至電腦環境變數。</span><span class="sxs-lookup"><span data-stu-id="37488-144">If this bit is set, actions are applied to the machine environment variables.</span></span><br/> <span data-ttu-id="37488-145">如果未設定此位，則會將動作套用至使用者的環境變數。</span><span class="sxs-lookup"><span data-stu-id="37488-145">If this bit is not set, actions are applied to the user's environment variables.</span></span><br/> |
| <span data-ttu-id="37488-146">0x40000000</span><span class="sxs-lookup"><span data-stu-id="37488-146">0x40000000</span></span> | <span data-ttu-id="37488-147">Append。</span><span class="sxs-lookup"><span data-stu-id="37488-147">Append.</span></span> <span data-ttu-id="37488-148">這位是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="37488-148">This bit is optional.</span></span> <span data-ttu-id="37488-149">請勿同時設定 Append 和 Prefix 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="37488-149">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |
| <span data-ttu-id="37488-150">0x80000000</span><span class="sxs-lookup"><span data-stu-id="37488-150">0x80000000</span></span> | <span data-ttu-id="37488-151">首碼。</span><span class="sxs-lookup"><span data-stu-id="37488-151">Prefix.</span></span> <span data-ttu-id="37488-152">這位是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="37488-152">This bit is optional.</span></span> <span data-ttu-id="37488-153">請勿同時設定 Append 和 Prefix 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="37488-153">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |



 

 

 




