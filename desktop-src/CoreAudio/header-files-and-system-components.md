---
description: 標頭檔和系統元件
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: 標頭檔和系統元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4b93c63e7d32944dfdf2bf6872bd3a3153e4a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111324"
---
# <a name="header-files-and-system-components"></a><span data-ttu-id="7ddf9-103">標頭檔和系統元件</span><span class="sxs-lookup"><span data-stu-id="7ddf9-103">Header Files and System Components</span></span>

<span data-ttu-id="7ddf9-104">下表列出包含四個核心音訊元件之介面定義的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-104">The following table lists the header files that contain the interface definitions for the four Core Audio components.</span></span>



|                                              |                              |
|----------------------------------------------|------------------------------|
| <span data-ttu-id="7ddf9-105">核心音訊元件</span><span class="sxs-lookup"><span data-stu-id="7ddf9-105">Core Audio component</span></span>                         | <span data-ttu-id="7ddf9-106">標頭檔</span><span class="sxs-lookup"><span data-stu-id="7ddf9-106">Header file</span></span>                  |
| [<span data-ttu-id="7ddf9-107">MMDevice API</span><span class="sxs-lookup"><span data-stu-id="7ddf9-107">MMDevice API</span></span>](mmdevice-api.md)             | <span data-ttu-id="7ddf9-108">Mmdeviceapi。h</span><span class="sxs-lookup"><span data-stu-id="7ddf9-108">Mmdeviceapi.h</span></span>                |
| [<span data-ttu-id="7ddf9-109">WASAPI</span><span class="sxs-lookup"><span data-stu-id="7ddf9-109">WASAPI</span></span>](wasapi.md)                         | <span data-ttu-id="7ddf9-110">Audioclient .h、Audiopolicy。h</span><span class="sxs-lookup"><span data-stu-id="7ddf9-110">Audioclient.h, Audiopolicy.h</span></span> |
| [<span data-ttu-id="7ddf9-111">DeviceTopology API</span><span class="sxs-lookup"><span data-stu-id="7ddf9-111">DeviceTopology API</span></span>](devicetopology-api.md) | <span data-ttu-id="7ddf9-112">Devicetopology。h</span><span class="sxs-lookup"><span data-stu-id="7ddf9-112">Devicetopology.h</span></span>             |
| [<span data-ttu-id="7ddf9-113">EndpointVolume API</span><span class="sxs-lookup"><span data-stu-id="7ddf9-113">EndpointVolume API</span></span>](endpointvolume-api.md) | <span data-ttu-id="7ddf9-114">Endpointvolume。h</span><span class="sxs-lookup"><span data-stu-id="7ddf9-114">Endpointvolume.h</span></span>             |



 

<span data-ttu-id="7ddf9-115">另一個標頭檔 Audiosessiontypes 則定義 WASAPI 所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-115">Another header file, Audiosessiontypes.h, defines constants that are used by WASAPI.</span></span> <span data-ttu-id="7ddf9-116">這些標頭檔位於目錄% MSSdk% \\ include 中，其中% MSSdk% 是您電腦上 Windows SDK 安裝的根目錄。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-116">These header files are located in the directory %MSSdk%\\include, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>

<span data-ttu-id="7ddf9-117">上表中的每個 API 都包含一組相關的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-117">Each API in the preceding table consists of a set of related COM interfaces.</span></span> <span data-ttu-id="7ddf9-118">因為音訊串流的某些層面取決於低延遲和精確的同步處理，所以 MMDevice、WASAPI、DeviceTopology 和 EndpointVolume Api 的執行不會使用 Microsoft .NET Framework 或受控執行環境。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-118">Because some aspects of audio streaming depend on low latency and precise synchronization, the implementations of the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs do not use the Microsoft .NET Framework or managed-execution environment.</span></span>

<span data-ttu-id="7ddf9-119">核心音訊 Api 會在使用者模式系統元件中執行，Audioses.dll 和 Mmdevapi.dll。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-119">The Core Audio APIs are implemented in the user-mode system components Audioses.dll and Mmdevapi.dll.</span></span> <span data-ttu-id="7ddf9-120">用戶端應用程式不會直接存取這些 Dll 中的進入點。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-120">Client applications do not access the entry points in these DLLs directly.</span></span> <span data-ttu-id="7ddf9-121">相反地，用戶端會呼叫 **CoCreateInstance** 或 **CoCreateInstanceEx** 函數來取得 MMDeviceEnumerator 類別物件的 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-121">Instead, clients call the **CoCreateInstance** or **CoCreateInstanceEx** function to obtain the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface of the MMDeviceEnumerator class object.</span></span> <span data-ttu-id="7ddf9-122">此物件會列舉系統中的 [音訊端點裝置](audio-endpoint-devices.md) 。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-122">This object enumerates the [audio endpoint devices](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="7ddf9-123">**IMMDeviceEnumerator** 介面是 MMDevice API 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-123">The **IMMDeviceEnumerator** interface is part of the MMDevice API.</span></span> <span data-ttu-id="7ddf9-124">從這個介面，用戶端可以直接或間接取得 MMDevice API 中的其他介面，包括 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-124">From this interface, clients can directly or indirectly obtain the other interfaces in the MMDevice API, including the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span> <span data-ttu-id="7ddf9-125">**IMMDevice** 代表特定的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-125">**IMMDevice** represents a particular audio endpoint device.</span></span> <span data-ttu-id="7ddf9-126">透過 **IMMDevice**，用戶端可以直接或間接取得 WASAPI、DeviceTopology API 和 EndpointVolume API 中的裝置特定介面。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-126">Through **IMMDevice**, clients can directly or indirectly obtain the device-specific interfaces in WASAPI, the DeviceTopology API, and the EndpointVolume API.</span></span> <span data-ttu-id="7ddf9-127">如需有關 **CoCreateInstance** 和 **CoCreateInstanceEx** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-127">For more information about **CoCreateInstance** and **CoCreateInstanceEx**, see the Windows SDK documentation.</span></span> <span data-ttu-id="7ddf9-128">如需有關存取核心音訊 Api 介面的詳細資訊，請參閱 [列舉音訊裝置](enumerating-audio-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="7ddf9-128">For more information about accessing the interfaces in the Core Audio APIs, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ddf9-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="7ddf9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ddf9-130">關於 Windows Core 音訊 Api</span><span class="sxs-lookup"><span data-stu-id="7ddf9-130">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



