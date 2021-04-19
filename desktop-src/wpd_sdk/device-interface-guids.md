---
description: 您可以使用 GUID 值來描述裝置介面。 Windows 可攜式裝置會定義下列裝置介面。
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: '裝置介面 Guid (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977555"
---
# <a name="device-interface-guids"></a><span data-ttu-id="97d19-104">裝置介面 Guid</span><span class="sxs-lookup"><span data-stu-id="97d19-104">Device Interface GUIDs</span></span>

<span data-ttu-id="97d19-105">您可以使用 **GUID** 值來描述裝置介面。</span><span class="sxs-lookup"><span data-stu-id="97d19-105">The device interface can be described by a **GUID** value.</span></span> <span data-ttu-id="97d19-106">Windows 可攜式裝置會定義下列裝置介面。</span><span class="sxs-lookup"><span data-stu-id="97d19-106">Windows Portable Devices defines the following device interface.</span></span>



| <span data-ttu-id="97d19-107">常數</span><span class="sxs-lookup"><span data-stu-id="97d19-107">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="97d19-108">描述</span><span class="sxs-lookup"><span data-stu-id="97d19-108">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <span data-ttu-id="97d19-109"><dt>**GUID \_ DEVINTERFACE \_ WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="97d19-109"><dt>**GUID\_DEVINTERFACE\_WPD**</dt></span></span> </dl>                          | <span data-ttu-id="97d19-110">識別出現在一般 WPD 列舉中的裝置。</span><span class="sxs-lookup"><span data-stu-id="97d19-110">Identifies devices that appear in a normal WPD enumeration.</span></span> <span data-ttu-id="97d19-111">當應用程式呼叫 [**IPortableDeviceManager：： GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) 方法時，將會列舉任何註冊此介面 GUID 的裝置。</span><span class="sxs-lookup"><span data-stu-id="97d19-111">Any device that registers this interface GUID will be enumerated when an application calls the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.</span></span><br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <span data-ttu-id="97d19-112"><dt>**GUID \_ DEVINTERFACE \_ WPD \_ 私用**</dt></span><span class="sxs-lookup"><span data-stu-id="97d19-112"><dt>**GUID\_DEVINTERFACE\_WPD\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="97d19-113">識別不會在一般 WPD 列舉期間出現的裝置。</span><span class="sxs-lookup"><span data-stu-id="97d19-113">Identifies devices that will not appear during a normal WPD enumeration.</span></span> <span data-ttu-id="97d19-114">只有當應用程式呼叫 [**IPortableDeviceManager：： GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) 方法時，才會列舉任何註冊此介面 GUID 的裝置。</span><span class="sxs-lookup"><span data-stu-id="97d19-114">Any device that registers this interface GUID will be enumerated only when an application calls the [**IPortableDeviceManager::GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) method.</span></span><br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <span data-ttu-id="97d19-115"><dt>**GUID \_ DEVINTERFACE \_ WPD \_ 服務**</dt></span><span class="sxs-lookup"><span data-stu-id="97d19-115"><dt>**GUID\_DEVINTERFACE\_WPD\_SERVICE**</dt></span></span> </dl> | <span data-ttu-id="97d19-116">在 Windows 7 中，應用程式可以藉由呼叫 [**IPortableDeviceServiceManager：： GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) ，並使用此介面類別別做為服務類型 GUID，來列舉所有 WPD 的裝置服務。</span><span class="sxs-lookup"><span data-stu-id="97d19-116">In Windows 7, applications can enumerate all WPD device services by calling [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) and using this interface class as the service-type GUID.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="97d19-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="97d19-117">Requirements</span></span>



| <span data-ttu-id="97d19-118">需求</span><span class="sxs-lookup"><span data-stu-id="97d19-118">Requirement</span></span> | <span data-ttu-id="97d19-119">值</span><span class="sxs-lookup"><span data-stu-id="97d19-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="97d19-120">標頭</span><span class="sxs-lookup"><span data-stu-id="97d19-120">Header</span></span><br/> | <dl> <span data-ttu-id="97d19-121"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="97d19-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97d19-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97d19-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d19-123">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="97d19-123">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




