---
title: 'INapClientManagement UnregisterEnforcementClient 方法 (NapManagement .h) '
description: 使用 NAP 系統取消註冊強制用戶端。
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- UnregisterEnforcementClient 方法 NAP
- UnregisterEnforcementClient 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，UnregisterEnforcementClient 方法
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104693"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a><span data-ttu-id="2deaf-106">INapClientManagement：： UnregisterEnforcementClient 方法</span><span class="sxs-lookup"><span data-stu-id="2deaf-106">INapClientManagement::UnregisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="2deaf-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="2deaf-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2deaf-108">**UnregisterEnforcementClient** 方法會向 NAP 系統取消註冊強制用戶端。</span><span class="sxs-lookup"><span data-stu-id="2deaf-108">The **UnregisterEnforcementClient** method unregisters an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2deaf-109">語法</span><span class="sxs-lookup"><span data-stu-id="2deaf-109">Syntax</span></span>


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="2deaf-110">參數</span><span class="sxs-lookup"><span data-stu-id="2deaf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2deaf-111"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="2deaf-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2deaf-112">[**EnforcementEntityId**](nap-datatypes.md)值，識別要取消註冊的強制用戶端。</span><span class="sxs-lookup"><span data-stu-id="2deaf-112">An [**EnforcementEntityId**](nap-datatypes.md) value that identifies the enforcement client to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2deaf-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2deaf-113">Return value</span></span>

<span data-ttu-id="2deaf-114">方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="2deaf-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="2deaf-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2deaf-115">Return code</span></span>                                                                                         | <span data-ttu-id="2deaf-116">Description</span><span class="sxs-lookup"><span data-stu-id="2deaf-116">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2deaf-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2deaf-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="2deaf-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="2deaf-118">Operation successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="2deaf-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2deaf-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="2deaf-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="2deaf-120">Permissions error, access denied.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2deaf-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2deaf-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="2deaf-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="2deaf-122">System resource limit, could not perform the operation.</span></span><br/>             |
| <dl> <span data-ttu-id="2deaf-123"><dt>**NAP \_ E \_ 仍系結 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2deaf-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="2deaf-124">強制用戶端無法取消註冊並保持系結。</span><span class="sxs-lookup"><span data-stu-id="2deaf-124">The enforcement client could not be unregistered and remains bound.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2deaf-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="2deaf-125">Requirements</span></span>



| <span data-ttu-id="2deaf-126">需求</span><span class="sxs-lookup"><span data-stu-id="2deaf-126">Requirement</span></span> | <span data-ttu-id="2deaf-127">值</span><span class="sxs-lookup"><span data-stu-id="2deaf-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2deaf-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2deaf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2deaf-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2deaf-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2deaf-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2deaf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2deaf-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2deaf-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2deaf-132">標頭</span><span class="sxs-lookup"><span data-stu-id="2deaf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2deaf-133"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="2deaf-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="2deaf-134">Idl</span><span class="sxs-lookup"><span data-stu-id="2deaf-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2deaf-135"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2deaf-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="2deaf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2deaf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2deaf-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2deaf-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="2deaf-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2deaf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2deaf-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="2deaf-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





