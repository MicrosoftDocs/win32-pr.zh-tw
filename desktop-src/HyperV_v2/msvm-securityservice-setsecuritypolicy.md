---
description: Msvm_SecurityService 類別的 SetSecurityPolicy 方法：設定虛擬系統的金鑰保護裝置。
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Msvm_SecurityService 類別的 SetSecurityPolicy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31b03ee8a941b0715b85f6a749c4ba59ade032f7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118726"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="d49e1-103">Msvm SecurityService 類別的 SetSecurityPolicy 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d49e1-103">SetSecurityPolicy method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="d49e1-104">設定虛擬系統的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="d49e1-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d49e1-105">語法</span><span class="sxs-lookup"><span data-stu-id="d49e1-105">Syntax</span></span>


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d49e1-106">參數</span><span class="sxs-lookup"><span data-stu-id="d49e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d49e1-107">*SecuritySettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d49e1-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d49e1-108">字串包含 [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) 類別的內嵌實例，代表虛擬系統的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="d49e1-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="d49e1-109">*SecurityPolicy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d49e1-109">*SecurityPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d49e1-110">原始位元組陣列，包含要設定的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="d49e1-110">Raw byte array that contains the security policy to set.</span></span>

</dd> <dt>

<span data-ttu-id="d49e1-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d49e1-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d49e1-112">用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="d49e1-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="d49e1-113">如果作業是以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="d49e1-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d49e1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d49e1-114">Return value</span></span>

<span data-ttu-id="d49e1-115">在上，success 會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d49e1-115">On, success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d49e1-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="d49e1-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="d49e1-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="d49e1-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="d49e1-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="d49e1-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="d49e1-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="d49e1-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="d49e1-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="d49e1-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="d49e1-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="d49e1-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="d49e1-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d49e1-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="d49e1-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d49e1-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d49e1-129">Requirements</span></span>



| <span data-ttu-id="d49e1-130">需求</span><span class="sxs-lookup"><span data-stu-id="d49e1-130">Requirement</span></span> | <span data-ttu-id="d49e1-131">值</span><span class="sxs-lookup"><span data-stu-id="d49e1-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d49e1-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d49e1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d49e1-133">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d49e1-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d49e1-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d49e1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d49e1-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d49e1-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d49e1-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="d49e1-136">Namespace</span></span><br/>                | <span data-ttu-id="d49e1-137">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d49e1-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d49e1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d49e1-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d49e1-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d49e1-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d49e1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d49e1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d49e1-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d49e1-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d49e1-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d49e1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d49e1-143">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="d49e1-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




