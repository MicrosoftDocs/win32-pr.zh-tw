---
description: 還原回最後一個已知的正確金鑰保護裝置。
ms.assetid: 0d1ea5d8-d25e-400c-be65-afe1bd65b1f0
title: Msvm_SecurityService 類別的 RestoreLastKnownGoodKeyProtector 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.RestoreLastKnownGoodKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e82fb3b40f4b85e74f92ed2690a411932af2eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976607"
---
# <a name="restorelastknowngoodkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="2b612-103">Msvm SecurityService 類別的 RestoreLastKnownGoodKeyProtector 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2b612-103">RestoreLastKnownGoodKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="2b612-104">還原回最後一個已知的正確金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="2b612-104">Restores back to the last known good key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b612-105">語法</span><span class="sxs-lookup"><span data-stu-id="2b612-105">Syntax</span></span>


```mof
uint32 RestoreLastKnownGoodKeyProtector(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2b612-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b612-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b612-107">*SecuritySettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b612-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b612-108">字串包含 [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) 類別的內嵌實例，代表虛擬系統的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="2b612-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="2b612-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b612-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b612-110">用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="2b612-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="2b612-111">如果作業是以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="2b612-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b612-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b612-112">Return value</span></span>

<span data-ttu-id="2b612-113">成功時，會傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2b612-113">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2b612-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="2b612-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-115">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="2b612-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="2b612-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="2b612-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="2b612-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="2b612-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="2b612-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="2b612-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-122">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="2b612-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="2b612-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="2b612-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="2b612-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2b612-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="2b612-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2b612-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b612-127">Requirements</span></span>



| <span data-ttu-id="2b612-128">需求</span><span class="sxs-lookup"><span data-stu-id="2b612-128">Requirement</span></span> | <span data-ttu-id="2b612-129">值</span><span class="sxs-lookup"><span data-stu-id="2b612-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b612-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b612-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2b612-131">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b612-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2b612-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b612-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2b612-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2b612-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2b612-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="2b612-134">Namespace</span></span><br/>                | <span data-ttu-id="2b612-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2b612-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2b612-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2b612-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b612-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2b612-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b612-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2b612-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b612-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b612-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b612-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b612-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b612-141">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="2b612-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




