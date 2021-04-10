---
title: IMsTscAxEvents OnRemoteProgramResult 方法
description: 當 RemoteApp 程式傳回結果給用戶端控制項時呼叫。
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- OnRemoteProgramResult 方法遠端桌面服務
- OnRemoteProgramResult 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRemoteProgramResult 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880e4fb3f6453114415f5bcc07a0afb9c176a1bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104315"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a><span data-ttu-id="8849b-106">IMsTscAxEvents：： OnRemoteProgramResult 方法</span><span class="sxs-lookup"><span data-stu-id="8849b-106">IMsTscAxEvents::OnRemoteProgramResult method</span></span>

<span data-ttu-id="8849b-107">當 RemoteApp 程式傳回結果給用戶端控制項時呼叫。</span><span class="sxs-lookup"><span data-stu-id="8849b-107">Called when a RemoteApp program returns a result to the client control.</span></span>

## <a name="syntax"></a><span data-ttu-id="8849b-108">語法</span><span class="sxs-lookup"><span data-stu-id="8849b-108">Syntax</span></span>


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a><span data-ttu-id="8849b-109">參數</span><span class="sxs-lookup"><span data-stu-id="8849b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8849b-110">*bstrRemoteProgram* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8849b-110">*bstrRemoteProgram* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8849b-111">RemoteApp 程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="8849b-111">The name of the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="8849b-112">*lError* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8849b-112">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8849b-113">嘗試啟動 RemoteApp 程式的結果。</span><span class="sxs-lookup"><span data-stu-id="8849b-113">The result of the attempt to launch the RemoteApp program.</span></span>

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span data-ttu-id="8849b-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="8849b-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8849b-115">RemoteApp 程式已順利啟動。</span><span class="sxs-lookup"><span data-stu-id="8849b-115">The RemoteApp program launched successfully.</span></span>

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span data-ttu-id="8849b-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="8849b-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="8849b-117">遠端會話已鎖定，而且無法啟動 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="8849b-117">The remote session is locked and the RemoteApp program cannot be launched.</span></span> <span data-ttu-id="8849b-118">使用者必須輸入其認證才能解除鎖定會話，然後啟動 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="8849b-118">The user must enter their credentials to unlock the session, and then launch the RemoteApp program.</span></span>

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span data-ttu-id="8849b-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="8849b-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="8849b-120">RemoteApp 程式傳回通訊協定錯誤。</span><span class="sxs-lookup"><span data-stu-id="8849b-120">The RemoteApp program returned a protocol error.</span></span>

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span data-ttu-id="8849b-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3) ) </span><span class="sxs-lookup"><span data-stu-id="8849b-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="8849b-122">RemoteApp 程式不在 RD 工作階段主機伺服器的核准清單中。</span><span class="sxs-lookup"><span data-stu-id="8849b-122">The RemoteApp program is not in the approved list of the RD Session Host server.</span></span>

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span data-ttu-id="8849b-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="8849b-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="8849b-124">已拒絕 RemoteApp 程式的網路路徑。</span><span class="sxs-lookup"><span data-stu-id="8849b-124">The network path to the RemoteApp program was denied.</span></span>

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span data-ttu-id="8849b-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5) ) </span><span class="sxs-lookup"><span data-stu-id="8849b-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="8849b-126">找不到 RemoteApp 程式檔。</span><span class="sxs-lookup"><span data-stu-id="8849b-126">The RemoteApp program file was not found.</span></span>

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span data-ttu-id="8849b-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6) ) </span><span class="sxs-lookup"><span data-stu-id="8849b-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="8849b-128">RemoteApp 程式無法啟動。</span><span class="sxs-lookup"><span data-stu-id="8849b-128">The RemoteApp program failed to launch.</span></span>

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span data-ttu-id="8849b-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7) ) </span><span class="sxs-lookup"><span data-stu-id="8849b-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span></span>


</dt> <dd>

<span data-ttu-id="8849b-130">因為會話目前顯示安全桌面，所以無法啟動 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="8849b-130">The RemoteApp program cannot be launched because the session is currently displaying the secure desktop.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8849b-131">*vbIsExecutable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8849b-131">*vbIsExecutable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8849b-132">指出是否已使用檔案關聯，直接使用可執行檔名稱或間接啟動 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="8849b-132">Indicates whether the RemoteApp program was launched directly, by using the executable name or indirectly, by using a file association.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8849b-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="8849b-133">Return value</span></span>

<span data-ttu-id="8849b-134">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8849b-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8849b-135">備註</span><span class="sxs-lookup"><span data-stu-id="8849b-135">Remarks</span></span>

<span data-ttu-id="8849b-136">在事件接收中執行此方法，以接收 RemoteApp 程式傳回結果的通知。</span><span class="sxs-lookup"><span data-stu-id="8849b-136">Implement this method in your event sink to receive notification that a RemoteApp program returned a result.</span></span>

<span data-ttu-id="8849b-137">這個方法會在 ActiveX 控制項嘗試啟動 RemoteApp 程式之後立即呼叫，而 *lError* 參數會指出嘗試的結果。</span><span class="sxs-lookup"><span data-stu-id="8849b-137">This method is called immediately after the ActiveX control attempts to launch the RemoteApp program, and the *lError* parameter indicates the result of the attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="8849b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="8849b-138">Requirements</span></span>



| <span data-ttu-id="8849b-139">需求</span><span class="sxs-lookup"><span data-stu-id="8849b-139">Requirement</span></span> | <span data-ttu-id="8849b-140">值</span><span class="sxs-lookup"><span data-stu-id="8849b-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8849b-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8849b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8849b-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="8849b-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8849b-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8849b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8849b-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8849b-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8849b-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8849b-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="8849b-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8849b-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8849b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8849b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8849b-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8849b-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8849b-149">IID</span><span class="sxs-lookup"><span data-stu-id="8849b-149">IID</span></span><br/>                      | <span data-ttu-id="8849b-150">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="8849b-150">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8849b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8849b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8849b-152">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="8849b-152">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





