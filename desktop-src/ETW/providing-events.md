---
description: 提供者是包含事件追蹤檢測的應用程式。
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: 提供事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972189"
---
# <a name="providing-events"></a><span data-ttu-id="0abde-103">提供事件</span><span class="sxs-lookup"><span data-stu-id="0abde-103">Providing Events</span></span>

<span data-ttu-id="0abde-104">提供者是包含事件追蹤檢測的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0abde-104">Providers are applications that contain event tracing instrumentation.</span></span> <span data-ttu-id="0abde-105">在提供者註冊本身之後，控制器就可以在提供者中啟用或停用事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="0abde-105">After a provider registers itself, a controller can then enable or disable event tracing in the provider.</span></span> <span data-ttu-id="0abde-106">提供者會定義要啟用或停用的解釋。</span><span class="sxs-lookup"><span data-stu-id="0abde-106">The provider defines its interpretation of being enabled or disabled.</span></span> <span data-ttu-id="0abde-107">一般而言，啟用的提供者會產生事件，而停用的提供者則不會產生事件。</span><span class="sxs-lookup"><span data-stu-id="0abde-107">Generally, an enabled provider generates events, and a disabled provider does not.</span></span> <span data-ttu-id="0abde-108">這可讓您在應用程式中新增事件追蹤，而不需要每次都產生事件。</span><span class="sxs-lookup"><span data-stu-id="0abde-108">This lets you add event tracing to your application without requiring that it generate events all the time.</span></span>

<span data-ttu-id="0abde-109">本節說明如何：</span><span class="sxs-lookup"><span data-stu-id="0abde-109">This section shows you how to:</span></span>

-   [<span data-ttu-id="0abde-110">寫入事件</span><span class="sxs-lookup"><span data-stu-id="0abde-110">Write events</span></span>](writing-events.md)
-   [<span data-ttu-id="0abde-111">寫入相關事件</span><span class="sxs-lookup"><span data-stu-id="0abde-111">Write related events</span></span>](writing-related-events-in-an-end-to-end-scenario.md)
-   [<span data-ttu-id="0abde-112">發佈您的事件架構以與取用者共用</span><span class="sxs-lookup"><span data-stu-id="0abde-112">Publish your event schema to share with consumers</span></span>](publishing-your-event-schema.md)

<span data-ttu-id="0abde-113">如需控制事件追蹤會話的詳細資訊，請參閱 [控制事件追蹤會話](controlling-event-tracing-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="0abde-113">For information about controlling event tracing sessions, see [Controlling Event Tracing Sessions](controlling-event-tracing-sessions.md).</span></span> <span data-ttu-id="0abde-114">如需從事件追蹤提供者取用事件的詳細資訊，請參閱 [使用事件](consuming-events.md)。</span><span class="sxs-lookup"><span data-stu-id="0abde-114">For information about consuming events from an event trace provider, see [Consuming Events](consuming-events.md).</span></span>

 

 



