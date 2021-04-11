---
title: 'INapServerManagement RegisterSystemHealthValidator 方法 (NapServerManagement .h) '
description: 註冊 SHV。
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- RegisterSystemHealthValidator 方法 NAP
- RegisterSystemHealthValidator 方法 NAP，INapServerManagement 介面
- INapServerManagement 介面 NAP，RegisterSystemHealthValidator 方法
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187322"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a><span data-ttu-id="39d3f-106">INapServerManagement：： RegisterSystemHealthValidator 方法</span><span class="sxs-lookup"><span data-stu-id="39d3f-106">INapServerManagement::RegisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="39d3f-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="39d3f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="39d3f-108">**INapServerManagement：： RegisterSystemHealthValidator** 方法會註冊 SHV。</span><span class="sxs-lookup"><span data-stu-id="39d3f-108">The **INapServerManagement::RegisterSystemHealthValidator** method registers an SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d3f-109">語法</span><span class="sxs-lookup"><span data-stu-id="39d3f-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a><span data-ttu-id="39d3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="39d3f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39d3f-111">*驗證* \[ 程式在\]</span><span class="sxs-lookup"><span data-stu-id="39d3f-111">*validator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d3f-112">[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)結構的指標，其中包含 SHV 註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="39d3f-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="39d3f-113">*validatorClsid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d3f-113">*validatorClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d3f-114">COM 類別 CLSID 的指標，該類別會實 [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="39d3f-114">A pointer to the CLSID of the COM class that implements the [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39d3f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="39d3f-115">Return value</span></span>

<span data-ttu-id="39d3f-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="39d3f-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="39d3f-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="39d3f-117">Return code</span></span>                                                                                            | <span data-ttu-id="39d3f-118">Description</span><span class="sxs-lookup"><span data-stu-id="39d3f-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="39d3f-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="39d3f-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="39d3f-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="39d3f-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="39d3f-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="39d3f-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="39d3f-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="39d3f-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="39d3f-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="39d3f-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="39d3f-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="39d3f-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="39d3f-125"><dt>**NAP \_ E \_ 衝突 \_ 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="39d3f-125"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="39d3f-126">SHV 識別碼已註冊。</span><span class="sxs-lookup"><span data-stu-id="39d3f-126">SHV id is already registered.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="39d3f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="39d3f-127">Requirements</span></span>



| <span data-ttu-id="39d3f-128">需求</span><span class="sxs-lookup"><span data-stu-id="39d3f-128">Requirement</span></span> | <span data-ttu-id="39d3f-129">值</span><span class="sxs-lookup"><span data-stu-id="39d3f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d3f-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39d3f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="39d3f-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="39d3f-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="39d3f-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39d3f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="39d3f-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39d3f-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39d3f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="39d3f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="39d3f-135"><dt>NapServerManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="39d3f-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="39d3f-136">Idl</span><span class="sxs-lookup"><span data-stu-id="39d3f-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39d3f-137"><dt>NapServerManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="39d3f-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="39d3f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="39d3f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39d3f-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39d3f-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="39d3f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39d3f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d3f-141">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="39d3f-141">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





