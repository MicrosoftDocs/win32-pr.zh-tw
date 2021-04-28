---
description: 將沒有回應的服務降至最低的最佳作法
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: 將沒有回應的服務降至最低的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90416e8256383e16fd78c436dfaa8d6a2186c540
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087996"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="90bab-103">將沒有回應的服務降至最低的最佳作法</span><span class="sxs-lookup"><span data-stu-id="90bab-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="90bab-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="90bab-104">Affected Platform</span></span>

 <span data-ttu-id="90bab-105">**用戶端** -windows Vista \| windows 7</span><span class="sxs-lookup"><span data-stu-id="90bab-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="90bab-106">Description</span><span class="sxs-lookup"><span data-stu-id="90bab-106">Description</span></span>

<span data-ttu-id="90bab-107">沒有回應的服務可能會導致超時、終止會話，甚至遺失資料。</span><span class="sxs-lookup"><span data-stu-id="90bab-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="90bab-108">採用最佳作法可大幅減少沒有回應的服務發生。</span><span class="sxs-lookup"><span data-stu-id="90bab-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="90bab-109">最佳做法</span><span class="sxs-lookup"><span data-stu-id="90bab-109">Best Practices</span></span>

<span data-ttu-id="90bab-110">請確定您的應用程式及其所有相依的服務和驅動程式都會回應系統電源和關機通知。</span><span class="sxs-lookup"><span data-stu-id="90bab-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="90bab-111">所有應用程式都應該立即和適當地回應，以關閉指出正在進行關機的訊息，例如 WM \_ QUERYENDSESSION 和 wm \_ ENDSESSION。</span><span class="sxs-lookup"><span data-stu-id="90bab-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="90bab-112">所有服務都應該立即回應 SCM 關機通知。</span><span class="sxs-lookup"><span data-stu-id="90bab-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="90bab-113">如果無法這麼做，電腦會將它們視為沒有回應，並起始20秒的時間，並將其停止，以開啟遺失資料的可能性。</span><span class="sxs-lookup"><span data-stu-id="90bab-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="90bab-114">這也增加了20秒的時間，關閉電腦關機的關機時間。</span><span class="sxs-lookup"><span data-stu-id="90bab-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="90bab-115">具有核心設備磁碟機相依性的所有服務都應該立即和適當地回應，以 \_ \_ 在其 DispatchShutdown 常式中 IRP MJ 關閉通知。</span><span class="sxs-lookup"><span data-stu-id="90bab-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="90bab-116">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="90bab-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="90bab-117">Windows Performance Toolkit</span><span class="sxs-lookup"><span data-stu-id="90bab-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



