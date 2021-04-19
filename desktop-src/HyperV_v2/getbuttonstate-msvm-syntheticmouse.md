---
description: 抓取指定裝置按鈕的目前狀態。
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Msvm_SyntheticMouse 類別的 GetButtonState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3812d3e019a303656305471fc097fb1479fa1ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973090"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="46787-103">Msvm SyntheticMouse 類別的 GetButtonState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="46787-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="46787-104">抓取指定裝置按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="46787-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="46787-105">語法</span><span class="sxs-lookup"><span data-stu-id="46787-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="46787-106">參數</span><span class="sxs-lookup"><span data-stu-id="46787-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46787-107">*buttonIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46787-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46787-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="46787-108">Type: **uint32**</span></span>

<span data-ttu-id="46787-109">要查詢之按鈕的索引（以1為基礎）。</span><span class="sxs-lookup"><span data-stu-id="46787-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="46787-110">*isDown* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46787-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46787-111">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="46787-111">Type: **boolean**</span></span>

<span data-ttu-id="46787-112">按鈕目前的關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="46787-112">The current down state of the button.</span></span> <span data-ttu-id="46787-113">**True** 值表示按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="46787-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46787-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="46787-114">Return value</span></span>

<span data-ttu-id="46787-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="46787-115">Type: **uint32**</span></span>

<span data-ttu-id="46787-116">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="46787-116">A return value of zero indicates success.</span></span> <span data-ttu-id="46787-117">非零值表示查詢失敗。</span><span class="sxs-lookup"><span data-stu-id="46787-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="46787-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="46787-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46787-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="46787-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="46787-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="46787-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="46787-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="46787-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="46787-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="46787-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="46787-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="46787-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="46787-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="46787-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="46787-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="46787-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="46787-126">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="46787-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="46787-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="46787-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="46787-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="46787-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="46787-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="46787-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="46787-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="46787-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="46787-131">備註</span><span class="sxs-lookup"><span data-stu-id="46787-131">Remarks</span></span>

<span data-ttu-id="46787-132">存取 [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="46787-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="46787-133">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="46787-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="46787-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="46787-134">Requirements</span></span>



| <span data-ttu-id="46787-135">需求</span><span class="sxs-lookup"><span data-stu-id="46787-135">Requirement</span></span> | <span data-ttu-id="46787-136">值</span><span class="sxs-lookup"><span data-stu-id="46787-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46787-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46787-137">Minimum supported client</span></span><br/> | <span data-ttu-id="46787-138">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46787-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="46787-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46787-139">Minimum supported server</span></span><br/> | <span data-ttu-id="46787-140">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46787-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46787-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="46787-141">Namespace</span></span><br/>                | <span data-ttu-id="46787-142">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="46787-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="46787-143">MOF</span><span class="sxs-lookup"><span data-stu-id="46787-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46787-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="46787-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46787-145">DLL</span><span class="sxs-lookup"><span data-stu-id="46787-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46787-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46787-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46787-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46787-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46787-148">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="46787-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

