---
title: 'INapEnforcementClientConnection2 SetInstalledShvs 方法 (NapEnforcementClient .h) '
description: NAP 代理程式用來將已安裝的系統健康狀態驗證 (Shv) 安裝在用戶端上。
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- SetInstalledShvs 方法 NAP
- SetInstalledShvs 方法 NAP，INapEnforcementClientConnection2 介面
- INapEnforcementClientConnection2 介面 NAP，SetInstalledShvs 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106512"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a><span data-ttu-id="ff610-106">INapEnforcementClientConnection2：： SetInstalledShvs 方法</span><span class="sxs-lookup"><span data-stu-id="ff610-106">INapEnforcementClientConnection2::SetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="ff610-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="ff610-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ff610-108">NAP 代理程式會使用 **SetInstalledShvs** 方法，將已安裝的系統健康狀態驗證 (shv) 安裝在用戶端上。</span><span class="sxs-lookup"><span data-stu-id="ff610-108">The **SetInstalledShvs** method is used by the NAP Agent to set the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff610-109">語法</span><span class="sxs-lookup"><span data-stu-id="ff610-109">Syntax</span></span>


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a><span data-ttu-id="ff610-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff610-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff610-111">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff610-111">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff610-112">[SystemHealthEntityCount](nap-datatypes.md)值，指定要在 *識別碼* 中安裝的 shv 數目。</span><span class="sxs-lookup"><span data-stu-id="ff610-112">A [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of SHVs to install in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="ff610-113">*識別碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff610-113">*ids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff610-114">[SystemHealthEntityId](nap-datatypes.md)值的指標，其中包含要安裝的 SHV 識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="ff610-114">A pointer to a [SystemHealthEntityId](nap-datatypes.md) value that contains a list of SHV IDs to install.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff610-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff610-115">Return value</span></span>

<span data-ttu-id="ff610-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ff610-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ff610-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ff610-117">Return code</span></span>                                                                                  | <span data-ttu-id="ff610-118">Description</span><span class="sxs-lookup"><span data-stu-id="ff610-118">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ff610-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ff610-119"><dt>**S\_OK** </dt></span></span> </dl>        | <span data-ttu-id="ff610-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="ff610-120">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="ff610-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ff610-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ff610-122">*Count* 參數為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="ff610-122">The *count* parameter was 0 (zero).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ff610-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff610-123">Requirements</span></span>



| <span data-ttu-id="ff610-124">需求</span><span class="sxs-lookup"><span data-stu-id="ff610-124">Requirement</span></span> | <span data-ttu-id="ff610-125">值</span><span class="sxs-lookup"><span data-stu-id="ff610-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff610-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff610-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ff610-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff610-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ff610-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff610-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ff610-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff610-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ff610-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ff610-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff610-131"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff610-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff610-132">Idl</span><span class="sxs-lookup"><span data-stu-id="ff610-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff610-133"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff610-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="ff610-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ff610-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff610-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff610-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ff610-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff610-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff610-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="ff610-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





