---
description: Winlogon 會執行兩個超時作業，一個用於安全對話方塊，另一個用於啟用和終止螢幕保護裝置。
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: 支援的對話方塊服務超時作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690511"
---
# <a name="supported-dialog-box-service-time-out-operations"></a><span data-ttu-id="5428c-103">支援的對話方塊服務超時作業</span><span class="sxs-lookup"><span data-stu-id="5428c-103">Supported Dialog Box Service Time-out Operations</span></span>

<span data-ttu-id="5428c-104">[*Winlogon*](../secgloss/w-gly.md) 會執行兩個超時作業，一個用於安全對話方塊，另一個用於啟用和終止螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="5428c-104">[*Winlogon*](../secgloss/w-gly.md) implements two time-out operations, one for secure dialog boxes and the other for screen saver activation and termination.</span></span>

<span data-ttu-id="5428c-105">在顯示安全的對話方塊時（例如登入或解除鎖定工作站），Winlogon 可以超時對話方塊，並將適當的結果碼傳回到對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="5428c-105">While displaying a secure dialog box, such as logon or unlocking a workstation, Winlogon can time-out the dialog boxes and return an appropriate result code to the dialog box procedure.</span></span> <span data-ttu-id="5428c-106">Winlogon 提供一組 [*GINA*](../secgloss/g-gly.md)的對話方塊支援功能。</span><span class="sxs-lookup"><span data-stu-id="5428c-106">Winlogon provides a set of dialog box support functions for the [*GINA*](../secgloss/g-gly.md).</span></span> <span data-ttu-id="5428c-107">GINA 必須使用這些函式，而不是其 Windows 對應項，以確保 GINA 和 Winlogon 維持適當的控制對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5428c-107">The GINA must use these functions instead of their Windows counterparts to ensure that the GINA and Winlogon maintain appropriate control over the dialog boxes.</span></span> <span data-ttu-id="5428c-108">若無法使用這些函式的 Winlogon 版本，可能會導致未經授權的使用者取得系統的存取權。</span><span class="sxs-lookup"><span data-stu-id="5428c-108">Failure to use the Winlogon versions of these functions could result in unauthorized users gaining access to the system.</span></span>

<span data-ttu-id="5428c-109">Winlogon 對話方塊服務是由下列支援功能所提供。</span><span class="sxs-lookup"><span data-stu-id="5428c-109">Winlogon dialog box services are provided by the following support functions.</span></span>



| <span data-ttu-id="5428c-110">Support 函數</span><span class="sxs-lookup"><span data-stu-id="5428c-110">Support function</span></span>                                               | <span data-ttu-id="5428c-111">Description</span><span class="sxs-lookup"><span data-stu-id="5428c-111">Description</span></span>                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5428c-112">**WlxMessageBox**</span><span class="sxs-lookup"><span data-stu-id="5428c-112">**WlxMessageBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | <span data-ttu-id="5428c-113">類似于 Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) 函數。</span><span class="sxs-lookup"><span data-stu-id="5428c-113">Similar to the Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>                         |
| [<span data-ttu-id="5428c-114">**WlxDialogBox**</span><span class="sxs-lookup"><span data-stu-id="5428c-114">**WlxDialogBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | <span data-ttu-id="5428c-115">類似于 Windows [**對話方塊**](/windows/win32/api/winuser/nf-winuser-dialogboxa) 函數。</span><span class="sxs-lookup"><span data-stu-id="5428c-115">Similar to the Windows [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function.</span></span>                           |
| [<span data-ttu-id="5428c-116">**WlxDialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="5428c-116">**WlxDialogBoxIndirect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | <span data-ttu-id="5428c-117">類似于 Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) 函數。</span><span class="sxs-lookup"><span data-stu-id="5428c-117">Similar to the Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) function.</span></span>           |
| [<span data-ttu-id="5428c-118">**WlxDialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="5428c-118">**WlxDialogBoxParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | <span data-ttu-id="5428c-119">類似于 Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) 函數。</span><span class="sxs-lookup"><span data-stu-id="5428c-119">Similar to the Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) function.</span></span>                 |
| [<span data-ttu-id="5428c-120">**WlxDialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="5428c-120">**WlxDialogBoxIndirectParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | <span data-ttu-id="5428c-121">類似于 Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) 函數。</span><span class="sxs-lookup"><span data-stu-id="5428c-121">Similar to the Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) function.</span></span> |



 

