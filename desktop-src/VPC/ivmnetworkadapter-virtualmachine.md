---
title: 'IVMNetworkAdapter VirtualMachine 屬性 (VPCCOMInterfaces .h) '
description: 抓取與此網路介面相關聯的虛擬機器。
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- VirtualMachine 屬性 Virtual PC
- VirtualMachine 屬性 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，VirtualMachine 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024535"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a><span data-ttu-id="44c84-106">IVMNetworkAdapter：： VirtualMachine 屬性</span><span class="sxs-lookup"><span data-stu-id="44c84-106">IVMNetworkAdapter::VirtualMachine property</span></span>

<span data-ttu-id="44c84-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="44c84-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="44c84-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="44c84-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="44c84-109">抓取與此網路介面相關聯的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="44c84-109">Retrieves the virtual machine associated with this network interface.</span></span>

<span data-ttu-id="44c84-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="44c84-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44c84-111">語法</span><span class="sxs-lookup"><span data-stu-id="44c84-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="44c84-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="44c84-112">Property value</span></span>

<span data-ttu-id="44c84-113">代表虛擬機器的 [**IVMVirtualMachine**](ivmvirtualmachine.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="44c84-113">An [**IVMVirtualMachine**](ivmvirtualmachine.md) interface that represents the virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44c84-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="44c84-114">Error codes</span></span>



| <span data-ttu-id="44c84-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="44c84-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="44c84-116">意義</span><span class="sxs-lookup"><span data-stu-id="44c84-116">Meaning</span></span>                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="44c84-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="44c84-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="44c84-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="44c84-118">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="44c84-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="44c84-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="44c84-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="44c84-120">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="44c84-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="44c84-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="44c84-122">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="44c84-122">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="44c84-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="44c84-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="44c84-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="44c84-124">An unexpected error has occurred.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="44c84-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="44c84-125">Requirements</span></span>



| <span data-ttu-id="44c84-126">需求</span><span class="sxs-lookup"><span data-stu-id="44c84-126">Requirement</span></span> | <span data-ttu-id="44c84-127">值</span><span class="sxs-lookup"><span data-stu-id="44c84-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="44c84-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44c84-128">Minimum supported client</span></span><br/> | <span data-ttu-id="44c84-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44c84-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44c84-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44c84-130">Minimum supported server</span></span><br/> | <span data-ttu-id="44c84-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="44c84-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="44c84-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="44c84-132">End of client support</span></span><br/>    | <span data-ttu-id="44c84-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="44c84-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="44c84-134">產品</span><span class="sxs-lookup"><span data-stu-id="44c84-134">Product</span></span><br/>                  | <span data-ttu-id="44c84-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="44c84-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="44c84-136">標頭</span><span class="sxs-lookup"><span data-stu-id="44c84-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="44c84-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="44c84-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="44c84-138">IID</span><span class="sxs-lookup"><span data-stu-id="44c84-138">IID</span></span><br/>                      | <span data-ttu-id="44c84-139">IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="44c84-139">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="44c84-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44c84-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c84-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="44c84-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

