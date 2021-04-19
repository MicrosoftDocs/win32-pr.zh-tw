---
description: 邏輯感應器會提供資料，而不需視硬體裝置而定。
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: 關於邏輯感應器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6f8687575aaedbb006eb2ad6ebaad9cf8d3ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990394"
---
# <a name="about-logical-sensors"></a><span data-ttu-id="279a8-103">關於邏輯感應器</span><span class="sxs-lookup"><span data-stu-id="279a8-103">About Logical Sensors</span></span>

<span data-ttu-id="279a8-104">*邏輯感應器* 會提供資料，而不需視硬體裝置而定。</span><span class="sxs-lookup"><span data-stu-id="279a8-104">*Logical sensors* provide data without depending on hardware devices.</span></span> <span data-ttu-id="279a8-105">例如，邏輯感應器可以使用在資料表中查閱 IP 位址的服務，來提供使用者目前位置的相關資料。</span><span class="sxs-lookup"><span data-stu-id="279a8-105">For example, a logical sensor could provide data about the user's current location by using a service that looks up an IP address in a table.</span></span> <span data-ttu-id="279a8-106">邏輯感應器會實作為感應器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="279a8-106">Logical sensors are implemented as sensor drivers.</span></span> <span data-ttu-id="279a8-107">如需如何執行感應器驅動程式的相關資訊，請參閱 Windows 驅動程式套件。</span><span class="sxs-lookup"><span data-stu-id="279a8-107">For information about how to implement a sensor driver, see the Windows Driver Kit.</span></span>

<span data-ttu-id="279a8-108">在使用者的電腦上安裝邏輯感應器之後，您可以使用與以硬體為基礎的感應器一樣的方式來使用它。</span><span class="sxs-lookup"><span data-stu-id="279a8-108">After a logical sensor is installed on the user's computer, you can use it in the same way as a hardware-based sensor.</span></span> <span data-ttu-id="279a8-109">感應器 API 會提供代表邏輯感應器的 [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) 介面，而您的程式可以透過與用於任何其他類型感應器的相同機制來要求資料。</span><span class="sxs-lookup"><span data-stu-id="279a8-109">The Sensor API will provide an [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface to represent the logical sensor, and your program can request data through the same mechanisms as you would use for any other type of sensor.</span></span> <span data-ttu-id="279a8-110">邏輯感應器也可以使用平臺定義的感應器類別、類型、資料類型、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="279a8-110">Logical sensors can also use the platform-defined sensor categories, types, data types, properties, and events.</span></span> <span data-ttu-id="279a8-111">或者，您也可以定義自訂值。</span><span class="sxs-lookup"><span data-stu-id="279a8-111">Or you can define custom values.</span></span>

<span data-ttu-id="279a8-112">[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85))介面可讓開發人員建立邏輯感應器來管理感應器和位置平臺的連接。</span><span class="sxs-lookup"><span data-stu-id="279a8-112">The [**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) interface enables developers who create logical sensors to manage connections to the Sensor and Location platform.</span></span>

> [!Note]  
> <span data-ttu-id="279a8-113">如同其他驅動程式，安裝或卸載邏輯感應器驅動程式需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="279a8-113">As with other drivers, installing or uninstalling a logical sensor driver requires administrator privileges.</span></span>

 

