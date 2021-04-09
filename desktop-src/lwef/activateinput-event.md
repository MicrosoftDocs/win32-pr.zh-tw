---
title: ActivateInput 事件
description: ActivateInput 事件
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021967"
---
# <a name="activateinput-event"></a><span data-ttu-id="3e1f3-103">ActivateInput 事件</span><span class="sxs-lookup"><span data-stu-id="3e1f3-103">ActivateInput Event</span></span>

<span data-ttu-id="3e1f3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3e1f3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3e1f3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="3e1f3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3e1f3-106">當用戶端變成輸入主動時發生。</span><span class="sxs-lookup"><span data-stu-id="3e1f3-106">Occurs when a client becomes input-active.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="3e1f3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3e1f3-108">**Sub** *Agent* \_ ActivateInput **(ByVal** *CharacterID \* \* \* )*\*</span><span class="sxs-lookup"><span data-stu-id="3e1f3-108">**Sub** *agent*\_ActivateInput **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="3e1f3-109">部分</span><span class="sxs-lookup"><span data-stu-id="3e1f3-109">Part</span></span>          | <span data-ttu-id="3e1f3-110">描述</span><span class="sxs-lookup"><span data-stu-id="3e1f3-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="3e1f3-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="3e1f3-111">*CharacterID*</span></span> | <span data-ttu-id="3e1f3-112">傳回用戶端變成輸入活動的字元識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e1f3-112">Returns the ID of the character through which the client becomes input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3e1f3-113">備註</span><span class="sxs-lookup"><span data-stu-id="3e1f3-113">Remarks</span></span>

<span data-ttu-id="3e1f3-114">輸入-主動用戶端會接收伺服器所提供的滑鼠和語音輸入事件。</span><span class="sxs-lookup"><span data-stu-id="3e1f3-114">The input-active client receives mouse and speech input events supplied by the server.</span></span> <span data-ttu-id="3e1f3-115">伺服器只會將此事件傳送給變成進入主動輸入的用戶端。</span><span class="sxs-lookup"><span data-stu-id="3e1f3-115">The server sends this event only to the client that becomes input-active.</span></span>

<span data-ttu-id="3e1f3-116">當使用者切換至您的 [命令](the-command-object.md) 物件（例如，在 [命令] 視窗中選擇命令物件專案，或在字元的快顯功能表中選擇）時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="3e1f3-116">This event can occur when the user switches to your [Command](the-command-object.md) object, for example, by choosing your Command object entry in the Commands Window or in the pop-up menu for a character.</span></span> <span data-ttu-id="3e1f3-117">當使用者選取字元 (時，也可能會發生此問題，方法是按一下或說出其名稱) 、當字元變成可見時，以及其他用戶端應用程式的字元變成隱藏時。</span><span class="sxs-lookup"><span data-stu-id="3e1f3-117">It can also occur when the user selects a character (by clicking or speaking its name), when a character becomes visible, and when the character of another client application becomes hidden.</span></span> <span data-ttu-id="3e1f3-118">您也可以呼叫 [啟動方法](activate-method.md) (，將 **狀態** 設定為 2) 以明確地將字元設為最上層，這會導致您的用戶端應用程式變成輸入主動，並觸發此事件。</span><span class="sxs-lookup"><span data-stu-id="3e1f3-118">You can also call the [Activate Method](activate-method.md) (with **State** set to 2) to explicitly make the character topmost, which results in your client application becoming input-active and triggers this event.</span></span> <span data-ttu-id="3e1f3-119">但是，如果您只使用 Activate 方法方法來指定用戶端是否為字元的作用中用戶端，就不會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="3e1f3-119">However, this event does not occur if you use the Activate Method method only to specify whether your client is the active client of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="3e1f3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e1f3-120">See Also</span></span>

<span data-ttu-id="3e1f3-121">[**DeactivateInput** 事件](deactivateinput-event.md)， [ **Activate** 方法](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="3e1f3-121">[**DeactivateInput** event](deactivateinput-event.md), [**Activate** method](activate-method.md)</span></span>


 

 




