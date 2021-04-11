---
title: 'INapEnforcementClientConnection 介面 (NapEnforcementClient .h) '
description: '允許用戶端連接管理。 |INapEnforcementClientConnection 介面 (NapEnforcementClient .h) '
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- INapEnforcementClientConnection 介面 NAP
- INapEnforcementClientConnection 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195928"
---
# <a name="inapenforcementclientconnection-interface"></a><span data-ttu-id="6f35e-106">INapEnforcementClientConnection 介面</span><span class="sxs-lookup"><span data-stu-id="6f35e-106">INapEnforcementClientConnection interface</span></span>

> [!Note]  
> <span data-ttu-id="6f35e-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="6f35e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6f35e-108">**INapEnforcementClientConnection** 提供允許用戶端連接管理的方法。</span><span class="sxs-lookup"><span data-stu-id="6f35e-108">The **INapEnforcementClientConnection** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="6f35e-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) 會繼承此介面的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="6f35e-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="6f35e-110">成員</span><span class="sxs-lookup"><span data-stu-id="6f35e-110">Members</span></span>

<span data-ttu-id="6f35e-111">**INapEnforcementClientConnection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="6f35e-111">The **INapEnforcementClientConnection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6f35e-112">**INapEnforcementClientConnection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6f35e-112">**INapEnforcementClientConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="6f35e-113">方法</span><span class="sxs-lookup"><span data-stu-id="6f35e-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f35e-114">方法</span><span class="sxs-lookup"><span data-stu-id="6f35e-114">Methods</span></span>

<span data-ttu-id="6f35e-115">**INapEnforcementClientConnection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6f35e-115">The **INapEnforcementClientConnection** interface has these methods.</span></span>



