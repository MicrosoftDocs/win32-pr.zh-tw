---
description: Dataadapter.doaction ControlEvent 會通知安裝程式執行自訂動作。 這個事件可以透過按鈕控制項、CheckBox 控制項或 SelectionTree 控制項來發行。 此事件應該撰寫至 ControlEvent 資料表。
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: Dataadapter.doaction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112272"
---
# <a name="doaction-controlevent"></a><span data-ttu-id="d8165-105">Dataadapter.doaction ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d8165-105">DoAction ControlEvent</span></span>

<span data-ttu-id="d8165-106">Dataadapter.doaction ControlEvent 會通知安裝程式執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="d8165-106">The DoAction ControlEvent notifies the installer to execute a custom action.</span></span> <span data-ttu-id="d8165-107">這個事件可以透過 [按鈕](pushbutton-control.md) 控制項、 [CheckBox](checkbox-control.md) 控制項或 [SelectionTree](selectiontree-control.md) 控制項來發行。</span><span class="sxs-lookup"><span data-stu-id="d8165-107">This event can be published by a [PushButton](pushbutton-control.md) control, [CheckBox](checkbox-control.md) control, or a [SelectionTree](selectiontree-control.md) control.</span></span> <span data-ttu-id="d8165-108">此事件應該撰寫至 [ControlEvent](controlevent-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="d8165-108">This event should be authored into the [ControlEvent](controlevent-table.md) table.</span></span>

<span data-ttu-id="d8165-109">請注意，Dataadapter.doaction ControlEvent 啟動的自訂動作可以傳送具有 [**Message 方法**](session-message.md)的訊息，但無法傳送具有 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)的訊息。</span><span class="sxs-lookup"><span data-stu-id="d8165-109">Note that custom actions launched by a DoAction ControlEvent can send a message with the [**Message Method**](session-message.md), but cannot send a message with [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="d8165-110">在 Windows Server 2003 之前的系統上，由 Dataadapter.doaction ControlEvent 啟動的自訂動作無法使用 **MsiProcessMessage** 或 **Message 方法** 傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="d8165-110">On systems prior to Windows Server 2003, custom actions launched by a DoAction ControlEvent cannot send messages with **MsiProcessMessage** or **Message Method**.</span></span> <span data-ttu-id="d8165-111">如需詳細資訊，請參閱 [使用 MsiProcessMessage 將訊息傳送至 Windows Installer](sending-messages-to-windows-installer-using-msiprocessmessage.md)。</span><span class="sxs-lookup"><span data-stu-id="d8165-111">For more information, see [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="d8165-112">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="d8165-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d8165-113">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="d8165-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="d8165-114">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="d8165-114">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="d8165-115">發佈者</span><span class="sxs-lookup"><span data-stu-id="d8165-115">Published By</span></span>

<span data-ttu-id="d8165-116">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="d8165-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="d8165-117">引數</span><span class="sxs-lookup"><span data-stu-id="d8165-117">Argument</span></span>

<span data-ttu-id="d8165-118">字串，這是要執行之自訂動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8165-118">A string, the name of the custom action to be executed.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d8165-119">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="d8165-119">Action on Subscribers</span></span>

<span data-ttu-id="d8165-120">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="d8165-120">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d8165-121">一般用法</span><span class="sxs-lookup"><span data-stu-id="d8165-121">Typical Use</span></span>

<span data-ttu-id="d8165-122">對話方塊中的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以叫用自訂動作。</span><span class="sxs-lookup"><span data-stu-id="d8165-122">A [PushButton](pushbutton-control.md) control on a dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to invoke a custom action.</span></span>

 

 



