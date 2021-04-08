---
title: IAgentCharacterEx
description: IAgentCharacterEx
ms.assetid: 8defc836-cc54-40c7-8afc-ec90f941861b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92a9f9c39804d6b5d3ac777457fff5b7f03823c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840360"
---
# <a name="iagentcharacterex"></a><span data-ttu-id="977bb-103">IAgentCharacterEx</span><span class="sxs-lookup"><span data-stu-id="977bb-103">IAgentCharacterEx</span></span>

<span data-ttu-id="977bb-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="977bb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="977bb-105">**IAgentCharacterEx** 衍生自 [**IAgentCharacter**](iagentcharacter.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="977bb-105">**IAgentCharacterEx** derives from the [**IAgentCharacter**](iagentcharacter.md) interface.</span></span> <span data-ttu-id="977bb-106">它包含所有的 **IAgentCharacter** 方法，以及提供其他函式的存取權。</span><span class="sxs-lookup"><span data-stu-id="977bb-106">It includes all the **IAgentCharacter** methods as well as provides access to additional functions.</span></span>

<span data-ttu-id="977bb-107">**依照 Vtable 順序的方法**</span><span class="sxs-lookup"><span data-stu-id="977bb-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="977bb-108">IAgentCharacterEx 方法</span><span class="sxs-lookup"><span data-stu-id="977bb-108">IAgentCharacterEx Methods</span></span>                                         | <span data-ttu-id="977bb-109">Description</span><span class="sxs-lookup"><span data-stu-id="977bb-109">Description</span></span>                                                                    |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="977bb-110">**ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="977bb-110">**ShowPopupMenu**</span></span>](iagentcharacterex--showpopupmenu.md)         | <span data-ttu-id="977bb-111">顯示字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="977bb-111">Displays the pop-up menu for the character.</span></span>                                    |
| [<span data-ttu-id="977bb-112">**SetAutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="977bb-112">**SetAutoPopupMenu**</span></span>](iagentcharacterex--setautopopupmenu.md)   | <span data-ttu-id="977bb-113">設定伺服器是否自動顯示字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="977bb-113">Sets whether the server automatically displays the character's pop-up menu.</span></span>    |
| [<span data-ttu-id="977bb-114">**GetAutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="977bb-114">**GetAutoPopupMenu**</span></span>](iagentcharacterex--getautopopupmenu.md)   | <span data-ttu-id="977bb-115">傳回伺服器是否自動顯示字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="977bb-115">Returns whether the server automatically displays the character's pop-up menu.</span></span> |
| [<span data-ttu-id="977bb-116">**GetHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="977bb-116">**GetHelpFileName**</span></span>](iagentcharacterex--gethelpfilename.md)     | <span data-ttu-id="977bb-117">傳回字元的說明文件名。</span><span class="sxs-lookup"><span data-stu-id="977bb-117">Returns the Help filename for the character.</span></span>                                   |
| [<span data-ttu-id="977bb-118">**SetHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="977bb-118">**SetHelpFileName**</span></span>](iagentcharacterex--sethelpfilename.md)     | <span data-ttu-id="977bb-119">設定字元的說明文件名。</span><span class="sxs-lookup"><span data-stu-id="977bb-119">Sets the Help filename for the character.</span></span>                                      |
| [<span data-ttu-id="977bb-120">**SetHelpModeOn**</span><span class="sxs-lookup"><span data-stu-id="977bb-120">**SetHelpModeOn**</span></span>](iagentcharacterex--sethelpmodeon.md)         | <span data-ttu-id="977bb-121">將說明模式設定為開啟。</span><span class="sxs-lookup"><span data-stu-id="977bb-121">Sets Help mode on.</span></span>                                                             |
| [<span data-ttu-id="977bb-122">**GetHelpModeOn**</span><span class="sxs-lookup"><span data-stu-id="977bb-122">**GetHelpModeOn**</span></span>](iagentcharacterex--gethelpmodeon.md)         | <span data-ttu-id="977bb-123">傳回說明模式是否為開啟。</span><span class="sxs-lookup"><span data-stu-id="977bb-123">Returns whether Help mode is on.</span></span>                                               |
| [<span data-ttu-id="977bb-124">**SetHelpCoNtextID**</span><span class="sxs-lookup"><span data-stu-id="977bb-124">**SetHelpContextID**</span></span>](iagentcharacterex--sethelpcontextid.md)   | <span data-ttu-id="977bb-125">設定字元的提供。</span><span class="sxs-lookup"><span data-stu-id="977bb-125">Sets the HelpContextID for the character.</span></span>                                      |
| [<span data-ttu-id="977bb-126">**GetHelpCoNtextID**</span><span class="sxs-lookup"><span data-stu-id="977bb-126">**GetHelpContextID**</span></span>](iagentcharacterex--gethelpcontextid.md)   | <span data-ttu-id="977bb-127">傳回字元的提供。</span><span class="sxs-lookup"><span data-stu-id="977bb-127">Returns the HelpContextID for the character.</span></span>                                   |
| [<span data-ttu-id="977bb-128">**GetActive**</span><span class="sxs-lookup"><span data-stu-id="977bb-128">**GetActive**</span></span>](iagentcharacterex--getactive.md)                 | <span data-ttu-id="977bb-129">傳回字元的現用狀態。</span><span class="sxs-lookup"><span data-stu-id="977bb-129">Returns the active state for the character.</span></span>                                    |
| [<span data-ttu-id="977bb-130">**接聽**</span><span class="sxs-lookup"><span data-stu-id="977bb-130">**Listen**</span></span>](iagentcharacterex--listen.md)                       | <span data-ttu-id="977bb-131">設定字元的接聽狀態。</span><span class="sxs-lookup"><span data-stu-id="977bb-131">Sets the listening state for the character.</span></span>                                    |
| [<span data-ttu-id="977bb-132">**SetLanguageID**</span><span class="sxs-lookup"><span data-stu-id="977bb-132">**SetLanguageID**</span></span>](iagentcharacterex--setlanguageid.md)         | <span data-ttu-id="977bb-133">設定字元的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="977bb-133">Sets the language ID for the character.</span></span>                                        |
| [<span data-ttu-id="977bb-134">**getLanguageID**</span><span class="sxs-lookup"><span data-stu-id="977bb-134">**getLanguageID**</span></span>](iagentcharacterex--getlanguageid.md)         | <span data-ttu-id="977bb-135">傳回字元的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="977bb-135">Returns the language ID for the character.</span></span>                                     |
| [<span data-ttu-id="977bb-136">**getTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="977bb-136">**getTTSModeID**</span></span>](iagentcharacterex--getttsmodeid.md)           | <span data-ttu-id="977bb-137">傳回為字元設定的 TTS 模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="977bb-137">Returns the TTS mode ID set for the character.</span></span>                                 |
| [<span data-ttu-id="977bb-138">**SetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="977bb-138">**SetTTSModeID**</span></span>](iagentcharacterex--setttsmodeid.md)           | <span data-ttu-id="977bb-139">設定字元的 TTS 模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="977bb-139">Sets the TTS mode ID for the character.</span></span>                                        |
| [<span data-ttu-id="977bb-140">**getSRModeID**</span><span class="sxs-lookup"><span data-stu-id="977bb-140">**getSRModeID**</span></span>](iagentcharacterex--getsrmodeid.md)             | <span data-ttu-id="977bb-141">傳回目前的語音辨識引擎的模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="977bb-141">Returns the current speech recognition engine's mode ID.</span></span>                       |
| [<span data-ttu-id="977bb-142">**setSRModeID**</span><span class="sxs-lookup"><span data-stu-id="977bb-142">**setSRModeID**</span></span>](iagentcharacterex--setsrmodeid.md)             | <span data-ttu-id="977bb-143">設定語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="977bb-143">Sets the speech recognition engine.</span></span>                                            |
| [<span data-ttu-id="977bb-144">**GetGUID**</span><span class="sxs-lookup"><span data-stu-id="977bb-144">**GetGUID**</span></span>](iagentcharacterex--getguid.md)                     | <span data-ttu-id="977bb-145">傳回字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="977bb-145">Returns the character's identifier.</span></span>                                            |
| [<span data-ttu-id="977bb-146">**GetOriginalSize**</span><span class="sxs-lookup"><span data-stu-id="977bb-146">**GetOriginalSize**</span></span>](iagentcharacterex--getoriginalsize.md)     | <span data-ttu-id="977bb-147">傳回字元框架的原始大小。</span><span class="sxs-lookup"><span data-stu-id="977bb-147">Returns the original size of the character frame.</span></span>                              |
| [<span data-ttu-id="977bb-148">**認為**</span><span class="sxs-lookup"><span data-stu-id="977bb-148">**Think**</span></span>](iagentcharacterex--think.md)                         | <span data-ttu-id="977bb-149">在字元的「想法」氣球中顯示指定的文字。</span><span class="sxs-lookup"><span data-stu-id="977bb-149">Displays the specified text in the character's "thought" balloon.</span></span>              |
| [<span data-ttu-id="977bb-150">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="977bb-150">**GetVersion**</span></span>](iagentcharacterex--getversion.md)               | <span data-ttu-id="977bb-151">傳回字元的版本。</span><span class="sxs-lookup"><span data-stu-id="977bb-151">Returns the version of the character.</span></span>                                          |
| [<span data-ttu-id="977bb-152">**GetAnimationNames**</span><span class="sxs-lookup"><span data-stu-id="977bb-152">**GetAnimationNames**</span></span>](iagentcharacterex--getanimationnames.md) | <span data-ttu-id="977bb-153">傳回字元的動畫名稱。</span><span class="sxs-lookup"><span data-stu-id="977bb-153">Returns the names of the animations for the character.</span></span>                         |
| [<span data-ttu-id="977bb-154">**getSRStatus**</span><span class="sxs-lookup"><span data-stu-id="977bb-154">**getSRStatus**</span></span>](iagentcharacterex--getsrstatus.md)             | <span data-ttu-id="977bb-155">傳回支援語音輸入所需的條件。</span><span class="sxs-lookup"><span data-stu-id="977bb-155">Returns the conditions necessary to support speech input.</span></span>                      |



 

 

 




