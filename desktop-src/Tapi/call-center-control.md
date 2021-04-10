---
description: 您可以使用基本的 TAPI 2.2 來管理電話中心以及電話語音網路基礎結構 (的其他元素，例如透過協力廠商呼叫控制) 的 IVR 和語音信箱伺服器。
ms.assetid: e920dc4a-adb4-4a36-ac04-f265538531eb
title: 撥置中心控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4200ff434249856507109915f41f7f1479eddfd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850812"
---
# <a name="call-center-control"></a><span data-ttu-id="9fad0-103">撥置中心控制項</span><span class="sxs-lookup"><span data-stu-id="9fad0-103">Call Center Control</span></span>

<span data-ttu-id="9fad0-104">您可以使用基本的 TAPI 2.2 來管理電話中心以及電話語音網路基礎結構 (的其他元素，例如透過協力廠商呼叫控制) 的 IVR 和語音信箱伺服器。</span><span class="sxs-lookup"><span data-stu-id="9fad0-104">Basic TAPI 2.2 can be used to manage call centers and other elements of Telephony network infrastructure (such as IVR and voice mail servers) through third-party call control.</span></span> <span data-ttu-id="9fad0-105">為了協助建立將在伺服器上執行的 ACD proxy，已將功能新增至 TAPI 2.2，以提供應用程式開發人員額外的協助。</span><span class="sxs-lookup"><span data-stu-id="9fad0-105">To help create ACD proxies that will run on servers, functions have been added to TAPI 2.2 to provide additional assistance to application developers.</span></span>

<span data-ttu-id="9fad0-106">下列主題說明您可以用來執行電話中心控制項的 TAPI 2.2 功能：</span><span class="sxs-lookup"><span data-stu-id="9fad0-106">The following topics describe the TAPI 2.2 features that you can use to implement call center controls:</span></span>

-   [<span data-ttu-id="9fad0-107">撥打電話中心的模型</span><span class="sxs-lookup"><span data-stu-id="9fad0-107">Modeling of a Call Center</span></span>](modeling-of-a-call-center.md)
-   [<span data-ttu-id="9fad0-108">站</span><span class="sxs-lookup"><span data-stu-id="9fad0-108">Stations</span></span>](stations.md)
-   [<span data-ttu-id="9fad0-109">預測撥號</span><span class="sxs-lookup"><span data-stu-id="9fad0-109">Predictive Dialing</span></span>](predictive-dialing.md)
-   [<span data-ttu-id="9fad0-110">呼叫佇列和路由點</span><span class="sxs-lookup"><span data-stu-id="9fad0-110">Call Queues and Route Points</span></span>](call-queues-and-route-points.md)
-   [<span data-ttu-id="9fad0-111">ACD 代理程式監視和控制</span><span class="sxs-lookup"><span data-stu-id="9fad0-111">ACD Agent Monitoring and Control</span></span>](acd-agent-monitoring-and-control.md)
-   [<span data-ttu-id="9fad0-112">站狀態控制</span><span class="sxs-lookup"><span data-stu-id="9fad0-112">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="9fad0-113">站狀態控制</span><span class="sxs-lookup"><span data-stu-id="9fad0-113">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="9fad0-114">撥號狀態計時器</span><span class="sxs-lookup"><span data-stu-id="9fad0-114">Call State Timer</span></span>](call-state-timer.md)
-   [<span data-ttu-id="9fad0-115">媒體事件計時器</span><span class="sxs-lookup"><span data-stu-id="9fad0-115">Media Event Timers</span></span>](media-event-timers.md)

<span data-ttu-id="9fad0-116">TAPI 3.x 是撰寫 ACD 代理程式應用程式的慣用 API。</span><span class="sxs-lookup"><span data-stu-id="9fad0-116">TAPI 3.x is the preferred API of writing ACD Agent applications.</span></span> <span data-ttu-id="9fad0-117">如需有關使用這些介面和方法的詳細資訊，請參閱「 [撥置中心控制項](./about-call-center-controls.md) 」一節。</span><span class="sxs-lookup"><span data-stu-id="9fad0-117">Please see the [Call Center Controls](./about-call-center-controls.md) section for information on using these interfaces and methods.</span></span> <span data-ttu-id="9fad0-118">不過，如有需要，TAPI 2.2 仍可供完整的 ACD 應用程式套件使用。</span><span class="sxs-lookup"><span data-stu-id="9fad0-118">However, TAPI 2.2 remains usable for full ACD application suites if desired.</span></span>

 

 