<span data-ttu-id="5428c-122">GINA Dll 也可以接收 \_ \_ 來自 WINLOGON 的 WLX WM SAS 訊息。</span><span class="sxs-lookup"><span data-stu-id="5428c-122">GINA DLLs can also receive WLX\_WM\_SAS messages from Winlogon.</span></span> <span data-ttu-id="5428c-123">如果收到 (SAS) 的 [*安全注意順序*](../secgloss/s-gly.md) ，則會將這些訊息傳送至使用中的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5428c-123">These messages are sent to active dialog boxes if an [*secure attention sequence*](../secgloss/s-gly.md) (SAS) is received.</span></span> <span data-ttu-id="5428c-124">如果 GINA 正在提示 [*智慧卡*](../secgloss/s-gly.md)的相符 PIN，而且卡片已從智慧卡 [*讀卡機*](../secgloss/r-gly.md)中移除，這就很有用。</span><span class="sxs-lookup"><span data-stu-id="5428c-124">This is useful if the GINA is in the process of prompting for the matching PIN for a [*smart card*](../secgloss/s-gly.md), and the card is removed from the smart card [*reader*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="5428c-125">\_當在對話方塊作業 \_ 期間發生 SAS 事件時，Winlogon 會使用 WLX DLG SAS 作為 EndDialog 結果碼。</span><span class="sxs-lookup"><span data-stu-id="5428c-125">Winlogon uses WLX\_DLG\_SAS as the EndDialog result code when an SAS event occurs during a dialog box operation.</span></span>

<span data-ttu-id="5428c-126">您也可以透過這種方式來傳遞超時時間。</span><span class="sxs-lookup"><span data-stu-id="5428c-126">Time-outs are also delivered in this manner.</span></span> <span data-ttu-id="5428c-127">WLX 的 \_ WM \_ SAS 訊息會以 WLX \_ sas \_ 類型 \_ SCRNSVR \_ TIMEOUT 或 WLX \_ sas \_ 類型 timeout 傳送 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5428c-127">A WLX\_WM\_SAS message is sent with WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT or WLX\_SAS\_TYPE\_TIMEOUT.</span></span> <span data-ttu-id="5428c-128">對話方塊會以適當的結束代碼結束，讓 GINA 開發人員攔截超時通知。</span><span class="sxs-lookup"><span data-stu-id="5428c-128">The dialog box will end with an appropriate exit code to allow GINA developers to hook the time-out notifications.</span></span>

<span data-ttu-id="5428c-129">您可以使用程式碼 WLX 使用者登出，來終止 GINA 對話方塊 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="5428c-129">GINA dialog boxes can be terminated by Winlogon by using the code WLX\_DLG\_USER\_LOGOFF.</span></span> <span data-ttu-id="5428c-130">這表示使用者已在執行對話方塊期間登出 (例如，從另一個執行緒) 呼叫 [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) 函數。</span><span class="sxs-lookup"><span data-stu-id="5428c-130">This indicates that the user has logged off during the running of the dialog box (for example, by calling the [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) function from another thread).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5428c-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="5428c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5428c-132">正在初始化 Winlogon</span><span class="sxs-lookup"><span data-stu-id="5428c-132">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="5428c-133">Winlogon 狀態</span><span class="sxs-lookup"><span data-stu-id="5428c-133">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="5428c-134">將訊息傳送至 GINA</span><span class="sxs-lookup"><span data-stu-id="5428c-134">Sending Messages to the GINA</span></span>](sending-messages-to-the-gina.md)
</dt> <dt>

[<span data-ttu-id="5428c-135">Winlogon 支援函式</span><span class="sxs-lookup"><span data-stu-id="5428c-135">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
