---
title: 'IVMSerialPort ConnectImmediately 屬性 (VPCCOMInterfaces .h) '
description: 判斷是否應該在不等候數據機命令的情況下開啟序列埠。
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- ConnectImmediately 屬性 Virtual PC
- ConnectImmediately 屬性 Virtual PC，IVMSerialPort 介面
- IVMSerialPort 介面 Virtual PC，ConnectImmediately 屬性
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685968"
---
# <a name="ivmserialportconnectimmediately-property"></a><span data-ttu-id="3442e-106">IVMSerialPort：： ConnectImmediately 屬性</span><span class="sxs-lookup"><span data-stu-id="3442e-106">IVMSerialPort::ConnectImmediately property</span></span>

<span data-ttu-id="3442e-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3442e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3442e-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3442e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3442e-109">判斷是否應該在不等候數據機命令的情況下開啟序列埠。</span><span class="sxs-lookup"><span data-stu-id="3442e-109">Determines whether the serial port should be opened without waiting for a modem command to be received.</span></span>

<span data-ttu-id="3442e-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="3442e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3442e-111">語法</span><span class="sxs-lookup"><span data-stu-id="3442e-111">Syntax</span></span>


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a><span data-ttu-id="3442e-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="3442e-112">Property value</span></span>

<span data-ttu-id="3442e-113">**變異 \_** 如果應該在不等候數據機命令的情況下開啟序列埠，則為 TRUE;**變異 \_否則為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3442e-113">**VARIANT\_TRUE** if the serial port should be opened without waiting for a modem command to be received; **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3442e-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3442e-114">Error codes</span></span>



| <span data-ttu-id="3442e-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="3442e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3442e-116">意義</span><span class="sxs-lookup"><span data-stu-id="3442e-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="3442e-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3442e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3442e-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="3442e-118">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="3442e-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3442e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3442e-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3442e-120">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="3442e-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="3442e-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="3442e-122">此虛擬機器的設定無效。</span><span class="sxs-lookup"><span data-stu-id="3442e-122">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="3442e-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3442e-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3442e-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3442e-124">An unexpected error has occurred.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="3442e-125">備註</span><span class="sxs-lookup"><span data-stu-id="3442e-125">Remarks</span></span>

<span data-ttu-id="3442e-126">只有在 [埠 [**類型**](ivmserialport-type.md) ] 屬性是 [ **vmSerialPort \_ HostPort**] 時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="3442e-126">This property is valid only if the port [**Type**](ivmserialport-type.md) property is **vmSerialPort\_HostPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3442e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3442e-127">Requirements</span></span>



| <span data-ttu-id="3442e-128">需求</span><span class="sxs-lookup"><span data-stu-id="3442e-128">Requirement</span></span> | <span data-ttu-id="3442e-129">值</span><span class="sxs-lookup"><span data-stu-id="3442e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3442e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3442e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3442e-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3442e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3442e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3442e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3442e-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="3442e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3442e-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3442e-134">End of client support</span></span><br/>    | <span data-ttu-id="3442e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3442e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3442e-136">產品</span><span class="sxs-lookup"><span data-stu-id="3442e-136">Product</span></span><br/>                  | <span data-ttu-id="3442e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3442e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3442e-138">標頭</span><span class="sxs-lookup"><span data-stu-id="3442e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3442e-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3442e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3442e-140">IID</span><span class="sxs-lookup"><span data-stu-id="3442e-140">IID</span></span><br/>                      | <span data-ttu-id="3442e-141">IID \_ IVMSerialPort 定義為 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="3442e-141">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="3442e-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3442e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3442e-143">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="3442e-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

