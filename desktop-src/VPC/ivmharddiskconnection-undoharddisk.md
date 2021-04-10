---
title: 'IVMHardDiskConnection UndoHardDisk 屬性 (VPCCOMInterfaces .h) '
description: 抓取與此連接之復原磁片映射對應的硬碟物件。
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- UndoHardDisk 屬性 Virtual PC
- UndoHardDisk 屬性 Virtual PC，IVMHardDiskConnection 介面
- IVMHardDiskConnection 介面 Virtual PC，UndoHardDisk 屬性
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093768"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a><span data-ttu-id="83c90-106">IVMHardDiskConnection：： UndoHardDisk 屬性</span><span class="sxs-lookup"><span data-stu-id="83c90-106">IVMHardDiskConnection::UndoHardDisk property</span></span>

<span data-ttu-id="83c90-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="83c90-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="83c90-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="83c90-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="83c90-109">抓取與此連接之復原磁片映射對應的硬碟物件。</span><span class="sxs-lookup"><span data-stu-id="83c90-109">Retrieves a hard disk object corresponding to this connection's undo disk image.</span></span>

<span data-ttu-id="83c90-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="83c90-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c90-111">語法</span><span class="sxs-lookup"><span data-stu-id="83c90-111">Syntax</span></span>


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="83c90-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="83c90-112">Property value</span></span>

<span data-ttu-id="83c90-113">描述與此連接相關聯之復原硬碟的 [**IVMHardDisk**](ivmharddisk.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="83c90-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the undo hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="83c90-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="83c90-114">Error codes</span></span>



| <span data-ttu-id="83c90-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="83c90-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="83c90-116">意義</span><span class="sxs-lookup"><span data-stu-id="83c90-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83c90-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="83c90-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="83c90-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="83c90-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="83c90-119"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="83c90-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="83c90-120">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="83c90-120">An unexpected error has occurred.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="83c90-121"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="83c90-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="83c90-122">參數為 **Null** 或無效。</span><span class="sxs-lookup"><span data-stu-id="83c90-122">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="83c90-123"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="83c90-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="83c90-124">找不到此連接的復原磁片。</span><span class="sxs-lookup"><span data-stu-id="83c90-124">The undo disk for this connection was not found.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="83c90-125"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="83c90-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="83c90-126">目前的虛擬機器設定無效。</span><span class="sxs-lookup"><span data-stu-id="83c90-126">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="83c90-127"><dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="83c90-127"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="83c90-128">此連線的匯流排位置未正確地初始化，或此位置的裝置不是有效的硬碟。</span><span class="sxs-lookup"><span data-stu-id="83c90-128">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="83c90-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="83c90-129">Requirements</span></span>



| <span data-ttu-id="83c90-130">需求</span><span class="sxs-lookup"><span data-stu-id="83c90-130">Requirement</span></span> | <span data-ttu-id="83c90-131">值</span><span class="sxs-lookup"><span data-stu-id="83c90-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c90-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83c90-132">Minimum supported client</span></span><br/> | <span data-ttu-id="83c90-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83c90-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83c90-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83c90-134">Minimum supported server</span></span><br/> | <span data-ttu-id="83c90-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="83c90-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="83c90-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="83c90-136">End of client support</span></span><br/>    | <span data-ttu-id="83c90-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="83c90-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="83c90-138">產品</span><span class="sxs-lookup"><span data-stu-id="83c90-138">Product</span></span><br/>                  | <span data-ttu-id="83c90-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="83c90-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="83c90-140">標頭</span><span class="sxs-lookup"><span data-stu-id="83c90-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c90-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="83c90-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="83c90-142">IID</span><span class="sxs-lookup"><span data-stu-id="83c90-142">IID</span></span><br/>                      | <span data-ttu-id="83c90-143">IID \_ IVMHardDiskconnection 定義為 aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="83c90-143">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="83c90-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83c90-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c90-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="83c90-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

