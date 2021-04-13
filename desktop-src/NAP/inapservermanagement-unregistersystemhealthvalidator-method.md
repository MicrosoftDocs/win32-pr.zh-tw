---
title: 'INapServerManagement UnregisterSystemHealthValidator 方法 (NapServerManagement .h) '
description: 用來向 NAP 伺服器取消註冊 SHV。
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- UnregisterSystemHealthValidator 方法 NAP
- UnregisterSystemHealthValidator 方法 NAP，INapServerManagement 介面
- INapServerManagement 介面 NAP，UnregisterSystemHealthValidator 方法
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509143"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a><span data-ttu-id="6936f-106">INapServerManagement：： UnregisterSystemHealthValidator 方法</span><span class="sxs-lookup"><span data-stu-id="6936f-106">INapServerManagement::UnregisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="6936f-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="6936f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6936f-108">**INapServerManagement：： UnregisterSystemHealthValidator** 方法是用來向 NAP 伺服器取消註冊 SHV。</span><span class="sxs-lookup"><span data-stu-id="6936f-108">The **INapServerManagement::UnregisterSystemHealthValidator** method is used to unregister an SHV with the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6936f-109">語法</span><span class="sxs-lookup"><span data-stu-id="6936f-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="6936f-110">參數</span><span class="sxs-lookup"><span data-stu-id="6936f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6936f-111"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="6936f-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6936f-112">[**SystemHealthEntityId**](nap-type-constants.md) ，其中包含要取消註冊之 SHV 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6936f-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6936f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6936f-113">Return value</span></span>

<span data-ttu-id="6936f-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6936f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6936f-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6936f-115">Return code</span></span>                                                                                     | <span data-ttu-id="6936f-116">Description</span><span class="sxs-lookup"><span data-stu-id="6936f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6936f-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6936f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6936f-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="6936f-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6936f-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6936f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6936f-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="6936f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6936f-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6936f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6936f-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="6936f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6936f-123">備註</span><span class="sxs-lookup"><span data-stu-id="6936f-123">Remarks</span></span>

<span data-ttu-id="6936f-124">如果 SHV 上有任何擱置中的非同步呼叫，它們將會在稍後完成，並將被捨棄。</span><span class="sxs-lookup"><span data-stu-id="6936f-124">If there are any asynchronous calls pending on the SHV, they will complete at a later time and will be discarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="6936f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6936f-125">Requirements</span></span>



| <span data-ttu-id="6936f-126">需求</span><span class="sxs-lookup"><span data-stu-id="6936f-126">Requirement</span></span> | <span data-ttu-id="6936f-127">值</span><span class="sxs-lookup"><span data-stu-id="6936f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6936f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6936f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6936f-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="6936f-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="6936f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6936f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6936f-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6936f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6936f-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6936f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6936f-133"><dt>NapServerManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="6936f-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="6936f-134">Idl</span><span class="sxs-lookup"><span data-stu-id="6936f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6936f-135"><dt>NapServerManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6936f-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="6936f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6936f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6936f-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6936f-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="6936f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6936f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6936f-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="6936f-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





