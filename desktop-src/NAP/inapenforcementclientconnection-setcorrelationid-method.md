---
title: 'INapEnforcementClientConnection SetCorrelationId 方法 (NapEnforcementClient .h) '
description: 設定用來相互關聯 SoH 要求和 SoH 回應的識別碼。
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- SetCorrelationId 方法 NAP
- SetCorrelationId 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetCorrelationId 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508440"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a><span data-ttu-id="b149e-106">INapEnforcementClientConnection：： SetCorrelationId 方法</span><span class="sxs-lookup"><span data-stu-id="b149e-106">INapEnforcementClientConnection::SetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="b149e-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="b149e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b149e-108">**INapEnforcementClientConnection：： SetCorrelationId** 方法會設定用來相互關聯 soh 要求和 soh 回應的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b149e-108">The **INapEnforcementClientConnection::SetCorrelationId** method sets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="b149e-109">語法</span><span class="sxs-lookup"><span data-stu-id="b149e-109">Syntax</span></span>


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="b149e-110">參數</span><span class="sxs-lookup"><span data-stu-id="b149e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b149e-111">*correlationId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b149e-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b149e-112">識別特定 SoH 交換的唯一 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) 結構。</span><span class="sxs-lookup"><span data-stu-id="b149e-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies a specific SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b149e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b149e-113">Return value</span></span>

<span data-ttu-id="b149e-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b149e-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b149e-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b149e-115">Return code</span></span>                                                                                     | <span data-ttu-id="b149e-116">Description</span><span class="sxs-lookup"><span data-stu-id="b149e-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b149e-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b149e-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b149e-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b149e-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b149e-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b149e-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b149e-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="b149e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b149e-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b149e-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b149e-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="b149e-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b149e-123">備註</span><span class="sxs-lookup"><span data-stu-id="b149e-123">Remarks</span></span>

<span data-ttu-id="b149e-124">相互關聯識別碼是由 NapAgent 所設定，並以連接識別碼為基礎。</span><span class="sxs-lookup"><span data-stu-id="b149e-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="b149e-125">此識別碼是用來讓要求和回應相互關聯，也就是它可唯一描述 SoH 交換，而且一律會包含連線物件上最新 SoH 集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b149e-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="b149e-126">收到 SoH-Response 時，NapAgent 會先確保識別碼相符;如果沒有，則會傳回錯誤，且 enforcer 必須卸載封包。</span><span class="sxs-lookup"><span data-stu-id="b149e-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="b149e-127">如需詳細資訊，請參閱 [**INapEnforcementClientBinding：:P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="b149e-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="b149e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b149e-128">Requirements</span></span>



| <span data-ttu-id="b149e-129">需求</span><span class="sxs-lookup"><span data-stu-id="b149e-129">Requirement</span></span> | <span data-ttu-id="b149e-130">值</span><span class="sxs-lookup"><span data-stu-id="b149e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b149e-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b149e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b149e-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b149e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b149e-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b149e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b149e-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b149e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b149e-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b149e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b149e-136"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="b149e-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b149e-137">Idl</span><span class="sxs-lookup"><span data-stu-id="b149e-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b149e-138"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b149e-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="b149e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b149e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b149e-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b149e-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b149e-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b149e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b149e-142">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="b149e-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





