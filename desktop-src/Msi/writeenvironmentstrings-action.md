---
description: WriteEnvironmentStrings 動作會修改環境變數的值。
ms.assetid: a91c1ffe-1bdd-49bb-aa6a-71667a1ed812
title: WriteEnvironmentStrings 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a9d64a1140fc883d94e8d3733608d29dc2d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026982"
---
# <a name="writeenvironmentstrings-action"></a><span data-ttu-id="4b03c-103">WriteEnvironmentStrings 動作</span><span class="sxs-lookup"><span data-stu-id="4b03c-103">WriteEnvironmentStrings Action</span></span>

<span data-ttu-id="4b03c-104">WriteEnvironmentStrings 動作會修改環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="4b03c-104">The WriteEnvironmentStrings action modifies the values of environment variables.</span></span>

<span data-ttu-id="4b03c-105">執行 WriteEnvironmentStrings 動作或 [RemoveEnvironmentStrings 動作](removeenvironmentstrings-action.md) 時，不會變更環境變數以進行安裝。</span><span class="sxs-lookup"><span data-stu-id="4b03c-105">Environment variables do not change for the installation in progress when the WriteEnvironmentStrings action or [RemoveEnvironmentStrings action](removeenvironmentstrings-action.md) are run.</span></span> <span data-ttu-id="4b03c-106">在 Windows 2000、Windows Server 2003、Windows XP 和 Windows Vista 上，這項資訊會儲存在登錄中，並傳送 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) 訊息，以在安裝完成時通知系統變更。</span><span class="sxs-lookup"><span data-stu-id="4b03c-106">On Windows 2000, Windows Server 2003, Windows XP, and Windows Vista this information is stored in the registry and a [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message is sent to notify the system of the changes when the installation completes.</span></span> <span data-ttu-id="4b03c-107">另一個進程可以藉由處理這些訊息來接收變更的通知。</span><span class="sxs-lookup"><span data-stu-id="4b03c-107">Another process can receive notification of the changes by handling these messages.</span></span> <span data-ttu-id="4b03c-108">如果系統重新開機已暫止，則不會傳送任何訊息。</span><span class="sxs-lookup"><span data-stu-id="4b03c-108">No message is sent if a restart of the system is pending.</span></span> <span data-ttu-id="4b03c-109">封裝可以使用 [**MsiSystemRebootPending**](msisystemrebootpending.md) 屬性來檢查系統重新開機是否暫止。</span><span class="sxs-lookup"><span data-stu-id="4b03c-109">A package can use the [**MsiSystemRebootPending**](msisystemrebootpending.md) property to check whether a system restart is pending.</span></span>

<span data-ttu-id="4b03c-110">安裝程式只會在安裝或重新安裝元件期間執行 WriteEnvironmentStrings 動作，而且只會在移除元件期間執行 [RemoveEnvironmentStrings 動作](removeenvironmentstrings-action.md) 。</span><span class="sxs-lookup"><span data-stu-id="4b03c-110">The installer runs the WriteEnvironmentStrings action only during the installation or reinstallation of a component, and runs the [RemoveEnvironmentStrings action](removeenvironmentstrings-action.md) only during the removal of a component.</span></span>

<span data-ttu-id="4b03c-111">系統會根據選取的主要動作和修飾詞來寫入或移除值。</span><span class="sxs-lookup"><span data-stu-id="4b03c-111">Values are written or removed based on the selection of primary actions and modifiers.</span></span> <span data-ttu-id="4b03c-112">下列 ActionData 訊息章節將說明這些情況。</span><span class="sxs-lookup"><span data-stu-id="4b03c-112">These are described in the following ActionData Messages section.</span></span> <span data-ttu-id="4b03c-113">請注意，根據指定的動作而定，WriteEnvironmentStrings 可能會移除變數，而 RemoveEnvironmentStrings 可以根據 [環境資料表](environment-table.md)的編寫來加入這些變數。</span><span class="sxs-lookup"><span data-stu-id="4b03c-113">Note that depending on the action specified, WriteEnvironmentStrings may remove variables, and RemoveEnvironmentStrings may add them based on the authoring of the [Environment table](environment-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4b03c-114">順序限制</span><span class="sxs-lookup"><span data-stu-id="4b03c-114">Sequence Restrictions</span></span>

<span data-ttu-id="4b03c-115">[InstallValidate 動作](installvalidate-action.md)必須在 RemoveEnvironmentStrings 動作之前執行。</span><span class="sxs-lookup"><span data-stu-id="4b03c-115">The [InstallValidate action](installvalidate-action.md) must be executed before the RemoveEnvironmentStrings action.</span></span> <span data-ttu-id="4b03c-116">因為 WriteEnvironmentStrings 動作和 RemoveEnvironmentStrings 動作絕不會在安裝或移除元件期間套用，所以不會限制它們的相對順序。</span><span class="sxs-lookup"><span data-stu-id="4b03c-116">Because the WriteEnvironmentStrings action and RemoveEnvironmentStrings action are never both applied during an install or removal of a component, their relative sequence is not restricted.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4b03c-117">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="4b03c-117">ActionData Messages</span></span>



| <span data-ttu-id="4b03c-118">欄位</span><span class="sxs-lookup"><span data-stu-id="4b03c-118">Field</span></span> | <span data-ttu-id="4b03c-119">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="4b03c-119">Description of action data</span></span>                                                                                                                                                                                                  |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b03c-120">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4b03c-120">\[1\]</span></span> | <span data-ttu-id="4b03c-121">要修改的環境變數名稱。</span><span class="sxs-lookup"><span data-stu-id="4b03c-121">Name of the environment variable to modify.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="4b03c-122">\[2\]</span><span class="sxs-lookup"><span data-stu-id="4b03c-122">\[2\]</span></span> | <span data-ttu-id="4b03c-123">環境變數值。</span><span class="sxs-lookup"><span data-stu-id="4b03c-123">The environment variable value.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="4b03c-124">\[3\]</span><span class="sxs-lookup"><span data-stu-id="4b03c-124">\[3\]</span></span> | <span data-ttu-id="4b03c-125">這是位旗標的欄位，可指定要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="4b03c-125">This is a field of bit flags that specifies the action to be performed.</span></span> <span data-ttu-id="4b03c-126">主要動作只包含一個位。</span><span class="sxs-lookup"><span data-stu-id="4b03c-126">Include only one bit for a primary action.</span></span> <span data-ttu-id="4b03c-127">此欄位中可能包含一個以上的修飾詞位。</span><span class="sxs-lookup"><span data-stu-id="4b03c-127">There may be more than one modifier bit included in this field.</span></span> <span data-ttu-id="4b03c-128">請參閱下列位旗標描述。</span><span class="sxs-lookup"><span data-stu-id="4b03c-128">See the following bit flag descriptions.</span></span> |



 



| <span data-ttu-id="4b03c-129">位值</span><span class="sxs-lookup"><span data-stu-id="4b03c-129">Bit Value</span></span> | <span data-ttu-id="4b03c-130">主要動作的描述</span><span class="sxs-lookup"><span data-stu-id="4b03c-130">Description of primary actions</span></span>                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b03c-131">0x1</span><span class="sxs-lookup"><span data-stu-id="4b03c-131">0x1</span></span>       | <span data-ttu-id="4b03c-132">設定。</span><span class="sxs-lookup"><span data-stu-id="4b03c-132">Set.</span></span> <span data-ttu-id="4b03c-133">在所有情況下設定環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="4b03c-133">Sets the value of the environment variable in all cases.</span></span><br/> <span data-ttu-id="4b03c-134">如果這個位結合了附加或前置詞修飾詞位，此動作會將值加入至變數中的任何現有值。</span><span class="sxs-lookup"><span data-stu-id="4b03c-134">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/> |
| <span data-ttu-id="4b03c-135">0x2</span><span class="sxs-lookup"><span data-stu-id="4b03c-135">0x2</span></span>       | <span data-ttu-id="4b03c-136">設定。</span><span class="sxs-lookup"><span data-stu-id="4b03c-136">Set.</span></span> <span data-ttu-id="4b03c-137">如果變數不存在，則設定該值。</span><span class="sxs-lookup"><span data-stu-id="4b03c-137">Sets the value if the variable is absent.</span></span><br/> <span data-ttu-id="4b03c-138">如果這個位結合了附加或前置詞修飾詞位，此動作會將值加入至變數中的任何現有值。</span><span class="sxs-lookup"><span data-stu-id="4b03c-138">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/>                |
| <span data-ttu-id="4b03c-139">0x4</span><span class="sxs-lookup"><span data-stu-id="4b03c-139">0x4</span></span>       | <span data-ttu-id="4b03c-140">移除。</span><span class="sxs-lookup"><span data-stu-id="4b03c-140">Remove.</span></span> <span data-ttu-id="4b03c-141">從變數中移除值。</span><span class="sxs-lookup"><span data-stu-id="4b03c-141">Removes the value from the variable.</span></span><br/> <span data-ttu-id="4b03c-142">如果這個位結合了附加或前置詞修飾詞，則會從現有字串中移除值（如果值存在的話）。</span><span class="sxs-lookup"><span data-stu-id="4b03c-142">If this bit is combined with an Append or Prefix modifier bit, the value is removed from the existing string, if the value exists.</span></span><br/>               |



 



| <span data-ttu-id="4b03c-143">位值</span><span class="sxs-lookup"><span data-stu-id="4b03c-143">Bit Value</span></span>  | <span data-ttu-id="4b03c-144">修飾詞的描述</span><span class="sxs-lookup"><span data-stu-id="4b03c-144">Description of modifier</span></span>                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b03c-145">0x20000000</span><span class="sxs-lookup"><span data-stu-id="4b03c-145">0x20000000</span></span> | <span data-ttu-id="4b03c-146">如果設定此位，則會將動作套用至電腦環境變數。</span><span class="sxs-lookup"><span data-stu-id="4b03c-146">If this bit is set, actions are applied to the machine environment variables.</span></span><br/> <span data-ttu-id="4b03c-147">如果未設定此位，則會將動作套用至使用者的環境變數。</span><span class="sxs-lookup"><span data-stu-id="4b03c-147">If this bit is not set, actions are applied to the user's environment variables.</span></span><br/> |
| <span data-ttu-id="4b03c-148">0x40000000</span><span class="sxs-lookup"><span data-stu-id="4b03c-148">0x40000000</span></span> | <span data-ttu-id="4b03c-149">Append。</span><span class="sxs-lookup"><span data-stu-id="4b03c-149">Append.</span></span> <span data-ttu-id="4b03c-150">這位是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="4b03c-150">This bit is optional.</span></span> <span data-ttu-id="4b03c-151">請勿同時設定 Append 和 Prefix 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="4b03c-151">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |
| <span data-ttu-id="4b03c-152">0x80000000</span><span class="sxs-lookup"><span data-stu-id="4b03c-152">0x80000000</span></span> | <span data-ttu-id="4b03c-153">首碼。</span><span class="sxs-lookup"><span data-stu-id="4b03c-153">Prefix.</span></span> <span data-ttu-id="4b03c-154">這位是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="4b03c-154">This bit is optional.</span></span> <span data-ttu-id="4b03c-155">請勿同時設定 Append 和 Prefix 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="4b03c-155">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |



 

 

 
