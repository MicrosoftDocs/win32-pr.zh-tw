---
title: DeactivateInput 事件
description: DeactivateInput 事件
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932336"
---
# <a name="deactivateinput-event"></a><span data-ttu-id="35e39-103">DeactivateInput 事件</span><span class="sxs-lookup"><span data-stu-id="35e39-103">DeactivateInput Event</span></span>

<span data-ttu-id="35e39-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="35e39-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="35e39-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="35e39-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="35e39-106">當用戶端變成非輸入-主動時發生。</span><span class="sxs-lookup"><span data-stu-id="35e39-106">Occurs when a client becomes non-input-active.</span></span>

</dd> <dt>

<span data-ttu-id="35e39-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="35e39-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="35e39-108">**子\*\*\*代理程式 \* \* \* \_ DeactivateInput* \*  **(ByVal** *CharacterID \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="35e39-108">**Sub** *agent\*\*\*\_DeactivateInput*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="35e39-109">部分</span><span class="sxs-lookup"><span data-stu-id="35e39-109">Part</span></span>          | <span data-ttu-id="35e39-110">描述</span><span class="sxs-lookup"><span data-stu-id="35e39-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="35e39-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="35e39-111">*CharacterID*</span></span> | <span data-ttu-id="35e39-112">傳回讓用戶端變成非輸入-主動的字元識別碼。</span><span class="sxs-lookup"><span data-stu-id="35e39-112">Returns the ID of the character that makes the client become non-input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="35e39-113">備註</span><span class="sxs-lookup"><span data-stu-id="35e39-113">Remarks</span></span>

<span data-ttu-id="35e39-114">非輸入-主動用戶端不再接收來自伺服器 (的滑鼠或語音事件，除非它再次變成) 的輸入活動。</span><span class="sxs-lookup"><span data-stu-id="35e39-114">A non-input-active client no longer receives mouse or speech events from the server (unless it becomes input-active again).</span></span> <span data-ttu-id="35e39-115">伺服器只會將此事件傳送給變成非輸入-主動的用戶端。</span><span class="sxs-lookup"><span data-stu-id="35e39-115">The server sends this event only to the client that becomes non-input-active.</span></span>

<span data-ttu-id="35e39-116">當您的用戶端應用程式為輸入-主動，且使用者在字元的快顯功能表或 [語音命令] 視窗中選擇另一個用戶端的標題，或是您呼叫 [**Activate**](activate-method.md) 方法並將 **State** 參數設定為0時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="35e39-116">This event occurs when your client application is input-active and the user chooses the caption of another client in a character's pop-up menu or the Voice Commands Window or you call the [**Activate**](activate-method.md) method and set the **State** parameter to 0.</span></span> <span data-ttu-id="35e39-117">當使用者按一下或說話來選取其他字元的名稱時，也可能會發生此問題。</span><span class="sxs-lookup"><span data-stu-id="35e39-117">It may also occur when the user selects the name of another character by clicking or speaking.</span></span> <span data-ttu-id="35e39-118">當您隱藏字元或顯示其他字元時，也會收到此事件。</span><span class="sxs-lookup"><span data-stu-id="35e39-118">You also get this event when your character is hidden or another character becomes visible.</span></span>

### <a name="see-also"></a><span data-ttu-id="35e39-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35e39-119">See Also</span></span>

[<span data-ttu-id="35e39-120">**ActivateInput 事件**</span><span class="sxs-lookup"><span data-stu-id="35e39-120">**ActivateInput event**</span></span>](activateinput-event.md)


 

 




