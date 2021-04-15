---
description: PKEY \_ AudioEndpoint \_ FormFactor 屬性會指定音訊端點裝置的外型規格。 外型規格表示使用者操作之音訊端點裝置的實體屬性。
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: 'PKEY_AudioEndpoint_FormFactor (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468428"
---
# <a name="pkey_audioendpoint_formfactor"></a><span data-ttu-id="49b11-104">PKEY \_ AudioEndpoint \_ FormFactor</span><span class="sxs-lookup"><span data-stu-id="49b11-104">PKEY\_AudioEndpoint\_FormFactor</span></span>

<span data-ttu-id="49b11-105">**PKEY \_ AudioEndpoint \_ FormFactor** 屬性會指定音訊端點裝置的外型規格。</span><span class="sxs-lookup"><span data-stu-id="49b11-105">The **PKEY\_AudioEndpoint\_FormFactor** property specifies the form factor of the audio endpoint device.</span></span> <span data-ttu-id="49b11-106">外型規格表示使用者操作之音訊端點裝置的實體屬性。</span><span class="sxs-lookup"><span data-stu-id="49b11-106">The form factor indicates the physical attributes of the audio endpoint device that the user manipulates.</span></span>

<span data-ttu-id="49b11-107">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ UI4。</span><span class="sxs-lookup"><span data-stu-id="49b11-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="49b11-108">**PROPVARIANT** 結構的 **uintVal** 成員包含轉換成 UINT 類型的列舉值。</span><span class="sxs-lookup"><span data-stu-id="49b11-108">The **uintVal** member of the **PROPVARIANT** structure contains an enumeration value that is cast to type UINT.</span></span> <span data-ttu-id="49b11-109">它會設定為下列其中一個 [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) 列舉值：</span><span class="sxs-lookup"><span data-stu-id="49b11-109">It is set to one of the following [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) enumeration values:</span></span>

-   <span data-ttu-id="49b11-110">RemoteNetworkDevice</span><span class="sxs-lookup"><span data-stu-id="49b11-110">RemoteNetworkDevice</span></span>
-   <span data-ttu-id="49b11-111">Speakers</span><span class="sxs-lookup"><span data-stu-id="49b11-111">Speakers</span></span>
-   <span data-ttu-id="49b11-112">LineLevel</span><span class="sxs-lookup"><span data-stu-id="49b11-112">LineLevel</span></span>
-   <span data-ttu-id="49b11-113">耳機</span><span class="sxs-lookup"><span data-stu-id="49b11-113">Headphones</span></span>
-   <span data-ttu-id="49b11-114">麥克風</span><span class="sxs-lookup"><span data-stu-id="49b11-114">Microphone</span></span>
-   <span data-ttu-id="49b11-115">Headset</span><span class="sxs-lookup"><span data-stu-id="49b11-115">Headset</span></span>
-   <span data-ttu-id="49b11-116">手機</span><span class="sxs-lookup"><span data-stu-id="49b11-116">Handset</span></span>
-   <span data-ttu-id="49b11-117">UnknownDigitalPassthrough</span><span class="sxs-lookup"><span data-stu-id="49b11-117">UnknownDigitalPassthrough</span></span>
-   <span data-ttu-id="49b11-118">後部</span><span class="sxs-lookup"><span data-stu-id="49b11-118">SPDIF</span></span>
-   <span data-ttu-id="49b11-119">HDMI</span><span class="sxs-lookup"><span data-stu-id="49b11-119">HDMI</span></span>
-   <span data-ttu-id="49b11-120">UnknownFormFactor</span><span class="sxs-lookup"><span data-stu-id="49b11-120">UnknownFormFactor</span></span>

## <a name="requirements"></a><span data-ttu-id="49b11-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="49b11-121">Requirements</span></span>



| <span data-ttu-id="49b11-122">需求</span><span class="sxs-lookup"><span data-stu-id="49b11-122">Requirement</span></span> | <span data-ttu-id="49b11-123">值</span><span class="sxs-lookup"><span data-stu-id="49b11-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="49b11-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49b11-124">Minimum supported client</span></span><br/> | <span data-ttu-id="49b11-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49b11-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="49b11-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49b11-126">Minimum supported server</span></span><br/> | <span data-ttu-id="49b11-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49b11-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="49b11-128">標頭</span><span class="sxs-lookup"><span data-stu-id="49b11-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="49b11-129"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="49b11-129"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49b11-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49b11-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b11-131">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="49b11-131">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="49b11-132">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="49b11-132">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




