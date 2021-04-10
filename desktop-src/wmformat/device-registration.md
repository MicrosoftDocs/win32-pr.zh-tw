---
title: 裝置註冊
description: 裝置註冊
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media Format SDK、裝置註冊
- Windows Media Format SDK，裝置的註冊
- Advanced Systems Format (ASF) 、裝置註冊
- ASF (Advanced 系統格式) 、裝置註冊
- Advanced Systems Format (ASF) 、裝置註冊
- ASF (Advanced 系統格式) 、裝置註冊
- 數位版權管理 (DRM) 、裝置註冊
- DRM (數位版權管理) 、裝置註冊
- 數位版權管理 (DRM) 、裝置註冊
- DRM (數位版權管理) 、裝置註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023040"
---
# <a name="device-registration"></a><span data-ttu-id="ca85a-113">裝置註冊</span><span class="sxs-lookup"><span data-stu-id="ca85a-113">Device Registration</span></span>

<span data-ttu-id="ca85a-114">Windows Media Format SDK 可讓您存取裝置註冊資料庫。</span><span class="sxs-lookup"><span data-stu-id="ca85a-114">The Windows Media Format SDK provides access to the device registration database.</span></span> <span data-ttu-id="ca85a-115">此資料庫會在用戶端電腦上受到保護，並可用於為網路裝置註冊支援 Windows Media DRM 10 的裝置。</span><span class="sxs-lookup"><span data-stu-id="ca85a-115">This database is secured on the client computer and is used to register devices that support Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="ca85a-116">將裝置新增至用戶端電腦所連線的網路時，裝置會嘗試連線到網路裝置發送器應用程式的 Windows Media DRM 10。</span><span class="sxs-lookup"><span data-stu-id="ca85a-116">When a device is added to a network to which the client computer is connected, the device attempts to contact a Windows Media DRM 10 for Network Devices transmitter application.</span></span> <span data-ttu-id="ca85a-117">建立通訊之後，裝置會傳送註冊要求訊息。</span><span class="sxs-lookup"><span data-stu-id="ca85a-117">After establishing communications, the device sends a registration request message.</span></span>

<span data-ttu-id="ca85a-118">當您的應用程式收到註冊要求訊息時，應該執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="ca85a-118">Your application should perform the following steps when it receives a registration request message:</span></span>

1.  <span data-ttu-id="ca85a-119">藉由呼叫 [**IWMDRMMessageParser：:P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) 方法來剖析訊息。</span><span class="sxs-lookup"><span data-stu-id="ca85a-119">Parse the message by calling the [**IWMDRMMessageParser::ParseRegistrationReqMsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) method.</span></span> <span data-ttu-id="ca85a-120">這個方法會抓取裝置憑證和裝置序號，這兩者都需要識別裝置。</span><span class="sxs-lookup"><span data-stu-id="ca85a-120">This method retrieves the device certificate and the device serial number, both of which are needed to identify the device.</span></span>
2.  <span data-ttu-id="ca85a-121">呼叫 [**IWMDeviceRegistration：： GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) 方法，並傳入在步驟1中取出的憑證和裝置序號。</span><span class="sxs-lookup"><span data-stu-id="ca85a-121">Call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method, passing in the certificate and device serial number retrieved in step 1.</span></span> <span data-ttu-id="ca85a-122">如果找到裝置，則該裝置已註冊，您可以略過下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="ca85a-122">If the device is found, it is already registered and you can skip the next step.</span></span>
3.  <span data-ttu-id="ca85a-123">呼叫 [**IWMDeviceRegistration：： >registerdevice.js**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) 方法，將裝置新增至裝置註冊資料庫。</span><span class="sxs-lookup"><span data-stu-id="ca85a-123">Call the [**IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) method to add the device to the device registration database.</span></span>

