---
description: 感應器 API 會公開下列 COM 介面。
ms.assetid: 872de1e9-20f9-409b-9917-24b13a8cc08a
title: 'COM 介面 (感應器 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a73e506f5b2a59a7ce8373b810aeba779f5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991814"
---
# <a name="com-interfaces-sensor-api"></a><span data-ttu-id="bac76-103">COM 介面 (感應器 API) </span><span class="sxs-lookup"><span data-stu-id="bac76-103">COM Interfaces (Sensor API)</span></span>

<span data-ttu-id="bac76-104">感應器 API 會公開下列 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="bac76-104">The Sensor API exposes the following COM interfaces.</span></span>



| <span data-ttu-id="bac76-105">介面</span><span class="sxs-lookup"><span data-stu-id="bac76-105">Interface</span></span>                                              | <span data-ttu-id="bac76-106">描述</span><span class="sxs-lookup"><span data-stu-id="bac76-106">Description</span></span>                                                                                                      |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bac76-107">**ILocationPermissions**</span><span class="sxs-lookup"><span data-stu-id="bac76-107">**ILocationPermissions**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-ilocationpermissions)   | <span data-ttu-id="bac76-108">提供可讓使用者變更位置設定之系統設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="bac76-108">Provides the status of the system setting that allows users to change location settings.</span></span>                         |
| <span data-ttu-id="bac76-109">[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bac76-109">[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85))</span></span> | <span data-ttu-id="bac76-110">提供邏輯感應器作者用來管理邏輯感應器連接的方法。</span><span class="sxs-lookup"><span data-stu-id="bac76-110">Provides methods used by logical sensor authors to manage logical sensor connections.</span></span>                            |
| [<span data-ttu-id="bac76-111">**ISensor**</span><span class="sxs-lookup"><span data-stu-id="bac76-111">**ISensor**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor)                             | <span data-ttu-id="bac76-112">代表感應器。</span><span class="sxs-lookup"><span data-stu-id="bac76-112">Represents a sensor.</span></span>                                                                                             |
| [<span data-ttu-id="bac76-113">**ISensorCollection**</span><span class="sxs-lookup"><span data-stu-id="bac76-113">**ISensorCollection**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection)         | <span data-ttu-id="bac76-114">代表感應器的集合。</span><span class="sxs-lookup"><span data-stu-id="bac76-114">Represents a collection of sensors.</span></span>                                                                              |
| [<span data-ttu-id="bac76-115">**ISensorDataReport**</span><span class="sxs-lookup"><span data-stu-id="bac76-115">**ISensorDataReport**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport)         | <span data-ttu-id="bac76-116">代表感應器資料包表。</span><span class="sxs-lookup"><span data-stu-id="bac76-116">Represents a sensor data report.</span></span>                                                                                 |
| [<span data-ttu-id="bac76-117">**ISensorEvents**</span><span class="sxs-lookup"><span data-stu-id="bac76-117">**ISensorEvents**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)                 | <span data-ttu-id="bac76-118">接收感應器事件的回呼介面。</span><span class="sxs-lookup"><span data-stu-id="bac76-118">The callback interface for receiving sensor events.</span></span>                                                              |
| [<span data-ttu-id="bac76-119">**ISensorManager**</span><span class="sxs-lookup"><span data-stu-id="bac76-119">**ISensorManager**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)               | <span data-ttu-id="bac76-120">提供用來探索和取出可用感應器的方法，以及要求感應器管理員事件的方法。</span><span class="sxs-lookup"><span data-stu-id="bac76-120">Provides methods for discovering and retrieving available sensors and a method to request sensor manager events.</span></span> |
| [<span data-ttu-id="bac76-121">**ISensorManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="bac76-121">**ISensorManagerEvents**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents)   | <span data-ttu-id="bac76-122">用來接收感應器管理員事件的回呼介面。</span><span class="sxs-lookup"><span data-stu-id="bac76-122">The callback interface for receiving sensor manager events.</span></span>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="bac76-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="bac76-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bac76-124">感應器 API 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="bac76-124">Sensor API Programming Reference</span></span>](sensor-api-programming-reference.md)
</dt> </dl>

 

 
