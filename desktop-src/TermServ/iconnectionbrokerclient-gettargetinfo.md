---
title: 'IConnectionBrokerClient GetTargetInfo 方法 (Cbclient .h) '
description: 要求應重新導向連接之目的電腦的相關資訊。
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- GetTargetInfo 方法遠端桌面服務
- GetTargetInfo 方法遠端桌面服務，IConnectionBrokerClient 介面
- IConnectionBrokerClient 介面遠端桌面服務，GetTargetInfo 方法
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508303"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a><span data-ttu-id="a1134-106">IConnectionBrokerClient：： GetTargetInfo 方法</span><span class="sxs-lookup"><span data-stu-id="a1134-106">IConnectionBrokerClient::GetTargetInfo method</span></span>

<span data-ttu-id="a1134-107">要求應重新導向連接之目的電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1134-107">Requests information about the target computer where the connection should be redirected.</span></span> <span data-ttu-id="a1134-108">重新導向器會使用這個方法來取得連入連線要求的重新導向資訊。</span><span class="sxs-lookup"><span data-stu-id="a1134-108">This method is used by the redirector to get redirection information for the incoming connection request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1134-109">語法</span><span class="sxs-lookup"><span data-stu-id="a1134-109">Syntax</span></span>


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a><span data-ttu-id="a1134-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1134-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1134-111">*pConnectionInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1134-111">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1134-112">[**CB \_ 連接 \_ 資訊**](cb-connection-info.md)結構的位址，其中包含連入連線要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1134-112">The address of a [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure that contains information about the incoming connection request.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-113">*保留* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1134-113">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1134-114">此參數已保留供日後使用，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="a1134-114">This parameter is reserved for future use and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-115">*hStatusEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1134-115">*hStatusEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1134-116">每當要求的進度更新時，將會設定之事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a1134-116">The handle of an event that will get set whenever there is an update to the progress of the request.</span></span> <span data-ttu-id="a1134-117">您必須負責建立和關閉此事件。</span><span class="sxs-lookup"><span data-stu-id="a1134-117">You are responsible for creating and closing this event.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-118">*pTargetInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a1134-118">*pTargetInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1134-119">[**CB \_ 目標 \_ 資訊**](cb-target-info.md)結構的位址，此結構會接收應重新導向連入連線之目的電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1134-119">The address of a [**CB\_TARGET\_INFO**](cb-target-info.md) structure that receives information about the target computer where the incoming connection should be redirected.</span></span> <span data-ttu-id="a1134-120">因為這是非同步方法，所以在要求完成之前，此記憶體必須保持可用。</span><span class="sxs-lookup"><span data-stu-id="a1134-120">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="a1134-121">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a1134-121">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-122">*pResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a1134-122">*pResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1134-123">接收結果碼的 **DWORD** 變數位址。</span><span class="sxs-lookup"><span data-stu-id="a1134-123">The address of a **DWORD** variable that receives a result code.</span></span> <span data-ttu-id="a1134-124">因為這是非同步方法，所以在要求完成之前，此記憶體必須保持可用。</span><span class="sxs-lookup"><span data-stu-id="a1134-124">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="a1134-125">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a1134-125">For more information, see Remarks.</span></span>

<span data-ttu-id="a1134-126">此結果碼將會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a1134-126">This result code will be one of the following values.</span></span>

<dt>

<span data-ttu-id="a1134-127">0</span><span class="sxs-lookup"><span data-stu-id="a1134-127">0</span></span>
</dt> <dd>

<span data-ttu-id="a1134-128">成功。</span><span class="sxs-lookup"><span data-stu-id="a1134-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-129">0x0000400</span><span class="sxs-lookup"><span data-stu-id="a1134-129">0x0000400</span></span>
</dt> <dd>

<span data-ttu-id="a1134-130">找不到目的地電腦。</span><span class="sxs-lookup"><span data-stu-id="a1134-130">The destination computer could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-131">0x0000401</span><span class="sxs-lookup"><span data-stu-id="a1134-131">0x0000401</span></span>
</dt> <dd>

<span data-ttu-id="a1134-132">目的地電腦無法使用。</span><span class="sxs-lookup"><span data-stu-id="a1134-132">The destination computer is not available.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-133">0x0000402</span><span class="sxs-lookup"><span data-stu-id="a1134-133">0x0000402</span></span>
</dt> <dd>

<span data-ttu-id="a1134-134">載入目的地電腦時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1134-134">Error loading destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-135">0x0000403</span><span class="sxs-lookup"><span data-stu-id="a1134-135">0x0000403</span></span>
</dt> <dd>

<span data-ttu-id="a1134-136">將目的地電腦上線時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1134-136">Error bringing destination computer online.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-137">0x0000404</span><span class="sxs-lookup"><span data-stu-id="a1134-137">0x0000404</span></span>
</dt> <dd>

<span data-ttu-id="a1134-138">重新導向至目的地電腦時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1134-138">Error redirecting to destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-139">0x0000405</span><span class="sxs-lookup"><span data-stu-id="a1134-139">0x0000405</span></span>
</dt> <dd>

