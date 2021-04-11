---
title: 'IVMSerialPort Name 屬性 (VPCCOMInterfaces .h) '
description: 序列埠的名稱。
ms.assetid: 4d3fe008-f089-4a1b-9c90-2e0b3ded58fa
keywords:
- Name 屬性 Virtual PC
- Name 屬性 Virtual PC，IVMSerialPort 介面
- IVMSerialPort 介面 Virtual PC，Name 屬性
topic_type:
- apiref
api_name:
- IVMSerialPort.Name
- IVMSerialPort.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540540e2af91647b9c77735a1c601ed62aecdbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844147"
---
# <a name="ivmserialportname-property"></a><span data-ttu-id="5d890-106">IVMSerialPort：： Name 屬性</span><span class="sxs-lookup"><span data-stu-id="5d890-106">IVMSerialPort::Name property</span></span>

<span data-ttu-id="5d890-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="5d890-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5d890-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="5d890-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5d890-109">捕獲序列埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d890-109">Retrieves the name of the serial port.</span></span>

<span data-ttu-id="5d890-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5d890-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d890-111">語法</span><span class="sxs-lookup"><span data-stu-id="5d890-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="5d890-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="5d890-112">Property value</span></span>

<span data-ttu-id="5d890-113">序列埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d890-113">The name of the serial port.</span></span> <span data-ttu-id="5d890-114">例如，"COM1" 代表 **vmSerialPort \_ HostPort**，"C： \\SerialPort.txt" 代表 **vmSerialPort \_ TextFile**，" \\ \\ *servername* \\ pipe \\ *pipename*" 代表 **vmSerialPort \_ NamedPipe**。</span><span class="sxs-lookup"><span data-stu-id="5d890-114">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5d890-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5d890-115">Error codes</span></span>



| <span data-ttu-id="5d890-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="5d890-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="5d890-117">意義</span><span class="sxs-lookup"><span data-stu-id="5d890-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d890-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5d890-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5d890-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="5d890-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="5d890-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5d890-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="5d890-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5d890-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="5d890-122"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="5d890-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="5d890-123">此虛擬機器的設定無效。</span><span class="sxs-lookup"><span data-stu-id="5d890-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="5d890-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5d890-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5d890-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5d890-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="5d890-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d890-126">Requirements</span></span>



| <span data-ttu-id="5d890-127">需求</span><span class="sxs-lookup"><span data-stu-id="5d890-127">Requirement</span></span> | <span data-ttu-id="5d890-128">值</span><span class="sxs-lookup"><span data-stu-id="5d890-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d890-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d890-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5d890-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d890-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d890-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d890-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5d890-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="5d890-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5d890-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5d890-133">End of client support</span></span><br/>    | <span data-ttu-id="5d890-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5d890-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5d890-135">產品</span><span class="sxs-lookup"><span data-stu-id="5d890-135">Product</span></span><br/>                  | <span data-ttu-id="5d890-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5d890-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5d890-137">標頭</span><span class="sxs-lookup"><span data-stu-id="5d890-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d890-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d890-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5d890-139">IID</span><span class="sxs-lookup"><span data-stu-id="5d890-139">IID</span></span><br/>                      | <span data-ttu-id="5d890-140">IID \_ IVMSerialPort 定義為 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="5d890-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="5d890-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d890-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d890-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="5d890-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

