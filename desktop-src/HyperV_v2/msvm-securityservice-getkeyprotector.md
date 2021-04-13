---
description: 捕獲虛擬系統的金鑰保護裝置。
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: Msvm_SecurityService 類別的 GetKeyProtector 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49f2479660d0402c7b3d428c76f9fe454ecf64cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321236"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="3359a-103">Msvm SecurityService 類別的 GetKeyProtector 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3359a-103">GetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="3359a-104">捕獲虛擬系統的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="3359a-104">Retrieves the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3359a-105">語法</span><span class="sxs-lookup"><span data-stu-id="3359a-105">Syntax</span></span>


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a><span data-ttu-id="3359a-106">參數</span><span class="sxs-lookup"><span data-stu-id="3359a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3359a-107">*SecuritySettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3359a-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3359a-108">字串包含 [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) 類別的內嵌實例，代表虛擬系統的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="3359a-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="3359a-109">*KeyProtector* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3359a-109">*KeyProtector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3359a-110">接收原始位元組陣列，其中包含目前使用中的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="3359a-110">Receives the raw byte array that contains the key protector currently in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3359a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3359a-111">Return value</span></span>

<span data-ttu-id="3359a-112">成功時，會傳回0或4096。</span><span class="sxs-lookup"><span data-stu-id="3359a-112">On success, returns a 0 or 4096.</span></span> <span data-ttu-id="3359a-113">否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3359a-113">Otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3359a-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="3359a-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-115">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="3359a-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="3359a-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="3359a-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="3359a-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="3359a-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="3359a-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="3359a-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-122">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="3359a-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="3359a-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="3359a-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="3359a-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3359a-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="3359a-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3359a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3359a-127">Requirements</span></span>



| <span data-ttu-id="3359a-128">需求</span><span class="sxs-lookup"><span data-stu-id="3359a-128">Requirement</span></span> | <span data-ttu-id="3359a-129">值</span><span class="sxs-lookup"><span data-stu-id="3359a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3359a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3359a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3359a-131">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3359a-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3359a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3359a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3359a-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3359a-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3359a-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="3359a-134">Namespace</span></span><br/>                | <span data-ttu-id="3359a-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="3359a-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3359a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3359a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3359a-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3359a-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3359a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3359a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3359a-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3359a-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3359a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3359a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3359a-141">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="3359a-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




