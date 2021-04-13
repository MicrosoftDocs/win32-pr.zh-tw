---
title: 'IVMVirtualMachine StartCommunicationChannel 方法 (VPCCOMInterfaces .h) '
description: 設定主機與客體作業系統之間的通道。
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- StartCommunicationChannel 方法 Virtual PC
- StartCommunicationChannel 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，StartCommunicationChannel 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466380"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a><span data-ttu-id="607ae-106">IVMVirtualMachine：： StartCommunicationChannel 方法</span><span class="sxs-lookup"><span data-stu-id="607ae-106">IVMVirtualMachine::StartCommunicationChannel method</span></span>

<span data-ttu-id="607ae-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="607ae-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="607ae-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="607ae-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="607ae-109">設定主機與客體作業系統之間的通道。</span><span class="sxs-lookup"><span data-stu-id="607ae-109">Sets up a communication channel between host and guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="607ae-110">語法</span><span class="sxs-lookup"><span data-stu-id="607ae-110">Syntax</span></span>


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a><span data-ttu-id="607ae-111">參數</span><span class="sxs-lookup"><span data-stu-id="607ae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="607ae-112">*inHostEndpointType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="607ae-112">*inHostEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="607ae-113">此參數必須是 **vmEndpoint \_ NamedPipe** (0) 。</span><span class="sxs-lookup"><span data-stu-id="607ae-113">This parameter must be **vmEndpoint\_NamedPipe** (0).</span></span>

</dd> <dt>

<span data-ttu-id="607ae-114">*inHostEndPointName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="607ae-114">*inHostEndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="607ae-115">唯一的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="607ae-115">The unique pipe name.</span></span> <span data-ttu-id="607ae-116">這個字串的格式必須如下： " \\ \\ 。 \\pipe \\ *pipename*」。</span><span class="sxs-lookup"><span data-stu-id="607ae-116">This string must have the following form: "\\\\.\\pipe\\*pipename*".</span></span> <span data-ttu-id="607ae-117">名稱的 *pipename* 部分可以包含反斜線以外的任何字元，包括數位和特殊字元。</span><span class="sxs-lookup"><span data-stu-id="607ae-117">The *pipename* part of the name can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="607ae-118">整個管道名稱字串的長度最多可達256個字元。</span><span class="sxs-lookup"><span data-stu-id="607ae-118">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="607ae-119">管道名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="607ae-119">Pipe names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="607ae-120">*inGuestEndpointType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="607ae-120">*inGuestEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="607ae-121">此參數必須是 **vmEndpoint \_ TCPIP** (1) 。</span><span class="sxs-lookup"><span data-stu-id="607ae-121">This parameter must be **vmEndpoint\_TCPIP** (1).</span></span>

</dd> <dt>

<span data-ttu-id="607ae-122">*inGuestEndpointName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="607ae-122">*inGuestEndpointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="607ae-123">來賓中 TCP 伺服器正在接聽的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="607ae-123">The port number on which the TCP server in the guest is listening.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="607ae-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="607ae-124">Return value</span></span>

<span data-ttu-id="607ae-125">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="607ae-125">This method can return one of these values.</span></span>



