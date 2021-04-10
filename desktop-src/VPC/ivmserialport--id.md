---
title: 'IVMSerialPort _ID 方法 (VPCCOMInterfaces .h) '
description: 序列埠的內部識別碼。
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- _ID 方法 Virtual PC
- _ID 方法 Virtual PC，IVMSerialPort 介面
- IVMSerialPort 介面 Virtual PC，_ID 方法
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e60f301f80f24681ee297d0fb579994561155
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094540"
---
# <a name="ivmserialport_id-method"></a><span data-ttu-id="0b03f-106">IVMSerialPort：： \_ ID 方法</span><span class="sxs-lookup"><span data-stu-id="0b03f-106">IVMSerialPort::\_ID method</span></span>

<span data-ttu-id="0b03f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="0b03f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0b03f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="0b03f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0b03f-109">捕獲序列埠的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b03f-109">Retrieves the internal identifier of the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b03f-110">語法</span><span class="sxs-lookup"><span data-stu-id="0b03f-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="0b03f-111">參數</span><span class="sxs-lookup"><span data-stu-id="0b03f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b03f-112">*portID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0b03f-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b03f-113">序列埠識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b03f-113">The serial port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b03f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b03f-114">Return value</span></span>

<span data-ttu-id="0b03f-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0b03f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="0b03f-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="0b03f-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="0b03f-117">Description</span><span class="sxs-lookup"><span data-stu-id="0b03f-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b03f-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0b03f-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0b03f-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0b03f-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="0b03f-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0b03f-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0b03f-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0b03f-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="0b03f-122"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0b03f-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0b03f-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b03f-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="0b03f-124"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="0b03f-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="0b03f-125">此虛擬機器的設定無效。</span><span class="sxs-lookup"><span data-stu-id="0b03f-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b03f-126">備註</span><span class="sxs-lookup"><span data-stu-id="0b03f-126">Remarks</span></span>

<span data-ttu-id="0b03f-127">指令碼語言無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0b03f-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b03f-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b03f-128">Requirements</span></span>



| <span data-ttu-id="0b03f-129">需求</span><span class="sxs-lookup"><span data-stu-id="0b03f-129">Requirement</span></span> | <span data-ttu-id="0b03f-130">值</span><span class="sxs-lookup"><span data-stu-id="0b03f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b03f-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b03f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0b03f-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b03f-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b03f-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b03f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0b03f-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="0b03f-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0b03f-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0b03f-135">End of client support</span></span><br/>    | <span data-ttu-id="0b03f-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b03f-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0b03f-137">產品</span><span class="sxs-lookup"><span data-stu-id="0b03f-137">Product</span></span><br/>                  | <span data-ttu-id="0b03f-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0b03f-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0b03f-139">標頭</span><span class="sxs-lookup"><span data-stu-id="0b03f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b03f-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b03f-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0b03f-141">IID</span><span class="sxs-lookup"><span data-stu-id="0b03f-141">IID</span></span><br/>                      | <span data-ttu-id="0b03f-142">IID \_ IVMSerialPort 定義為 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="0b03f-142">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="0b03f-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b03f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b03f-144">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="0b03f-144">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

