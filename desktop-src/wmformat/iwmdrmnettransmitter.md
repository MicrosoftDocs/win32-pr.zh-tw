---
title: IWMDRMNetTransmitter 介面
description: IWMDRMNetTransmitter 介面提供了使用網路裝置的 Windows Media DRM 作為傳輸器所需的方法。若要取得這個介面的實例，請呼叫 IWMDRMProvider CreateObject。 將 IID \_ IWMDRMNetTransmitter 傳遞為 riid 參數。
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- IWMDRMNetTransmitter 介面 windows 媒體格式
- IWMDRMNetTransmitter 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315754"
---
# <a name="iwmdrmnettransmitter-interface"></a><span data-ttu-id="3b4ba-106">IWMDRMNetTransmitter 介面</span><span class="sxs-lookup"><span data-stu-id="3b4ba-106">IWMDRMNetTransmitter interface</span></span>

<span data-ttu-id="3b4ba-107">**IWMDRMNetTransmitter** 介面提供了使用網路裝置的 WINDOWS Media DRM 作為傳輸器所需的方法。</span><span class="sxs-lookup"><span data-stu-id="3b4ba-107">The **IWMDRMNetTransmitter** interface provides methods needed to use Windows Media DRM for Network Devices as a transmitter.</span></span>

<span data-ttu-id="3b4ba-108">若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。</span><span class="sxs-lookup"><span data-stu-id="3b4ba-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="3b4ba-109">將 **IID \_ IWMDRMNetTransmitter** 傳遞為 *riid* 參數。</span><span class="sxs-lookup"><span data-stu-id="3b4ba-109">Pass **IID\_IWMDRMNetTransmitter** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="3b4ba-110">成員</span><span class="sxs-lookup"><span data-stu-id="3b4ba-110">Members</span></span>

<span data-ttu-id="3b4ba-111">**IWMDRMNetTransmitter** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="3b4ba-111">The **IWMDRMNetTransmitter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3b4ba-112">**IWMDRMNetTransmitter** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3b4ba-112">**IWMDRMNetTransmitter** also has these types of members:</span></span>

-   [<span data-ttu-id="3b4ba-113">方法</span><span class="sxs-lookup"><span data-stu-id="3b4ba-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3b4ba-114">方法</span><span class="sxs-lookup"><span data-stu-id="3b4ba-114">Methods</span></span>

<span data-ttu-id="3b4ba-115">**IWMDRMNetTransmitter** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3b4ba-115">The **IWMDRMNetTransmitter** interface has these methods.</span></span>



| <span data-ttu-id="3b4ba-116">方法</span><span class="sxs-lookup"><span data-stu-id="3b4ba-116">Method</span></span>                                                                        | <span data-ttu-id="3b4ba-117">描述</span><span class="sxs-lookup"><span data-stu-id="3b4ba-117">Description</span></span>                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b4ba-118">**GetLeafLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="3b4ba-118">**GetLeafLicenseResponse**</span></span>](iwmdrmnettransmitter-getleaflicenseresponse.md) | <span data-ttu-id="3b4ba-119">產生分葉授權回應訊息。</span><span class="sxs-lookup"><span data-stu-id="3b4ba-119">Generates a leaf license response message.</span></span><br/>                                                       |
| [<span data-ttu-id="3b4ba-120">**GetRootLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="3b4ba-120">**GetRootLicenseResponse**</span></span>](iwmdrmnettransmitter-getrootlicenseresponse.md) | <span data-ttu-id="3b4ba-121">產生根授權回應訊息</span><span class="sxs-lookup"><span data-stu-id="3b4ba-121">Generates a root license response message</span></span><br/>                                                        |
| [<span data-ttu-id="3b4ba-122">**SetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="3b4ba-122">**SetLicenseChallenge**</span></span>](iwmdrmnettransmitter-setlicensechallenge.md)       | <span data-ttu-id="3b4ba-123">處理 Microsoft Windows Media DRM 為網路裝置接收器傳送的授權挑戰</span><span class="sxs-lookup"><span data-stu-id="3b4ba-123">Processes a license challenge sent by a Microsoft Windows Media DRM for Network Devices receiver</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="3b4ba-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b4ba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b4ba-125">**介面**</span><span class="sxs-lookup"><span data-stu-id="3b4ba-125">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3b4ba-126">**IWMDRMNetReceiver 介面**</span><span class="sxs-lookup"><span data-stu-id="3b4ba-126">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> </dl>

 

