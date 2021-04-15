---
title: IMsRdpDeviceV2 IsUSBDevice 屬性
description: 指定裝置是否用於 USB 重新導向。
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- IsUSBDevice 屬性遠端桌面服務
- IsUSBDevice 屬性遠端桌面服務，IMsRdpDeviceV2 介面
- IMsRdpDeviceV2 介面遠端桌面服務，IsUSBDevice 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3741972fdd81887713e75ed5b596e0ba1a10fd3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383877"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a><span data-ttu-id="9909f-106">IMsRdpDeviceV2：： IsUSBDevice 屬性</span><span class="sxs-lookup"><span data-stu-id="9909f-106">IMsRdpDeviceV2::IsUSBDevice property</span></span>

<span data-ttu-id="9909f-107">指定裝置是否用於 USB 重新導向。</span><span class="sxs-lookup"><span data-stu-id="9909f-107">Specifies if the device is for USB redirection.</span></span>

<span data-ttu-id="9909f-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9909f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9909f-109">語法</span><span class="sxs-lookup"><span data-stu-id="9909f-109">Syntax</span></span>


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a><span data-ttu-id="9909f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9909f-110">Property value</span></span>

<span data-ttu-id="9909f-111">如果裝置適用于 USB 重新導向，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="9909f-111">**true** if the device is for USB redirection; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9909f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9909f-112">Requirements</span></span>



| <span data-ttu-id="9909f-113">需求</span><span class="sxs-lookup"><span data-stu-id="9909f-113">Requirement</span></span> | <span data-ttu-id="9909f-114">值</span><span class="sxs-lookup"><span data-stu-id="9909f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9909f-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9909f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9909f-116">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="9909f-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="9909f-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9909f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9909f-118">Windows Server 2008 R2 包含 SP1</span><span class="sxs-lookup"><span data-stu-id="9909f-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="9909f-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9909f-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="9909f-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9909f-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9909f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9909f-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9909f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9909f-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9909f-123">IID</span><span class="sxs-lookup"><span data-stu-id="9909f-123">IID</span></span><br/>                      | <span data-ttu-id="9909f-124">IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="9909f-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="9909f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9909f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9909f-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="9909f-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





