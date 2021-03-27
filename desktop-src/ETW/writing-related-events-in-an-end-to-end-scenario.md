---
description: ETW 提供從多個元件群組相關事件的方法。
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: 在端對端案例中撰寫相關事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972256"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a><span data-ttu-id="7ad2d-103">在端對端案例中撰寫相關事件</span><span class="sxs-lookup"><span data-stu-id="7ad2d-103">Writing Related Events in an End-to-End Scenario</span></span>

<span data-ttu-id="7ad2d-104">ETW 提供從多個元件群組相關事件的方法。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-104">ETW provides a way to group related events from more than one component.</span></span> <span data-ttu-id="7ad2d-105">例如，如果有數個元件 (在同一部電腦或不同的電腦上) 牽涉到處理相同的資料，而且每個元件都會記錄活動部分的事件，您可以將所有相關事件群組在一起。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-105">For example, if several components (either on the same computer or on different computers) are involved in processing the same data, and each component logs events for their portion of the activity, you can group all of the related events together.</span></span> <span data-ttu-id="7ad2d-106">這可讓取用者從進程開始到進程結束時取用所有的事件。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-106">This will allow a consumer to consume all of the events, from the beginning of the process to the end of the process.</span></span>

<span data-ttu-id="7ad2d-107">若要在以 [資訊清單為基礎](about-event-tracing.md) 的提供者中寫入相關事件，請參閱 [在以資訊清單為基礎的提供者中撰寫相關事件](writing-related-events-in-a-manifest-base-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-107">To write related events in a [manifest-based](about-event-tracing.md) provider, see [Writing Related Events in a Manifest-based Provider](writing-related-events-in-a-manifest-base-provider.md).</span></span>

<span data-ttu-id="7ad2d-108">若要在 [傳統](about-event-tracing.md) 提供者中寫入相關的事件，請參閱 [在傳統提供者中撰寫相關的事件](tracing-event-instances.md)。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-108">To write related events in a [classic](about-event-tracing.md) provider, see [Writing Related Events in a Classic Provider](tracing-event-instances.md).</span></span>

 

 



