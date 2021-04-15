---
title: 'IVMNetworkAdapter AttachToVirtualNetwork 方法 (VPCCOMInterfaces .h) '
description: 將網路介面附加至指定的虛擬網路。
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- AttachToVirtualNetwork 方法 Virtual PC
- AttachToVirtualNetwork 方法 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，AttachToVirtualNetwork 方法
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465621"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a><span data-ttu-id="c4998-106">IVMNetworkAdapter：： AttachToVirtualNetwork 方法</span><span class="sxs-lookup"><span data-stu-id="c4998-106">IVMNetworkAdapter::AttachToVirtualNetwork method</span></span>

<span data-ttu-id="c4998-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="c4998-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c4998-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="c4998-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c4998-109">將網路介面附加至指定的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c4998-109">Attaches the network interface to the specified virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4998-110">語法</span><span class="sxs-lookup"><span data-stu-id="c4998-110">Syntax</span></span>


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="c4998-111">參數</span><span class="sxs-lookup"><span data-stu-id="c4998-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4998-112">*virtualNetwork* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4998-112">*virtualNetwork* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4998-113">將連接此虛擬 NIC 的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c4998-113">The virtual network to which this virtual NIC will be connected.</span></span> <span data-ttu-id="c4998-114">請參閱 [**IVMVirtualNetwork**](ivmvirtualnetwork.md)。</span><span class="sxs-lookup"><span data-stu-id="c4998-114">See [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4998-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4998-115">Return value</span></span>

<span data-ttu-id="c4998-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c4998-116">This method can return one of these values.</span></span>



| <span data-ttu-id="c4998-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="c4998-117">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="c4998-118">Description</span><span class="sxs-lookup"><span data-stu-id="c4998-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4998-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c4998-119"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                       | <span data-ttu-id="c4998-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c4998-120">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="c4998-121"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c4998-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="c4998-122">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c4998-122">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="c4998-123"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="c4998-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="c4998-124">參數不包含有效的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c4998-124">The parameter does not contain a valid virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="c4998-125"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="c4998-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="c4998-126">已拒絕存取要求的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c4998-126">Access was denied to the requested virtual network.</span></span><br/>     |
| <dl> <span data-ttu-id="c4998-127"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="c4998-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="c4998-128">虛擬機器無效或已不存在。</span><span class="sxs-lookup"><span data-stu-id="c4998-128">The virtual machine is invalid or no longer exists.</span></span><br/>     |
| <dl> <span data-ttu-id="c4998-129"><dt>**VM \_ E \_ 不正確 \_ 虛擬 \_ 網路 \_ 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="c4998-129"><dt>**VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID**</dt></span></span> </dl>                                                                        | <span data-ttu-id="c4998-130">參數不是現有的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c4998-130">The parameter is not an existing virtual network.</span></span><br/>       |
| <dl> <span data-ttu-id="c4998-131"><dt>**出現 \_ E \_ 例外狀況**</dt></span><span class="sxs-lookup"><span data-stu-id="c4998-131"><dt>**DISP\_E\_EXCEPTION**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="c4998-132">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c4998-132">An unexpected error has occurred.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="c4998-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4998-133">Requirements</span></span>



| <span data-ttu-id="c4998-134">需求</span><span class="sxs-lookup"><span data-stu-id="c4998-134">Requirement</span></span> | <span data-ttu-id="c4998-135">值</span><span class="sxs-lookup"><span data-stu-id="c4998-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4998-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4998-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c4998-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4998-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4998-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4998-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c4998-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="c4998-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c4998-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c4998-140">End of client support</span></span><br/>    | <span data-ttu-id="c4998-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c4998-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c4998-142">產品</span><span class="sxs-lookup"><span data-stu-id="c4998-142">Product</span></span><br/>                  | <span data-ttu-id="c4998-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c4998-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c4998-144">標頭</span><span class="sxs-lookup"><span data-stu-id="c4998-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4998-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4998-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c4998-146">IID</span><span class="sxs-lookup"><span data-stu-id="c4998-146">IID</span></span><br/>                      | <span data-ttu-id="c4998-147">IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="c4998-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c4998-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4998-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4998-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="c4998-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

