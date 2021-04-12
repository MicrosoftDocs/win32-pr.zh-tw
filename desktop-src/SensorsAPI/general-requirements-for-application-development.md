---
description: 本主題說明開始建立使用感應器 API 的程式時，必須執行的動作。
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: 應用程式開發 (感應器 API) 的一般需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320035"
---
# <a name="general-requirements-for-application-development-sensor-api"></a><span data-ttu-id="cb6f6-103">應用程式開發 (感應器 API) 的一般需求</span><span class="sxs-lookup"><span data-stu-id="cb6f6-103">General Requirements for Application Development (Sensor API)</span></span>

<span data-ttu-id="cb6f6-104">本主題說明開始建立使用感應器 API 的程式時，必須執行的動作。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-104">This topic describes what you must do to start to create programs that use the Sensor API.</span></span>

<span data-ttu-id="cb6f6-105">若要建立感應器 API 應用程式，您必須在電腦上安裝 Windows 7 和 Windows 7 軟體發展工具組 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-105">To create a Sensor API application, you must install Windows 7 and the Windows 7 Software Development Kit (SDK) on your computer.</span></span> <span data-ttu-id="cb6f6-106">下表說明您將需要的特定檔案。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-106">The following table describes the specific files that you will need.</span></span>



| <span data-ttu-id="cb6f6-107">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="cb6f6-107">File name</span></span>               | <span data-ttu-id="cb6f6-108">描述</span><span class="sxs-lookup"><span data-stu-id="cb6f6-108">Description</span></span>                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6f6-109">Sensorsapi。h</span><span class="sxs-lookup"><span data-stu-id="cb6f6-109">Sensorsapi.h</span></span>            | <span data-ttu-id="cb6f6-110">感應器 API 的主要標頭檔。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-110">The main header file for the Sensor API.</span></span> <span data-ttu-id="cb6f6-111">此標頭檔包含介面定義。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-111">This header file contains the interface definitions.</span></span>               |
| <span data-ttu-id="cb6f6-112">感應器。h</span><span class="sxs-lookup"><span data-stu-id="cb6f6-112">Sensors.h</span></span>               | <span data-ttu-id="cb6f6-113">包含平臺定義常數定義的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-113">The header file that contains definitions of platform-defined constants.</span></span>                                    |
| <span data-ttu-id="cb6f6-114">Initguid。h</span><span class="sxs-lookup"><span data-stu-id="cb6f6-114">Initguid.h</span></span>              | <span data-ttu-id="cb6f6-115">包含用於控制 **GUID** 初始化之定義的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-115">The header file that contains definitions for controlling **GUID** initialization.</span></span>                          |
| <span data-ttu-id="cb6f6-116">FunctionDiscoveryKeys。h</span><span class="sxs-lookup"><span data-stu-id="cb6f6-116">FunctionDiscoveryKeys.h</span></span> | <span data-ttu-id="cb6f6-117">標頭檔，定義當您連接到邏輯感應器時，所需的裝置識別碼屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-117">The header file that defines device ID property keys that are required when you connect to logical sensors.</span></span> |
| <span data-ttu-id="cb6f6-118">Sensorsapi .lib</span><span class="sxs-lookup"><span data-stu-id="cb6f6-118">Sensorsapi.lib</span></span>          | <span data-ttu-id="cb6f6-119">靜態程式庫，其中包含感應器 API 的 **GUID** 定義。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-119">A static library that contains **GUID** definitions for the Sensor API.</span></span>                                     |
| <span data-ttu-id="cb6f6-120">PortableDeviceGuids .lib</span><span class="sxs-lookup"><span data-stu-id="cb6f6-120">PortableDeviceGuids.lib</span></span> | <span data-ttu-id="cb6f6-121">靜態程式庫，其中包含 Windows 可攜式裝置物件的 **GUID** 定義。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-121">A static library that contains **GUID** definitions for Windows Portable Devices objects.</span></span>                   |



 

<span data-ttu-id="cb6f6-122">您的程式可能需要額外的檔案。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-122">Your program may require additional files.</span></span>

## <a name="supported-operating-systems"></a><span data-ttu-id="cb6f6-123">支援的作業系統</span><span class="sxs-lookup"><span data-stu-id="cb6f6-123">Supported Operating Systems</span></span>

<span data-ttu-id="cb6f6-124">感應器 API 應用程式將會在 windows 7 Starter edition 以外的所有 Windows 7 版本上執行。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-124">Sensor API applications will run on all editions of Windows 7, except for Windows 7 Starter edition.</span></span>

## <a name="windows-portable-devices-interfaces"></a><span data-ttu-id="cb6f6-125">Windows 可攜式裝置介面</span><span class="sxs-lookup"><span data-stu-id="cb6f6-125">Windows Portable Devices Interfaces</span></span>

<span data-ttu-id="cb6f6-126">感應器 API 會使用某些 Windows 可攜式裝置 (WPD) 物件來封裝屬性索引鍵和值。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-126">The Sensor API uses certain Windows Portable Devices (WPD) objects to encapsulate property keys and values.</span></span> <span data-ttu-id="cb6f6-127">下表描述這些物件的介面。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-127">The following table describes the interfaces for these objects.</span></span>



| <span data-ttu-id="cb6f6-128">介面</span><span class="sxs-lookup"><span data-stu-id="cb6f6-128">Interface</span></span>                                                                       | <span data-ttu-id="cb6f6-129">描述</span><span class="sxs-lookup"><span data-stu-id="cb6f6-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6f6-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb6f6-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span></span>        | <span data-ttu-id="cb6f6-131">這個介面可讓您輕鬆地建立名稱/值配對的屬性包。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-131">This interface provides a convenient way to create a property bag of name/value pairs.</span></span> <span data-ttu-id="cb6f6-132">名稱會以 **PROPERTYKEY** 來表示，而值則是以 **PROPVARIANT** s 表示。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-132">Names are represented by **PROPERTYKEY** s and values are represented by **PROPVARIANT** s.</span></span> <br/> <span data-ttu-id="cb6f6-133">API 會使用此介面來設定和同時抓取單一值和值的集合。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-133">The API uses this interface for setting and retrieving both single values and sets of values.</span></span> <span data-ttu-id="cb6f6-134">您可以從方法中取出這個介面，或者，如果需要新的物件，請呼叫具有 CLSID PortableDeviceValues 的 **CoCreateInstance** \_ 。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-134">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceValues.</span></span><br/> |
| <span data-ttu-id="cb6f6-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb6f6-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span></span> | <span data-ttu-id="cb6f6-136">這個介面包含 **PROPERTYKEY** 的集合。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-136">This interface contains a collection of **PROPERTYKEY** s.</span></span> <span data-ttu-id="cb6f6-137">這些索引鍵代表可由 **IPortableDeviceValues** 儲存的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-137">These keys represent property names that can be stored by **IPortableDeviceValues**.</span></span> <span data-ttu-id="cb6f6-138">API 會使用此集合物件來設定和抓取單一屬性名稱和屬性名稱的集合。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-138">The API uses this collection object for setting and retrieving both single property names and sets of property names.</span></span><br/> <span data-ttu-id="cb6f6-139">您可以從方法中取出這個介面，或者，如果需要新的物件，請呼叫具有 CLSID PortableDeviceKeyCollection 的 **CoCreateInstance** \_ 。</span><span class="sxs-lookup"><span data-stu-id="cb6f6-139">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceKeyCollection.</span></span> <br/>    |



 

 

