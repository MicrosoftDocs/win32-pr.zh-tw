---
title: 'INapEnforcementClientConnection SetMaxSize 方法 (NapEnforcementClient .h) '
description: 設定此用戶端的 SoH 封包大小上限。
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- SetMaxSize 方法 NAP
- SetMaxSize 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetMaxSize 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b10d7bc1a023371683f17bb3e6e12cd578fa964
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384386"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a><span data-ttu-id="d551b-106">INapEnforcementClientConnection：： SetMaxSize 方法</span><span class="sxs-lookup"><span data-stu-id="d551b-106">INapEnforcementClientConnection::SetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="d551b-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="d551b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d551b-108">**INapEnforcementClientConnection：： SetMaxSize** 方法會設定此用戶端的 SoH 封包大小上限。</span><span class="sxs-lookup"><span data-stu-id="d551b-108">The **INapEnforcementClientConnection::SetMaxSize** method sets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="d551b-109">語法</span><span class="sxs-lookup"><span data-stu-id="d551b-109">Syntax</span></span>


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="d551b-110">參數</span><span class="sxs-lookup"><span data-stu-id="d551b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d551b-111">*maxSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d551b-111">*maxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d551b-112">[**ProtocolMaxSize**](nap-datatypes.md)結構，指出 SoH 封包的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d551b-112">A [**ProtocolMaxSize**](nap-datatypes.md) structure that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d551b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d551b-113">Return value</span></span>

<span data-ttu-id="d551b-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d551b-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d551b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d551b-115">Return code</span></span>                                                                                     | <span data-ttu-id="d551b-116">Description</span><span class="sxs-lookup"><span data-stu-id="d551b-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d551b-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d551b-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d551b-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d551b-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d551b-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d551b-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d551b-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="d551b-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d551b-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d551b-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d551b-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d551b-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d551b-123">備註</span><span class="sxs-lookup"><span data-stu-id="d551b-123">Remarks</span></span>

<span data-ttu-id="d551b-124">此值是由強制用戶端設定。</span><span class="sxs-lookup"><span data-stu-id="d551b-124">This value is set by the enforcement client.</span></span>

## <a name="requirements"></a><span data-ttu-id="d551b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d551b-125">Requirements</span></span>



| <span data-ttu-id="d551b-126">需求</span><span class="sxs-lookup"><span data-stu-id="d551b-126">Requirement</span></span> | <span data-ttu-id="d551b-127">值</span><span class="sxs-lookup"><span data-stu-id="d551b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d551b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d551b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d551b-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d551b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d551b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d551b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d551b-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d551b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d551b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="d551b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d551b-133"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="d551b-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="d551b-134">Idl</span><span class="sxs-lookup"><span data-stu-id="d551b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d551b-135"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d551b-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="d551b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d551b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d551b-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d551b-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="d551b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d551b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d551b-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="d551b-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





