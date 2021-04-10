---
title: 'IVMGuestOS IntegrationComponentsVersion 屬性 (VPCCOMInterfaces .h) '
description: 抓取在客體作業系統中安裝之整合元件的版本。
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- IntegrationComponentsVersion 屬性 Virtual PC
- IntegrationComponentsVersion 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，IntegrationComponentsVersion 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85352614b89ab208377fe44fe3b970c693d60dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685574"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a><span data-ttu-id="3ab45-106">IVMGuestOS：： IntegrationComponentsVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="3ab45-106">IVMGuestOS::IntegrationComponentsVersion property</span></span>

<span data-ttu-id="3ab45-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3ab45-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3ab45-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3ab45-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3ab45-109">抓取在客體作業系統中安裝之整合元件的版本。</span><span class="sxs-lookup"><span data-stu-id="3ab45-109">Retrieves the version of the Integration Components installed in the guest operating system.</span></span>

<span data-ttu-id="3ab45-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="3ab45-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab45-111">語法</span><span class="sxs-lookup"><span data-stu-id="3ab45-111">Syntax</span></span>


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a><span data-ttu-id="3ab45-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="3ab45-112">Property value</span></span>

<span data-ttu-id="3ab45-113">版本。</span><span class="sxs-lookup"><span data-stu-id="3ab45-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3ab45-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3ab45-114">Error codes</span></span>



| <span data-ttu-id="3ab45-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="3ab45-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="3ab45-116">意義</span><span class="sxs-lookup"><span data-stu-id="3ab45-116">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ab45-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3ab45-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="3ab45-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="3ab45-118">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="3ab45-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3ab45-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="3ab45-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3ab45-120">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3ab45-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="3ab45-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="3ab45-122">找不到虛擬機器 (VM) 。</span><span class="sxs-lookup"><span data-stu-id="3ab45-122">The virtual machine (VM) could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="3ab45-123"><dt>VM \_E \_ 新增 \_ 專案 \_ 無法</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="3ab45-123"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="3ab45-124">此 VM 未安裝整合元件，或 VM 從未啟動。</span><span class="sxs-lookup"><span data-stu-id="3ab45-124">Integration Components are not installed in this VM, or the VM was never started.</span></span><br/> |
| <dl> <span data-ttu-id="3ab45-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3ab45-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="3ab45-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3ab45-126">An unexpected error has occurred.</span></span><br/>                                                 |



## <a name="requirements"></a><span data-ttu-id="3ab45-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ab45-127">Requirements</span></span>



| <span data-ttu-id="3ab45-128">需求</span><span class="sxs-lookup"><span data-stu-id="3ab45-128">Requirement</span></span> | <span data-ttu-id="3ab45-129">值</span><span class="sxs-lookup"><span data-stu-id="3ab45-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab45-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ab45-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3ab45-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ab45-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ab45-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ab45-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3ab45-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="3ab45-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3ab45-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3ab45-134">End of client support</span></span><br/>    | <span data-ttu-id="3ab45-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ab45-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3ab45-136">產品</span><span class="sxs-lookup"><span data-stu-id="3ab45-136">Product</span></span><br/>                  | <span data-ttu-id="3ab45-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3ab45-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3ab45-138">標頭</span><span class="sxs-lookup"><span data-stu-id="3ab45-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ab45-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ab45-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3ab45-140">IID</span><span class="sxs-lookup"><span data-stu-id="3ab45-140">IID</span></span><br/>                      | <span data-ttu-id="3ab45-141">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="3ab45-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3ab45-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ab45-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab45-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="3ab45-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

