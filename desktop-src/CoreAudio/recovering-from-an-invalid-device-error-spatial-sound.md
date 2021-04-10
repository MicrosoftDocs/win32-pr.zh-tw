---
description: '從 (空間音效的 Invalid-Device 錯誤中復原) '
title: '從 (空間音效的 Invalid-Device 錯誤中復原) '
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111308"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a><span data-ttu-id="d302a-103">從 (空間音效的 Invalid-Device 錯誤中復原) </span><span class="sxs-lookup"><span data-stu-id="d302a-103">Recovering from an Invalid-Device Error (Spatial Sound)</span></span>

<span data-ttu-id="d302a-104">Microsoft 空間音訊 API 的許多方法（例如 [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)、 [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)和 [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)）會傳回錯誤碼（如果用戶端應用程式所使用的音訊端點裝置變得無效，或端點上的空間音訊轉譯格式有所變更）。</span><span class="sxs-lookup"><span data-stu-id="d302a-104">Many of the methods of the Microsoft Spatial Audio API, such as [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream), and [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), return error codes if the audio endpoint device that the client application is using becomes invalid or the spatial audio rendering format is changed on the endpoint.</span></span> <span data-ttu-id="d302a-105">這些錯誤碼表示端點裝置已卸載，或音訊硬體或相關聯的硬體資源已重新設定、停用、移除、空間音訊模式已變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d302a-105">These error codes indicates that the endpoint device has been unplugged, or that the audio hardware or associated hardware resources have been reconfigured, disabled, removed, spatial audio mode is changed or otherwise made unavailable for use.</span></span> <span data-ttu-id="d302a-106">通常，應用程式可以從這個錯誤中復原。</span><span class="sxs-lookup"><span data-stu-id="d302a-106">Frequently, the application can recover from this error.</span></span>

<span data-ttu-id="d302a-107">指出無效裝置錯誤的錯誤碼包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="d302a-107">Error codes that indicate an invalid-device error include the following:</span></span>

- <span data-ttu-id="d302a-108">SPTLAUDCLNT_E_DESTROYED</span><span class="sxs-lookup"><span data-stu-id="d302a-108">SPTLAUDCLNT_E_DESTROYED</span></span>
- <span data-ttu-id="d302a-109">AUDCLNT_E_DEVICE_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="d302a-109">AUDCLNT_E_DEVICE_INVALIDATED</span></span>
- <span data-ttu-id="d302a-110">AUDCLNT_E_RESOURCES_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="d302a-110">AUDCLNT_E_RESOURCES_INVALIDATED</span></span>
- <span data-ttu-id="d302a-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span><span class="sxs-lookup"><span data-stu-id="d302a-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span></span>
- <span data-ttu-id="d302a-112">SPTLAUDCLNT_E_INTERNAL</span><span class="sxs-lookup"><span data-stu-id="d302a-112">SPTLAUDCLNT_E_INTERNAL</span></span>

## <a name="strategies-for-handling-invalid-device-errors"></a><span data-ttu-id="d302a-113">處理無效裝置錯誤的策略</span><span class="sxs-lookup"><span data-stu-id="d302a-113">Strategies for handling invalid-device errors</span></span>

<span data-ttu-id="d302a-114">從無效裝置錯誤中復原的建議策略，取決於應用程式是否根據內部需求自動選取特定裝置，或允許使用者從可用裝置清單中明確選取裝置。</span><span class="sxs-lookup"><span data-stu-id="d302a-114">The recommended strategy for recovering from an invalid-device error depends on whether the application automatically selects a specific device based on internal requirements or it allows the user to explicitly select a device from a list of available devices.</span></span> 

### <a name="default-audio-device"></a><span data-ttu-id="d302a-115">預設音訊裝置</span><span class="sxs-lookup"><span data-stu-id="d302a-115">Default audio device</span></span>

<span data-ttu-id="d302a-116">如果應用程式自動選取預設裝置，請使用下列步驟來復原。</span><span class="sxs-lookup"><span data-stu-id="d302a-116">If the application automatically selects the default device, use the following steps to recover.</span></span>

1. <span data-ttu-id="d302a-117">釋放 [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) 和 [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) 介面，以及用來呈現的任何其他空間音訊介面。</span><span class="sxs-lookup"><span data-stu-id="d302a-117">Release the [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) and [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interface and any other spatial audio interfaces that are used for rendering.</span></span> 
1. <span data-ttu-id="d302a-118">呼叫 [IMMDeviceEnumerator：： GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 來取得目前的預設音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="d302a-118">Call [IMMDeviceEnumerator::GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the current default audio device.</span></span>
1. <span data-ttu-id="d302a-119">嘗試在音訊裝置上啟用 **ISpatialAudioClient** 。</span><span class="sxs-lookup"><span data-stu-id="d302a-119">Attempt to activate **ISpatialAudioClient** on the audio device.</span></span>
1. <span data-ttu-id="d302a-120">啟動 **ISpatialAudioObjectRenderStream**。</span><span class="sxs-lookup"><span data-stu-id="d302a-120">Activate **ISpatialAudioObjectRenderStream**.</span></span> 

### <a name="specifically-selected-audio-device"></a><span data-ttu-id="d302a-121">特別選取的音訊裝置</span><span class="sxs-lookup"><span data-stu-id="d302a-121">Specifically selected audio device</span></span>

<span data-ttu-id="d302a-122">如果應用程式選取特定音訊裝置，請使用下列步驟來復原。</span><span class="sxs-lookup"><span data-stu-id="d302a-122">If the application selects a specific audio device, use the following steps to recover.</span></span>

1. <span data-ttu-id="d302a-123">釋放 ISpatialAudioObjectRenderStream 介面以及用於轉譯的任何其他空間音訊介面，但不要發行 **ISpatialAudioClient**。</span><span class="sxs-lookup"><span data-stu-id="d302a-123">Release the ISpatialAudioObjectRenderStream interface and any other spatial audio interfaces that are used for rendering, but don't release **ISpatialAudioClient**.</span></span>
1. <span data-ttu-id="d302a-124">使用目前的 **ISpatialAudioClient** 實例來啟用 **ISpatialAudioObjectRenderStream**。</span><span class="sxs-lookup"><span data-stu-id="d302a-124">Use the current **ISpatialAudioClient** instance to activate **ISpatialAudioObjectRenderStream**.</span></span>

<span data-ttu-id="d302a-125">請注意，上述兩個策略都可以將相同的步驟套用至使用 [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) 或 [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) 介面的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d302a-125">Note that for both strategies listed above, the same steps can be applied to applications that use the [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) or [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) interfaces.</span></span> <span data-ttu-id="d302a-126">只要以中繼資料或 Hrtf 介面取代上述步驟中的 **ISpatialAudioObjectRenderStream** 即可。</span><span class="sxs-lookup"><span data-stu-id="d302a-126">Simply replace **ISpatialAudioObjectRenderStream** in the above steps with the metadata or Hrtf interfaces.</span></span>


## <a name="related-topics"></a><span data-ttu-id="d302a-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="d302a-127">Related topics</span></span>

<dl> <span data-ttu-id="d302a-128"><dt>
[從 Invalid-Device 錯誤](recovering-from-an-invalid-device-error.md) 
 中復原[串流管理](stream-management.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="d302a-128"><dt>
[Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md)
[Stream Management](stream-management.md)
</dt> </span></span></dl>

 

 



