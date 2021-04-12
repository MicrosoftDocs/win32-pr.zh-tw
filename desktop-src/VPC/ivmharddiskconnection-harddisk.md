---
title: 'IVMHardDiskConnection 硬碟屬性 (VPCCOMInterfaces .h) '
description: 抓取對應至此連接的硬碟物件。
ms.assetid: dbe369d8-ec05-4039-9494-fc196262f697
keywords:
- 硬碟屬性虛擬電腦
- 硬碟屬性虛擬 PC，IVMHardDiskConnection 介面
- IVMHardDiskConnection 介面 Virtual PC，硬碟屬性
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.HardDisk
- IVMHardDiskConnection.get_HardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9baa365606b71b693dd841471d50a475a42677d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384858"
---
# <a name="ivmharddiskconnectionharddisk-property"></a><span data-ttu-id="d7957-106">IVMHardDiskConnection：：硬碟屬性</span><span class="sxs-lookup"><span data-stu-id="d7957-106">IVMHardDiskConnection::HardDisk property</span></span>

<span data-ttu-id="d7957-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="d7957-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d7957-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="d7957-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d7957-109">抓取對應至此連接的硬碟物件。</span><span class="sxs-lookup"><span data-stu-id="d7957-109">Retrieves a hard disk object corresponding to this connection.</span></span>

<span data-ttu-id="d7957-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d7957-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7957-111">語法</span><span class="sxs-lookup"><span data-stu-id="d7957-111">Syntax</span></span>


```C++
HRESULT get_HardDisk(
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="d7957-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="d7957-112">Property value</span></span>

<span data-ttu-id="d7957-113">[**IVMHardDisk**](ivmharddisk.md)物件，描述與此連接相關聯的硬碟。</span><span class="sxs-lookup"><span data-stu-id="d7957-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d7957-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d7957-114">Error codes</span></span>



| <span data-ttu-id="d7957-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="d7957-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="d7957-116">意義</span><span class="sxs-lookup"><span data-stu-id="d7957-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7957-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d7957-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="d7957-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d7957-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="d7957-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d7957-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="d7957-120">參數為 **Null** 或無效。</span><span class="sxs-lookup"><span data-stu-id="d7957-120">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="d7957-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="d7957-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="d7957-122">目前的虛擬機器設定無效。</span><span class="sxs-lookup"><span data-stu-id="d7957-122">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="d7957-123"><dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="d7957-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="d7957-124">此連線的匯流排位置未正確地初始化，或此位置的裝置不是有效的硬碟。</span><span class="sxs-lookup"><span data-stu-id="d7957-124">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |
| <dl> <span data-ttu-id="d7957-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d7957-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="d7957-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d7957-126">An unexpected error has occurred.</span></span><br/>                                                                                                |



## <a name="requirements"></a><span data-ttu-id="d7957-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7957-127">Requirements</span></span>



| <span data-ttu-id="d7957-128">需求</span><span class="sxs-lookup"><span data-stu-id="d7957-128">Requirement</span></span> | <span data-ttu-id="d7957-129">值</span><span class="sxs-lookup"><span data-stu-id="d7957-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7957-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7957-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d7957-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7957-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7957-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7957-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d7957-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="d7957-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d7957-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d7957-134">End of client support</span></span><br/>    | <span data-ttu-id="d7957-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7957-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d7957-136">產品</span><span class="sxs-lookup"><span data-stu-id="d7957-136">Product</span></span><br/>                  | <span data-ttu-id="d7957-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d7957-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d7957-138">標頭</span><span class="sxs-lookup"><span data-stu-id="d7957-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7957-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7957-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d7957-140">IID</span><span class="sxs-lookup"><span data-stu-id="d7957-140">IID</span></span><br/>                      | <span data-ttu-id="d7957-141">IID \_ IVMHardDiskconnection 定義為 aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="d7957-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="d7957-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7957-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7957-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="d7957-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

