---
description: 位置 API 會定義下列列舉類型。
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: " (位置 API) 的結構和列舉類型"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978040"
---
# <a name="structures-and-enumeration-types-location-api"></a><span data-ttu-id="a5c3f-103"> (位置 API) 的結構和列舉類型</span><span class="sxs-lookup"><span data-stu-id="a5c3f-103">Structures and Enumeration Types (Location API)</span></span>

<span data-ttu-id="a5c3f-104">\[Win32 位置 API 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a5c3f-104">\[The Win32 Location API is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a5c3f-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a5c3f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a5c3f-106">相反地，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。</span><span class="sxs-lookup"><span data-stu-id="a5c3f-106">Instead, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.</span></span> <span data-ttu-id="a5c3f-107">\]</span><span class="sxs-lookup"><span data-stu-id="a5c3f-107">\]</span></span>

<span data-ttu-id="a5c3f-108">位置 API 會定義下列列舉類型。</span><span class="sxs-lookup"><span data-stu-id="a5c3f-108">The Location API defines the following enumeration types.</span></span>



| <span data-ttu-id="a5c3f-109">列舉型別</span><span class="sxs-lookup"><span data-stu-id="a5c3f-109">Enumeration</span></span>                                                                       | <span data-ttu-id="a5c3f-110">描述</span><span class="sxs-lookup"><span data-stu-id="a5c3f-110">Description</span></span>                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="a5c3f-111">[**需要的位置 \_ \_ 精確度**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5c3f-111">[**LOCATION\_DESIRED\_ACCURACY**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span></span>                  | <span data-ttu-id="a5c3f-112">定義可能需要的精確度類型。</span><span class="sxs-lookup"><span data-stu-id="a5c3f-112">Defines the possible desired accuracy types.</span></span>                         |
| [<span data-ttu-id="a5c3f-113">**位置 \_ 報告 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="a5c3f-113">**LOCATION\_REPORT\_STATUS**</span></span>](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | <span data-ttu-id="a5c3f-114">針對特定報表類型的新報表定義可能的狀態。</span><span class="sxs-lookup"><span data-stu-id="a5c3f-114">Defines possible status for new reports of a particular report type.</span></span> |



 

## <a name="location-constants-from-the-sensor-api"></a><span data-ttu-id="a5c3f-115">來自感應器 API 的位置常數</span><span class="sxs-lookup"><span data-stu-id="a5c3f-115">Location Constants from the Sensor API</span></span>

<span data-ttu-id="a5c3f-116">感應器 API 也會定義位置相關的屬性索引鍵和常數。</span><span class="sxs-lookup"><span data-stu-id="a5c3f-116">The Sensor API also defines location-related property keys and constants.</span></span> <span data-ttu-id="a5c3f-117">您可以藉由呼叫 [**ILocationReport：： GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue)，使用在 [感應器] 中定義的屬性索引鍵來從報表取出位置資料。</span><span class="sxs-lookup"><span data-stu-id="a5c3f-117">The property keys defined in sensors.h can be used to retrieve location data from a report by calling [**ILocationReport::GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span></span>

 

 
