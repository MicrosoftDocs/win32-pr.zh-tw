---
title: 'IVMVirtualPC FindVirtualNetwork 方法 (VPCCOMInterfaces .h) '
description: 抓取符合所要求名稱的虛擬網路物件。
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- FindVirtualNetwork 方法 Virtual PC
- FindVirtualNetwork 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，FindVirtualNetwork 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509036"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a><span data-ttu-id="cf2d5-106">IVMVirtualPC：： FindVirtualNetwork 方法</span><span class="sxs-lookup"><span data-stu-id="cf2d5-106">IVMVirtualPC::FindVirtualNetwork method</span></span>

<span data-ttu-id="cf2d5-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cf2d5-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="cf2d5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cf2d5-109">抓取符合所要求名稱的虛擬網路物件。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-109">Retrieves a virtual network object that matches the requested name.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf2d5-110">語法</span><span class="sxs-lookup"><span data-stu-id="cf2d5-110">Syntax</span></span>


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="cf2d5-111">參數</span><span class="sxs-lookup"><span data-stu-id="cf2d5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf2d5-112">*virtualNetworkName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf2d5-112">*virtualNetworkName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf2d5-113">要尋找之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-113">The name of the virtual network to find.</span></span>

</dd> <dt>

<span data-ttu-id="cf2d5-114">*virtualNetwork* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="cf2d5-114">*virtualNetwork* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cf2d5-115">代表此虛擬網路之新 [**IVMVirtualNetwork**](ivmvirtualnetwork.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-115">A pointer to a new [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that represents this virtual network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf2d5-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf2d5-116">Return value</span></span>

<span data-ttu-id="cf2d5-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-117">This method can return one of these values.</span></span>



| <span data-ttu-id="cf2d5-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="cf2d5-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="cf2d5-119">Description</span><span class="sxs-lookup"><span data-stu-id="cf2d5-119">Description</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf2d5-120"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cf2d5-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="cf2d5-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="cf2d5-122"><dt>**S \_FALSE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cf2d5-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="cf2d5-123">找不到指定的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-123">The specified virtual network could not be found.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cf2d5-124"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cf2d5-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="cf2d5-125">*VirtualNetwork* 參數為 **Null** ，或找不到虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-125">The *virtualNetwork* parameter is **NULL** or the virtual network cannot be found.</span></span><br/>   |
| <dl> <span data-ttu-id="cf2d5-126"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="cf2d5-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="cf2d5-127">*VirtualNetworkName* 參數無效或為空字串。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-127">The *virtualNetworkName* parameter is not valid or is an empty string.</span></span><br/>               |
| <dl> <span data-ttu-id="cf2d5-128"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="cf2d5-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="cf2d5-129">找不到虛擬網路檔案。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-129">The virtual network file could not be found.</span></span><br/>                                         |
| <dl> <span data-ttu-id="cf2d5-130"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cf2d5-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="cf2d5-131">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-131">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="cf2d5-132"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="cf2d5-132"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="cf2d5-133">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-133">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf2d5-134">備註</span><span class="sxs-lookup"><span data-stu-id="cf2d5-134">Remarks</span></span>

<span data-ttu-id="cf2d5-135">虛擬網路名稱不區分大小寫，例如 "MyNetwork" 和 "MyNetwork" 指的是相同的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cf2d5-135">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf2d5-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf2d5-136">Requirements</span></span>



| <span data-ttu-id="cf2d5-137">需求</span><span class="sxs-lookup"><span data-stu-id="cf2d5-137">Requirement</span></span> | <span data-ttu-id="cf2d5-138">值</span><span class="sxs-lookup"><span data-stu-id="cf2d5-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf2d5-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf2d5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="cf2d5-140">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf2d5-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf2d5-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf2d5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="cf2d5-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="cf2d5-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cf2d5-143">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cf2d5-143">End of client support</span></span><br/>    | <span data-ttu-id="cf2d5-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cf2d5-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cf2d5-145">產品</span><span class="sxs-lookup"><span data-stu-id="cf2d5-145">Product</span></span><br/>                  | <span data-ttu-id="cf2d5-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cf2d5-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cf2d5-147">標頭</span><span class="sxs-lookup"><span data-stu-id="cf2d5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf2d5-148"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf2d5-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cf2d5-149">IID</span><span class="sxs-lookup"><span data-stu-id="cf2d5-149">IID</span></span><br/>                      | <span data-ttu-id="cf2d5-150">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="cf2d5-150">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="cf2d5-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf2d5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf2d5-152">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="cf2d5-152">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

