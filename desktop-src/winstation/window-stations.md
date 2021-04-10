---
title: 視窗工作站
description: 視窗工作站包含剪貼簿、atom 資料表，以及一或多個桌面物件。 每個視窗工作站物件都是安全物件。 建立視窗站時，它會與呼叫進程建立關聯，並指派給目前的會話。
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- 視窗站物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023648"
---
# <a name="window-stations"></a><span data-ttu-id="c86e7-106">視窗工作站</span><span class="sxs-lookup"><span data-stu-id="c86e7-106">Window Stations</span></span>

<span data-ttu-id="c86e7-107">*視窗工作站* 包含剪貼簿、atom 資料表，以及一或多個 [桌面](desktops.md)物件。</span><span class="sxs-lookup"><span data-stu-id="c86e7-107">A *window station* contains a clipboard, an atom table, and one or more [desktop](desktops.md) objects.</span></span> <span data-ttu-id="c86e7-108">每個視窗工作站物件都是安全物件。</span><span class="sxs-lookup"><span data-stu-id="c86e7-108">Each window station object is a securable object.</span></span> <span data-ttu-id="c86e7-109">建立視窗站時，它會與呼叫進程建立關聯，並指派給目前的會話。</span><span class="sxs-lookup"><span data-stu-id="c86e7-109">When a window station is created, it is associated with the calling process and assigned to the current session.</span></span>

<span data-ttu-id="c86e7-110">*互動式視窗工作站* 是唯一可以顯示使用者介面或接收使用者輸入的視窗站。</span><span class="sxs-lookup"><span data-stu-id="c86e7-110">The *interactive window station* is the only window station that can display a user interface or receive user input.</span></span> <span data-ttu-id="c86e7-111">它會指派給互動式使用者的登入會話，並包含鍵盤、滑鼠和顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="c86e7-111">It is assigned to the logon session of the interactive user, and contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="c86e7-112">它一律命名為 "WinSta0"。</span><span class="sxs-lookup"><span data-stu-id="c86e7-112">It is always named "WinSta0".</span></span> <span data-ttu-id="c86e7-113">所有其他視窗工作站都是非互動式的，這表示它們無法顯示使用者介面或接收使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="c86e7-113">All other window stations are noninteractive, which means they cannot display a user interface or receive user input.</span></span>

<span data-ttu-id="c86e7-114">當使用者使用遠端桌面服務登入電腦時，就會啟動使用者的會話。</span><span class="sxs-lookup"><span data-stu-id="c86e7-114">When a user logs on to a computer using Remote Desktop Services, a session is started for the user.</span></span> <span data-ttu-id="c86e7-115">每個會話都與其本身的互動式視窗工作站（名為 "WinSta0"）相關聯。</span><span class="sxs-lookup"><span data-stu-id="c86e7-115">Each session is associated with its own interactive window station named "WinSta0".</span></span> <span data-ttu-id="c86e7-116">如需詳細資訊，請參閱 [遠端桌面會話](/windows/desktop/TermServ/terminal-services-sessions)。</span><span class="sxs-lookup"><span data-stu-id="c86e7-116">For more information, see [Remote Desktop Sessions](/windows/desktop/TermServ/terminal-services-sessions).</span></span>

<span data-ttu-id="c86e7-117">如需視窗工作站的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="c86e7-117">For more information on window stations, see the following topics:</span></span>

-   [<span data-ttu-id="c86e7-118">視窗工作站和桌面建立</span><span class="sxs-lookup"><span data-stu-id="c86e7-118">Window Station and Desktop Creation</span></span>](window-station-and-desktop-creation.md)
-   [<span data-ttu-id="c86e7-119">處理與視窗工作站的連接</span><span class="sxs-lookup"><span data-stu-id="c86e7-119">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
-   [<span data-ttu-id="c86e7-120">Windows 工作站安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="c86e7-120">Window Station Security and Access Rights</span></span>](window-station-security-and-access-rights.md)

 

 