<span data-ttu-id="a1134-140">喚醒虛擬機器時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1134-140">Error waking virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-141">0x0000406</span><span class="sxs-lookup"><span data-stu-id="a1134-141">0x0000406</span></span>
</dt> <dd>

<span data-ttu-id="a1134-142">啟動虛擬機器時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1134-142">Error booting virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-143">0x0000407</span><span class="sxs-lookup"><span data-stu-id="a1134-143">0x0000407</span></span>
</dt> <dd>

<span data-ttu-id="a1134-144">尋找虛擬機器的 IP 位址時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1134-144">Error finding the IP address of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-145">0x0000408</span><span class="sxs-lookup"><span data-stu-id="a1134-145">0x0000408</span></span>
</dt> <dd>

<span data-ttu-id="a1134-146">Session broker 在集區中找不到任何可用的電腦。</span><span class="sxs-lookup"><span data-stu-id="a1134-146">The session broker could not find any available computers in the pool.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-147">0x0000409</span><span class="sxs-lookup"><span data-stu-id="a1134-147">0x0000409</span></span>
</dt> <dd>

<span data-ttu-id="a1134-148">會話代理人取消了連接。</span><span class="sxs-lookup"><span data-stu-id="a1134-148">The session broker canceled the connection.</span></span>

</dd> <dt>

<span data-ttu-id="a1134-149">0x0000410</span><span class="sxs-lookup"><span data-stu-id="a1134-149">0x0000410</span></span>
</dt> <dd>

<span data-ttu-id="a1134-150">Session broker 無法驗證連接設定。</span><span class="sxs-lookup"><span data-stu-id="a1134-150">The session broker could not validate the connection settings.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a1134-151">*ppCbReq* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a1134-151">*ppCbReq* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1134-152">[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)介面指標的位址，您可用來取得非同步作業的狀態更新。</span><span class="sxs-lookup"><span data-stu-id="a1134-152">The address of an [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) interface pointer that you use to obtain status updates for an asynchronous operation.</span></span> <span data-ttu-id="a1134-153">此介面會與 *hStatusEvent* 參數搭配使用，以等候並取得此非同步作業的結果。</span><span class="sxs-lookup"><span data-stu-id="a1134-153">This interface is used in conjunction with the *hStatusEvent* parameter to wait for and get the results of this asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1134-154">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1134-154">Return value</span></span>

<span data-ttu-id="a1134-155">如果已建立異步要求，則傳回 **E \_ 暫** 止。</span><span class="sxs-lookup"><span data-stu-id="a1134-155">Returns **E\_PENDING** if the asynchronous request is created.</span></span> <span data-ttu-id="a1134-156">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a1134-156">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1134-157">備註</span><span class="sxs-lookup"><span data-stu-id="a1134-157">Remarks</span></span>

<span data-ttu-id="a1134-158">這個方法是非同步方法。</span><span class="sxs-lookup"><span data-stu-id="a1134-158">This method is asynchronous.</span></span> <span data-ttu-id="a1134-159">*PTargetInfo* 和 *pResult* 參數必須維持有效，直到 [**IConnectionBrokerRequest：： CheckStatus**](iconnectionbrokerrequest-checkstatus.md)方法取得 **CB \_ 狀態 \_ 要求 \_ 已完成**。</span><span class="sxs-lookup"><span data-stu-id="a1134-159">The *pTargetInfo* and *pResult* parameters must remain valid until the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method obtains **CB\_STATUS\_REQUEST\_COMPLETED**.</span></span>

<span data-ttu-id="a1134-160">如需如何使用此方法的詳細資訊，請參閱 [如何使用遠端桌面連線代理人用戶端 API](use-the-remote-desktop-connection-broker-client-api.md)。</span><span class="sxs-lookup"><span data-stu-id="a1134-160">For more information about how to use this method, see [How to use the Remote Desktop Connection Broker client API](use-the-remote-desktop-connection-broker-client-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1134-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1134-161">Requirements</span></span>



| <span data-ttu-id="a1134-162">需求</span><span class="sxs-lookup"><span data-stu-id="a1134-162">Requirement</span></span> | <span data-ttu-id="a1134-163">值</span><span class="sxs-lookup"><span data-stu-id="a1134-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1134-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1134-164">Minimum supported client</span></span><br/> | <span data-ttu-id="a1134-165">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a1134-165">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="a1134-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1134-166">Minimum supported server</span></span><br/> | <span data-ttu-id="a1134-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1134-167">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="a1134-168">標頭</span><span class="sxs-lookup"><span data-stu-id="a1134-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1134-169"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1134-169"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1134-170">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1134-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1134-171"><dt>Cbclient .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1134-171"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="a1134-172">DLL</span><span class="sxs-lookup"><span data-stu-id="a1134-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1134-173"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1134-173"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1134-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1134-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1134-175">**IConnectionBrokerClient**</span><span class="sxs-lookup"><span data-stu-id="a1134-175">**IConnectionBrokerClient**</span></span>](iconnectionbrokerclient.md)
</dt> </dl>

 

 





