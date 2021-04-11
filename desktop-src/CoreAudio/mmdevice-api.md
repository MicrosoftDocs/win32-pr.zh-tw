---
description: 關於 MMDevice API
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: 關於 MMDevice API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689067"
---
# <a name="about-mmdevice-api"></a><span data-ttu-id="238be-103">關於 MMDevice API</span><span class="sxs-lookup"><span data-stu-id="238be-103">About MMDevice API</span></span>

<span data-ttu-id="238be-104">Windows 多媒體裝置 (MMDevice) API 可讓音訊用戶端探索 [音訊端點裝置](audio-endpoint-devices.md)、判斷其功能，以及為這些裝置建立驅動程式實例。</span><span class="sxs-lookup"><span data-stu-id="238be-104">The Windows Multimedia Device (MMDevice) API enables audio clients to discover [audio endpoint devices](audio-endpoint-devices.md), determine their capabilities, and create driver instances for those devices.</span></span>

<span data-ttu-id="238be-105">標頭檔 Mmdeviceapi 會定義 MMDevice API 中的介面。</span><span class="sxs-lookup"><span data-stu-id="238be-105">Header file Mmdeviceapi.h defines the interfaces in the MMDevice API.</span></span>

<span data-ttu-id="238be-106">MMDevice API 包含數個介面。</span><span class="sxs-lookup"><span data-stu-id="238be-106">The MMDevice API consists of several interfaces.</span></span> <span data-ttu-id="238be-107">其中第一個是 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面。</span><span class="sxs-lookup"><span data-stu-id="238be-107">The first of these is the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="238be-108">若要存取 MMDevice API 中的介面，用戶端會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)函式來取得裝置列舉值物件的 **IMMDeviceEnumerator** 介面參考，如下列程式碼片段所示：</span><span class="sxs-lookup"><span data-stu-id="238be-108">To access the interfaces in the MMDevice API, a client obtains a reference to the **IMMDeviceEnumerator** interface of a device-enumerator object by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, as shown in the following code fragment:</span></span>


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



<span data-ttu-id="238be-109">在上述的程式碼片段中，CLSID \_ MMDeviceEnumerator 和 IID \_ IMMDeviceEnumerator 是以屬性形式附加至 **MMDeviceEnumerator** 類別物件和 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="238be-109">In the preceding code fragment, CLSID\_MMDeviceEnumerator and IID\_IMMDeviceEnumerator are the GUID values that are attached as attributes to the **MMDeviceEnumerator** class object and to the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="238be-110">[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)呼叫會以傳址方式傳遞這些值。</span><span class="sxs-lookup"><span data-stu-id="238be-110">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call passes these values by reference.</span></span> <span data-ttu-id="238be-111">變數 `hr` 的類型為 **HRESULT**，而變數 `pEnumerator` 則是裝置列舉值物件之 **IMMDeviceEnumerator** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="238be-111">Variable `hr` is of type **HRESULT**, and variable `pEnumerator` is a pointer to the **IMMDeviceEnumerator** interface of a device-enumerator object.</span></span> <span data-ttu-id="238be-112">**IMMDeviceEnumerator** 提供列舉音訊端點裝置的方法。</span><span class="sxs-lookup"><span data-stu-id="238be-112">**IMMDeviceEnumerator** provides methods for enumerating audio endpoint devices.</span></span> <span data-ttu-id="238be-113">如需 **\_ \_ uuidof** 運算子、 **CoCreateInstance** 函數和 CLSCTX Xxx 常數的詳細資訊 \_  ，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="238be-113">For information about the **\_\_uuidof** operator, the **CoCreateInstance** function, and the CLSCTX\_*Xxx* constants, see the Windows SDK documentation.</span></span>

<span data-ttu-id="238be-114">透過 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面，用戶端可以取得 MMDevice API 中其他介面的參考。</span><span class="sxs-lookup"><span data-stu-id="238be-114">Through the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, the client can obtain references to the other interfaces in the MMDevice API.</span></span> <span data-ttu-id="238be-115">MMDevice API 會執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="238be-115">The MMDevice API implements the following interfaces.</span></span>



| <span data-ttu-id="238be-116">介面</span><span class="sxs-lookup"><span data-stu-id="238be-116">Interface</span></span>                                          | <span data-ttu-id="238be-117">描述</span><span class="sxs-lookup"><span data-stu-id="238be-117">Description</span></span>                                     |
|----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="238be-118">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="238be-118">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | <span data-ttu-id="238be-119">代表音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="238be-119">Represents an audio device.</span></span>                     |
| [<span data-ttu-id="238be-120">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="238be-120">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | <span data-ttu-id="238be-121">代表音訊裝置的集合。</span><span class="sxs-lookup"><span data-stu-id="238be-121">Represents a collection of audio devices.</span></span>       |
| [<span data-ttu-id="238be-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="238be-122">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | <span data-ttu-id="238be-123">提供列舉音訊裝置的方法。</span><span class="sxs-lookup"><span data-stu-id="238be-123">Provides methods for enumerating audio devices.</span></span> |
| [<span data-ttu-id="238be-124">**IMMEndpoint**</span><span class="sxs-lookup"><span data-stu-id="238be-124">**IMMEndpoint**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | <span data-ttu-id="238be-125">代表音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="238be-125">Represents an audio endpoint device.</span></span>            |



 

<span data-ttu-id="238be-126">此外，MMDevice API 的用戶端必須在音訊端點裝置中執行狀態變更的通知，才能執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="238be-126">In addition, clients of the MMDevice API that require notification of status changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="238be-127">介面</span><span class="sxs-lookup"><span data-stu-id="238be-127">Interface</span></span>                                              | <span data-ttu-id="238be-128">描述</span><span class="sxs-lookup"><span data-stu-id="238be-128">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="238be-129">**IMMNotificationClient**</span><span class="sxs-lookup"><span data-stu-id="238be-129">**IMMNotificationClient**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | <span data-ttu-id="238be-130">當新增或移除音訊端點裝置、裝置的狀態或屬性變更時，或指派給裝置的預設角色變更時，會提供通知。</span><span class="sxs-lookup"><span data-stu-id="238be-130">Provides notifications when an audio endpoint device is added or removed, when the state or properties of a device change, or when there is a change in the default role assigned to a device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="238be-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="238be-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="238be-132">音訊端點裝置</span><span class="sxs-lookup"><span data-stu-id="238be-132">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="238be-133">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="238be-133">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 
