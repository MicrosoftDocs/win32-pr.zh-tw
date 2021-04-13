---
title: 'INapClientManagement GetRegisteredEnforcementClients 方法 (NapManagement .h) '
description: 抓取已註冊的強制用戶端的相關資訊。
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- GetRegisteredEnforcementClients 方法 NAP
- GetRegisteredEnforcementClients 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，GetRegisteredEnforcementClients 方法
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466044"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a><span data-ttu-id="8470a-106">INapClientManagement：： GetRegisteredEnforcementClients 方法</span><span class="sxs-lookup"><span data-stu-id="8470a-106">INapClientManagement::GetRegisteredEnforcementClients method</span></span>

> [!Note]  
> <span data-ttu-id="8470a-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="8470a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8470a-108">**GetRegisteredEnforcementClients** 方法會抓取已註冊的強制用戶端的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8470a-108">The **GetRegisteredEnforcementClients** method retrieves information about the registered enforcement clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="8470a-109">語法</span><span class="sxs-lookup"><span data-stu-id="8470a-109">Syntax</span></span>


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a><span data-ttu-id="8470a-110">參數</span><span class="sxs-lookup"><span data-stu-id="8470a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8470a-111">*計數* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8470a-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8470a-112">[**EnforcementEntityCount**](nap-datatypes.md)的指標，其中包含已註冊的強制用戶端數目。</span><span class="sxs-lookup"><span data-stu-id="8470a-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of registered enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="8470a-113">*enforcers* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8470a-113">*enforcers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8470a-114">[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)結構陣列的指標，這些結構描述已註冊的強制用戶端。</span><span class="sxs-lookup"><span data-stu-id="8470a-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered enforcement clients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8470a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8470a-115">Return value</span></span>

<span data-ttu-id="8470a-116">方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="8470a-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="8470a-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8470a-117">Return code</span></span>                                                                                         | <span data-ttu-id="8470a-118">Description</span><span class="sxs-lookup"><span data-stu-id="8470a-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8470a-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8470a-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="8470a-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="8470a-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8470a-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8470a-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="8470a-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="8470a-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8470a-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8470a-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="8470a-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="8470a-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8470a-125"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="8470a-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8470a-126">NapAgent 未執行。</span><span class="sxs-lookup"><span data-stu-id="8470a-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="8470a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8470a-127">Requirements</span></span>



| <span data-ttu-id="8470a-128">需求</span><span class="sxs-lookup"><span data-stu-id="8470a-128">Requirement</span></span> | <span data-ttu-id="8470a-129">值</span><span class="sxs-lookup"><span data-stu-id="8470a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8470a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8470a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8470a-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8470a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8470a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8470a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8470a-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8470a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8470a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="8470a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8470a-135"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="8470a-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="8470a-136">Idl</span><span class="sxs-lookup"><span data-stu-id="8470a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8470a-137"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8470a-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="8470a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8470a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8470a-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8470a-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="8470a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8470a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8470a-141">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="8470a-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





