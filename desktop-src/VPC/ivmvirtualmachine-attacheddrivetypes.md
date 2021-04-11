---
title: 'IVMVirtualMachine AttachedDriveTypes 屬性 (VPCCOMInterfaces .h) '
description: 陣列，指出連接到 VM 中每個位置的磁片磁碟機類型。
ms.assetid: 6896c9cd-5448-4fbb-8c8e-eef306a5cea1
keywords:
- AttachedDriveTypes 屬性 Virtual PC
- AttachedDriveTypes 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，AttachedDriveTypes 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachedDriveTypes
- IVMVirtualMachine.get_AttachedDriveTypes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5f01802b7fa7e3a4f1ccbfc1b5c4bf70e06614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105654"
---
# <a name="ivmvirtualmachineattacheddrivetypes-property"></a><span data-ttu-id="03072-106">IVMVirtualMachine：： AttachedDriveTypes 屬性</span><span class="sxs-lookup"><span data-stu-id="03072-106">IVMVirtualMachine::AttachedDriveTypes property</span></span>

<span data-ttu-id="03072-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="03072-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="03072-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="03072-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="03072-109">抓取陣列，指出連接到虛擬機器中每個位置的磁片磁碟機類型 (VM) 。</span><span class="sxs-lookup"><span data-stu-id="03072-109">Retrieves an array indicating the type of drive attached to each location in the virtual machine (VM).</span></span>

<span data-ttu-id="03072-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="03072-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03072-111">語法</span><span class="sxs-lookup"><span data-stu-id="03072-111">Syntax</span></span>


```C++
HRESULT get_AttachedDriveTypes(
  [out, retval] VARIANT *driveTypes
);
```



## <a name="property-value"></a><span data-ttu-id="03072-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="03072-112">Property value</span></span>

<span data-ttu-id="03072-113">型別 **vt \_ ARRAY** \| **VT \_ variant** 的變數，其中包含 **VT \_ UI1** 型別的專案。</span><span class="sxs-lookup"><span data-stu-id="03072-113">A variant of type **VT\_ARRAY** \| **VT\_VARIANT** containing entries of type **VT\_UI1**.</span></span> <span data-ttu-id="03072-114">陣列包含每個連線到每個匯流排位置之裝置的 [**VMDriveType**](vmdrivetype.md) 值。</span><span class="sxs-lookup"><span data-stu-id="03072-114">The array contains the [**VMDriveType**](vmdrivetype.md) value of each device connected to every bus location.</span></span> <span data-ttu-id="03072-115">陣列會依 \[ *busNumber* \] \[ *deviceID* 排序 \] 。</span><span class="sxs-lookup"><span data-stu-id="03072-115">The array is ordered by \[*busNumber*\]\[*deviceID*\].</span></span>

## <a name="error-codes"></a><span data-ttu-id="03072-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="03072-116">Error codes</span></span>



| <span data-ttu-id="03072-117">名稱/值</span><span class="sxs-lookup"><span data-stu-id="03072-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="03072-118">意義</span><span class="sxs-lookup"><span data-stu-id="03072-118">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="03072-119"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="03072-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="03072-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="03072-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="03072-121"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="03072-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="03072-122">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="03072-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="03072-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="03072-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="03072-124">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="03072-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="03072-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="03072-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="03072-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="03072-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="03072-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="03072-127">Requirements</span></span>



| <span data-ttu-id="03072-128">需求</span><span class="sxs-lookup"><span data-stu-id="03072-128">Requirement</span></span> | <span data-ttu-id="03072-129">值</span><span class="sxs-lookup"><span data-stu-id="03072-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="03072-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03072-130">Minimum supported client</span></span><br/> | <span data-ttu-id="03072-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03072-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03072-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03072-132">Minimum supported server</span></span><br/> | <span data-ttu-id="03072-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="03072-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="03072-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="03072-134">End of client support</span></span><br/>    | <span data-ttu-id="03072-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="03072-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="03072-136">產品</span><span class="sxs-lookup"><span data-stu-id="03072-136">Product</span></span><br/>                  | <span data-ttu-id="03072-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="03072-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="03072-138">標頭</span><span class="sxs-lookup"><span data-stu-id="03072-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="03072-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="03072-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="03072-140">IID</span><span class="sxs-lookup"><span data-stu-id="03072-140">IID</span></span><br/>                      | <span data-ttu-id="03072-141">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="03072-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="03072-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03072-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03072-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="03072-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

