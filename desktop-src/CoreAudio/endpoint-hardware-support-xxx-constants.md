---
description: 端點 \_ 硬體 \_ 支援 \_ XXX 常數是音訊端點裝置的硬體支援旗標。
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: 'ENDPOINT_HARDWARE_SUPPORT_XXX 常數 (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111549"
---
# <a name="endpoint_hardware_support_xxx-constants"></a><span data-ttu-id="fe990-103">端點 \_ 硬體 \_ 支援 \_ XXX 常數</span><span class="sxs-lookup"><span data-stu-id="fe990-103">ENDPOINT\_HARDWARE\_SUPPORT\_XXX Constants</span></span>

<span data-ttu-id="fe990-104">端點 \_ 硬體 \_ 支援 \_ XXX 常數是音訊端點裝置的硬體支援旗標。</span><span class="sxs-lookup"><span data-stu-id="fe990-104">The ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants are hardware support flags for an audio endpoint device.</span></span>



| <span data-ttu-id="fe990-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="fe990-105">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="fe990-106">Description</span><span class="sxs-lookup"><span data-stu-id="fe990-106">Description</span></span>                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <span data-ttu-id="fe990-107"><dt>**端點 \_硬體 \_ 支援 \_ 磁片**</dt>區 <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="fe990-107"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_VOLUME**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="fe990-108">音訊端點裝置支援硬體磁片區控制。</span><span class="sxs-lookup"><span data-stu-id="fe990-108">The audio endpoint device supports a hardware volume control.</span></span><br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <span data-ttu-id="fe990-109"><dt>**端點 \_硬體 \_ 支援 \_ 靜音**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="fe990-109"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_MUTE**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="fe990-110">音訊端點裝置支援硬體靜音控制。</span><span class="sxs-lookup"><span data-stu-id="fe990-110">The audio endpoint device supports a hardware mute control.</span></span><br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <span data-ttu-id="fe990-111"><dt>**端點 \_硬體 \_ 支援 \_ 計量表**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="fe990-111"><dt>**ENDPOINT\_HARDWARE\_SUPPORT\_METER**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="fe990-112">音訊端點裝置支援硬體尖峰計量表。</span><span class="sxs-lookup"><span data-stu-id="fe990-112">The audio endpoint device supports a hardware peak meter.</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="fe990-113">備註</span><span class="sxs-lookup"><span data-stu-id="fe990-113">Remarks</span></span>

<span data-ttu-id="fe990-114">[**IAudioEndpointVolume：： QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)和 [**IAudioMeterInformation：： QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)方法會使用端點 \_ 硬體 \_ 支援 \_ XXX 常數。</span><span class="sxs-lookup"><span data-stu-id="fe990-114">The [**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) and [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) methods use the ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span>

<span data-ttu-id="fe990-115">硬體支援遮罩會指出音訊端點裝置在硬體中執行的功能。</span><span class="sxs-lookup"><span data-stu-id="fe990-115">A hardware support mask indicates which functions an audio endpoint device implements in hardware.</span></span> <span data-ttu-id="fe990-116">遮罩可以是0，或一或多個端點 \_ 硬體 \_ 支援 XXX 常數的位 or 組合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fe990-116">The mask can be either 0 or the bitwise-OR combination of one or more ENDPOINT\_HARDWARE\_SUPPORT\_XXX constants.</span></span> <span data-ttu-id="fe990-117">如果在遮罩中設定對應至特定端點 \_ 硬體 \_ 支援 XXX 常數的位，則表示該常數所代表的函式 \_ 會由裝置在硬體中實作為。</span><span class="sxs-lookup"><span data-stu-id="fe990-117">If a bit that corresponds to a particular ENDPOINT\_HARDWARE\_SUPPORT\_XXX constant is set in the mask, then the meaning is that the function represented by that constant is implemented in hardware by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe990-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe990-118">Requirements</span></span>



| <span data-ttu-id="fe990-119">需求</span><span class="sxs-lookup"><span data-stu-id="fe990-119">Requirement</span></span> | <span data-ttu-id="fe990-120">值</span><span class="sxs-lookup"><span data-stu-id="fe990-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe990-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe990-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fe990-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe990-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fe990-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe990-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fe990-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe990-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fe990-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fe990-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe990-126"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe990-126"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe990-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe990-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe990-128">核心音訊常數</span><span class="sxs-lookup"><span data-stu-id="fe990-128">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="fe990-129">**IAudioEndpointVolume::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="fe990-129">**IAudioEndpointVolume::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[<span data-ttu-id="fe990-130">**IAudioMeterInformation::QueryHardwareSupport**</span><span class="sxs-lookup"><span data-stu-id="fe990-130">**IAudioMeterInformation::QueryHardwareSupport**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




