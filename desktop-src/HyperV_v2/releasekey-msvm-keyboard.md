---
description: 模擬金鑰版本。
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Msvm_Keyboard 類別的 ReleaseKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514061"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="64fa6-103">Msvm 鍵盤類別的 ReleaseKey 方法 \_</span><span class="sxs-lookup"><span data-stu-id="64fa6-103">ReleaseKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="64fa6-104">模擬金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="64fa6-104">Simulates a key release.</span></span> <span data-ttu-id="64fa6-105">成功時，金鑰會處於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="64fa6-105">When successful, the key will be in the up state.</span></span>

## <a name="syntax"></a><span data-ttu-id="64fa6-106">語法</span><span class="sxs-lookup"><span data-stu-id="64fa6-106">Syntax</span></span>


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="64fa6-107">參數</span><span class="sxs-lookup"><span data-stu-id="64fa6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64fa6-108">*keyCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64fa6-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64fa6-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64fa6-109">Type: **uint32**</span></span>

<span data-ttu-id="64fa6-110">要釋放之金鑰的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="64fa6-110">The virtual key code of the key to release.</span></span> <span data-ttu-id="64fa6-111">如需虛擬機器碼的清單，請參閱 [**虛擬金鑰代碼**](../inputdev/virtual-key-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="64fa6-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64fa6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="64fa6-112">Return value</span></span>

<span data-ttu-id="64fa6-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64fa6-113">Type: **uint32**</span></span>

<span data-ttu-id="64fa6-114">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="64fa6-114">A return value of zero indicates success.</span></span> <span data-ttu-id="64fa6-115">非零值表示無法修改金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="64fa6-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="64fa6-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="64fa6-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="64fa6-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="64fa6-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="64fa6-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="64fa6-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="64fa6-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="64fa6-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="64fa6-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-124">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="64fa6-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="64fa6-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="64fa6-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="64fa6-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="64fa6-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="64fa6-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="64fa6-129">備註</span><span class="sxs-lookup"><span data-stu-id="64fa6-129">Remarks</span></span>

<span data-ttu-id="64fa6-130">**ReleaseKey** 方法會將 [VK] **\_ 功能表** 的參考（ (18) 、 **VK \_ CONTROL** (17) 和 **VK \_ SHIFT** (16) 分別對應至 **VK \_ LMENU** (164) 、 **VK \_ LCONTROL** (162) 和 **VK \_ LSHIFT** (160) ，因為 **VK \_ 功能表**、 **VK \_ 控制項** 和 **VK \_ SHIFT** 虛擬按鍵代碼不代表鍵盤上的實際按鍵。</span><span class="sxs-lookup"><span data-stu-id="64fa6-130">The **ReleaseKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="64fa6-131">[**Msvm \_ 鍵盤**](msvm-keyboard.md)類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="64fa6-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="64fa6-132">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="64fa6-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="64fa6-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="64fa6-133">Requirements</span></span>



| <span data-ttu-id="64fa6-134">需求</span><span class="sxs-lookup"><span data-stu-id="64fa6-134">Requirement</span></span> | <span data-ttu-id="64fa6-135">值</span><span class="sxs-lookup"><span data-stu-id="64fa6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64fa6-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64fa6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="64fa6-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64fa6-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="64fa6-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64fa6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="64fa6-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64fa6-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64fa6-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="64fa6-140">Namespace</span></span><br/>                | <span data-ttu-id="64fa6-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="64fa6-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="64fa6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="64fa6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64fa6-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="64fa6-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64fa6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="64fa6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64fa6-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64fa6-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64fa6-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64fa6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64fa6-147">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="64fa6-147">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="64fa6-148">**虛擬金鑰碼**</span><span class="sxs-lookup"><span data-stu-id="64fa6-148">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

