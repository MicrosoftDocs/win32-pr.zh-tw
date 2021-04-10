---
title: 'IVMNetworkAdapter _ID 方法 (VPCCOMInterfaces .h) '
description: 抓取此網路介面的內部識別碼。
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- _ID 方法 Virtual PC
- _ID 方法 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，_ID 方法
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9df514d24f9826b58964b4c51c9a76a9ba982e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934501"
---
# <a name="ivmnetworkadapter_id-method"></a><span data-ttu-id="397b7-106">IVMNetworkAdapter：： \_ ID 方法</span><span class="sxs-lookup"><span data-stu-id="397b7-106">IVMNetworkAdapter::\_ID method</span></span>

<span data-ttu-id="397b7-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="397b7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="397b7-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="397b7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="397b7-109">抓取此網路介面的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="397b7-109">Retrieves the internal identifier of this network interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="397b7-110">語法</span><span class="sxs-lookup"><span data-stu-id="397b7-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a><span data-ttu-id="397b7-111">參數</span><span class="sxs-lookup"><span data-stu-id="397b7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="397b7-112">*識別碼* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="397b7-112">*identifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="397b7-113">內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="397b7-113">The internal identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="397b7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="397b7-114">Return value</span></span>

<span data-ttu-id="397b7-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="397b7-115">This method can return one of these values.</span></span>



| <span data-ttu-id="397b7-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="397b7-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="397b7-117">Description</span><span class="sxs-lookup"><span data-stu-id="397b7-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="397b7-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="397b7-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="397b7-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="397b7-119">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="397b7-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="397b7-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="397b7-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="397b7-121">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="397b7-122"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="397b7-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="397b7-123">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="397b7-123">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="397b7-124"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="397b7-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="397b7-125">作業發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="397b7-125">The operation had an unknown error.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="397b7-126">備註</span><span class="sxs-lookup"><span data-stu-id="397b7-126">Remarks</span></span>

<span data-ttu-id="397b7-127">指令碼語言無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="397b7-127">This method is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="397b7-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="397b7-128">Requirements</span></span>



| <span data-ttu-id="397b7-129">需求</span><span class="sxs-lookup"><span data-stu-id="397b7-129">Requirement</span></span> | <span data-ttu-id="397b7-130">值</span><span class="sxs-lookup"><span data-stu-id="397b7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="397b7-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="397b7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="397b7-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="397b7-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="397b7-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="397b7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="397b7-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="397b7-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="397b7-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="397b7-135">End of client support</span></span><br/>    | <span data-ttu-id="397b7-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="397b7-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="397b7-137">產品</span><span class="sxs-lookup"><span data-stu-id="397b7-137">Product</span></span><br/>                  | <span data-ttu-id="397b7-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="397b7-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="397b7-139">標頭</span><span class="sxs-lookup"><span data-stu-id="397b7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="397b7-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="397b7-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="397b7-141">IID</span><span class="sxs-lookup"><span data-stu-id="397b7-141">IID</span></span><br/>                      | <span data-ttu-id="397b7-142">IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="397b7-142">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="397b7-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="397b7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="397b7-144">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="397b7-144">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

