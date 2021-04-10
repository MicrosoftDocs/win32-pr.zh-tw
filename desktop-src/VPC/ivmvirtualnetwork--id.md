---
title: 'IVMVirtualNetwork _ID 方法 (VPCCOMInterfaces .h) '
description: 抓取虛擬網路的內部識別碼。
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- _ID 方法 Virtual PC
- _ID 方法 Virtual PC，IVMVirtualNetwork 介面
- IVMVirtualNetwork 介面 Virtual PC，_ID 方法
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025395"
---
# <a name="ivmvirtualnetwork_id-method"></a><span data-ttu-id="eda9d-106">IVMVirtualNetwork：： \_ ID 方法</span><span class="sxs-lookup"><span data-stu-id="eda9d-106">IVMVirtualNetwork::\_ID method</span></span>

<span data-ttu-id="eda9d-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="eda9d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eda9d-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="eda9d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="eda9d-109">抓取虛擬網路的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="eda9d-109">Retrieves the internal identifier of the virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="eda9d-110">語法</span><span class="sxs-lookup"><span data-stu-id="eda9d-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a><span data-ttu-id="eda9d-111">參數</span><span class="sxs-lookup"><span data-stu-id="eda9d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eda9d-112">*virtualNetworkID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eda9d-112">*virtualNetworkID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eda9d-113">虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="eda9d-113">The virtual network identifier.</span></span> <span data-ttu-id="eda9d-114">共用網路 (NAT) 虛擬網路的識別碼是01010101010101010101010101010101。</span><span class="sxs-lookup"><span data-stu-id="eda9d-114">The identifier for the Shared Networking (NAT) virtual network is 01010101010101010101010101010101.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eda9d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="eda9d-115">Return value</span></span>

<span data-ttu-id="eda9d-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="eda9d-116">This method can return one of these values.</span></span>



| <span data-ttu-id="eda9d-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="eda9d-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="eda9d-118">Description</span><span class="sxs-lookup"><span data-stu-id="eda9d-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="eda9d-119"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eda9d-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="eda9d-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="eda9d-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="eda9d-121"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="eda9d-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="eda9d-122">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="eda9d-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="eda9d-123"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="eda9d-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="eda9d-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="eda9d-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eda9d-125">備註</span><span class="sxs-lookup"><span data-stu-id="eda9d-125">Remarks</span></span>

<span data-ttu-id="eda9d-126">指令碼語言無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="eda9d-126">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="eda9d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="eda9d-127">Requirements</span></span>



| <span data-ttu-id="eda9d-128">需求</span><span class="sxs-lookup"><span data-stu-id="eda9d-128">Requirement</span></span> | <span data-ttu-id="eda9d-129">值</span><span class="sxs-lookup"><span data-stu-id="eda9d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eda9d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eda9d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eda9d-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eda9d-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eda9d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eda9d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eda9d-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="eda9d-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="eda9d-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="eda9d-134">End of client support</span></span><br/>    | <span data-ttu-id="eda9d-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eda9d-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eda9d-136">產品</span><span class="sxs-lookup"><span data-stu-id="eda9d-136">Product</span></span><br/>                  | <span data-ttu-id="eda9d-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="eda9d-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="eda9d-138">標頭</span><span class="sxs-lookup"><span data-stu-id="eda9d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="eda9d-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="eda9d-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="eda9d-140">IID</span><span class="sxs-lookup"><span data-stu-id="eda9d-140">IID</span></span><br/>                      | <span data-ttu-id="eda9d-141">IID \_ IVMVirtualNetwork 定義為431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="eda9d-141">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="eda9d-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eda9d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda9d-143">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="eda9d-143">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

