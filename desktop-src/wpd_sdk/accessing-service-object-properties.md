---
description: 存取服務物件屬性
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: 存取服務物件屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973049"
---
# <a name="accessing-service-object-properties"></a><span data-ttu-id="277f2-103">存取服務物件屬性</span><span class="sxs-lookup"><span data-stu-id="277f2-103">Accessing Service Object Properties</span></span>

<span data-ttu-id="277f2-104">應用程式可以針對服務、物件識別碼所識別的多個物件，或相同類型的多個物件，讀取和寫入單一物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="277f2-104">An application can read and write properties for a single object on a service, for multiple objects identified by object identifiers, or for multiple objects of the same type.</span></span> <span data-ttu-id="277f2-105">「 [正在取得物件屬性](retrieving-content-object-properties.md) 」主題描述如何讀取服務上單一物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="277f2-105">The [Retrieving Object Properties](retrieving-content-object-properties.md) topic describes reading properties for a single object on a service.</span></span> <span data-ttu-id="277f2-106">[撰寫物件屬性](writing-content-object-properties.md)主題描述如何在服務上撰寫單一物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="277f2-106">The [Writing Object Properties](writing-content-object-properties.md) topic describes writing properties for a single object on a service.</span></span>

<span data-ttu-id="277f2-107">如需多個物件的屬性抓取說明，請參閱「 [Advanced Tasks](advanced-tasks.md) 」一節。</span><span class="sxs-lookup"><span data-stu-id="277f2-107">Refer to the [Advanced Tasks](advanced-tasks.md) section for a description of property retrieval for multiple objects.</span></span>

## <a name="when-to-use-service-property-definitions"></a><span data-ttu-id="277f2-108">使用服務屬性定義的時機</span><span class="sxs-lookup"><span data-stu-id="277f2-108">When to use Service Property Definitions</span></span>

<span data-ttu-id="277f2-109">用來抓取和設定服務物件屬性的 WPD API 呼叫，與用來抓取裝置之物件屬性的呼叫相同 (比較「抓取單一物件的屬性」以取得範例) 。</span><span class="sxs-lookup"><span data-stu-id="277f2-109">The WPD API calls used for retrieving and setting object properties for a service are the same as the calls for retrieving object properties for a device (compare "Retrieving Properties for a Single Object" for an example).</span></span> <span data-ttu-id="277f2-110">主要差異在於使用不同的 PROPERTYKEYs 集合來查詢物件屬性。</span><span class="sxs-lookup"><span data-stu-id="277f2-110">The key difference is that a different set of PROPERTYKEYs are used to query object properties.</span></span> <span data-ttu-id="277f2-111">針對 WpdServiceApiSample，會使用裝置服務 PROPERTYKEYs (例如 **PKEY \_ GenericObj \_ 名稱**) ; 針對 WPDAPISAMPLE，會使用 WPD PROPERTYKEYs (例如 **WPD \_ 物件 \_ 名稱**) 。</span><span class="sxs-lookup"><span data-stu-id="277f2-111">For the WpdServiceApiSample, device service PROPERTYKEYs are used (such as **PKEY\_GenericObj\_Name**); for the WpdApiSample, WPD PROPERTYKEYs are used (such as **WPD\_OBJECT\_NAME**).</span></span>

<span data-ttu-id="277f2-112">裝置服務 PROPERTYKEYs 定義于每個服務標頭檔) 所包含的 BridgeDeviceServices (中，並代表裝置服務應用程式和裝置上的固件執行所採用的一組通用 PROPERTYKEYS。</span><span class="sxs-lookup"><span data-stu-id="277f2-112">Device service PROPERTYKEYs are defined in BridgeDeviceServices.h (included by each service header file), and represent the common set of PROPERTYKEYS employed by both device services applications and the firmware implementation on the device.</span></span> <span data-ttu-id="277f2-113">如此一來，就能以最少量的轉譯、以服務為基礎的 PROPERTYKEYs 群組，在整個裝置堆疊中提供一組一致的定義，並可讓您更輕鬆地定義新的服務，而不需要更新 WPD 架構。</span><span class="sxs-lookup"><span data-stu-id="277f2-113">This allows a consistent set of definitions throughout the device stack with minimal translation, groups PROPERTYKEYs based on the service, and enables new services to be more easily defined without having to update the WPD schema.</span></span>

<span data-ttu-id="277f2-114">使用的 PROPERTYKEYs 集將視您的應用程式需求而定：</span><span class="sxs-lookup"><span data-stu-id="277f2-114">The set of PROPERTYKEYs used will depend on your application's needs:</span></span>

-   <span data-ttu-id="277f2-115">如果您的應用程式是藉由呼叫 [**IPortableDevice：： Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)來與裝置通訊，請使用 PortableDevice 中所定義的 PROPERTYKEYs。</span><span class="sxs-lookup"><span data-stu-id="277f2-115">If your application is communicating with the device by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use the PROPERTYKEYs defined in PortableDevice.h.</span></span> <span data-ttu-id="277f2-116">這類應用程式的其中一個範例是 WpdApiSample。</span><span class="sxs-lookup"><span data-stu-id="277f2-116">An example of such an application is the WpdApiSample.</span></span>
-   <span data-ttu-id="277f2-117">如果您的應用程式是藉由呼叫 [**IPortableDeviceService：： Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)來與裝置服務通訊，請使用 BridgeDeviceServices 中所定義的 PROPERTYKEYS。</span><span class="sxs-lookup"><span data-stu-id="277f2-117">If your application is communicating with device services by calling [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use the PROPERTYKEYS defined in BridgeDeviceServices.h.</span></span> <span data-ttu-id="277f2-118">這類應用程式的其中一個範例是 WpdServicesApiSample。</span><span class="sxs-lookup"><span data-stu-id="277f2-118">An example of such an application is the WpdServicesApiSample.</span></span>
-   <span data-ttu-id="277f2-119">如果您撰寫的複雜應用程式需要同時支援裝置服務和裝置的混合 (這表示您的應用程式會同時呼叫 **IPortableDevice：： Open** 和 **IPortableDeviceService：： Open**) ，您必須在使用 IPortableDevice 及其衍生介面時使用 WPD PROPERTYKEYs，並在使用 [PROPERTYKEYs](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) 及其衍生介面時使用裝置服務 IPortableDeviceService。</span><span class="sxs-lookup"><span data-stu-id="277f2-119">If you are writing a complex application that needs to support a hybrid of both device services and the device (this means your application calls both **IPortableDevice::Open** and **IPortableDeviceService::Open**), you will need to use the WPD PROPERTYKEYs when using IPortableDevice and its derived interfaces, and device service PROPERTYKEYs when using [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) and its derived interfaces.</span></span>

<span data-ttu-id="277f2-120">大部分的 WPD 應用程式都應該落在第一個或第二個類別中。</span><span class="sxs-lookup"><span data-stu-id="277f2-120">Most WPD applications should fall into the first or second category.</span></span>

## <a name="related-topics"></a><span data-ttu-id="277f2-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="277f2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="277f2-122">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="277f2-122">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="277f2-123">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="277f2-123">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="277f2-124">正在抓取物件屬性</span><span class="sxs-lookup"><span data-stu-id="277f2-124">Retrieving Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="277f2-125">撰寫物件屬性</span><span class="sxs-lookup"><span data-stu-id="277f2-125">Writing Object Properties</span></span>](writing-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="277f2-126">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="277f2-126">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



