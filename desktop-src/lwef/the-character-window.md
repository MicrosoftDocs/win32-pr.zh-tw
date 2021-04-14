---
title: 字元視窗
description: 字元視窗
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383357"
---
# <a name="the-character-window"></a><span data-ttu-id="58d87-103">字元視窗</span><span class="sxs-lookup"><span data-stu-id="58d87-103">The Character Window</span></span>

<span data-ttu-id="58d87-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="58d87-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="58d87-105">Microsoft Agent 會在自己的視窗中顯示動畫字元，這些字元一律會出現在視窗迭置順序的最上方， (也就是一律在最上層) 。</span><span class="sxs-lookup"><span data-stu-id="58d87-105">Microsoft Agent displays animated characters in their own windows that always appear at the top of the window z-order (that is, always on top).</span></span> <span data-ttu-id="58d87-106">使用者可以拖曳字元與滑鼠左鍵，以移動字元的視窗。</span><span class="sxs-lookup"><span data-stu-id="58d87-106">A user can move a character's window by dragging the character with the left mouse button.</span></span> <span data-ttu-id="58d87-107">字元影像會隨著指標移動。</span><span class="sxs-lookup"><span data-stu-id="58d87-107">The character image moves with the pointer.</span></span> <span data-ttu-id="58d87-108">此外，應用程式可以使用 [**MoveTo**](moveto-method.md) 方法移動字元。</span><span class="sxs-lookup"><span data-stu-id="58d87-108">In addition, an application can move a character using the [**MoveTo**](moveto-method.md) method.</span></span>

<span data-ttu-id="58d87-109">當使用者以滑鼠右鍵按一下某個字元時，會出現顯示下列命令的快顯功能表：</span><span class="sxs-lookup"><span data-stu-id="58d87-109">When the user right-clicks a character, a pop-up menu appears that displays the following commands:</span></span>

<span data-ttu-id="58d87-110">開啟 \| Close <span class="underline">V</span>oice 命令視窗</span><span class="sxs-lookup"><span data-stu-id="58d87-110">Open \| Close <span class="underline">V</span>oice Commands Window</span></span>

<span data-ttu-id="58d87-111"><span class="underline">H</span>ide</span><span class="sxs-lookup"><span data-stu-id="58d87-111"><span class="underline">H</span>ide</span></span>

<span data-ttu-id="58d87-112">----------------------------…</span><span class="sxs-lookup"><span data-stu-id="58d87-112">----------------------------…</span></span>

<span data-ttu-id="58d87-113">命令\*</span><span class="sxs-lookup"><span data-stu-id="58d87-113">Command\*</span></span>


<span data-ttu-id="58d87-114">*OtherHostingApplicationCaption\*\**</span><span class="sxs-lookup"><span data-stu-id="58d87-114">*OtherHostingApplicationCaption\*\**</span></span>

<span data-ttu-id="58d87-115">\*列出的命令是以輸入-主動用戶端為基礎。</span><span class="sxs-lookup"><span data-stu-id="58d87-115">\*Commands listed are based on the input-active client.</span></span> <span data-ttu-id="58d87-116">如需有關定義快顯功能表中所顯示命令的詳細資訊，請參閱 Microsoft Agent 程式設計介面總覽。</span><span class="sxs-lookup"><span data-stu-id="58d87-116">For more information on defining commands that appear in the pop-up menu, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="58d87-117">\*\*列出的專案是目前裝載該字元的其他所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="58d87-117">\*\*Entries listed are all other applications currently hosting the character.</span></span> <span data-ttu-id="58d87-118">如需定義此專案的詳細資訊，請參閱 Microsoft Agent 程式設計介面總覽。</span><span class="sxs-lookup"><span data-stu-id="58d87-118">For more information on defining this entry, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="58d87-119">[開啟 \| 關閉語音命令] 視窗命令會控制目前作用中字元的 [命令] 視窗的顯示。</span><span class="sxs-lookup"><span data-stu-id="58d87-119">The Open \| Close Voice Commands Window command controls the display of the Commands Window of the current active character.</span></span> <span data-ttu-id="58d87-120">如果已停用語音辨識服務，則會停用此命令。</span><span class="sxs-lookup"><span data-stu-id="58d87-120">If speech recognition services are disabled, this command is disabled.</span></span> <span data-ttu-id="58d87-121">如果未安裝語音辨識服務，則不會出現此命令。</span><span class="sxs-lookup"><span data-stu-id="58d87-121">If speech recognition services are not installed, this command does not appear.</span></span>

<span data-ttu-id="58d87-122">隱藏命令會隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="58d87-122">The Hide command hides the character.</span></span> <span data-ttu-id="58d87-123">指派給字元 **隱藏** 狀態的動畫會播放並隱藏該字元。</span><span class="sxs-lookup"><span data-stu-id="58d87-123">The animation assigned to the character's **Hiding** state plays and hides the character.</span></span> <span data-ttu-id="58d87-124">[隱藏] 中的字母 "H" 是命令的存取金鑰 (助憶鍵) 。</span><span class="sxs-lookup"><span data-stu-id="58d87-124">The letter "H" in hide is the command's access key (mnemonic).</span></span>

<span data-ttu-id="58d87-125">應用程式 (s 的命令) 目前裝載字元在 Hide 命令後面，前面會加上分隔符號。</span><span class="sxs-lookup"><span data-stu-id="58d87-125">The commands for the application(s) currently hosting the character follow the Hide command, preceded by a separator.</span></span> <span data-ttu-id="58d87-126">然後，其他使用該字元的應用程式名稱也會出現在分隔符號前面。</span><span class="sxs-lookup"><span data-stu-id="58d87-126">Then the names of other applications using the character appear, also preceded by a separator.</span></span>

 

 




