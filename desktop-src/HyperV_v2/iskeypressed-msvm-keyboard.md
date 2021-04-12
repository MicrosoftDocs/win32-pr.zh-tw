---
description: 捕獲索引鍵的索引鍵狀態。
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Msvm_Keyboard 類別的 IsKeyPressed 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191875"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="c7518-103">Msvm 鍵盤類別的 IsKeyPressed 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c7518-103">IsKeyPressed method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="c7518-104">捕獲索引鍵的索引鍵狀態。</span><span class="sxs-lookup"><span data-stu-id="c7518-104">Retrieves the key state of a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7518-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7518-105">Syntax</span></span>


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a><span data-ttu-id="c7518-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7518-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7518-107">*keyCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7518-107">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7518-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7518-108">Type: **uint32**</span></span>

<span data-ttu-id="c7518-109">要查詢之索引鍵的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="c7518-109">The virtual key code of the key to query.</span></span> <span data-ttu-id="c7518-110">如需虛擬機器碼的清單，請參閱 [**虛擬金鑰代碼**](../inputdev/virtual-key-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="c7518-110">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7518-111">*keyState* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c7518-111">*keyState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7518-112">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c7518-112">Type: **boolean**</span></span>

<span data-ttu-id="c7518-113">機碼目前的關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="c7518-113">The current down state of the key.</span></span> <span data-ttu-id="c7518-114">**True** 值表示金鑰已關閉。</span><span class="sxs-lookup"><span data-stu-id="c7518-114">A **True** value means the key is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7518-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7518-115">Return value</span></span>

<span data-ttu-id="c7518-116">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7518-116">Type: **uint32**</span></span>

<span data-ttu-id="c7518-117">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="c7518-117">A return value of zero indicates success.</span></span> <span data-ttu-id="c7518-118">非零值表示無法查詢索引鍵狀態。</span><span class="sxs-lookup"><span data-stu-id="c7518-118">A nonzero value indicates a failure to query the key state.</span></span>

<dl> <dt>

<span data-ttu-id="c7518-119">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="c7518-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-120">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="c7518-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-121">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="c7518-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-122">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="c7518-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-123">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="c7518-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-124">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="c7518-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-125">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="c7518-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-126">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="c7518-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-127">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="c7518-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-128">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="c7518-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-129">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="c7518-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-130">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="c7518-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c7518-131">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="c7518-131">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c7518-132">備註</span><span class="sxs-lookup"><span data-stu-id="c7518-132">Remarks</span></span>

<span data-ttu-id="c7518-133">**IsKeyPressed** 方法一律會針對 [ **VK] \_ 功能表** (18) 、 **VK \_ CONTROL** (17) 和 **VK \_ SHIFT** (16) 傳回 **False** ，因為這些不是鍵盤上的實際按鍵。</span><span class="sxs-lookup"><span data-stu-id="c7518-133">The **IsKeyPressed** method will always return **False** for the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) because these are not real keys on a keyboard.</span></span> <span data-ttu-id="c7518-134">這些虛擬機器碼程式碼一律會分別對應到 **VK \_ LMENU** (164) 、 **VK \_ LCONTROL** (162) 和 **VK \_ LSHIFT** (160) ，方法是 [**PressKey**](presskey-msvm-keyboard.md) 和 [**ReleaseKey**](releasekey-msvm-keyboard.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c7518-134">These virtual key codes are always mapped to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, by the [**PressKey**](presskey-msvm-keyboard.md) and [**ReleaseKey**](releasekey-msvm-keyboard.md) methods.</span></span>

<span data-ttu-id="c7518-135">[**Msvm \_ 鍵盤**](msvm-keyboard.md)類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="c7518-135">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c7518-136">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="c7518-136">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7518-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7518-137">Requirements</span></span>



| <span data-ttu-id="c7518-138">需求</span><span class="sxs-lookup"><span data-stu-id="c7518-138">Requirement</span></span> | <span data-ttu-id="c7518-139">值</span><span class="sxs-lookup"><span data-stu-id="c7518-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7518-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7518-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c7518-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7518-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7518-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7518-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c7518-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7518-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7518-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="c7518-144">Namespace</span></span><br/>                | <span data-ttu-id="c7518-145">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c7518-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7518-146">MOF</span><span class="sxs-lookup"><span data-stu-id="c7518-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7518-147"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c7518-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7518-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c7518-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7518-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7518-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7518-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7518-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7518-151">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="c7518-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="c7518-152">**虛擬金鑰碼**</span><span class="sxs-lookup"><span data-stu-id="c7518-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

