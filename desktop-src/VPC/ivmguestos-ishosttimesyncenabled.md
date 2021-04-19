---
title: 'IVMGuestOS IsHostTimeSyncEnabled 屬性 (VPCCOMInterfaces .h) '
description: 指出此 VM 中的整合元件是否應將來賓的時鐘與主機的時鐘同步。
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- IsHostTimeSyncEnabled 屬性 Virtual PC
- IsHostTimeSyncEnabled 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，IsHostTimeSyncEnabled 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87afddb2e3bc940c5dba7e2548e4355d36142012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968352"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a><span data-ttu-id="33a96-106">IVMGuestOS：： IsHostTimeSyncEnabled 屬性</span><span class="sxs-lookup"><span data-stu-id="33a96-106">IVMGuestOS::IsHostTimeSyncEnabled property</span></span>

<span data-ttu-id="33a96-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="33a96-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="33a96-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="33a96-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="33a96-109">指出此虛擬機器中的整合元件 (VM) 是否應將來賓的時鐘與主機的時鐘同步。</span><span class="sxs-lookup"><span data-stu-id="33a96-109">Indicates whether the Integration Components in this virtual machine (VM) should synchronize the guest's clock with the host's clock.</span></span>

<span data-ttu-id="33a96-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="33a96-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a96-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="33a96-111">Syntax</span></span>


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="33a96-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="33a96-112">Property value</span></span>

<span data-ttu-id="33a96-113">如果此 VM 中的整合元件應該使用主機的時鐘來同步處理來賓的時鐘，則使用 **variant \_ TRUE** ，否則為 **\_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="33a96-113">Use **VARIANT\_TRUE** if the integration components in this VM should synchronize the guest's clock with the host's clock and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="33a96-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="33a96-114">Error codes</span></span>



| <span data-ttu-id="33a96-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="33a96-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="33a96-116">意義</span><span class="sxs-lookup"><span data-stu-id="33a96-116">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="33a96-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="33a96-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="33a96-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="33a96-118">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="33a96-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="33a96-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="33a96-120">未指定 *isEnabled* 參數。</span><span class="sxs-lookup"><span data-stu-id="33a96-120">The *isEnabled* parameter is not specified.</span></span><br/> |
| <dl> <span data-ttu-id="33a96-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="33a96-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="33a96-122">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="33a96-122">The configuration is unknown.</span></span><br/>               |
| <dl> <span data-ttu-id="33a96-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="33a96-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="33a96-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="33a96-124">An unexpected error has occurred.</span></span><br/>           |



## <a name="remarks"></a><span data-ttu-id="33a96-125">備註</span><span class="sxs-lookup"><span data-stu-id="33a96-125">Remarks</span></span>

<span data-ttu-id="33a96-126">當虛擬機器處於作用中狀態時，您就無法變更此設定 (也就是執行中或處於已儲存狀態) 。</span><span class="sxs-lookup"><span data-stu-id="33a96-126">You cannot change this setting while the virtual machine is active (that is, running or in saved state).</span></span>

## <a name="requirements"></a><span data-ttu-id="33a96-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="33a96-127">Requirements</span></span>



| <span data-ttu-id="33a96-128">需求</span><span class="sxs-lookup"><span data-stu-id="33a96-128">Requirement</span></span> | <span data-ttu-id="33a96-129">值</span><span class="sxs-lookup"><span data-stu-id="33a96-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a96-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33a96-130">Minimum supported client</span></span><br/> | <span data-ttu-id="33a96-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33a96-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33a96-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33a96-132">Minimum supported server</span></span><br/> | <span data-ttu-id="33a96-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="33a96-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="33a96-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="33a96-134">End of client support</span></span><br/>    | <span data-ttu-id="33a96-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="33a96-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="33a96-136">產品</span><span class="sxs-lookup"><span data-stu-id="33a96-136">Product</span></span><br/>                  | <span data-ttu-id="33a96-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="33a96-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="33a96-138">標頭</span><span class="sxs-lookup"><span data-stu-id="33a96-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="33a96-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="33a96-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="33a96-140">IID</span><span class="sxs-lookup"><span data-stu-id="33a96-140">IID</span></span><br/>                      | <span data-ttu-id="33a96-141">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="33a96-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="33a96-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33a96-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a96-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="33a96-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

