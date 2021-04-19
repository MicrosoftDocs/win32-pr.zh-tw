---
description: 設備磁碟機會使用 IWpdSerializer 介面，將 IPortableDeviceValues 介面序列化為與應用程式通訊所用的原始資料緩衝區。應用程式不需要使用此介面，因為資料會在呼叫 IPortableDevice：： SendCommand 時自動序列化和還原序列化。若要取得此介面，請呼叫 CoCreateInstance 並傳入 IID \_ IWpdSerializer。
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: 'IWpdSerializer 介面 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978802"
---
# <a name="iwpdserializer-interface"></a><span data-ttu-id="f0e0a-103">IWpdSerializer 介面</span><span class="sxs-lookup"><span data-stu-id="f0e0a-103">IWpdSerializer interface</span></span>

<span data-ttu-id="f0e0a-104">設備磁碟機會使用 **IWpdSerializer** 介面，將 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面序列化為與應用程式通訊所用的原始資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f0e0a-104">The **IWpdSerializer** interface is used by the device driver to serialize [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces to and from the raw data buffers used to communicate with the application.</span></span>

<span data-ttu-id="f0e0a-105">應用程式不需要使用此介面，因為資料會在呼叫 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)時自動序列化和還原序列化。</span><span class="sxs-lookup"><span data-stu-id="f0e0a-105">Applications do not need to use this interface, because the data is serialized and deserialized automatically when calling [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

<span data-ttu-id="f0e0a-106">若要取得此介面，請呼叫 **CoCreateInstance** 並傳入 **IID \_ IWpdSerializer**。</span><span class="sxs-lookup"><span data-stu-id="f0e0a-106">To get this interface, call **CoCreateInstance** and pass in **IID\_IWpdSerializer**.</span></span>

## <a name="members"></a><span data-ttu-id="f0e0a-107">成員</span><span class="sxs-lookup"><span data-stu-id="f0e0a-107">Members</span></span>

<span data-ttu-id="f0e0a-108">**IWpdSerializer** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="f0e0a-108">The **IWpdSerializer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f0e0a-109">**IWpdSerializer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f0e0a-109">**IWpdSerializer** also has these types of members:</span></span>

-   [<span data-ttu-id="f0e0a-110">方法</span><span class="sxs-lookup"><span data-stu-id="f0e0a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f0e0a-111">方法</span><span class="sxs-lookup"><span data-stu-id="f0e0a-111">Methods</span></span>

<span data-ttu-id="f0e0a-112">**IWpdSerializer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f0e0a-112">The **IWpdSerializer** interface has these methods.</span></span>



| <span data-ttu-id="f0e0a-113">方法</span><span class="sxs-lookup"><span data-stu-id="f0e0a-113">Method</span></span>                                                                                          | <span data-ttu-id="f0e0a-114">描述</span><span class="sxs-lookup"><span data-stu-id="f0e0a-114">Description</span></span>                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0e0a-115">**GetBufferFromIPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f0e0a-115">**GetBufferFromIPortableDeviceValues**</span></span>](iwpdserializer-getbufferfromiportabledevicevalues.md) | <span data-ttu-id="f0e0a-116">將提交的 **IPortableDeviceValues** 介面序列化為配置的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="f0e0a-116">Serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span><br/>                |
| [<span data-ttu-id="f0e0a-117">**GetIPortableDeviceValuesFromBuffer**</span><span class="sxs-lookup"><span data-stu-id="f0e0a-117">**GetIPortableDeviceValuesFromBuffer**</span></span>](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | <span data-ttu-id="f0e0a-118">將位元組陣列還原序列化為 **IPortableDeviceValues** 介面。</span><span class="sxs-lookup"><span data-stu-id="f0e0a-118">Deserializes a byte array to an **IPortableDeviceValues** interface.</span></span><br/>                                  |
| [<span data-ttu-id="f0e0a-119">**GetSerializedSize**</span><span class="sxs-lookup"><span data-stu-id="f0e0a-119">**GetSerializedSize**</span></span>](iwpdserializer-getserializedsize.md)                                   | <span data-ttu-id="f0e0a-120">計算保存序列化 **IPortableDeviceValues** 介面所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="f0e0a-120">Calculates the buffer size that is required to hold a serialized **IPortableDeviceValues** interface.</span></span><br/> |
| [<span data-ttu-id="f0e0a-121">**WriteIPortableDeviceValuesToBuffer**</span><span class="sxs-lookup"><span data-stu-id="f0e0a-121">**WriteIPortableDeviceValuesToBuffer**</span></span>](iwpdserializer-writeiportabledevicevaluestobuffer.md) | <span data-ttu-id="f0e0a-122">將 **IPortableDeviceValues** 介面序列化為呼叫端配置的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="f0e0a-122">Serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="f0e0a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0e0a-123">Requirements</span></span>



| <span data-ttu-id="f0e0a-124">需求</span><span class="sxs-lookup"><span data-stu-id="f0e0a-124">Requirement</span></span> | <span data-ttu-id="f0e0a-125">值</span><span class="sxs-lookup"><span data-stu-id="f0e0a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e0a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f0e0a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f0e0a-127"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0e0a-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0e0a-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="f0e0a-128">Library</span></span><br/> | <dl> <span data-ttu-id="f0e0a-129"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0e0a-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0e0a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0e0a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e0a-131">**驅動程式介面**</span><span class="sxs-lookup"><span data-stu-id="f0e0a-131">**Driver Interfaces**</span></span>](driver-interfaces.md)
</dt> </dl>

 

