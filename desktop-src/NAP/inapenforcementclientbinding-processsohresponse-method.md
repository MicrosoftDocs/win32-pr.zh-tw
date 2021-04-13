---
title: 'INapEnforcementClientBinding ProcessSoHResponse 方法 (NapEnforcementClient .h) '
description: 會在強制用戶端從強制服務器收到 SoHResponse 資料 blob 時，用來處理 SoHResponse。
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- ProcessSoHResponse 方法 NAP
- ProcessSoHResponse 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，ProcessSoHResponse 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509456"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a><span data-ttu-id="49337-106">INapEnforcementClientBinding：:P rocessSoHResponse 方法</span><span class="sxs-lookup"><span data-stu-id="49337-106">INapEnforcementClientBinding::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="49337-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="49337-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="49337-108">**INapEnforcementClientBinding：:P rocesssohresponse** 方法可供強制用戶端在每次從強制服務器收到 SoHResponse 資料 blob 時處理 SoHResponse。</span><span class="sxs-lookup"><span data-stu-id="49337-108">The **INapEnforcementClientBinding::ProcessSoHResponse** method is used by enforcement clients to process an SoHResponse whenever they receive an SoHResponse data blob from the enforcement server.</span></span>

## <a name="syntax"></a><span data-ttu-id="49337-109">語法</span><span class="sxs-lookup"><span data-stu-id="49337-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a><span data-ttu-id="49337-110">參數</span><span class="sxs-lookup"><span data-stu-id="49337-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49337-111">*連接* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49337-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49337-112">用戶端連接之 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 介面的 COM 指標。</span><span class="sxs-lookup"><span data-stu-id="49337-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the client connection.</span></span> <span data-ttu-id="49337-113">在這個方法呼叫完成之後，NapAgent 不會保留與這個介面相關聯之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="49337-113">The NapAgent does not hold references to the object associated with this interface after this method call completes.</span></span>

<span data-ttu-id="49337-114">您必須使用先前建立的連接來處理 SOHResponse 資料 blob。</span><span class="sxs-lookup"><span data-stu-id="49337-114">You must use a previously established connection for processing SOHResponse data blobs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49337-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="49337-115">Return value</span></span>

<span data-ttu-id="49337-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="49337-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="49337-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="49337-117">Return code</span></span>                                                                                             | <span data-ttu-id="49337-118">Description</span><span class="sxs-lookup"><span data-stu-id="49337-118">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49337-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="49337-119"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="49337-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="49337-120">The operation is successful.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="49337-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="49337-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="49337-122">先前未在強制用戶端上建立任何連接。</span><span class="sxs-lookup"><span data-stu-id="49337-122">No connections have previously been created on the enforcement client.</span></span> <br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="49337-123"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="49337-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="49337-124">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="49337-124">Permissions error, access denied.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="49337-125"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="49337-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="49337-126">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="49337-126">System resource limit, could not perform the operation.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="49337-127"><dt>**NAP \_ E \_ 不正確封 \_ 包**</dt></span><span class="sxs-lookup"><span data-stu-id="49337-127"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl>  | <span data-ttu-id="49337-128">如果傳回這個值，強制用戶端必須卸載封包（如果 NapAgent 傳回 NAP \_ 電子 \_ 不正確封包） \_ 。</span><span class="sxs-lookup"><span data-stu-id="49337-128">If this value is returned the enforcement client must drop the packet if the NapAgent returns NAP\_E\_INVALID\_PACKET.</span></span> <span data-ttu-id="49337-129">在這種情況下，enforcer 必須假設正在交談的伺服器不是啟用 NAP 的，並且會從使用中的清單中移除連接 (也就是通知 NapAgent 線上狀態為 [關閉]) 。</span><span class="sxs-lookup"><span data-stu-id="49337-129">In this case, the enforcer must assume that the server it is talking to is not NAP-enabled and remove the connection from the active list (i.e. notify the NapAgent of a connection state down).</span></span><br/> |
| <dl> <span data-ttu-id="49337-130"><dt>**NAP \_ E 不符的 \_ \_ 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="49337-130"><dt>**NAP\_E\_MISMATCHED\_ID**</dt></span></span> </dl>   | <span data-ttu-id="49337-131">如果傳回這個值，則表示 SoH-Response 封包中的相互關聯識別碼，與未處理的 SoH 回應不符。</span><span class="sxs-lookup"><span data-stu-id="49337-131">If this value is returned it indicates that the correlation id in the SoH-Response packet did not match the outstanding SoH-Response.</span></span> <span data-ttu-id="49337-132">在此情況下，enforcer 應該捨棄封包，並等候另一個較新的 SoH-Response 封包。</span><span class="sxs-lookup"><span data-stu-id="49337-132">In this case, the enforcer should drop the packet and wait for another newer SoH-Response packet.</span></span><br/> <span data-ttu-id="49337-133">這可能是因回應較舊的要求訊息所造成。</span><span class="sxs-lookup"><span data-stu-id="49337-133">This may be caused by a response to an older request message.</span></span><br/>        |
| <dl> <span data-ttu-id="49337-134"><dt>**NAP \_ E \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="49337-134"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="49337-135">Enforcer 先前尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="49337-135">The enforcer has not been previously initialized.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="49337-136">備註</span><span class="sxs-lookup"><span data-stu-id="49337-136">Remarks</span></span>

<span data-ttu-id="49337-137">NapAgent 會從連線物件查詢 SoH-Response 資料 blob、處理它，然後設定產生的決策 (例如</span><span class="sxs-lookup"><span data-stu-id="49337-137">The NapAgent queries the SoH-Response data blob from the connection object, processes it, and sets the resulting decision (eg.</span></span> <span data-ttu-id="49337-138">連線物件上的完整/受限制存取/等) 。</span><span class="sxs-lookup"><span data-stu-id="49337-138">full/restricted access/etc) on the connection object.</span></span>

<span data-ttu-id="49337-139">強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="49337-139">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="49337-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="49337-140">Requirements</span></span>



| <span data-ttu-id="49337-141">需求</span><span class="sxs-lookup"><span data-stu-id="49337-141">Requirement</span></span> | <span data-ttu-id="49337-142">值</span><span class="sxs-lookup"><span data-stu-id="49337-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49337-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49337-143">Minimum supported client</span></span><br/> | <span data-ttu-id="49337-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49337-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="49337-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49337-145">Minimum supported server</span></span><br/> | <span data-ttu-id="49337-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49337-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="49337-147">標頭</span><span class="sxs-lookup"><span data-stu-id="49337-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="49337-148"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="49337-148"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="49337-149">Idl</span><span class="sxs-lookup"><span data-stu-id="49337-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49337-150"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="49337-150"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="49337-151">DLL</span><span class="sxs-lookup"><span data-stu-id="49337-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49337-152"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49337-152"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="49337-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49337-153">See also</span></span>

<dl> <span data-ttu-id="49337-154"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="49337-154"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="49337-155">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="49337-155">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="49337-156">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="49337-156">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





