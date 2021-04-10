---
description: 感應器 API 可以提供事件通知。
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: 關於感應器 API 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851504"
---
# <a name="about-sensor-api-events"></a><span data-ttu-id="9c8b4-103">關於感應器 API 事件</span><span class="sxs-lookup"><span data-stu-id="9c8b4-103">About Sensor API Events</span></span>

<span data-ttu-id="9c8b4-104">感應器 API 可以提供事件通知。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-104">The Sensor API can provide event notifications.</span></span>

<span data-ttu-id="9c8b4-105">當您透過 [**ISensor：： SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) 或 [**ISensorManager：： SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)註冊來接收事件時，您必須提供回呼介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-105">When you register to receive events, through either [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) or [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), you must provide a pointer to a callback interface.</span></span> <span data-ttu-id="9c8b4-106">您必須在程式碼中執行回呼介面的方法。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-106">You must implement the methods of the callback interface in your code.</span></span> <span data-ttu-id="9c8b4-107">感應器 API 會定義下列回呼介面：</span><span class="sxs-lookup"><span data-stu-id="9c8b4-107">The Sensor API defines the following callback interfaces:</span></span>

-   <span data-ttu-id="9c8b4-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="9c8b4-109">執行此介面以接收來自感應器的事件。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-109">Implement this interface to receive events from sensors.</span></span> <span data-ttu-id="9c8b4-110">感應器可以通知應用程式有關新資料、感應器狀態變更、感應器中斷連線，以及由感應器製造商定義的自訂事件。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-110">Sensors can notify your application about new data, changes in sensor state, sensor disconnection, and custom events defined by the sensor manufacturer.</span></span>
-   <span data-ttu-id="9c8b4-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents)。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span> <span data-ttu-id="9c8b4-112">執行此介面以接收來自感應器管理員的事件。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-112">Implement this interface to receive events from the sensor manager.</span></span> <span data-ttu-id="9c8b4-113">感應器管理員可以在感應器連線時通知您的應用程式，因此可能會可供使用。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-113">The sensor manager can notify your application when a sensor connects, and therefore may be available for use.</span></span>

<span data-ttu-id="9c8b4-114">您可以再次呼叫 [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) 來取消事件通知，這次會透過參數傳遞 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="9c8b4-114">You can cancel event notifications by calling [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) again, this time passing a **NULL** value through the parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c8b4-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c8b4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c8b4-116">使用感應器 API 事件</span><span class="sxs-lookup"><span data-stu-id="9c8b4-116">Using Sensor API Events</span></span>](using-sensor-api-events.md)
</dt> </dl>

 

 
