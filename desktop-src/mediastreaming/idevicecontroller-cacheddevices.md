---
title: IDeviceController CachedDevices 方法
description: 抓取 IBasicDevice 介面指標的集合，表示所有可探索的 DLNA 裝置的快取視圖。 |IDeviceController CachedDevices 方法
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- CachedDevices 方法媒體串流 API
- CachedDevices 方法媒體串流 API，IDeviceController 介面
- IDeviceController 介面媒體串流 API，CachedDevices 方法
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103946016"
---
# <a name="idevicecontrollercacheddevices-method"></a><span data-ttu-id="a9424-107">IDeviceController：： CachedDevices 方法</span><span class="sxs-lookup"><span data-stu-id="a9424-107">IDeviceController::CachedDevices method</span></span>

<span data-ttu-id="a9424-108">抓取 [**IBasicDevice**](ibasicdevice.md) 介面指標的集合，表示所有可探索的 DLNA 裝置的快取視圖。</span><span class="sxs-lookup"><span data-stu-id="a9424-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9424-109">語法</span><span class="sxs-lookup"><span data-stu-id="a9424-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="a9424-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9424-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9424-111">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a9424-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9424-112">接收 [**IBasicDevice**](ibasicdevice.md) 介面指標的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="a9424-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9424-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9424-113">Return value</span></span>

<span data-ttu-id="a9424-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="a9424-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a9424-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="a9424-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a9424-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a9424-116">Return code</span></span>                                                                          | <span data-ttu-id="a9424-117">Description</span><span class="sxs-lookup"><span data-stu-id="a9424-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a9424-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a9424-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a9424-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="a9424-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a9424-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9424-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9424-121">**IDeviceController**</span><span class="sxs-lookup"><span data-stu-id="a9424-121">**IDeviceController**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

