---
description: 模擬電子報按鍵序列。
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Msvm_Keyboard 類別的 TypeKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945068"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="cde1a-103">Msvm 鍵盤類別的 TypeKey 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cde1a-103">TypeKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="cde1a-104">模擬電子報按鍵序列。</span><span class="sxs-lookup"><span data-stu-id="cde1a-104">Simulates a press-release key sequence.</span></span> <span data-ttu-id="cde1a-105">這相當於呼叫 [**PressKey**](presskey-msvm-keyboard.md) ，後面接著 [**ReleaseKey**](releasekey-msvm-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="cde1a-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cde1a-106">語法</span><span class="sxs-lookup"><span data-stu-id="cde1a-106">Syntax</span></span>


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="cde1a-107">參數</span><span class="sxs-lookup"><span data-stu-id="cde1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cde1a-108">*keyCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cde1a-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde1a-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cde1a-109">Type: **uint32**</span></span>

<span data-ttu-id="cde1a-110">要按下之按鍵的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="cde1a-110">The virtual key code of the key to press.</span></span> <span data-ttu-id="cde1a-111">如需虛擬機器碼的清單，請參閱 [**虛擬金鑰代碼**](../inputdev/virtual-key-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="cde1a-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cde1a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cde1a-112">Return value</span></span>

<span data-ttu-id="cde1a-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cde1a-113">Type: **uint32**</span></span>

<span data-ttu-id="cde1a-114">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="cde1a-114">A return value of zero indicates success.</span></span> <span data-ttu-id="cde1a-115">非零值表示無法修改金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="cde1a-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="cde1a-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="cde1a-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="cde1a-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="cde1a-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="cde1a-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="cde1a-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="cde1a-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="cde1a-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="cde1a-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-124">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="cde1a-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="cde1a-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="cde1a-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="cde1a-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cde1a-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="cde1a-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cde1a-129">備註</span><span class="sxs-lookup"><span data-stu-id="cde1a-129">Remarks</span></span>

<span data-ttu-id="cde1a-130">[**Msvm \_ 鍵盤**](msvm-keyboard.md)類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="cde1a-130">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cde1a-131">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="cde1a-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cde1a-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="cde1a-132">Requirements</span></span>



| <span data-ttu-id="cde1a-133">需求</span><span class="sxs-lookup"><span data-stu-id="cde1a-133">Requirement</span></span> | <span data-ttu-id="cde1a-134">值</span><span class="sxs-lookup"><span data-stu-id="cde1a-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cde1a-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cde1a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cde1a-136">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cde1a-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cde1a-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cde1a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cde1a-138">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cde1a-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cde1a-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="cde1a-139">Namespace</span></span><br/>                | <span data-ttu-id="cde1a-140">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="cde1a-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cde1a-141">MOF</span><span class="sxs-lookup"><span data-stu-id="cde1a-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cde1a-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="cde1a-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cde1a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cde1a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde1a-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cde1a-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cde1a-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cde1a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde1a-146">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="cde1a-146">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="cde1a-147">**虛擬金鑰碼**</span><span class="sxs-lookup"><span data-stu-id="cde1a-147">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

