---
title: 'IVMUSBDevice AttachedToVM 屬性 (VPCCOMInterfaces .h) '
description: 抓取 USB 裝置所連接之虛擬機器的名稱。
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- AttachedToVM 屬性 Virtual PC
- AttachedToVM 屬性 Virtual PC，IVMUSBDevice 介面
- IVMUSBDevice 介面 Virtual PC，AttachedToVM 屬性
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025164"
---
# <a name="ivmusbdeviceattachedtovm-property"></a><span data-ttu-id="53896-106">IVMUSBDevice：： AttachedToVM 屬性</span><span class="sxs-lookup"><span data-stu-id="53896-106">IVMUSBDevice::AttachedToVM property</span></span>

<span data-ttu-id="53896-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="53896-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="53896-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="53896-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="53896-109">抓取 USB 裝置所連接之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="53896-109">Retrieves the name of the virtual machine to which the USB Device is attached.</span></span>

<span data-ttu-id="53896-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="53896-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="53896-111">語法</span><span class="sxs-lookup"><span data-stu-id="53896-111">Syntax</span></span>


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a><span data-ttu-id="53896-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="53896-112">Property value</span></span>

<span data-ttu-id="53896-113">虛擬機器 (VM) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="53896-113">The name of the virtual machine (VM).</span></span>

## <a name="error-codes"></a><span data-ttu-id="53896-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="53896-114">Error codes</span></span>



| <span data-ttu-id="53896-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="53896-115">Name/value</span></span>                                                                                                                                                           | <span data-ttu-id="53896-116">意義</span><span class="sxs-lookup"><span data-stu-id="53896-116">Meaning</span></span>                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="53896-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53896-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="53896-118">裝置會連接到 VM，並傳回其名稱。</span><span class="sxs-lookup"><span data-stu-id="53896-118">The device is attached to the VM, and its name is returned.</span></span><br/> |
| <dl> <span data-ttu-id="53896-119"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="53896-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                           | <span data-ttu-id="53896-120">裝置已附加至主機。</span><span class="sxs-lookup"><span data-stu-id="53896-120">The device is attached to the host.</span></span><br/>                         |
| <dl> <span data-ttu-id="53896-121"><dt>VM \_E \_ USB \_ 外部 \_ VM</dt> <dt>0xA00400929</dt></span><span class="sxs-lookup"><span data-stu-id="53896-121"><dt>VM\_E\_USB\_EXTERNAL\_VM</dt> <dt>0xA00400929</dt></span></span> </dl> | <span data-ttu-id="53896-122">裝置會附加至另一個使用者會話中的 VM。</span><span class="sxs-lookup"><span data-stu-id="53896-122">The device is attached to a VM in another user session.</span></span><br/>     |
| <dl> <span data-ttu-id="53896-123"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="53896-123"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="53896-124">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="53896-124">The parameter is **NULL**.</span></span><br/>                                  |



## <a name="requirements"></a><span data-ttu-id="53896-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="53896-125">Requirements</span></span>



| <span data-ttu-id="53896-126">需求</span><span class="sxs-lookup"><span data-stu-id="53896-126">Requirement</span></span> | <span data-ttu-id="53896-127">值</span><span class="sxs-lookup"><span data-stu-id="53896-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="53896-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53896-128">Minimum supported client</span></span><br/> | <span data-ttu-id="53896-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53896-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53896-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53896-130">Minimum supported server</span></span><br/> | <span data-ttu-id="53896-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="53896-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="53896-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="53896-132">End of client support</span></span><br/>    | <span data-ttu-id="53896-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="53896-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="53896-134">產品</span><span class="sxs-lookup"><span data-stu-id="53896-134">Product</span></span><br/>                  | <span data-ttu-id="53896-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="53896-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="53896-136">標頭</span><span class="sxs-lookup"><span data-stu-id="53896-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="53896-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="53896-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="53896-138">IID</span><span class="sxs-lookup"><span data-stu-id="53896-138">IID</span></span><br/>                      | <span data-ttu-id="53896-139">IID \_ IVMUSBDevice 定義為 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="53896-139">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="53896-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53896-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53896-141">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="53896-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

