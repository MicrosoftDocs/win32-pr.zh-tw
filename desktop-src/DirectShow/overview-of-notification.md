---
description: 事件通知總覽
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: 事件通知總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687960"
---
# <a name="overview-of-event-notification"></a><span data-ttu-id="bce2e-103">事件通知總覽</span><span class="sxs-lookup"><span data-stu-id="bce2e-103">Overview of Event Notification</span></span>

<span data-ttu-id="bce2e-104">篩選會透過張貼事件通知，通知篩選圖形管理員有關事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="bce2e-104">A filter notifies the Filter Graph Manager about an event by posting an event notification.</span></span> <span data-ttu-id="bce2e-105">事件可能是預期的內容，例如資料流程的結尾，或可能代表錯誤，例如轉譯資料流程失敗。</span><span class="sxs-lookup"><span data-stu-id="bce2e-105">The event could be something expected, such as the end of a stream, or it could represent an error, such as a failure to render a stream.</span></span> <span data-ttu-id="bce2e-106">篩選圖形管理員本身會處理一些篩選事件，並讓應用程式的其他事件保持處理。</span><span class="sxs-lookup"><span data-stu-id="bce2e-106">The Filter Graph Manager handles some filter events by itself, and it leaves others for the application to handle.</span></span> <span data-ttu-id="bce2e-107">如果篩選圖形管理員沒有處理篩選事件，它會將事件通知放入佇列中。</span><span class="sxs-lookup"><span data-stu-id="bce2e-107">If the Filter Graph Manager does not handle a filter event, it places the event notification into a queue.</span></span> <span data-ttu-id="bce2e-108">篩選圖形也可以將應用程式的事件通知排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="bce2e-108">The filter graph can also queue its own event notifications for the application.</span></span>

<span data-ttu-id="bce2e-109">應用程式會從佇列抓取事件，並根據事件種類來回應事件。</span><span class="sxs-lookup"><span data-stu-id="bce2e-109">An application retrieves events from the queue and responds to them based on the type of event.</span></span> <span data-ttu-id="bce2e-110">因此，DirectShow 中的事件通知與 Microsoft Windows 訊息佇列配置類似。</span><span class="sxs-lookup"><span data-stu-id="bce2e-110">Event notification in DirectShow is therefore similar to the Microsoft Windows message queuing scheme.</span></span> <span data-ttu-id="bce2e-111">應用程式也可以針對指定的事件種類，取消篩選圖形管理員的預設行為。</span><span class="sxs-lookup"><span data-stu-id="bce2e-111">An application can also cancel the Filter Graph Manager's default behavior for a given event type.</span></span> <span data-ttu-id="bce2e-112">篩選圖形管理員接著會將這些事件直接放入佇列中，以便讓應用程式處理。</span><span class="sxs-lookup"><span data-stu-id="bce2e-112">The Filter Graph Manager then puts those events directly into the queue for the application to handle.</span></span>

<span data-ttu-id="bce2e-113">這種機制可讓</span><span class="sxs-lookup"><span data-stu-id="bce2e-113">This mechanism enables</span></span>

-   <span data-ttu-id="bce2e-114">用來與應用程式通訊的篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="bce2e-114">The Filter Graph Manager to communicate with the application.</span></span>
-   <span data-ttu-id="bce2e-115">篩選器可與應用程式和篩選器圖形管理員進行通訊。</span><span class="sxs-lookup"><span data-stu-id="bce2e-115">Filters to communicate with both the application and the Filter Graph Manager.</span></span>
-   <span data-ttu-id="bce2e-116">判斷其對處理事件之介入程度的應用程式。</span><span class="sxs-lookup"><span data-stu-id="bce2e-116">The application to determine its degree of involvement in handling events.</span></span>

 

 



