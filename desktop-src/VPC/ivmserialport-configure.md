---
title: 'IVMSerialPort Configure 方法 (VPCCOMInterfaces .h) '
description: 設定序列埠。
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- 設定方法 Virtual PC
- 設定方法 Virtual PC，IVMSerialPort 介面
- IVMSerialPort 介面 Virtual PC，Configure 方法
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025166"
---
# <a name="ivmserialportconfigure-method"></a><span data-ttu-id="541cd-106">IVMSerialPort：： Configure 方法</span><span class="sxs-lookup"><span data-stu-id="541cd-106">IVMSerialPort::Configure method</span></span>

<span data-ttu-id="541cd-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="541cd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="541cd-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="541cd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="541cd-109">設定序列埠。</span><span class="sxs-lookup"><span data-stu-id="541cd-109">Configures the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="541cd-110">語法</span><span class="sxs-lookup"><span data-stu-id="541cd-110">Syntax</span></span>


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a><span data-ttu-id="541cd-111">參數</span><span class="sxs-lookup"><span data-stu-id="541cd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="541cd-112">*portType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="541cd-112">*portType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541cd-113">序列埠的類型。</span><span class="sxs-lookup"><span data-stu-id="541cd-113">The type of serial port.</span></span> <span data-ttu-id="541cd-114">如需值的清單，請參閱 [**VMSerialPortType**](vmserialporttype.md)。</span><span class="sxs-lookup"><span data-stu-id="541cd-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

</dd> <dt>

<span data-ttu-id="541cd-115">*portName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="541cd-115">*portName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541cd-116">序列埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="541cd-116">The name of the serial port.</span></span> <span data-ttu-id="541cd-117">例如，"COM1" 代表 **vmSerialPort \_ HostPort**，"C： \\SerialPort.txt" 代表 **vmSerialPort \_ TextFile**，" \\ \\ *servername* \\ pipe \\ *pipename*" 代表 **vmSerialPort \_ NamedPipe**。</span><span class="sxs-lookup"><span data-stu-id="541cd-117">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

</dd> <dt>

<span data-ttu-id="541cd-118">*vmConnectImmediately* \[在\]</span><span class="sxs-lookup"><span data-stu-id="541cd-118">*vmConnectImmediately* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541cd-119">如果啟動虛擬機器時應立即開啟主機序列埠，則 **為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="541cd-119">**TRUE** if the host serial port should be opened immediately when the virtual machine is started and **FALSE** otherwise.</span></span> <span data-ttu-id="541cd-120">如果 *portType* 不是 **vmSerialPort \_ HostPort**，則會忽略。</span><span class="sxs-lookup"><span data-stu-id="541cd-120">Ignored if *portType* is not **vmSerialPort\_HostPort**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="541cd-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="541cd-121">Return value</span></span>

<span data-ttu-id="541cd-122">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="541cd-122">This method can return one of these values.</span></span>



| <span data-ttu-id="541cd-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="541cd-123">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="541cd-124">Description</span><span class="sxs-lookup"><span data-stu-id="541cd-124">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="541cd-125"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-125"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="541cd-126">作業成功。</span><span class="sxs-lookup"><span data-stu-id="541cd-126">The operation was successful.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="541cd-127"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="541cd-128">*PortType* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="541cd-128">The *portType* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="541cd-129"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="541cd-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="541cd-130">An unexpected error has occurred.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="541cd-131"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-131"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="541cd-132">*PortName* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="541cd-132">The *portName* parameter is **NULL**.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="541cd-133"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="541cd-134">沒有足夠的記憶體可完成此要求。</span><span class="sxs-lookup"><span data-stu-id="541cd-134">There is not enough memory available to complete this request.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="541cd-135"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="541cd-136">*PortName* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="541cd-136">The path specified by the *portName* parameter is too long.</span></span> <span data-ttu-id="541cd-137">路徑必須小於 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="541cd-137">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="541cd-138"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="541cd-139">*PortName* 參數包含不正確字元 (" \* ？ <>/ \| "： ") 之一。</span><span class="sxs-lookup"><span data-stu-id="541cd-139">The *portName* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="541cd-140"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="541cd-141">*PortName* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="541cd-141">The *portName* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="541cd-142">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="541cd-142">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="541cd-143"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-143"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="541cd-144">此虛擬機器的設定無效。</span><span class="sxs-lookup"><span data-stu-id="541cd-144">The configuration for this virtual machine is not valid.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="541cd-145"><dt>**VM \_E \_ PREF 不 \_ 合法的 \_ 值**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-145"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>                   | <span data-ttu-id="541cd-146">指定的埠已在使用中。</span><span class="sxs-lookup"><span data-stu-id="541cd-146">The specified port is already in use.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="541cd-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="541cd-147">Requirements</span></span>



| <span data-ttu-id="541cd-148">需求</span><span class="sxs-lookup"><span data-stu-id="541cd-148">Requirement</span></span> | <span data-ttu-id="541cd-149">值</span><span class="sxs-lookup"><span data-stu-id="541cd-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="541cd-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="541cd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="541cd-151">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="541cd-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="541cd-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="541cd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="541cd-153">都不支援</span><span class="sxs-lookup"><span data-stu-id="541cd-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="541cd-154">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="541cd-154">End of client support</span></span><br/>    | <span data-ttu-id="541cd-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="541cd-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="541cd-156">產品</span><span class="sxs-lookup"><span data-stu-id="541cd-156">Product</span></span><br/>                  | <span data-ttu-id="541cd-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="541cd-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="541cd-158">標頭</span><span class="sxs-lookup"><span data-stu-id="541cd-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="541cd-159"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="541cd-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="541cd-160">IID</span><span class="sxs-lookup"><span data-stu-id="541cd-160">IID</span></span><br/>                      | <span data-ttu-id="541cd-161">IID \_ IVMSerialPort 定義為 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="541cd-161">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="541cd-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="541cd-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541cd-163">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="541cd-163">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

