---
description: Msvm_SecurityService 類別的 SetKeyProtector 方法：設定虛擬系統的金鑰保護裝置。
ms.assetid: 84c114cb-a3a0-44f2-b862-38b05b96bd46
title: Msvm_SecurityService 類別的 SetKeyProtector 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3b5eca7ddcc506d158175782e3e13796e56de267
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111406"
---
# <a name="setkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="d57d6-103">Msvm SecurityService 類別的 SetKeyProtector 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d57d6-103">SetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="d57d6-104">設定虛擬系統的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="d57d6-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="d57d6-105">Syntax</span></span>


```mof
uint32 SetKeyProtector(
  [in]  string              SecuritySettingData,
  [in]  uint8               KeyProtector[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d57d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="d57d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57d6-107">*SecuritySettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d57d6-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57d6-108">字串包含 [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) 類別的內嵌實例，代表虛擬系統的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="d57d6-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="d57d6-109">*KeyProtector* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d57d6-109">*KeyProtector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d57d6-110">原始位元組陣列，包含要設定的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="d57d6-110">Raw byte array that contains the key protector to set.</span></span>

</dd> <dt>

<span data-ttu-id="d57d6-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d57d6-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d57d6-112">用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="d57d6-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="d57d6-113">如果作業是以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="d57d6-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d57d6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d57d6-114">Return value</span></span>

<span data-ttu-id="d57d6-115">成功時，會傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d57d6-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d57d6-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="d57d6-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="d57d6-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="d57d6-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="d57d6-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="d57d6-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="d57d6-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="d57d6-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="d57d6-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="d57d6-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="d57d6-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="d57d6-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="d57d6-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d57d6-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="d57d6-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d57d6-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d57d6-129">Requirements</span></span>



| <span data-ttu-id="d57d6-130">需求</span><span class="sxs-lookup"><span data-stu-id="d57d6-130">Requirement</span></span> | <span data-ttu-id="d57d6-131">值</span><span class="sxs-lookup"><span data-stu-id="d57d6-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d57d6-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d57d6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d57d6-133">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d57d6-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d57d6-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d57d6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d57d6-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d57d6-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d57d6-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="d57d6-136">Namespace</span></span><br/>                | <span data-ttu-id="d57d6-137">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d57d6-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d57d6-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d57d6-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d57d6-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d57d6-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d57d6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d57d6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d57d6-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d57d6-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d57d6-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d57d6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57d6-143">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="d57d6-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




