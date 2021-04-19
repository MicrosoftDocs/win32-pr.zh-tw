---
title: IMsRdpDeviceV2 CmDeviceInstance 屬性
description: 包含裝置的 configuration manager 裝置實例。
ms.assetid: 2a3e7001-7889-417f-8f9d-cc7a1776249f
ms.tgt_platform: multiple
keywords:
- CmDeviceInstance 屬性遠端桌面服務
- CmDeviceInstance 屬性遠端桌面服務，IMsRdpDeviceV2 介面
- IMsRdpDeviceV2 介面遠端桌面服務，CmDeviceInstance 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmDeviceInstance
- IMsRdpDeviceV2.get_CmDeviceInstance
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec036d5e2497f45fff389ec8af457a05fcc9fef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967947"
---
# <a name="imsrdpdevicev2cmdeviceinstance-property"></a><span data-ttu-id="ce778-106">IMsRdpDeviceV2：： CmDeviceInstance 屬性</span><span class="sxs-lookup"><span data-stu-id="ce778-106">IMsRdpDeviceV2::CmDeviceInstance property</span></span>

<span data-ttu-id="ce778-107">包含裝置的 configuration manager 裝置實例。</span><span class="sxs-lookup"><span data-stu-id="ce778-107">Contains the configuration manager device instance of the device.</span></span>

<span data-ttu-id="ce778-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ce778-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce778-109">語法</span><span class="sxs-lookup"><span data-stu-id="ce778-109">Syntax</span></span>


```C++
HRESULT get_CmDeviceInstance(
  [out, retval] DWORD *pCmDeviceInstance
);
```



## <a name="property-value"></a><span data-ttu-id="ce778-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ce778-110">Property value</span></span>

<span data-ttu-id="ce778-111">裝置的 configuration manager 裝置實例。</span><span class="sxs-lookup"><span data-stu-id="ce778-111">The configuration manager device instance of the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce778-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce778-112">Requirements</span></span>



| <span data-ttu-id="ce778-113">需求</span><span class="sxs-lookup"><span data-stu-id="ce778-113">Requirement</span></span> | <span data-ttu-id="ce778-114">值</span><span class="sxs-lookup"><span data-stu-id="ce778-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce778-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce778-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ce778-116">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="ce778-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="ce778-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce778-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ce778-118">Windows Server 2008 R2 包含 SP1</span><span class="sxs-lookup"><span data-stu-id="ce778-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="ce778-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ce778-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce778-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce778-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ce778-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ce778-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce778-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce778-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ce778-123">IID</span><span class="sxs-lookup"><span data-stu-id="ce778-123">IID</span></span><br/>                      | <span data-ttu-id="ce778-124">IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="ce778-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="ce778-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce778-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce778-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="ce778-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





