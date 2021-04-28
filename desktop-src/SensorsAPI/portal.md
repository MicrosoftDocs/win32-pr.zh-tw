---
description: 感應器 API
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: 感應器 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a36259910fb7583c91b695f69066aa2abf9be1e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118406"
---
# <a name="sensor-api"></a><span data-ttu-id="bb82b-103">感應器 API</span><span class="sxs-lookup"><span data-stu-id="bb82b-103">Sensor API</span></span>

## <a name="purpose"></a><span data-ttu-id="bb82b-104">目的</span><span class="sxs-lookup"><span data-stu-id="bb82b-104">Purpose</span></span>

<span data-ttu-id="bb82b-105">Windows 7 包括感應器的原生支援，也就是可以測量實體現象（例如溫度或地點）的裝置。</span><span class="sxs-lookup"><span data-stu-id="bb82b-105">Windows 7 includes native support for sensors, which are devices that can measure physical phenomena such as temperature or location.</span></span> <span data-ttu-id="bb82b-106">本檔說明感應器 API，可讓應用程式以標準化的方式從感應器取得及使用資料。</span><span class="sxs-lookup"><span data-stu-id="bb82b-106">This documentation describes the Sensor API, which enables applications to get and use data from sensors in a standardized way.</span></span>

<span data-ttu-id="bb82b-107">就像人一樣，我們會依賴我們的做法，為我們提供有關我們的世界資訊。</span><span class="sxs-lookup"><span data-stu-id="bb82b-107">As humans, we rely on our senses to provide us with information about the world around us.</span></span> <span data-ttu-id="bb82b-108">當我們建立電腦以進行某些工作時，我們會新增感應器機制，讓機器可以適當地回應變更的狀況。</span><span class="sxs-lookup"><span data-stu-id="bb82b-108">When we create machines to take on some of our work, we add sensor mechanisms so the machines can respond appropriately to changing conditions.</span></span>

<span data-ttu-id="bb82b-109">例如，汽車引擎通常會使用各種不同的感應器。</span><span class="sxs-lookup"><span data-stu-id="bb82b-109">For example, automobile engines typically use a variety of sensors.</span></span> <span data-ttu-id="bb82b-110">這些感應器會由上線的電腦監視，以持續調整設定，例如引擎時間，以最大化電源和效率。</span><span class="sxs-lookup"><span data-stu-id="bb82b-110">These sensors are monitored by an onboard computer that continuously adjusts settings, such as engine timing, to maximize power and efficiency.</span></span> <span data-ttu-id="bb82b-111">電視可能會使用環境光線感應器來調整圖片的亮度，以符合變更房間的情況。</span><span class="sxs-lookup"><span data-stu-id="bb82b-111">A television may use an ambient light sensor to adjust the brightness of the picture to match changing room conditions.</span></span> <span data-ttu-id="bb82b-112">即使是簡單的門鈴按鈕，也能作為基本感應器來偵測門上的人類存在。</span><span class="sxs-lookup"><span data-stu-id="bb82b-112">Even something as simple as a doorbell button acts as a rudimentary sensor to detect a human presence at the door.</span></span>

<span data-ttu-id="bb82b-113">雖然純粹的機械門鈴能滿足其目的，但是複雜感應器提供的資訊在結合軟體時變得更強大。</span><span class="sxs-lookup"><span data-stu-id="bb82b-113">While the purely mechanical doorbell fulfills its purpose, the information provided by complex sensors becomes far more powerful when it is combined with software.</span></span> <span data-ttu-id="bb82b-114">新式感應器可非常快速地提供大量資料，而且採用各種不同的格式，因此軟體會提供自然的機制來讓感應器資料發揮意義。</span><span class="sxs-lookup"><span data-stu-id="bb82b-114">Modern sensors can provide a lot of data very quickly, and in a variety of formats, so software provides a natural mechanism for making sense of sensor data.</span></span>

<span data-ttu-id="bb82b-115">現今，軟體發展人員可以撰寫使用感應器的程式，但缺乏標準化會讓感應器進行程式設計棘手工作。</span><span class="sxs-lookup"><span data-stu-id="bb82b-115">Today, software developers can write programs that use sensors, but a lack of standardization makes programming for sensors an arduous task.</span></span> <span data-ttu-id="bb82b-116">以感應器為基礎的程式完成後，通常會永遠相依于特定類型的硬體。</span><span class="sxs-lookup"><span data-stu-id="bb82b-116">After a sensor-based program is completed, it is usually forever dependent on a particular type of hardware.</span></span> <span data-ttu-id="bb82b-117">使用一或多個垂直解決方案來啟用以軟體為基礎的系統部署，會限制感應器與電腦硬體的整合，到目前為止，Windows 電腦都沒有例外。</span><span class="sxs-lookup"><span data-stu-id="bb82b-117">Using one or more vertical solutions to enable deployment of a software-based system has limited the integration of sensors with computer hardware and, until now, Windows-based computers have been no exception.</span></span>

