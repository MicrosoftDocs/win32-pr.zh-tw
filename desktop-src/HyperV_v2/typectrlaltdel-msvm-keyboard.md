---
description: 模擬 Ctrl + Alt + Del 鍵序列。
ms.assetid: C24C9C42-844F-4560-B8C1-0054F5E913D6
title: Msvm_Keyboard 類別的 TypeCtrlAltDel 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeCtrlAltDel
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 64ebc4bddf8adccd7098cafed1df43d1cf1cb4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320244"
---
# <a name="typectrlaltdel-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="f736c-103">Msvm 鍵盤類別的 TypeCtrlAltDel 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f736c-103">TypeCtrlAltDel method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="f736c-104">模擬 Ctrl + Alt + Del 鍵序列。</span><span class="sxs-lookup"><span data-stu-id="f736c-104">Simulates a Ctrl+Alt+Del key sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f736c-105">語法</span><span class="sxs-lookup"><span data-stu-id="f736c-105">Syntax</span></span>


```mof
uint32 TypeCtrlAltDel();
```



## <a name="parameters"></a><span data-ttu-id="f736c-106">參數</span><span class="sxs-lookup"><span data-stu-id="f736c-106">Parameters</span></span>

<span data-ttu-id="f736c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f736c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f736c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f736c-108">Return value</span></span>

<span data-ttu-id="f736c-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f736c-109">Type: **uint32**</span></span>

<span data-ttu-id="f736c-110">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="f736c-110">A return value of zero indicates success.</span></span> <span data-ttu-id="f736c-111">非零值表示傳送失敗。</span><span class="sxs-lookup"><span data-stu-id="f736c-111">A nonzero value indicates a failure to send.</span></span>

<dl> <dt>

<span data-ttu-id="f736c-112">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f736c-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-113">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="f736c-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-114">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="f736c-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-115">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="f736c-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-116">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="f736c-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-117">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="f736c-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-118">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="f736c-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-119">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="f736c-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-120">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="f736c-120">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-121">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="f736c-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-122">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="f736c-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-123">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="f736c-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f736c-124">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="f736c-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f736c-125">備註</span><span class="sxs-lookup"><span data-stu-id="f736c-125">Remarks</span></span>

<span data-ttu-id="f736c-126">[**Msvm \_ 鍵盤**](msvm-keyboard.md)類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="f736c-126">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f736c-127">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="f736c-127">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f736c-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="f736c-128">Requirements</span></span>



| <span data-ttu-id="f736c-129">需求</span><span class="sxs-lookup"><span data-stu-id="f736c-129">Requirement</span></span> | <span data-ttu-id="f736c-130">值</span><span class="sxs-lookup"><span data-stu-id="f736c-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f736c-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f736c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f736c-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f736c-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f736c-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f736c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f736c-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f736c-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f736c-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="f736c-135">Namespace</span></span><br/>                | <span data-ttu-id="f736c-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f736c-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f736c-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f736c-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f736c-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f736c-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f736c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f736c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f736c-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f736c-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f736c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f736c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f736c-142">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="f736c-142">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

