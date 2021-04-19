---
description: 本節中的 WMI 應用程式範例是以 c + + 撰寫。
ms.assetid: 5c4c4c4c-adbc-4702-a6fe-5f98a6db3ba1
ms.tgt_platform: multiple
title: WMI c + + 應用程式範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883b51bd00de5e3938fef8467c68d299ac60683a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974376"
---
# <a name="wmi-c-application-examples"></a><span data-ttu-id="08946-103">WMI c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="08946-103">WMI C++ Application Examples</span></span>

<span data-ttu-id="08946-104">本節中的 WMI 應用程式範例是以 c + + 撰寫。</span><span class="sxs-lookup"><span data-stu-id="08946-104">The WMI application examples in this section are written in C++.</span></span> <span data-ttu-id="08946-105">它們示範可以使用 WMI 元件完成的各種工作，並提供使用 Visual Basic 腳本的替代方案。</span><span class="sxs-lookup"><span data-stu-id="08946-105">They demonstrate a range of tasks that can be completed using WMI components and offer an alternative over using Visual Basic scripts.</span></span> <span data-ttu-id="08946-106">每個應用程式會以類似的方式分成一系列的步驟，讓來自不同範例的程式碼區段可以輕鬆地結合以形成自訂應用程式。</span><span class="sxs-lookup"><span data-stu-id="08946-106">Each application is separated into a series of steps in a similar way so that code sections from different examples can easily be combined to form customized applications.</span></span>

<span data-ttu-id="08946-107">下表列出本節中的 c + + 範例。</span><span class="sxs-lookup"><span data-stu-id="08946-107">The following table lists the C++ examples in this section.</span></span>



| <span data-ttu-id="08946-108">範例</span><span class="sxs-lookup"><span data-stu-id="08946-108">Example</span></span>                                                                                                                                  | <span data-ttu-id="08946-109">描述</span><span class="sxs-lookup"><span data-stu-id="08946-109">Description</span></span>                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08946-110">範例：從本機電腦取得 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="08946-110">Example: Getting WMI Data from the Local Computer</span></span>](example--getting-wmi-data-from-the-local-computer.md)                               | <span data-ttu-id="08946-111">此範例會連接到本機電腦上的 WMI 命名空間，並從本機電腦上的查詢取得資料。</span><span class="sxs-lookup"><span data-stu-id="08946-111">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="08946-112">半同步方式會收集資料。</span><span class="sxs-lookup"><span data-stu-id="08946-112">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="08946-113">範例：以非同步方式從本機電腦取得 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="08946-113">Example: Getting WMI Data from the Local Computer Asynchronously</span></span>](example--getting-wmi-data-from-the-local-computer-asynchronously.md) | <span data-ttu-id="08946-114">此範例會連接到本機電腦上的 WMI 命名空間，並從本機電腦上的查詢取得資料。</span><span class="sxs-lookup"><span data-stu-id="08946-114">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="08946-115">資料會以非同步方式收集。</span><span class="sxs-lookup"><span data-stu-id="08946-115">The data is gathered asynchronously.</span></span>    |
| [<span data-ttu-id="08946-116">範例：從遠端電腦取得 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="08946-116">Example: Getting WMI Data from a Remote Computer</span></span>](example--getting-wmi-data-from-a-remote-computer.md)                                 | <span data-ttu-id="08946-117">此範例會連接到遠端電腦上的 WMI 命名空間，並從遠端電腦上的查詢取得資料。</span><span class="sxs-lookup"><span data-stu-id="08946-117">This example connects to the WMI namespace on a remote computer and gets data from a query on the remote computer.</span></span> <span data-ttu-id="08946-118">半同步方式會收集資料。</span><span class="sxs-lookup"><span data-stu-id="08946-118">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="08946-119">範例：呼叫提供者方法</span><span class="sxs-lookup"><span data-stu-id="08946-119">Example: Calling a Provider Method</span></span>](example--calling-a-provider-method.md)                                                             | <span data-ttu-id="08946-120">此範例會連接到本機電腦上的 WMI 命名空間，並在 WMI 中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="08946-120">This example connects to the WMI namespace on the local computer and calls a method in WMI.</span></span> <span data-ttu-id="08946-121">方法會以同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="08946-121">The method is executed synchronously.</span></span>                          |
| [<span data-ttu-id="08946-122">範例：透過 WMI 接收事件通知</span><span class="sxs-lookup"><span data-stu-id="08946-122">Example: Receiving Event Notifications Through WMI</span></span>](example--receiving-event-notifications-through-wmi-.md)                            | <span data-ttu-id="08946-123">此範例會連接到本機電腦上的 WMI 命名空間，並接收來自本機電腦的事件。</span><span class="sxs-lookup"><span data-stu-id="08946-123">This example connects to the WMI namespace on the local computer and receives an event from the local computer.</span></span> <span data-ttu-id="08946-124">半同步方式收到事件。</span><span class="sxs-lookup"><span data-stu-id="08946-124">The event is received semisynchronously.</span></span>   |



 

 

 



