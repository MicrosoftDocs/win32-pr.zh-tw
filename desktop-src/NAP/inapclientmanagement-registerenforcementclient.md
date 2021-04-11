---
title: 'INapClientManagement RegisterEnforcementClient 方法 (NapManagement .h) '
description: 向 NAP 系統註冊強制用戶端。
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- RegisterEnforcementClient 方法 NAP
- RegisterEnforcementClient 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，RegisterEnforcementClient 方法
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104694"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a><span data-ttu-id="563ae-106">INapClientManagement：： RegisterEnforcementClient 方法</span><span class="sxs-lookup"><span data-stu-id="563ae-106">INapClientManagement::RegisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="563ae-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="563ae-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="563ae-108">**RegisterEnforcementClient** 方法會向 NAP 系統註冊強制用戶端。</span><span class="sxs-lookup"><span data-stu-id="563ae-108">The **RegisterEnforcementClient** method registers an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="563ae-109">語法</span><span class="sxs-lookup"><span data-stu-id="563ae-109">Syntax</span></span>


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a><span data-ttu-id="563ae-110">參數</span><span class="sxs-lookup"><span data-stu-id="563ae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="563ae-111">*enforcer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="563ae-111">*enforcer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="563ae-112">[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)資料結構的指標，其中包含與強制用戶端相關聯的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="563ae-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structure that contains the registration information that is associated with the enforcement client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="563ae-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="563ae-113">Return value</span></span>

<span data-ttu-id="563ae-114">方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="563ae-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="563ae-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="563ae-115">Return code</span></span>                                                                                            | <span data-ttu-id="563ae-116">Description</span><span class="sxs-lookup"><span data-stu-id="563ae-116">Description</span></span>                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="563ae-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="563ae-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="563ae-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="563ae-118">Operation successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="563ae-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="563ae-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="563ae-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="563ae-120">Permissions error, access denied.</span></span><br/>                                      |
| <dl> <span data-ttu-id="563ae-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="563ae-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="563ae-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="563ae-122">System resource limit, could not perform the operation.</span></span><br/>                |
| <dl> <span data-ttu-id="563ae-123"><dt>**NAP \_ E \_ 衝突 \_ 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="563ae-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="563ae-124">使用指定識別碼的強制代理程式已經註冊。</span><span class="sxs-lookup"><span data-stu-id="563ae-124">An enforcement agent using the given identifier is already registered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="563ae-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="563ae-125">Requirements</span></span>



| <span data-ttu-id="563ae-126">需求</span><span class="sxs-lookup"><span data-stu-id="563ae-126">Requirement</span></span> | <span data-ttu-id="563ae-127">值</span><span class="sxs-lookup"><span data-stu-id="563ae-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="563ae-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="563ae-128">Minimum supported client</span></span><br/> | <span data-ttu-id="563ae-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="563ae-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="563ae-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="563ae-130">Minimum supported server</span></span><br/> | <span data-ttu-id="563ae-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="563ae-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="563ae-132">標頭</span><span class="sxs-lookup"><span data-stu-id="563ae-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="563ae-133"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="563ae-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="563ae-134">Idl</span><span class="sxs-lookup"><span data-stu-id="563ae-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="563ae-135"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="563ae-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="563ae-136">DLL</span><span class="sxs-lookup"><span data-stu-id="563ae-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="563ae-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="563ae-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="563ae-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="563ae-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="563ae-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="563ae-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





