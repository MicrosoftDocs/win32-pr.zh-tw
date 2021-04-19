---
title: 'IVMDVDDrive SetBusLocation 方法 (VPCCOMInterfaces .h) '
description: 將 DVD 光碟機連接到虛擬機器中指定的匯流排位置。
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- SetBusLocation 方法 Virtual PC
- SetBusLocation 方法 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，SetBusLocation 方法
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106988037"
---
# <a name="ivmdvddrivesetbuslocation-method"></a><span data-ttu-id="b194f-106">IVMDVDDrive：： SetBusLocation 方法</span><span class="sxs-lookup"><span data-stu-id="b194f-106">IVMDVDDrive::SetBusLocation method</span></span>

<span data-ttu-id="b194f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="b194f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b194f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="b194f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b194f-109">將 DVD 光碟機連接到虛擬機器中指定的匯流排位置。</span><span class="sxs-lookup"><span data-stu-id="b194f-109">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b194f-110">語法</span><span class="sxs-lookup"><span data-stu-id="b194f-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="b194f-111">參數</span><span class="sxs-lookup"><span data-stu-id="b194f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b194f-112">*busNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b194f-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b194f-113">要連接此磁片磁碟機的匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="b194f-113">The bus number to which this drive is to be attached.</span></span> <span data-ttu-id="b194f-114">例如，在 IDE 匯流排上，這個數位會表示是否使用主要或次要匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="b194f-114">For example, on an IDE bus, this number would represent whether to use the primary or secondary bus number.</span></span>

</dd> <dt>

<span data-ttu-id="b194f-115">*deviceNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b194f-115">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b194f-116">要連接此磁片磁碟機的裝置編號。</span><span class="sxs-lookup"><span data-stu-id="b194f-116">The device number to which this drive is to be attached.</span></span> <span data-ttu-id="b194f-117">例如，在 IDE 匯流排上，這個數位會表示是否要使用主要或次要裝置位置。</span><span class="sxs-lookup"><span data-stu-id="b194f-117">For example, on an IDE bus, this number would represent whether to use the primary or secondary device location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b194f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b194f-118">Return value</span></span>

<span data-ttu-id="b194f-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b194f-119">This method can return one of these values.</span></span>



| <span data-ttu-id="b194f-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b194f-120">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="b194f-121">Description</span><span class="sxs-lookup"><span data-stu-id="b194f-121">Description</span></span>                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b194f-122"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b194f-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="b194f-123">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b194f-123">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="b194f-124"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b194f-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="b194f-125">指定的匯流排位置無效。</span><span class="sxs-lookup"><span data-stu-id="b194f-125">The bus location specified is not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="b194f-126"><dt>**E \_FAIL**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="b194f-126"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                       | <span data-ttu-id="b194f-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b194f-127">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="b194f-128"><dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="b194f-128"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="b194f-129">當虛擬機器正在執行或處於儲存狀態時，無法設定匯流排位置。</span><span class="sxs-lookup"><span data-stu-id="b194f-129">The bus location cannot be set while the virtual machine is running or in a saved state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b194f-130"><dt>**\_ \_ \_ \_ 使用中的 VM E 匯流排 LOC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b194f-130"><dt>**VM\_E\_BUS\_LOC\_IN\_USE**</dt></span></span> </dl>                                                                      | <span data-ttu-id="b194f-131">另一個裝置已附加至指定的匯流排位置。</span><span class="sxs-lookup"><span data-stu-id="b194f-131">Another device is already attached to the specified bus location.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="b194f-132"><dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="b194f-132"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="b194f-133">無法初始化目前磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b194f-133">The current drive could not be initialized.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="b194f-134"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="b194f-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="b194f-135">因為無法判斷此磁片磁碟機的虛擬機器，所以無法將變更寫入喜好設定檔案。</span><span class="sxs-lookup"><span data-stu-id="b194f-135">The changes could not be written to the preferences file because the virtual machine for this drive could not be determined.</span></span><br/> |
| <dl> <span data-ttu-id="b194f-136"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b194f-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="b194f-137">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b194f-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="b194f-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="b194f-138">Requirements</span></span>



| <span data-ttu-id="b194f-139">需求</span><span class="sxs-lookup"><span data-stu-id="b194f-139">Requirement</span></span> | <span data-ttu-id="b194f-140">值</span><span class="sxs-lookup"><span data-stu-id="b194f-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b194f-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b194f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b194f-142">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b194f-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b194f-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b194f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b194f-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="b194f-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b194f-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b194f-145">End of client support</span></span><br/>    | <span data-ttu-id="b194f-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b194f-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b194f-147">產品</span><span class="sxs-lookup"><span data-stu-id="b194f-147">Product</span></span><br/>                  | <span data-ttu-id="b194f-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b194f-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b194f-149">標頭</span><span class="sxs-lookup"><span data-stu-id="b194f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b194f-150"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="b194f-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b194f-151">IID</span><span class="sxs-lookup"><span data-stu-id="b194f-151">IID</span></span><br/>                      | <span data-ttu-id="b194f-152">IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="b194f-152">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b194f-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b194f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b194f-154">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="b194f-154">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

