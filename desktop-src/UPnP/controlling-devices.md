---
title: 控制裝置
description: 以 UPnP 為基礎的裝置是由其公開的服務所控制。
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a72a4ffdf91bca358124dbb0a0d95ff9a61e30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840532"
---
# <a name="controlling-devices"></a><span data-ttu-id="5d882-103">控制裝置</span><span class="sxs-lookup"><span data-stu-id="5d882-103">Controlling Devices</span></span>

<span data-ttu-id="5d882-104">以 UPnP 為基礎的裝置是由其公開的服務所控制。</span><span class="sxs-lookup"><span data-stu-id="5d882-104">UPnP-based devices are controlled by the services they expose.</span></span> <span data-ttu-id="5d882-105">UPnP 服務是 UPnP 架構中最小的可控制實體。</span><span class="sxs-lookup"><span data-stu-id="5d882-105">A UPnP service is the smallest controllable entity in the UPnP architecture.</span></span> <span data-ttu-id="5d882-106">裝置會針對其執行的每個主要功能公開一個服務。</span><span class="sxs-lookup"><span data-stu-id="5d882-106">Devices expose one service for each primary function they perform.</span></span> <span data-ttu-id="5d882-107">複雜裝置通常是由數個簡單的服務和其他裝置所組成。</span><span class="sxs-lookup"><span data-stu-id="5d882-107">Complex devices are typically composed of several simple services and other devices.</span></span>

<span data-ttu-id="5d882-108">服務包含一組狀態變數和一組動作，可讓應用程式在這些狀態變數上運作。</span><span class="sxs-lookup"><span data-stu-id="5d882-108">A service consists of a set of state variables and a set of actions an application can invoke that operate on those state variables.</span></span> <span data-ttu-id="5d882-109">在具有 UPnP 技術的控制點 API 中，服務會以公開 [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)介面的 **服務** 物件來表示。</span><span class="sxs-lookup"><span data-stu-id="5d882-109">In the Control Point API with UPnP technology, services are represented by **Service** objects that expose the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface.</span></span>

<span data-ttu-id="5d882-110">服務類型會定義特定服務所支援的狀態變數和動作。</span><span class="sxs-lookup"><span data-stu-id="5d882-110">A service type defines the state variables and actions supported by a particular service.</span></span> <span data-ttu-id="5d882-111">例如，時鐘服務的服務類型會定義 **GetTime** 和 **SetTime** 動作，以及 **時間** 狀態變數。</span><span class="sxs-lookup"><span data-stu-id="5d882-111">For example, the service type for a clock service defines **GetTime** and **SetTime** actions, along with a **Time** state variable.</span></span>

<span data-ttu-id="5d882-112">服務識別碼會區分單一裝置內的多個常見服務類型。</span><span class="sxs-lookup"><span data-stu-id="5d882-112">A service ID differentiates multiple common service types within a single device.</span></span> <span data-ttu-id="5d882-113">例如，警示時鐘中可以有兩個時鐘服務，一個用於正常時鐘，另一個用於警示。</span><span class="sxs-lookup"><span data-stu-id="5d882-113">For example, there can be two clock services in an alarm clock, one for the regular clock and the other for the alarm.</span></span> <span data-ttu-id="5d882-114">需要有一種方式來區別兩個具有相同服務類型的服務。</span><span class="sxs-lookup"><span data-stu-id="5d882-114">There needs to be a way to differentiate between the two services, which have identical service types.</span></span> <span data-ttu-id="5d882-115">服務識別碼提供唯一的方法來識別服務類型的實例。</span><span class="sxs-lookup"><span data-stu-id="5d882-115">The service ID provides a unique way of identifying an instance of a service type.</span></span> <span data-ttu-id="5d882-116">然後，此服務識別碼會用來從 [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) 集合存取正確的服務，因為服務類型不是唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d882-116">Then, this service ID is used to access the correct service from the [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) collection, because service type is not a unique identifier.</span></span> <span data-ttu-id="5d882-117">[**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)介面也可讓應用程式向服務物件註冊回呼函數。</span><span class="sxs-lookup"><span data-stu-id="5d882-117">The [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface also allows applications to register a callback function with the service object.</span></span> <span data-ttu-id="5d882-118">當服務的狀態變數值變更時，服務物件會叫用已註冊的回呼，以通知應用程式變更。</span><span class="sxs-lookup"><span data-stu-id="5d882-118">When the value of a service's state variable changes, the service object invokes the registered callback to notify the application of the change.</span></span> <span data-ttu-id="5d882-119">UPnP 架構也會叫用此回呼，以在服務實例變成無法使用時通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="5d882-119">The UPnP framework also invokes this callback to notify applications when a service instance has become unavailable.</span></span> <span data-ttu-id="5d882-120">服務可能因各種原因而變成無法使用，包括暫時性的網路失敗。</span><span class="sxs-lookup"><span data-stu-id="5d882-120">The service can become unavailable for a variety of reasons, including transient network failure.</span></span>

<span data-ttu-id="5d882-121">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="5d882-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="5d882-122">取得服務物件</span><span class="sxs-lookup"><span data-stu-id="5d882-122">Obtaining Service Objects</span></span>](obtaining-service-objects.md)
-   [<span data-ttu-id="5d882-123">註冊回呼</span><span class="sxs-lookup"><span data-stu-id="5d882-123">Registering a Callback</span></span>](registering-a-callback.md)
-   [<span data-ttu-id="5d882-124">查詢狀態變數</span><span class="sxs-lookup"><span data-stu-id="5d882-124">Querying State Variables</span></span>](querying-state-variables.md)
-   [<span data-ttu-id="5d882-125">叫用動作</span><span class="sxs-lookup"><span data-stu-id="5d882-125">Invoking Actions</span></span>](invoking-actions.md)

 

 




