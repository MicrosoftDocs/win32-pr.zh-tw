---
description: 使用掃描碼來模擬按鍵序列。
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: Msvm_Keyboard 類別的 TypeScancodes 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97479a1a0926894f72472b7459f77cd9325ac6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690856"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="ffeaf-103">Msvm 鍵盤類別的 TypeScancodes 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ffeaf-103">TypeScancodes method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="ffeaf-104">使用掃描碼來模擬按鍵序列。</span><span class="sxs-lookup"><span data-stu-id="ffeaf-104">Simulates a key sequence using scan codes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffeaf-105">語法</span><span class="sxs-lookup"><span data-stu-id="ffeaf-105">Syntax</span></span>


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a><span data-ttu-id="ffeaf-106">參數</span><span class="sxs-lookup"><span data-stu-id="ffeaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffeaf-107">*Scancodes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffeaf-107">*Scancodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffeaf-108">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="ffeaf-108">Type: **uint8\[\]**</span></span>

<span data-ttu-id="ffeaf-109">陣列，包含要輸入的掃描碼。</span><span class="sxs-lookup"><span data-stu-id="ffeaf-109">An array that contains the scan codes to type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffeaf-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffeaf-110">Return value</span></span>

<span data-ttu-id="ffeaf-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ffeaf-111">Type: **uint32**</span></span>

<span data-ttu-id="ffeaf-112">如果成功，這個方法會傳回0。</span><span class="sxs-lookup"><span data-stu-id="ffeaf-112">This method returns 0 if it succeeds.</span></span> <span data-ttu-id="ffeaf-113">任何其他傳回值表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="ffeaf-113">Any other return value indicates an error.</span></span> <span data-ttu-id="ffeaf-114">傳回值可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ffeaf-114">The return value can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ffeaf-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-123">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ffeaf-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="ffeaf-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ffeaf-128">備註</span><span class="sxs-lookup"><span data-stu-id="ffeaf-128">Remarks</span></span>

<span data-ttu-id="ffeaf-129">[**Msvm \_ 鍵盤**](msvm-keyboard.md)類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="ffeaf-129">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ffeaf-130">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="ffeaf-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffeaf-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffeaf-131">Requirements</span></span>



| <span data-ttu-id="ffeaf-132">需求</span><span class="sxs-lookup"><span data-stu-id="ffeaf-132">Requirement</span></span> | <span data-ttu-id="ffeaf-133">值</span><span class="sxs-lookup"><span data-stu-id="ffeaf-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffeaf-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffeaf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ffeaf-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffeaf-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ffeaf-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffeaf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ffeaf-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffeaf-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ffeaf-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="ffeaf-138">Namespace</span></span><br/>                | <span data-ttu-id="ffeaf-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="ffeaf-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ffeaf-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ffeaf-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffeaf-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ffeaf-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffeaf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ffeaf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffeaf-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffeaf-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffeaf-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffeaf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffeaf-145">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="ffeaf-145">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

