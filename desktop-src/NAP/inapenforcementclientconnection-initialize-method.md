---
title: 'INapEnforcementClientConnection Initialize 方法 (NapEnforcementClient .h) '
description: 初始化用戶端連接。
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Initialize 方法 NAP
- Initialize 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，Initialize 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51f12025bbddb8a9e795a97f2ed443344327a17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464825"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a><span data-ttu-id="5e48c-106">INapEnforcementClientConnection：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="5e48c-106">INapEnforcementClientConnection::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="5e48c-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="5e48c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5e48c-108">**INapEnforcementClientConnection：： Initialize** 方法會初始化用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="5e48c-108">The **INapEnforcementClientConnection::Initialize** method initializes the client connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e48c-109">語法</span><span class="sxs-lookup"><span data-stu-id="5e48c-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="5e48c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e48c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e48c-111"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="5e48c-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e48c-112">[**EnforementEntityId**](nap-datatypes.md)的指標，可識別要求連接的強制用戶端。</span><span class="sxs-lookup"><span data-stu-id="5e48c-112">A pointer to an [**EnforementEntityId**](nap-datatypes.md) that identifies the enforcement client requesting the connection.</span></span> <span data-ttu-id="5e48c-113">此值是在連接建立期間由 NapAgent 所設定。</span><span class="sxs-lookup"><span data-stu-id="5e48c-113">This value is set by the NapAgent during connection creation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e48c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e48c-114">Return value</span></span>

<span data-ttu-id="5e48c-115">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5e48c-115">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5e48c-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5e48c-116">Return code</span></span>                                                                                     | <span data-ttu-id="5e48c-117">Description</span><span class="sxs-lookup"><span data-stu-id="5e48c-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e48c-118"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5e48c-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5e48c-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="5e48c-119">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5e48c-120"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5e48c-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5e48c-121">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="5e48c-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5e48c-122"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5e48c-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5e48c-123">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="5e48c-123">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5e48c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e48c-124">Requirements</span></span>



| <span data-ttu-id="5e48c-125">需求</span><span class="sxs-lookup"><span data-stu-id="5e48c-125">Requirement</span></span> | <span data-ttu-id="5e48c-126">值</span><span class="sxs-lookup"><span data-stu-id="5e48c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e48c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e48c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5e48c-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e48c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5e48c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e48c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5e48c-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e48c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5e48c-131">標頭</span><span class="sxs-lookup"><span data-stu-id="5e48c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e48c-132"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e48c-132"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e48c-133">Idl</span><span class="sxs-lookup"><span data-stu-id="5e48c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e48c-134"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e48c-134"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e48c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5e48c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e48c-136"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e48c-136"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5e48c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e48c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e48c-138">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="5e48c-138">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





