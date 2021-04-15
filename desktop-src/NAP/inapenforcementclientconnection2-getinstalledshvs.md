---
title: 'INapEnforcementClientConnection2 GetInstalledShvs 方法 (NapEnforcementClient .h) '
description: NAP 代理程式用來查詢用戶端上已安裝的系統健康狀態驗證 (Shv) 。
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- GetInstalledShvs 方法 NAP
- GetInstalledShvs 方法 NAP，INapEnforcementClientConnection2 介面
- INapEnforcementClientConnection2 介面 NAP，GetInstalledShvs 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467068"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a><span data-ttu-id="96076-106">INapEnforcementClientConnection2：： GetInstalledShvs 方法</span><span class="sxs-lookup"><span data-stu-id="96076-106">INapEnforcementClientConnection2::GetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="96076-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="96076-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="96076-108">NAP 代理程式會使用 **GetInstalledShvs** 方法來查詢用戶端上已安裝的系統健康狀態驗證 (shv) 。</span><span class="sxs-lookup"><span data-stu-id="96076-108">The **GetInstalledShvs** method is used by the NAP Agent to query the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="96076-109">語法</span><span class="sxs-lookup"><span data-stu-id="96076-109">Syntax</span></span>


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a><span data-ttu-id="96076-110">參數</span><span class="sxs-lookup"><span data-stu-id="96076-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96076-111">*計數* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="96076-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96076-112">[SystemHealthEntityCount](nap-datatypes.md)值的指標，指定 *識別碼* 中已安裝的 shv 數目。</span><span class="sxs-lookup"><span data-stu-id="96076-112">A pointer to a [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of installed SHVs in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="96076-113">*識別碼* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="96076-113">*ids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96076-114">[SystemHealthEntityId](nap-datatypes.md)值陣列的指標，其中包含已安裝的 SHV 識別碼。</span><span class="sxs-lookup"><span data-stu-id="96076-114">A pointer to an array of [SystemHealthEntityId](nap-datatypes.md) values that contain the installed SHV IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96076-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="96076-115">Return value</span></span>

<span data-ttu-id="96076-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="96076-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="96076-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="96076-117">Return code</span></span>                                                                                   | <span data-ttu-id="96076-118">Description</span><span class="sxs-lookup"><span data-stu-id="96076-118">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="96076-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="96076-119"><dt>**S\_OK** </dt></span></span> </dl>         | <span data-ttu-id="96076-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="96076-120">Operation succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="96076-121"><dt>**E \_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="96076-121"><dt>**E\_INVALIDARG** </dt></span></span> </dl> | <span data-ttu-id="96076-122">傳遞給方法的引數無效。</span><span class="sxs-lookup"><span data-stu-id="96076-122">An invalid argument was passed to the method.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="96076-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="96076-123">Requirements</span></span>



| <span data-ttu-id="96076-124">需求</span><span class="sxs-lookup"><span data-stu-id="96076-124">Requirement</span></span> | <span data-ttu-id="96076-125">值</span><span class="sxs-lookup"><span data-stu-id="96076-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96076-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96076-126">Minimum supported client</span></span><br/> | <span data-ttu-id="96076-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96076-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="96076-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96076-128">Minimum supported server</span></span><br/> | <span data-ttu-id="96076-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96076-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="96076-130">標頭</span><span class="sxs-lookup"><span data-stu-id="96076-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="96076-131"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="96076-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="96076-132">Idl</span><span class="sxs-lookup"><span data-stu-id="96076-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96076-133"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="96076-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="96076-134">DLL</span><span class="sxs-lookup"><span data-stu-id="96076-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96076-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96076-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="96076-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96076-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96076-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="96076-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





