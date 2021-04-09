---
title: 使用 [使用] 控制項
description: 本章節提供適用于區段控制項的執行詳細資料和範例。
ms.assetid: 28078f3e-a3d1-4bb5-96c6-2191ff9f8d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d667a495dce918bdcfcf0391638eef8a3c6e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672880"
---
# <a name="using-trackbar-controls"></a><span data-ttu-id="4fb48-103">使用 [使用] 控制項</span><span class="sxs-lookup"><span data-stu-id="4fb48-103">Using Trackbar Controls</span></span>

<span data-ttu-id="4fb48-104">本章節提供適用于區段控制項的執行詳細資料和範例。</span><span class="sxs-lookup"><span data-stu-id="4fb48-104">This section provides implementation details and examples for Trackbar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4fb48-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="4fb48-105">In this section</span></span>



| <span data-ttu-id="4fb48-106">主題</span><span class="sxs-lookup"><span data-stu-id="4fb48-106">Topic</span></span>                                                                                                  | <span data-ttu-id="4fb48-107">描述</span><span class="sxs-lookup"><span data-stu-id="4fb48-107">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4fb48-108">如何建立跟蹤條</span><span class="sxs-lookup"><span data-stu-id="4fb48-108">How to Create a Trackbar</span></span>](create-a-trackbar.md)<br/>                                           | <span data-ttu-id="4fb48-109">建立程式時，會初始化其範圍及其選取範圍。</span><span class="sxs-lookup"><span data-stu-id="4fb48-109">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="4fb48-110">此時也會設定頁面大小。</span><span class="sxs-lookup"><span data-stu-id="4fb48-110">The page size is also set at this time.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="4fb48-111">如何處理資訊提示通知訊息</span><span class="sxs-lookup"><span data-stu-id="4fb48-111">How to Process Trackbar Notification Messages</span></span>](process-trackbar-notification-messages.md)<br/> | <span data-ttu-id="4fb48-112">Trackbars 會傳送一個 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息給父系，以通知其使用者動作的父視窗。</span><span class="sxs-lookup"><span data-stu-id="4fb48-112">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="4fb48-113">如何限制滑杆移動</span><span class="sxs-lookup"><span data-stu-id="4fb48-113">How to Limit Slider Movement</span></span>](limit-slider-movement.md)<br/>                                   | <span data-ttu-id="4fb48-114">如關於敘述區 [控制項](trackbar-controls.md)中所述，您可以將部分的部分部分的資料格範圍設定為選取範圍。</span><span class="sxs-lookup"><span data-stu-id="4fb48-114">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="4fb48-115">選取範圍的其中一個用途，就是限制滑杆的移動，讓部分的完整範圍超出限制。</span><span class="sxs-lookup"><span data-stu-id="4fb48-115">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span> <br/> |
| [<span data-ttu-id="4fb48-116">如何使用好友視窗</span><span class="sxs-lookup"><span data-stu-id="4fb48-116">How to Use Buddy Windows</span></span>](use-buddy-windows.md)<br/>                                           | <span data-ttu-id="4fb48-117">藉由將其他控制項設定為標題的合作者視窗，您就可以將這些控制項以標籤的形式自動放置在這些標題的結尾。</span><span class="sxs-lookup"><span data-stu-id="4fb48-117">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span><br/>                                                                                                                          |



 

 

 





