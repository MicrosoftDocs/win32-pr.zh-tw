---
title: 'IVMSerialPort Type 屬性 (VPCCOMInterfaces .h) '
description: 捕獲序列埠的類型。
ms.assetid: 0ec9c9d7-9387-458e-befe-42d58c38df35
keywords:
- 類型虛擬電腦
- Type property Virtual PC，IVMSerialPort 介面
- IVMSerialPort 介面 Virtual PC，Type 屬性
topic_type:
- apiref
api_name:
- IVMSerialPort.Type
- IVMSerialPort.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ab32ba6e205911fca85474c047e24b7ad7f1f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465537"
---
# <a name="ivmserialporttype-property"></a><span data-ttu-id="e8265-106">IVMSerialPort：： Type 屬性</span><span class="sxs-lookup"><span data-stu-id="e8265-106">IVMSerialPort::Type property</span></span>

<span data-ttu-id="e8265-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e8265-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8265-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e8265-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8265-109">捕獲序列埠的類型。</span><span class="sxs-lookup"><span data-stu-id="e8265-109">Retrieves the type of the serial port.</span></span>

<span data-ttu-id="e8265-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e8265-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8265-111">語法</span><span class="sxs-lookup"><span data-stu-id="e8265-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMSerialPortType *portType
);
```



## <a name="property-value"></a><span data-ttu-id="e8265-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="e8265-112">Property value</span></span>

<span data-ttu-id="e8265-113">序列埠的類型。</span><span class="sxs-lookup"><span data-stu-id="e8265-113">The type of serial port.</span></span> <span data-ttu-id="e8265-114">如需值的清單，請參閱 [**VMSerialPortType**](vmserialporttype.md)。</span><span class="sxs-lookup"><span data-stu-id="e8265-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="e8265-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e8265-115">Error codes</span></span>



| <span data-ttu-id="e8265-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="e8265-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e8265-117">意義</span><span class="sxs-lookup"><span data-stu-id="e8265-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8265-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e8265-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e8265-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e8265-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="e8265-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e8265-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e8265-121">參數為 Null。</span><span class="sxs-lookup"><span data-stu-id="e8265-121">The parameter is NULL.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e8265-122"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="e8265-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="e8265-123">此虛擬機器的設定無效。</span><span class="sxs-lookup"><span data-stu-id="e8265-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="e8265-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e8265-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e8265-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e8265-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="e8265-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8265-126">Requirements</span></span>



| <span data-ttu-id="e8265-127">需求</span><span class="sxs-lookup"><span data-stu-id="e8265-127">Requirement</span></span> | <span data-ttu-id="e8265-128">值</span><span class="sxs-lookup"><span data-stu-id="e8265-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8265-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8265-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e8265-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8265-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8265-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8265-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e8265-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="e8265-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e8265-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e8265-133">End of client support</span></span><br/>    | <span data-ttu-id="e8265-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8265-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8265-135">產品</span><span class="sxs-lookup"><span data-stu-id="e8265-135">Product</span></span><br/>                  | <span data-ttu-id="e8265-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8265-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e8265-137">標頭</span><span class="sxs-lookup"><span data-stu-id="e8265-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8265-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8265-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e8265-139">IID</span><span class="sxs-lookup"><span data-stu-id="e8265-139">IID</span></span><br/>                      | <span data-ttu-id="e8265-140">IID \_ IVMSerialPort 定義為 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="e8265-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="e8265-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8265-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8265-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="e8265-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