| <span data-ttu-id="607ae-126">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="607ae-126">Return code/value</span></span>                                                                                                                                                                                  | <span data-ttu-id="607ae-127">Description</span><span class="sxs-lookup"><span data-stu-id="607ae-127">Description</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="607ae-128"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-128"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                        | <span data-ttu-id="607ae-129">作業成功。</span><span class="sxs-lookup"><span data-stu-id="607ae-129">The operation was successful.</span></span><br/>                                                                                                                    |
| <dl> <span data-ttu-id="607ae-130"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-130"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                       | <span data-ttu-id="607ae-131">*InHostEndpointType* 參數不是 **vmEndpoint \_ NamedPipe** (0) 或 *inGuestEndpointType* 參數不是 **vmEndpoint \_ TCPIP** (1) 。</span><span class="sxs-lookup"><span data-stu-id="607ae-131">The *inHostEndpointType* parameter is not **vmEndpoint\_NamedPipe** (0) or the *inGuestEndpointType* parameter is not **vmEndpoint\_TCPIP** (1).</span></span><br/> |
| <dl> <span data-ttu-id="607ae-132"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-132"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                          | <span data-ttu-id="607ae-133">*InHostEndPointName* 或 *InGuestEndpointName* 參數為 **Null** 或不是有效的值。</span><span class="sxs-lookup"><span data-stu-id="607ae-133">The *inHostEndPointName* or *inGuestEndpointName* parameter is **NULL** or not a valid value.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="607ae-134"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                                  | <span data-ttu-id="607ae-135">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="607ae-135">An unexpected error has occurred.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="607ae-136"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 不正確 \_ 控制碼)**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_HANDLE)**</dt> <dt>0x80070006</dt></span></span> </dl>        | <span data-ttu-id="607ae-137">控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="607ae-137">A handle is not valid.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="607ae-138"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>            | <span data-ttu-id="607ae-139">沒有足夠的記憶體可完成此要求。</span><span class="sxs-lookup"><span data-stu-id="607ae-139">There is not enough memory available to complete this request.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="607ae-140"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 未 \_ 就緒)**</dt> <dt>0x80070015</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_READY)**</dt> <dt>0x80070015</dt></span></span> </dl>             | <span data-ttu-id="607ae-141">它用來提供網路服務的基礎系統目前正在初始化。</span><span class="sxs-lookup"><span data-stu-id="607ae-141">The underlying system it uses to provide network services is currently being initialized.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="607ae-142"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>        | <span data-ttu-id="607ae-143">管道名稱已在使用中。</span><span class="sxs-lookup"><span data-stu-id="607ae-143">The pipe name is already in use.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="607ae-144"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 管道 \_ 忙碌)**</dt> <dt>0x800700e7</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PIPE\_BUSY)**</dt> <dt>0x800700e7</dt></span></span> </dl>             | <span data-ttu-id="607ae-145">有一或多個通道正在執行，而且很快就會推出。</span><span class="sxs-lookup"><span data-stu-id="607ae-145">One or more channels are running down and may become available shortly.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="607ae-146"><dt>**HRESULT \_從 \_ WIN32 (已 \_ 達到錯誤的最大 \_ 會話 \_)**</dt> <dt>0x80070161</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_MAX\_SESSIONS\_REACHED)**</dt> <dt>0x80070161</dt></span></span> </dl> | <span data-ttu-id="607ae-147">可用的通訊通道數目上限已在使用中。</span><span class="sxs-lookup"><span data-stu-id="607ae-147">The maximum numbers of communication channels available are in-use.</span></span> <span data-ttu-id="607ae-148">目前無法啟動另一個通道。</span><span class="sxs-lookup"><span data-stu-id="607ae-148">Another channel cannot be started at this time.</span></span><br/>                              |
| <dl> <span data-ttu-id="607ae-149"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 修訂 \_ 不相符)**</dt> <dt>0x8007051a</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-149"><dt>**HRESULT\_FROM\_WIN32(ERROR\_REVISION\_MISMATCH)**</dt> <dt>0x8007051a</dt></span></span> </dl>     | <span data-ttu-id="607ae-150">主機和來賓子系統的版本不相符。</span><span class="sxs-lookup"><span data-stu-id="607ae-150">There is a mismatch between the version of the host and guest subsystems.</span></span> <span data-ttu-id="607ae-151">如需詳細資訊，請參閱 Windows 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="607ae-151">See the Windows Event Log for more detail.</span></span><br/>                             |
| <dl> <span data-ttu-id="607ae-152"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-152"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                             | <span data-ttu-id="607ae-153">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="607ae-153">The VM is not running.</span></span><br/>                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="607ae-154">備註</span><span class="sxs-lookup"><span data-stu-id="607ae-154">Remarks</span></span>

<span data-ttu-id="607ae-155">目前的執行僅支援在客體作業系統上的主機和 TCP/IP 介面上具名管道介面。</span><span class="sxs-lookup"><span data-stu-id="607ae-155">The current implementation supports only named pipe interface on the host and TCP/IP interface on the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="607ae-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="607ae-156">Requirements</span></span>



| <span data-ttu-id="607ae-157">需求</span><span class="sxs-lookup"><span data-stu-id="607ae-157">Requirement</span></span> | <span data-ttu-id="607ae-158">值</span><span class="sxs-lookup"><span data-stu-id="607ae-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="607ae-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="607ae-159">Minimum supported client</span></span><br/> | <span data-ttu-id="607ae-160">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="607ae-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="607ae-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="607ae-161">Minimum supported server</span></span><br/> | <span data-ttu-id="607ae-162">都不支援</span><span class="sxs-lookup"><span data-stu-id="607ae-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="607ae-163">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="607ae-163">End of client support</span></span><br/>    | <span data-ttu-id="607ae-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="607ae-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="607ae-165">產品</span><span class="sxs-lookup"><span data-stu-id="607ae-165">Product</span></span><br/>                  | <span data-ttu-id="607ae-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="607ae-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="607ae-167">標頭</span><span class="sxs-lookup"><span data-stu-id="607ae-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="607ae-168"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="607ae-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="607ae-169">IID</span><span class="sxs-lookup"><span data-stu-id="607ae-169">IID</span></span><br/>                      | <span data-ttu-id="607ae-170">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="607ae-170">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="607ae-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="607ae-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607ae-172">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="607ae-172">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="607ae-173">**VMEndpointType**</span><span class="sxs-lookup"><span data-stu-id="607ae-173">**VMEndpointType**</span></span>](vmendpointtype.md)
</dt> </dl>

 

