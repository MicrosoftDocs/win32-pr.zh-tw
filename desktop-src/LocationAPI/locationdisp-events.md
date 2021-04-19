---
description: 位置 API 物件模型提供下列事件。
ms.assetid: c7ac0d81-ce36-4991-a0fb-6d3c6cc8efe8
title: LocationDisp 事件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55dae79305547bf4e41ee27c727ab9204eb561cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001448"
---
# <a name="locationdisp-events"></a><span data-ttu-id="419b0-103">LocationDisp 事件</span><span class="sxs-lookup"><span data-stu-id="419b0-103">LocationDisp Events</span></span>

<span data-ttu-id="419b0-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="419b0-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="419b0-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="419b0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="419b0-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="419b0-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="419b0-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="419b0-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="419b0-108">位置 API 物件模型提供下列事件。</span><span class="sxs-lookup"><span data-stu-id="419b0-108">The Location API object model provides the following events.</span></span>



| <span data-ttu-id="419b0-109">事件</span><span class="sxs-lookup"><span data-stu-id="419b0-109">Event</span></span>                                                  | <span data-ttu-id="419b0-110">描述</span><span class="sxs-lookup"><span data-stu-id="419b0-110">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="419b0-111">**NewCivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="419b0-111">**NewCivicAddressReport**</span></span>](newcivicaddressreport.md) | <span data-ttu-id="419b0-112">產生新的市政位址報表時發生。</span><span class="sxs-lookup"><span data-stu-id="419b0-112">Occurs when a new civic address report is generated.</span></span>      |
| [<span data-ttu-id="419b0-113">**NewLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="419b0-113">**NewLatLongReport**</span></span>](newlatlongreport.md)           | <span data-ttu-id="419b0-114">當產生新的緯度/經度報表時發生。</span><span class="sxs-lookup"><span data-stu-id="419b0-114">Occurs when a new latitude/longitude report is generated.</span></span> |
| [<span data-ttu-id="419b0-115">**StatusChanged**</span><span class="sxs-lookup"><span data-stu-id="419b0-115">**StatusChanged**</span></span>](statuschanged.md)                 | <span data-ttu-id="419b0-116">當報表的操作狀態變更時發生。</span><span class="sxs-lookup"><span data-stu-id="419b0-116">Occurs when the operational status of a report changes.</span></span>   |



 

 

 
