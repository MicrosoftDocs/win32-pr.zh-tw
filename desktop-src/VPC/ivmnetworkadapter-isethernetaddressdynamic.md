---
title: 'IVMNetworkAdapter IsEthernetAddressDynamic 屬性 (VPCCOMInterfaces .h) '
description: 判斷是否動態產生乙太網路位址。
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- IsEthernetAddressDynamic 屬性 Virtual PC
- IsEthernetAddressDynamic 屬性 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，IsEthernetAddressDynamic 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b16074243094d410e8d39538b024120daa1871e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024536"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a><span data-ttu-id="70180-106">IVMNetworkAdapter：： IsEthernetAddressDynamic 屬性</span><span class="sxs-lookup"><span data-stu-id="70180-106">IVMNetworkAdapter::IsEthernetAddressDynamic property</span></span>

<span data-ttu-id="70180-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="70180-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="70180-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="70180-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="70180-109">判斷是否動態產生乙太網路位址。</span><span class="sxs-lookup"><span data-stu-id="70180-109">Determines whether the Ethernet address is dynamically generated.</span></span>

<span data-ttu-id="70180-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="70180-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70180-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="70180-111">Syntax</span></span>


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a><span data-ttu-id="70180-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="70180-112">Property value</span></span>

<span data-ttu-id="70180-113">\_如果應動態產生乙太網路位址，則設定為 variant TRUE， \_ 如果乙太網路位址為靜態，則為 variant FALSE。</span><span class="sxs-lookup"><span data-stu-id="70180-113">Set to VARIANT\_TRUE if the Ethernet address should be dynamically generated and VARIANT\_FALSE if the Ethernet address is static.</span></span>

## <a name="error-codes"></a><span data-ttu-id="70180-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="70180-114">Error codes</span></span>



| <span data-ttu-id="70180-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="70180-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="70180-116">意義</span><span class="sxs-lookup"><span data-stu-id="70180-116">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70180-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70180-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="70180-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="70180-118">The operation was successful.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="70180-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="70180-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="70180-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="70180-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="70180-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="70180-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="70180-122">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="70180-122">The virtual machine was not found.</span></span> <span data-ttu-id="70180-123">如果在建立 [**IVMNetworkAdapter**](ivmnetworkadapter.md) 物件之後移除電腦，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="70180-123">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/> |
| <dl> <span data-ttu-id="70180-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="70180-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="70180-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="70180-125">An unexpected error has occurred.</span></span><br/>                                                                                                                         |



## <a name="remarks"></a><span data-ttu-id="70180-126">備註</span><span class="sxs-lookup"><span data-stu-id="70180-126">Remarks</span></span>

<span data-ttu-id="70180-127">針對大部分的虛擬網路介面，這個屬性應該設定為 **TRUE** (預設) 。</span><span class="sxs-lookup"><span data-stu-id="70180-127">This property should be set to **TRUE** (default) for most virtual network interfaces.</span></span> <span data-ttu-id="70180-128">如果來賓中的軟體需要靜態乙太網路位址，則應該將此屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="70180-128">If software in the guest requires a static Ethernet address, this property should be set to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="70180-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="70180-129">Requirements</span></span>



| <span data-ttu-id="70180-130">需求</span><span class="sxs-lookup"><span data-stu-id="70180-130">Requirement</span></span> | <span data-ttu-id="70180-131">值</span><span class="sxs-lookup"><span data-stu-id="70180-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="70180-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70180-132">Minimum supported client</span></span><br/> | <span data-ttu-id="70180-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70180-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70180-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70180-134">Minimum supported server</span></span><br/> | <span data-ttu-id="70180-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="70180-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="70180-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="70180-136">End of client support</span></span><br/>    | <span data-ttu-id="70180-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="70180-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="70180-138">產品</span><span class="sxs-lookup"><span data-stu-id="70180-138">Product</span></span><br/>                  | <span data-ttu-id="70180-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="70180-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="70180-140">標頭</span><span class="sxs-lookup"><span data-stu-id="70180-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="70180-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="70180-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="70180-142">IID</span><span class="sxs-lookup"><span data-stu-id="70180-142">IID</span></span><br/>                      | <span data-ttu-id="70180-143">IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="70180-143">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="70180-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70180-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70180-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="70180-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

