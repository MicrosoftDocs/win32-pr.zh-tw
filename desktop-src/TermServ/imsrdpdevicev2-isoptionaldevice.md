---
title: IMsRdpDeviceV2 IsOptionalDevice 屬性
description: 指定裝置是否為 USB 重新導向的選用裝置。
ms.assetid: a7226c40-7e22-48af-9895-b1fb1f861b58
ms.tgt_platform: multiple
keywords:
- IsOptionalDevice 屬性遠端桌面服務
- IsOptionalDevice 屬性遠端桌面服務，IMsRdpDeviceV2 介面
- IMsRdpDeviceV2 介面遠端桌面服務，IsOptionalDevice 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsOptionalDevice
- IMsRdpDeviceV2.get_IsOptionalDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad0e459a91e88573515128ca37033768f7839ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465992"
---
# <a name="imsrdpdevicev2isoptionaldevice-property"></a><span data-ttu-id="fa54d-106">IMsRdpDeviceV2：： IsOptionalDevice 屬性</span><span class="sxs-lookup"><span data-stu-id="fa54d-106">IMsRdpDeviceV2::IsOptionalDevice property</span></span>

<span data-ttu-id="fa54d-107">指定裝置是否為 USB 重新導向的選用裝置。</span><span class="sxs-lookup"><span data-stu-id="fa54d-107">Specifies if the device is optional for USB redirection.</span></span>

<span data-ttu-id="fa54d-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fa54d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa54d-109">語法</span><span class="sxs-lookup"><span data-stu-id="fa54d-109">Syntax</span></span>


```C++
HRESULT get_IsOptionalDevice(
  [out, retval] VARIANT_BOOL *pvboolOptionalDevice
);
```



## <a name="property-value"></a><span data-ttu-id="fa54d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="fa54d-110">Property value</span></span>

<span data-ttu-id="fa54d-111">如果裝置是選擇性的，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="fa54d-111">**true** if the device is a optional; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa54d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa54d-112">Requirements</span></span>



| <span data-ttu-id="fa54d-113">需求</span><span class="sxs-lookup"><span data-stu-id="fa54d-113">Requirement</span></span> | <span data-ttu-id="fa54d-114">值</span><span class="sxs-lookup"><span data-stu-id="fa54d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa54d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa54d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fa54d-116">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="fa54d-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="fa54d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa54d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fa54d-118">Windows Server 2008 R2 包含 SP1</span><span class="sxs-lookup"><span data-stu-id="fa54d-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="fa54d-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fa54d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa54d-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa54d-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fa54d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="fa54d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa54d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa54d-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fa54d-123">IID</span><span class="sxs-lookup"><span data-stu-id="fa54d-123">IID</span></span><br/>                      | <span data-ttu-id="fa54d-124">IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="fa54d-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="fa54d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa54d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa54d-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="fa54d-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





