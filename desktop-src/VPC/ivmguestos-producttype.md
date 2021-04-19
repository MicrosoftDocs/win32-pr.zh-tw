---
title: 'IVMGuestOS ProductType 屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器中執行之客體作業系統的產品類型。
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- ProductType 屬性 Virtual PC
- ProductType 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，ProductType 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969162"
---
# <a name="ivmguestosproducttype-property"></a><span data-ttu-id="fb259-106">IVMGuestOS：:P roductType 屬性</span><span class="sxs-lookup"><span data-stu-id="fb259-106">IVMGuestOS::ProductType property</span></span>

<span data-ttu-id="fb259-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="fb259-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fb259-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="fb259-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fb259-109">抓取虛擬機器中執行之客體作業系統的產品類型。</span><span class="sxs-lookup"><span data-stu-id="fb259-109">Retrieves the product type of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="fb259-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fb259-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb259-111">語法</span><span class="sxs-lookup"><span data-stu-id="fb259-111">Syntax</span></span>


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a><span data-ttu-id="fb259-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="fb259-112">Property value</span></span>

<span data-ttu-id="fb259-113">產品類型。</span><span class="sxs-lookup"><span data-stu-id="fb259-113">The product type.</span></span> <span data-ttu-id="fb259-114">以下是支援的字串值。</span><span class="sxs-lookup"><span data-stu-id="fb259-114">The following string values are supported.</span></span>



| <span data-ttu-id="fb259-115">值</span><span class="sxs-lookup"><span data-stu-id="fb259-115">Value</span></span>                                                                                  | <span data-ttu-id="fb259-116">意義</span><span class="sxs-lookup"><span data-stu-id="fb259-116">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb259-117"><dt>"0x0000002"</dt></span><span class="sxs-lookup"><span data-stu-id="fb259-117"><dt>"0x0000002"</dt></span></span> </dl> | <span data-ttu-id="fb259-118">系統是網域控制站，而作業系統是 Windows Server 2008 R2、Windows Server 2008、Windows Server 2003 R2、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="fb259-118">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="fb259-119"><dt>"0x0000003"</dt></span><span class="sxs-lookup"><span data-stu-id="fb259-119"><dt>"0x0000003"</dt></span></span> </dl> | <span data-ttu-id="fb259-120">作業系統是 Windows Server 2008 R2、Windows Server 2008、Windows Server 2003 R2、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="fb259-120">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="fb259-121">請注意，同時也是網域控制站的伺服器會回報為 **ver \_ nt \_ 域 \_ 控制器**，而不是 **\_ nt \_ server**。</span><span class="sxs-lookup"><span data-stu-id="fb259-121">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <dl> <span data-ttu-id="fb259-122"><dt>"0x0000001"</dt></span><span class="sxs-lookup"><span data-stu-id="fb259-122"><dt>"0x0000001"</dt></span></span> </dl> | <span data-ttu-id="fb259-123">作業系統是 Windows 7、Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="fb259-123">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="fb259-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb259-124">Requirements</span></span>



| <span data-ttu-id="fb259-125">需求</span><span class="sxs-lookup"><span data-stu-id="fb259-125">Requirement</span></span> | <span data-ttu-id="fb259-126">值</span><span class="sxs-lookup"><span data-stu-id="fb259-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb259-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb259-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fb259-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb259-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb259-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb259-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fb259-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="fb259-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fb259-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fb259-131">End of client support</span></span><br/>    | <span data-ttu-id="fb259-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb259-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fb259-133">產品</span><span class="sxs-lookup"><span data-stu-id="fb259-133">Product</span></span><br/>                  | <span data-ttu-id="fb259-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fb259-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fb259-135">標頭</span><span class="sxs-lookup"><span data-stu-id="fb259-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb259-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb259-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fb259-137">IID</span><span class="sxs-lookup"><span data-stu-id="fb259-137">IID</span></span><br/>                      | <span data-ttu-id="fb259-138">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="fb259-138">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fb259-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb259-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb259-140">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="fb259-140">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