<span data-ttu-id="ca85a-124">您可以藉由取出與其相關聯的已註冊裝置物件，來存取註冊資料庫中任何裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ca85a-124">You can access information about any device in the registration database by retrieving the registered device object associated with it.</span></span> <span data-ttu-id="ca85a-125">有兩種方式可取得已註冊的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="ca85a-125">There are two ways to get a registered device object.</span></span> <span data-ttu-id="ca85a-126">如果您有裝置的憑證和序號，您可以呼叫 [**IWMDeviceRegistration：： GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) 方法。</span><span class="sxs-lookup"><span data-stu-id="ca85a-126">If you have the certificate and serial number of the device, you can call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method.</span></span> <span data-ttu-id="ca85a-127">如果您沒有裝置的憑證和序號，您可以藉由呼叫 IWMDeviceRegistration：： GetFirstRegisteredDevice 來列舉資料庫中的所有裝置，然後呼叫 [**：：**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) ，然後再呼叫 [**IWMDeviceRegistration：： GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) ，直到呼叫傳回 S \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="ca85a-127">If you do not have the certificate and serial number of the device, you can enumerate all the devices in the database by calling [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) followed by repeated calls to [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) until a call returns S\_FALSE.</span></span>

<span data-ttu-id="ca85a-128">在您的應用程式可以將資料傳送至裝置之前，您必須確定裝置已通過核准、驗證並開啟。</span><span class="sxs-lookup"><span data-stu-id="ca85a-128">Before your application can send data to a device, you must ensure that the device is approved, validated, and open.</span></span>

<span data-ttu-id="ca85a-129">裝置核准應牽涉到與使用者的互動。</span><span class="sxs-lookup"><span data-stu-id="ca85a-129">Device approval should involve interaction with the user.</span></span> <span data-ttu-id="ca85a-130">當裝置傳送註冊訊息時，您的應用程式可以提示使用者決定裝置是否為應該接收該使用者資料的裝置。</span><span class="sxs-lookup"><span data-stu-id="ca85a-130">When a device sends a registration message, your application can prompt the user to decide whether the device is one that should receive that user's data.</span></span> <span data-ttu-id="ca85a-131">然後，藉由呼叫 [**IWMRegisteredDevice：：核准**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) 方法來更新裝置註冊資料庫，並適當地傳遞 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ca85a-131">Then update the device registration database by calling the [**IWMRegisteredDevice::Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) method, passing **TRUE** or **FALSE** as appropriate.</span></span>

<span data-ttu-id="ca85a-132">驗證也稱為鄰近偵測。</span><span class="sxs-lookup"><span data-stu-id="ca85a-132">Validation is also called proximity detection.</span></span> <span data-ttu-id="ca85a-133">這是 Windows Media 格式 SDK 的內部 DRM 物件在執行應用程式以安全傳輸媒體時，所用的程式，可判斷裝置是否「接近」。</span><span class="sxs-lookup"><span data-stu-id="ca85a-133">This is a process by which the internal DRM objects of the Windows Media Format SDK determine whether the device is "near" enough to the computer running your application to securely transmit media.</span></span> <span data-ttu-id="ca85a-134">Nearness 是由取得訊息回應所需的時間來決定。</span><span class="sxs-lookup"><span data-stu-id="ca85a-134">Nearness is determined by the time it takes to get a response to a message.</span></span> <span data-ttu-id="ca85a-135">這項功能的目的是要防止未經授權的使用者存取您的網路，並取得安全的媒體。</span><span class="sxs-lookup"><span data-stu-id="ca85a-135">This feature is intended to prevent unauthorized users from accessing your network and obtaining your secured media.</span></span> <span data-ttu-id="ca85a-136">如需詳細資訊，請參閱 [執行鄰近性偵測](performing-proximity-detection.md)。</span><span class="sxs-lookup"><span data-stu-id="ca85a-136">For more information, see [Performing Proximity Detection](performing-proximity-detection.md).</span></span>

<span data-ttu-id="ca85a-137">若要開啟裝置，請呼叫 [**IWMRegisteredDevice：： open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open)。</span><span class="sxs-lookup"><span data-stu-id="ca85a-137">To open a device, call [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span></span>

> [!Note]  
> <span data-ttu-id="ca85a-138">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="ca85a-138">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ca85a-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca85a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca85a-140">**IWMRegisteredDevice**</span><span class="sxs-lookup"><span data-stu-id="ca85a-140">**IWMRegisteredDevice**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[<span data-ttu-id="ca85a-141">**使用 Windows Media DRM 10 進行網路裝置通訊協定**</span><span class="sxs-lookup"><span data-stu-id="ca85a-141">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




