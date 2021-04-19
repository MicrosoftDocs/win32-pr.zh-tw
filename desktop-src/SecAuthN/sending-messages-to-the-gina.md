---
description: Winlogon 會在對話方塊顯示時，將訊息傳送至 GINA。 這些訊息全都封裝在 WLX 的 \_ WM SAS 訊息中，如下所示 \_ 。
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: 將訊息傳送至 GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976874"
---
# <a name="sending-messages-to-the-gina"></a><span data-ttu-id="a0a57-104">將訊息傳送至 GINA</span><span class="sxs-lookup"><span data-stu-id="a0a57-104">Sending Messages to the GINA</span></span>

<span data-ttu-id="a0a57-105">[*Winlogon*](../secgloss/w-gly.md) 會在對話方塊顯示時，將訊息傳送至 [*GINA*](../secgloss/g-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="a0a57-105">[*Winlogon*](../secgloss/w-gly.md) sends messages to the [*GINA*](../secgloss/g-gly.md) while dialog boxes are displayed.</span></span> <span data-ttu-id="a0a57-106">這些訊息全都封裝在 WLX 的 \_ WM SAS 訊息中，如下所示 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a0a57-106">These messages are all encapsulated in the WLX\_WM\_SAS message as follows.</span></span>



| <span data-ttu-id="a0a57-107">WParam 參數中的安全注意順序類型</span><span class="sxs-lookup"><span data-stu-id="a0a57-107">Secure attention sequence type in wParam parameter</span></span> | <span data-ttu-id="a0a57-108">Description</span><span class="sxs-lookup"><span data-stu-id="a0a57-108">Description</span></span>                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a57-109">WLX \_ SAS \_ 類型 \_ CTRL \_ ALT \_ DEL</span><span class="sxs-lookup"><span data-stu-id="a0a57-109">WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL</span></span>                     | <span data-ttu-id="a0a57-110">指出已收到 CTRL + ALT + DEL 鍵序列。</span><span class="sxs-lookup"><span data-stu-id="a0a57-110">Indicates that a CTRL+ALT+DEL key sequence was received.</span></span>                                                                                      |
| <span data-ttu-id="a0a57-111">WLX \_ SAS \_ 類型 \_ SC \_ INSERT</span><span class="sxs-lookup"><span data-stu-id="a0a57-111">WLX\_SAS\_TYPE\_SC\_INSERT</span></span>                         | <span data-ttu-id="a0a57-112">指出 [*智慧卡*](../secgloss/s-gly.md) 已插入相容的裝置。</span><span class="sxs-lookup"><span data-stu-id="a0a57-112">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span> |
| <span data-ttu-id="a0a57-113">WLX \_ SAS \_ 類型 \_ SC \_ REMOVE</span><span class="sxs-lookup"><span data-stu-id="a0a57-113">WLX\_SAS\_TYPE\_SC\_REMOVE</span></span>                         | <span data-ttu-id="a0a57-114">表示已從相容裝置移除智慧卡。</span><span class="sxs-lookup"><span data-stu-id="a0a57-114">Indicates that a smart card has been removed from a compatible device.</span></span>                                                                        |
| <span data-ttu-id="a0a57-115">WLX \_ SAS \_ 類型 \_ 使用者 \_ 登出</span><span class="sxs-lookup"><span data-stu-id="a0a57-115">WLX\_SAS\_TYPE\_USER\_LOGOFF</span></span>                       | <span data-ttu-id="a0a57-116">指出使用者已要求登出。</span><span class="sxs-lookup"><span data-stu-id="a0a57-116">Indicates that a user requested logoff.</span></span>                                                                                                       |
| <span data-ttu-id="a0a57-117">WLX \_ SAS \_ 類型 \_ SCRNSVR \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a0a57-117">WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT</span></span>                   | <span data-ttu-id="a0a57-118">指出因為缺少使用者輸入而應執行螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="a0a57-118">Indicates that the screen saver should be run due to lack of user input.</span></span>                                                                      |
| <span data-ttu-id="a0a57-119">WLX \_ SAS \_ 類型 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="a0a57-119">WLX\_SAS\_TYPE\_TIMEOUT</span></span>                            | <span data-ttu-id="a0a57-120">表示在指定的超時時間內未收到任何使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="a0a57-120">Indicates that no user input was received within the specified time-out period.</span></span>                                                               |



 

<span data-ttu-id="a0a57-121">針對超時和登出，Winlogon 會在傳送訊息之後關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a0a57-121">For time-outs and logoffs, Winlogon will close the dialog box after the message has been sent.</span></span> <span data-ttu-id="a0a57-122">這則訊息會傳送，因此對話方塊作業可以用實用的方式回應 (例如，如果) 發生登出，請關閉自己的操作。</span><span class="sxs-lookup"><span data-stu-id="a0a57-122">This message is sent so the dialog box operation can respond in a useful manner (for example, by closing itself down if a logoff has occurred).</span></span>

<span data-ttu-id="a0a57-123">針對輸入超時，此對話方塊會以程式碼 WLX \_ DLG 輸入超時的方式 \_ 關閉 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a0a57-123">For input time-outs, the dialog box is closed with the code WLX\_DLG\_INPUT\_TIMEOUT.</span></span>

<span data-ttu-id="a0a57-124">若為螢幕保護裝置時間超時，則會關閉此對話方塊，並顯示程式碼 WLX \_ DLG \_ 螢幕 \_ 保護 \_ 超時。</span><span class="sxs-lookup"><span data-stu-id="a0a57-124">For screen saver time-outs, the dialog box is closed with the code WLX\_DLG\_SCREEN\_SAVER\_TIMEOUT.</span></span>

<span data-ttu-id="a0a57-125">若為登出，則會在程式碼 WLX 使用者登出時關閉對話方塊作業 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="a0a57-125">For logoffs, the dialog box operation is closed with the code WLX\_DLG\_USER\_LOGOFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0a57-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0a57-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a57-127">正在初始化 Winlogon</span><span class="sxs-lookup"><span data-stu-id="a0a57-127">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="a0a57-128">Winlogon 狀態</span><span class="sxs-lookup"><span data-stu-id="a0a57-128">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="a0a57-129">支援的對話方塊服務超時作業</span><span class="sxs-lookup"><span data-stu-id="a0a57-129">Supported Dialog Box Service Time-out Operations</span></span>](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[<span data-ttu-id="a0a57-130">Winlogon 支援函式</span><span class="sxs-lookup"><span data-stu-id="a0a57-130">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
