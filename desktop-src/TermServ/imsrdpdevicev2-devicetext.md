---
title: IMsRdpDeviceV2 DeviceText 屬性
description: 包含裝置文字。
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- DeviceText 屬性遠端桌面服務
- DeviceText 屬性遠端桌面服務，IMsRdpDeviceV2 介面
- IMsRdpDeviceV2 介面遠端桌面服務，DeviceText 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DeviceText
- IMsRdpDeviceV2.get_DeviceText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb35142a166db7e7c05fa5c0f00f7fdf2e1219c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187275"
---
# <a name="imsrdpdevicev2devicetext-property"></a><span data-ttu-id="e447c-106">IMsRdpDeviceV2：:D eviceText 屬性</span><span class="sxs-lookup"><span data-stu-id="e447c-106">IMsRdpDeviceV2::DeviceText property</span></span>

<span data-ttu-id="e447c-107">包含裝置文字。</span><span class="sxs-lookup"><span data-stu-id="e447c-107">Contains the device text.</span></span> <span data-ttu-id="e447c-108">這是 Windows 向使用者顯示的名稱。</span><span class="sxs-lookup"><span data-stu-id="e447c-108">This is the name that Windows displays to the user.</span></span>

<span data-ttu-id="e447c-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e447c-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e447c-110">語法</span><span class="sxs-lookup"><span data-stu-id="e447c-110">Syntax</span></span>


```C++
HRESULT get_DeviceText(
  [out, retval] BSTR *pDeviceText
);
```



## <a name="property-value"></a><span data-ttu-id="e447c-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="e447c-111">Property value</span></span>

<span data-ttu-id="e447c-112">裝置的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e447c-112">The display name for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="e447c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e447c-113">Requirements</span></span>



| <span data-ttu-id="e447c-114">需求</span><span class="sxs-lookup"><span data-stu-id="e447c-114">Requirement</span></span> | <span data-ttu-id="e447c-115">值</span><span class="sxs-lookup"><span data-stu-id="e447c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e447c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e447c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e447c-117">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="e447c-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="e447c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e447c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e447c-119">Windows Server 2008 R2 包含 SP1</span><span class="sxs-lookup"><span data-stu-id="e447c-119">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="e447c-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e447c-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e447c-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e447c-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e447c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e447c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e447c-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e447c-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e447c-124">IID</span><span class="sxs-lookup"><span data-stu-id="e447c-124">IID</span></span><br/>                      | <span data-ttu-id="e447c-125">IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="e447c-125">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="e447c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e447c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e447c-127">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="e447c-127">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





