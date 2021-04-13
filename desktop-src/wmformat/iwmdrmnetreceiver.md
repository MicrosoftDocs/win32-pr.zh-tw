---
title: IWMDRMNetReceiver 介面
description: IWMDRMNetReceiver 介面提供使用 Microsoft Windows Media DRM 做為接收器的網路裝置所需的方法。若要取得這個介面的實例，請呼叫 IWMDRMProvider CreateObject。 將 IID \_ IWMDRMNetReceiver 傳遞為 riid 參數。
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- IWMDRMNetReceiver 介面 windows 媒體格式
- IWMDRMNetReceiver 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373397"
---
# <a name="iwmdrmnetreceiver-interface"></a><span data-ttu-id="7ab44-106">IWMDRMNetReceiver 介面</span><span class="sxs-lookup"><span data-stu-id="7ab44-106">IWMDRMNetReceiver interface</span></span>

<span data-ttu-id="7ab44-107">**IWMDRMNetReceiver** 介面提供使用 Microsoft WINDOWS Media DRM 做為接收器的網路裝置所需的方法。</span><span class="sxs-lookup"><span data-stu-id="7ab44-107">The **IWMDRMNetReceiver** interface provides methods needed to use Microsoft Windows Media DRM for Network Devices as a receiver.</span></span>

<span data-ttu-id="7ab44-108">若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。</span><span class="sxs-lookup"><span data-stu-id="7ab44-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="7ab44-109">將 **IID \_ IWMDRMNetReceiver** 傳遞為 *riid* 參數。</span><span class="sxs-lookup"><span data-stu-id="7ab44-109">Pass **IID\_IWMDRMNetReceiver** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="7ab44-110">成員</span><span class="sxs-lookup"><span data-stu-id="7ab44-110">Members</span></span>

<span data-ttu-id="7ab44-111">**IWMDRMNetReceiver** 介面繼承自 [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)。</span><span class="sxs-lookup"><span data-stu-id="7ab44-111">The **IWMDRMNetReceiver** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="7ab44-112">**IWMDRMNetReceiver** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7ab44-112">**IWMDRMNetReceiver** also has these types of members:</span></span>

-   [<span data-ttu-id="7ab44-113">方法</span><span class="sxs-lookup"><span data-stu-id="7ab44-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7ab44-114">方法</span><span class="sxs-lookup"><span data-stu-id="7ab44-114">Methods</span></span>

<span data-ttu-id="7ab44-115">**IWMDRMNetReceiver** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7ab44-115">The **IWMDRMNetReceiver** interface has these methods.</span></span>



| <span data-ttu-id="7ab44-116">方法</span><span class="sxs-lookup"><span data-stu-id="7ab44-116">Method</span></span>                                                                               | <span data-ttu-id="7ab44-117">描述</span><span class="sxs-lookup"><span data-stu-id="7ab44-117">Description</span></span>                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ab44-118">**GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="7ab44-118">**GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)                 | <span data-ttu-id="7ab44-119">產生當要求受保護的內容時，傳送給發送器的授權挑戰。</span><span class="sxs-lookup"><span data-stu-id="7ab44-119">Generates a license challenge that is sent to the transmitter when requesting protected content.</span></span><br/>                     |
| [<span data-ttu-id="7ab44-120">**GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="7ab44-120">**GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)       | <span data-ttu-id="7ab44-121">產生註冊挑戰，在接收者註冊或重新驗證時傳送給發送器。</span><span class="sxs-lookup"><span data-stu-id="7ab44-121">Generates a registration challenge that is sent to the transmitter when the receiver is registering or revalidating.</span></span><br/> |
| [<span data-ttu-id="7ab44-122">**ProcessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="7ab44-122">**ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)           | <span data-ttu-id="7ab44-123">處理傳輸器在回復至授權挑戰時傳送的授權回應。</span><span class="sxs-lookup"><span data-stu-id="7ab44-123">Processes the license response sent by the transmitter in reply to a license challenge.</span></span><br/>                              |
| [<span data-ttu-id="7ab44-124">**ProcessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="7ab44-124">**ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md) | <span data-ttu-id="7ab44-125">處理傳輸器在回復註冊挑戰時傳送的註冊回應。</span><span class="sxs-lookup"><span data-stu-id="7ab44-125">Processes the registration response sent by the transmitter in reply to a registration challenge.</span></span><br/>                    |



 

## <a name="see-also"></a><span data-ttu-id="7ab44-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ab44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab44-127">**介面**</span><span class="sxs-lookup"><span data-stu-id="7ab44-127">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7ab44-128">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="7ab44-128">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> <dt>

[<span data-ttu-id="7ab44-129">**IWMDRMNetTransmitter 介面**</span><span class="sxs-lookup"><span data-stu-id="7ab44-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