| <span data-ttu-id="6f35e-116">方法</span><span class="sxs-lookup"><span data-stu-id="6f35e-116">Method</span></span>                                                                                                                           | <span data-ttu-id="6f35e-117">描述</span><span class="sxs-lookup"><span data-stu-id="6f35e-117">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f35e-118">**INapEnforcementClientConnection：： GetConnectionId**</span><span class="sxs-lookup"><span data-stu-id="6f35e-118">**INapEnforcementClientConnection::GetConnectionId**</span></span>](inapenforcementclientconnection-getconnectionid-method.md)               | <span data-ttu-id="6f35e-119">取得用戶端的連接識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f35e-119">Gets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="6f35e-120">**INapEnforcementClientConnection::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="6f35e-120">**INapEnforcementClientConnection::GetCorrelationId**</span></span>](inapenforcementclientconnection-getcorrelationid-method.md)             | <span data-ttu-id="6f35e-121">取得用來相互關聯 SoH 要求和 SoH 回應的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f35e-121">Gets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="6f35e-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="6f35e-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-getenforcerprivatedata-method.md) | <span data-ttu-id="6f35e-123">供 enforcer 用來取得私用資料。</span><span class="sxs-lookup"><span data-stu-id="6f35e-123">Used by the enforcer to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="6f35e-124">**INapEnforcementClientConnection：： GetFlags**</span><span class="sxs-lookup"><span data-stu-id="6f35e-124">**INapEnforcementClientConnection::GetFlags**</span></span>](inapenforcementclientconnection-getflags-method.md)                             | <span data-ttu-id="6f35e-125">取得旗標的值，這個值會區分因為 enforcers 快取的 SoHRequests，而回應的第一次回應。</span><span class="sxs-lookup"><span data-stu-id="6f35e-125">Gets the value of the flag that differentiates first-time responses from responses due to SoHRequests cached by the enforcers.</span></span><br/> |
| [<span data-ttu-id="6f35e-126">**INapEnforcementClientConnection::GetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="6f35e-126">**INapEnforcementClientConnection::GetIsolationInfo**</span></span>](inapenforcementclientconnection-getisolationinfo-method.md)             | <span data-ttu-id="6f35e-127">使用取得用戶端的隔離資訊。</span><span class="sxs-lookup"><span data-stu-id="6f35e-127">Used get the isolation information of the client.</span></span><br/>                                                                              |
| [<span data-ttu-id="6f35e-128">**INapEnforcementClientConnection::GetMaxSize**</span><span class="sxs-lookup"><span data-stu-id="6f35e-128">**INapEnforcementClientConnection::GetMaxSize**</span></span>](inapenforcementclientconnection-getmaxsize-method.md)                         | <span data-ttu-id="6f35e-129">取得此用戶端的 SoH 封包大小上限。</span><span class="sxs-lookup"><span data-stu-id="6f35e-129">Gets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="6f35e-130">**INapEnforcementClientConnection::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="6f35e-130">**INapEnforcementClientConnection::GetPrivateData**</span></span>](inapenforcementclientconnection-getprivatedata-method.md)                 | <span data-ttu-id="6f35e-131">供 NapAgent 用來取得私用資料。</span><span class="sxs-lookup"><span data-stu-id="6f35e-131">Used by the NapAgent to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="6f35e-132">**INapEnforcementClientConnection::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="6f35e-132">**INapEnforcementClientConnection::GetSoHRequest**</span></span>](inapenforcementclientconnection-getsohrequest-method.md)                   | <span data-ttu-id="6f35e-133">取得 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="6f35e-133">Gets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="6f35e-134">**INapEnforcementClientConnection::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="6f35e-134">**INapEnforcementClientConnection::GetSoHResponse**</span></span>](inapenforcementclientconnection-getsohresponse-method.md)                 | <span data-ttu-id="6f35e-135">取得強制用戶端接收的 SoH-Response。</span><span class="sxs-lookup"><span data-stu-id="6f35e-135">Gets the SoH-Response received by the enforcement client.</span></span><br/>                                                                      |
| [<span data-ttu-id="6f35e-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="6f35e-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span></span>](inapenforcementclientconnection-getstringcorrelationid-method.md) | <span data-ttu-id="6f35e-137">取得 CorrelationId 的字串版本。</span><span class="sxs-lookup"><span data-stu-id="6f35e-137">Gets the string version of the CorrelationId.</span></span> <span data-ttu-id="6f35e-138">主要用於記錄用途。</span><span class="sxs-lookup"><span data-stu-id="6f35e-138">Used primarily for logging purposes.</span></span><br/>                                             |
| [<span data-ttu-id="6f35e-139">**INapEnforcementClientConnection：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="6f35e-139">**INapEnforcementClientConnection::Initialize**</span></span>](inapenforcementclientconnection-initialize-method.md)                         | <span data-ttu-id="6f35e-140">初始化連接。</span><span class="sxs-lookup"><span data-stu-id="6f35e-140">Initializes the connection.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="6f35e-141">**INapEnforcementClientConnection::SetConnectionId**</span><span class="sxs-lookup"><span data-stu-id="6f35e-141">**INapEnforcementClientConnection::SetConnectionId**</span></span>](inapenforcementclientconnection-setconnectionid-method.md)               | <span data-ttu-id="6f35e-142">設定用戶端的連接識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f35e-142">Sets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="6f35e-143">**INapEnforcementClientConnection::SetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="6f35e-143">**INapEnforcementClientConnection::SetCorrelationId**</span></span>](inapenforcementclientconnection-setcorrelationid-method.md)             | <span data-ttu-id="6f35e-144">設定用來相互關聯 SoH 要求和 SoH 回應的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f35e-144">Sets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="6f35e-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="6f35e-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-setenforcerprivatedata-method.md) | <span data-ttu-id="6f35e-146">供 enforcer 用來設定私用資料。</span><span class="sxs-lookup"><span data-stu-id="6f35e-146">Used by the enforcer to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="6f35e-147">**INapEnforcementClientConnection::SetFlags**</span><span class="sxs-lookup"><span data-stu-id="6f35e-147">**INapEnforcementClientConnection::SetFlags**</span></span>](inapenforcementclientconnection-setflags-method.md)                             | <span data-ttu-id="6f35e-148">設定旗標，此旗標會根據 enforcers 快取的 SoHRequests，區分第一次回應與回應。</span><span class="sxs-lookup"><span data-stu-id="6f35e-148">Sets the flag that differentiates first-time responses from responses due to SoHRequests cached by enforcers.</span></span><br/>                  |
| [<span data-ttu-id="6f35e-149">**INapEnforcementClientConnection::SetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="6f35e-149">**INapEnforcementClientConnection::SetIsolationInfo**</span></span>](inapenforcementclientconnection-setisolationinfo-method.md)             | <span data-ttu-id="6f35e-150">供 NapAgent 用來設定用戶端的隔離資訊。</span><span class="sxs-lookup"><span data-stu-id="6f35e-150">Used by the NapAgent to set the isolation information of the client.</span></span><br/>                                                           |
| [<span data-ttu-id="6f35e-151">**INapEnforcementClientConnection::SetMaxSize**</span><span class="sxs-lookup"><span data-stu-id="6f35e-151">**INapEnforcementClientConnection::SetMaxSize**</span></span>](inapenforcementclientconnection-setmaxsize-method.md)                         | <span data-ttu-id="6f35e-152">設定此用戶端的 SoH 封包大小上限。</span><span class="sxs-lookup"><span data-stu-id="6f35e-152">Sets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="6f35e-153">**INapEnforcementClientConnection::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="6f35e-153">**INapEnforcementClientConnection::SetPrivateData**</span></span>](inapenforcementclientconnection-setprivatedata-method.md)                 | <span data-ttu-id="6f35e-154">供 NapAgent 用來設定私用資料。</span><span class="sxs-lookup"><span data-stu-id="6f35e-154">Used by the NapAgent to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="6f35e-155">**INapEnforcementClientConnection::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="6f35e-155">**INapEnforcementClientConnection::SetSoHRequest**</span></span>](inapenforcementclientconnection-setsohrequest-method.md)                   | <span data-ttu-id="6f35e-156">設定 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="6f35e-156">Sets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="6f35e-157">**INapEnforcementClientConnection::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="6f35e-157">**INapEnforcementClientConnection::SetSoHResponse**</span></span>](inapenforcementclientconnection-setsohresponse-method.md)                 | <span data-ttu-id="6f35e-158">設定 SoH-Response，並在接收封包時由強制用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="6f35e-158">Sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span><br/>                                             |



 

## <a name="requirements"></a><span data-ttu-id="6f35e-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f35e-159">Requirements</span></span>



| <span data-ttu-id="6f35e-160">需求</span><span class="sxs-lookup"><span data-stu-id="6f35e-160">Requirement</span></span> | <span data-ttu-id="6f35e-161">值</span><span class="sxs-lookup"><span data-stu-id="6f35e-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f35e-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f35e-162">Minimum supported client</span></span><br/> | <span data-ttu-id="6f35e-163">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f35e-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6f35e-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f35e-164">Minimum supported server</span></span><br/> | <span data-ttu-id="6f35e-165">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f35e-165">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6f35e-166">標頭</span><span class="sxs-lookup"><span data-stu-id="6f35e-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f35e-167"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="6f35e-167"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f35e-168">Idl</span><span class="sxs-lookup"><span data-stu-id="6f35e-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f35e-169"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f35e-169"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="6f35e-170">DLL</span><span class="sxs-lookup"><span data-stu-id="6f35e-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f35e-171"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f35e-171"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="6f35e-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f35e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f35e-173">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="6f35e-173">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6f35e-174">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="6f35e-174">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

