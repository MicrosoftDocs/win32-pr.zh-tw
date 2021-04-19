---
title: 'INapClientManagement UnregisterSystemHealthAgent 方法 (NapManagement .h) '
description: 向 NAP 系統取消註冊 SHA。
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- UnregisterSystemHealthAgent 方法 NAP
- UnregisterSystemHealthAgent 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，UnregisterSystemHealthAgent 方法
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967350"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a><span data-ttu-id="7dd8c-106">INapClientManagement：： UnregisterSystemHealthAgent 方法</span><span class="sxs-lookup"><span data-stu-id="7dd8c-106">INapClientManagement::UnregisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="7dd8c-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="7dd8c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7dd8c-108">**UnregisterSystemHealthAgent** 方法會向 NAP 系統取消註冊 SHA。</span><span class="sxs-lookup"><span data-stu-id="7dd8c-108">The **UnregisterSystemHealthAgent** method unregisters an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd8c-109">語法</span><span class="sxs-lookup"><span data-stu-id="7dd8c-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="7dd8c-110">參數</span><span class="sxs-lookup"><span data-stu-id="7dd8c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dd8c-111"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="7dd8c-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd8c-112">識別要取消註冊之系統健康狀態代理程式的 [**SystemHealthEntityId**](nap-datatypes.md) 。</span><span class="sxs-lookup"><span data-stu-id="7dd8c-112">A [**SystemHealthEntityId**](nap-datatypes.md) that identifies the System Health Agent to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dd8c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dd8c-113">Return value</span></span>

<span data-ttu-id="7dd8c-114">方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="7dd8c-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="7dd8c-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7dd8c-115">Return code</span></span>                                                                                         | <span data-ttu-id="7dd8c-116">Description</span><span class="sxs-lookup"><span data-stu-id="7dd8c-116">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7dd8c-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd8c-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="7dd8c-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="7dd8c-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7dd8c-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd8c-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="7dd8c-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="7dd8c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7dd8c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd8c-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="7dd8c-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="7dd8c-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7dd8c-123"><dt>**NAP \_ E \_ 仍系結 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd8c-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="7dd8c-124">SHA 仍保持系結狀態，無法取消註冊。</span><span class="sxs-lookup"><span data-stu-id="7dd8c-124">The SHA remains bound and could not be unregistered.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="7dd8c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dd8c-125">Requirements</span></span>



| <span data-ttu-id="7dd8c-126">需求</span><span class="sxs-lookup"><span data-stu-id="7dd8c-126">Requirement</span></span> | <span data-ttu-id="7dd8c-127">值</span><span class="sxs-lookup"><span data-stu-id="7dd8c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd8c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7dd8c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd8c-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dd8c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7dd8c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7dd8c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd8c-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dd8c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7dd8c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="7dd8c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dd8c-133"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd8c-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="7dd8c-134">Idl</span><span class="sxs-lookup"><span data-stu-id="7dd8c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7dd8c-135"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7dd8c-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="7dd8c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7dd8c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dd8c-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dd8c-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="7dd8c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dd8c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd8c-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="7dd8c-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