<span data-ttu-id="279a8-114">若要嘗試使用範例邏輯感應器，請參閱 [關於範例和工具](about-the-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="279a8-114">To try using a sample logical sensor, see [About the Samples and Tools](about-the-samples.md).</span></span>

## <a name="managing-logical-sensors"></a><span data-ttu-id="279a8-115">管理邏輯感應器</span><span class="sxs-lookup"><span data-stu-id="279a8-115">Managing Logical Sensors</span></span>

<span data-ttu-id="279a8-116">[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) 具有下列方法：</span><span class="sxs-lookup"><span data-stu-id="279a8-116">[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) has the following methods:</span></span>

-   <span data-ttu-id="279a8-117">[**連接**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="279a8-117">[**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))</span></span>
-   <span data-ttu-id="279a8-118">[**中斷連線**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="279a8-118">[**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))</span></span>
-   <span data-ttu-id="279a8-119">[**解除安裝**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="279a8-119">[**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))</span></span>

<span data-ttu-id="279a8-120">當您呼叫 [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))時，感應器 API 會建立感應器驅動程式的實例（如果尚未存在），然後將邏輯感應器連接到平臺。</span><span class="sxs-lookup"><span data-stu-id="279a8-120">When you call [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)), the Sensor API creates an instance of the sensor driver, if one does not already exist, and then connects the logical sensor to the platform.</span></span> <span data-ttu-id="279a8-121">這表示邏輯感應器會與 **定位和其他感應器** 主控台中的其他感應器一起出現。</span><span class="sxs-lookup"><span data-stu-id="279a8-121">This means that the logical sensor appears with other sensors in the **Location and Other Sensors** Control Panel.</span></span> <span data-ttu-id="279a8-122">當您呼叫 [**中斷**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))連線時，感應器 API 會中斷邏輯感應器的連線，並將其從主控台中移除。</span><span class="sxs-lookup"><span data-stu-id="279a8-122">When you call [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)), the Sensor API disconnects the logical sensor and removes it from the Control Panel.</span></span> <span data-ttu-id="279a8-123">呼叫 **中斷** 連線並不會從 **裝置管理員** 移除邏輯感應器。</span><span class="sxs-lookup"><span data-stu-id="279a8-123">Calling **Disconnect** does not remove the logical sensor from **Device Manager**.</span></span> <span data-ttu-id="279a8-124">因此，未來對 **連接** 的呼叫將會導致更快速地連接到邏輯感應器。</span><span class="sxs-lookup"><span data-stu-id="279a8-124">Therefore, future calls to **Connect** will result in a much faster connection to the logical sensor.</span></span>

<span data-ttu-id="279a8-125">若要移除邏輯感應器，您必須呼叫 [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="279a8-125">To remove a logical sensor, you must call [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)).</span></span> <span data-ttu-id="279a8-126">卸載邏輯感應器會移除 **裝置管理員** 的感應器。</span><span class="sxs-lookup"><span data-stu-id="279a8-126">Uninstalling a logical sensor removes the sensor from **Device Manager**.</span></span> <span data-ttu-id="279a8-127">由於邏輯感應器裝置只存在於記憶體中，因此當使用者重新開機 Windows 時，會卸載邏輯感應器。</span><span class="sxs-lookup"><span data-stu-id="279a8-127">Because logical sensor devices exist only in memory, a logical sensor is uninstalled when the user restarts Windows.</span></span>

<span data-ttu-id="279a8-128">感應器 API 會依 *邏輯識別碼*（ **GUID**）來識別特定的邏輯感應器。</span><span class="sxs-lookup"><span data-stu-id="279a8-128">The Sensor API identifies a particular logical sensor by its *logical ID*, which is a **GUID**.</span></span> <span data-ttu-id="279a8-129">每次連接到特定的邏輯感應器時，都必須提供邏輯識別碼。</span><span class="sxs-lookup"><span data-stu-id="279a8-129">Each time you connect to a particular logical sensor, you must provide a logical ID.</span></span> <span data-ttu-id="279a8-130">每次中斷連接或卸載特定感應器時，您必須提供您用來連線的相同邏輯識別碼。</span><span class="sxs-lookup"><span data-stu-id="279a8-130">Each time you disconnect or uninstall a particular sensor, you must provide the same logical ID that you used to connect.</span></span> <span data-ttu-id="279a8-131">如果您使用不同的邏輯識別碼多次連線到相同的邏輯感應器驅動程式，則會為每個新的邏輯識別碼建立個別的邏輯感應器實例。</span><span class="sxs-lookup"><span data-stu-id="279a8-131">If you connect to the same logical sensor driver multiple times by using different logical IDs, you will create a separate instance of the logical sensor for each new logical ID.</span></span> <span data-ttu-id="279a8-132">即使您為每個邏輯識別碼呼叫「 [**中斷**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) 連線」，這些個別的實例仍會保留在 **裝置管理員** 中，直到您針對每個邏輯感應器呼叫 [**卸載**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) ，或使用者重新開機 Windows 為止。</span><span class="sxs-lookup"><span data-stu-id="279a8-132">Even if you call [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) for each logical ID, these separate instances will remain in **Device Manager** until you call [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) for each logical sensor, or the user restarts Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="279a8-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="279a8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="279a8-134">使用邏輯感應器</span><span class="sxs-lookup"><span data-stu-id="279a8-134">Using Logical Sensors</span></span>](using-logical-sensors.md)
</dt> </dl>

 

 
