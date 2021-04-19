---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16616ccb86bf109dad85a8ee2ac5d2bd009827
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106980274"
---
# <a name="iagentcommandsex"></a><span data-ttu-id="81d8f-103">IAgentCommandsEx</span><span class="sxs-lookup"><span data-stu-id="81d8f-103">IAgentCommandsEx</span></span>

<span data-ttu-id="81d8f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="81d8f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="81d8f-105">[**IAgentCommandsEx**](iagentcommandex.md) 會定義擴充 [**IAgentCommands**](iagentcommands.md) 介面的介面。</span><span class="sxs-lookup"><span data-stu-id="81d8f-105">[**IAgentCommandsEx**](iagentcommandex.md) defines an interface that extends the [**IAgentCommands**](iagentcommands.md) interface.</span></span>

<span data-ttu-id="81d8f-106">**依照 Vtable 順序的方法**</span><span class="sxs-lookup"><span data-stu-id="81d8f-106">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="81d8f-107">IAgentCommandsEx 方法</span><span class="sxs-lookup"><span data-stu-id="81d8f-107">IAgentCommandsEx Methods</span></span>                                                             | <span data-ttu-id="81d8f-108">Description</span><span class="sxs-lookup"><span data-stu-id="81d8f-108">Description</span></span>                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81d8f-109">SetDefaultID</span><span class="sxs-lookup"><span data-stu-id="81d8f-109">SetDefaultID</span></span>](iagentcommandsex--setdefaultid.md)                                   | <span data-ttu-id="81d8f-110">設定字元快顯功能表的預設命令。</span><span class="sxs-lookup"><span data-stu-id="81d8f-110">Sets the default command for the character's pop-up menu.</span></span>                                                     |
| [<span data-ttu-id="81d8f-111">GetDefaultID</span><span class="sxs-lookup"><span data-stu-id="81d8f-111">GetDefaultID</span></span>](iagentcommandsex--getdefaultid.md)                                   | <span data-ttu-id="81d8f-112">傳回字元快顯功能表的預設命令。</span><span class="sxs-lookup"><span data-stu-id="81d8f-112">Returns the default command for the character's pop-up menu.</span></span>                                                  |
| [<span data-ttu-id="81d8f-113">**SetHelpCoNtextID**</span><span class="sxs-lookup"><span data-stu-id="81d8f-113">**SetHelpContextID**</span></span>](iagentcommandex--sethelpcontextid.md)                        | <span data-ttu-id="81d8f-114">設定 [**命令**](/windows/desktop/lwef/the-command-object) 物件的上下文相關說明主題識別碼。</span><span class="sxs-lookup"><span data-stu-id="81d8f-114">Sets the context-sensitive help topic ID for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>                     |
| [<span data-ttu-id="81d8f-115">**GetHelpCoNtextID**</span><span class="sxs-lookup"><span data-stu-id="81d8f-115">**GetHelpContextID**</span></span>](iagentcommandex--gethelpcontextid.md)                        | <span data-ttu-id="81d8f-116">傳回 [**命令**](/windows/desktop/lwef/the-command-object) 物件的上下文相關說明主題識別碼。</span><span class="sxs-lookup"><span data-stu-id="81d8f-116">Returns the context-sensitive help topic ID for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>                  |
| [<span data-ttu-id="81d8f-117">SetFontName</span><span class="sxs-lookup"><span data-stu-id="81d8f-117">SetFontName</span></span>](iagentcommandsex--setfontname.md)                                     | <span data-ttu-id="81d8f-118">設定要在字元的快顯功能表中使用的字型。</span><span class="sxs-lookup"><span data-stu-id="81d8f-118">Sets the font to use in the character's pop-up menu.</span></span>                                                          |
| [<span data-ttu-id="81d8f-119">GetFontName</span><span class="sxs-lookup"><span data-stu-id="81d8f-119">GetFontName</span></span>](iagentcommandsex--getfontname.md)                                     | <span data-ttu-id="81d8f-120">傳回字元快顯功能表中所使用的字型。</span><span class="sxs-lookup"><span data-stu-id="81d8f-120">Returns the font used in the character's pop-up menu.</span></span>                                                         |
| [<span data-ttu-id="81d8f-121">SetFontSize</span><span class="sxs-lookup"><span data-stu-id="81d8f-121">SetFontSize</span></span>](iagentcommandsex--setfontsize.md)                                     | <span data-ttu-id="81d8f-122">設定要在字元的快顯功能表中使用的字型大小。</span><span class="sxs-lookup"><span data-stu-id="81d8f-122">Sets the font size to use in the character's pop-up menu.</span></span>                                                     |
| [<span data-ttu-id="81d8f-123">GetFontSize</span><span class="sxs-lookup"><span data-stu-id="81d8f-123">GetFontSize</span></span>](iagentcommandsex--getfontsize.md)                                     | <span data-ttu-id="81d8f-124">傳回字元快顯功能表中所使用的字型大小。</span><span class="sxs-lookup"><span data-stu-id="81d8f-124">Returns the font size used in the character's pop-up menu.</span></span>                                                    |
| [<span data-ttu-id="81d8f-125">**SetVoiceCaption**</span><span class="sxs-lookup"><span data-stu-id="81d8f-125">**SetVoiceCaption**</span></span>](iagentcommandex--setvoicecaption.md)                          | <span data-ttu-id="81d8f-126">設定字元 [**命令**](/windows/desktop/lwef/the-command-object) 物件的語音標題。</span><span class="sxs-lookup"><span data-stu-id="81d8f-126">Sets the voice caption for the character's [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>                         |
| [<span data-ttu-id="81d8f-127">**GetVoiceCaption**</span><span class="sxs-lookup"><span data-stu-id="81d8f-127">**GetVoiceCaption**</span></span>](iagentcommandex--getvoicecaption.md)                          | <span data-ttu-id="81d8f-128">傳回字元 [**命令**](/windows/desktop/lwef/the-command-object) 物件的聲音標題。</span><span class="sxs-lookup"><span data-stu-id="81d8f-128">Returns the voice caption for the character's [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>                      |
| [<span data-ttu-id="81d8f-129">AddEx</span><span class="sxs-lookup"><span data-stu-id="81d8f-129">AddEx</span></span>](iagentcommandsex--addex.md)                                                 | <span data-ttu-id="81d8f-130">將 [**命令**](/windows/desktop/lwef/the-command-object) 物件加入至 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合。</span><span class="sxs-lookup"><span data-stu-id="81d8f-130">Adds a [**Command**](/windows/desktop/lwef/the-command-object) object to a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>    |
| [<span data-ttu-id="81d8f-131">InsertEx</span><span class="sxs-lookup"><span data-stu-id="81d8f-131">InsertEx</span></span>](iagentcommandsex--insertex.md)                                           | <span data-ttu-id="81d8f-132">在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中插入 [**Command**](/windows/desktop/lwef/the-command-object)物件。</span><span class="sxs-lookup"><span data-stu-id="81d8f-132">Inserts a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> |
| [<span data-ttu-id="81d8f-133">SetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="81d8f-133">SetGlobalVoiceCommandsEnabled</span></span>](iagentcommandsex--setglobalvoicecommandsenabled.md) | <span data-ttu-id="81d8f-134">啟用代理程式全域命令的語音文法。</span><span class="sxs-lookup"><span data-stu-id="81d8f-134">Enables the voice grammar for Agent's global commands.</span></span>                                                        |
| [<span data-ttu-id="81d8f-135">GetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="81d8f-135">GetGlobalVoiceCommandsEnabled</span></span>](iagentcommandsex--getglobalvoicecommandsenabled.md) | <span data-ttu-id="81d8f-136">傳回是否啟用代理程式全域命令的語音文法。</span><span class="sxs-lookup"><span data-stu-id="81d8f-136">Returns whether the voice grammar for Agent's global commands is enabled.</span></span>                                     |



 

 

 