<span data-ttu-id="bb82b-118">Windows 7 包含對感應器的原生支援，並透過新的開發平臺（包括定位感應器，例如 GPS 裝置）擴充。</span><span class="sxs-lookup"><span data-stu-id="bb82b-118">Windows 7 includes native support for sensors, expanded by a new development platform for working with sensors, including location sensors, such as GPS devices.</span></span> <span data-ttu-id="bb82b-119">Windows 感應器和位置平台提供了一種標準方式，讓裝置製造商向軟體發展人員和取用者公開感應器裝置，同時為開發人員提供標準化的應用程式開發介面， (API) 來處理感應器和感應器資料。</span><span class="sxs-lookup"><span data-stu-id="bb82b-119">The Windows Sensor and Location platform provides a standard way for device manufacturers to expose sensor devices to software developers and consumers, while providing developers with a standardized application programming interface (API) for working with sensors and sensor data.</span></span>

<span data-ttu-id="bb82b-120">感應器是可測量實體現象、提供描述性資料，或提供實體物件或環境狀態相關資訊的裝置或機制。</span><span class="sxs-lookup"><span data-stu-id="bb82b-120">Sensors are devices or mechanisms that can measure physical phenomena, provide descriptive data, or provide information about the state of a physical object or environment.</span></span> <span data-ttu-id="bb82b-121">電腦可以利用內建的感應器、透過有線或無線連線連線的感應器，或是透過網路或網際網路提供資料的感應器。</span><span class="sxs-lookup"><span data-stu-id="bb82b-121">Computers can make use of built-in sensors, sensors that are connected through wired or wireless connections, or sensors that provide data through a network or the Internet.</span></span>

<span data-ttu-id="bb82b-122">感應器 API 提供以程式設計方式存取感應器所提供資料的標準方式。</span><span class="sxs-lookup"><span data-stu-id="bb82b-122">The Sensor API provides a standard way to programmatically access data that sensors provide.</span></span> <span data-ttu-id="bb82b-123">感應器 API 會標準化：</span><span class="sxs-lookup"><span data-stu-id="bb82b-123">The Sensor API standardizes:</span></span>

-   <span data-ttu-id="bb82b-124">感應器類別、類型和屬性。</span><span class="sxs-lookup"><span data-stu-id="bb82b-124">Sensor categories, types, and properties.</span></span>
-   <span data-ttu-id="bb82b-125">標準感應器類型的資料格式。</span><span class="sxs-lookup"><span data-stu-id="bb82b-125">Data formats for standard sensor types.</span></span>
-   <span data-ttu-id="bb82b-126">用於處理感應器和感應器集合的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="bb82b-126">COM interfaces for working with sensors and collections of sensors.</span></span>
-   <span data-ttu-id="bb82b-127">非同步接收感應器資料的事件機制。</span><span class="sxs-lookup"><span data-stu-id="bb82b-127">Event mechanisms for asynchronously receiving sensor data.</span></span>

<span data-ttu-id="bb82b-128">感應器 API 也可讓您定義自訂的感應器類別、類型、屬性、資料格式和事件。</span><span class="sxs-lookup"><span data-stu-id="bb82b-128">The Sensor API also enables you to define custom sensor categories, types, properties, data formats, and events.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bb82b-129">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="bb82b-129">Developer audience</span></span>

<span data-ttu-id="bb82b-130">感應器 API 會透過一組 COM 介面提供其功能。</span><span class="sxs-lookup"><span data-stu-id="bb82b-130">The Sensor API provides its functionality through a set of COM interfaces.</span></span> <span data-ttu-id="bb82b-131">本檔假設您有使用 c + + 程式設計語言進行程式設計的實用知識，而且您對如何使用 COM 物件和介面具有基本的瞭解。</span><span class="sxs-lookup"><span data-stu-id="bb82b-131">This documentation assumes that you have a working knowledge of programming using the C++ programming language, and you have a basic understanding of how to use COM objects and interfaces.</span></span> <span data-ttu-id="bb82b-132">為了求簡潔，本檔中的許多程式碼範例 (以及程式碼範例中) 使用 Active Template Library (ATL) 物件來執行 COM 功能。</span><span class="sxs-lookup"><span data-stu-id="bb82b-132">For the sake of brevity, many code examples in this documentation (as well as in the code samples) use Active Template Library (ATL) objects to implement COM functionality.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bb82b-133">本節內容</span><span class="sxs-lookup"><span data-stu-id="bb82b-133">In this section</span></span>

-   [<span data-ttu-id="bb82b-134">快速入門</span><span class="sxs-lookup"><span data-stu-id="bb82b-134">Getting Started</span></span>](getting-started.md)
-   [<span data-ttu-id="bb82b-135">關於感應器 API</span><span class="sxs-lookup"><span data-stu-id="bb82b-135">About the Sensor API</span></span>](about-the-sensor-api.md)
-   [<span data-ttu-id="bb82b-136">感應器 API 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="bb82b-136">Sensor API Programming Guide</span></span>](sensor-api-programming-guide.md)
-   [<span data-ttu-id="bb82b-137">感應器 API 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="bb82b-137">Sensor API Programming Reference</span></span>](sensor-api-programming-reference.md)

 

 



