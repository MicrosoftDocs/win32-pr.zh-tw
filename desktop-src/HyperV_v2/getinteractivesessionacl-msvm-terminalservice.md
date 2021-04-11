---
description: 抓取 (DACL) 的目前任意存取控制清單，以控制對虛擬機器的互動式會話的存取。
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Msvm_TerminalService 類別的 GetInteractiveSessionACL 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690795"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="65d05-103">Msvm TerminalService 類別的 GetInteractiveSessionACL 方法 \_</span><span class="sxs-lookup"><span data-stu-id="65d05-103">GetInteractiveSessionACL method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="65d05-104">抓取 (DACL) 的目前 *任意存取控制清單* ，以控制對虛擬機器的互動式會話的存取。</span><span class="sxs-lookup"><span data-stu-id="65d05-104">Retrieves the current *discretionary access control list* (DACL) that controls access to the interactive session of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d05-105">語法</span><span class="sxs-lookup"><span data-stu-id="65d05-105">Syntax</span></span>


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a><span data-ttu-id="65d05-106">參數</span><span class="sxs-lookup"><span data-stu-id="65d05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d05-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="65d05-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65d05-108">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，該類別代表將抓取其 DACL 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="65d05-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine whose DACL will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="65d05-109">*AccessControlList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="65d05-109">*AccessControlList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65d05-110">字串陣列，其中每個字串都包含 [**Msvm \_ InteractiveSessionACE**](msvm-interactivesessionace.md) 類別的內嵌實例，表示虛擬機器互動式會話 DACL 中 (ACE) 的 *存取控制專案* 。</span><span class="sxs-lookup"><span data-stu-id="65d05-110">An array of strings, each containing an embedded instance of the [**Msvm\_InteractiveSessionACE**](msvm-interactivesessionace.md) class that represents an *access control entry* (ACE) in the virtual machine interactive session DACL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d05-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="65d05-111">Return value</span></span>

<span data-ttu-id="65d05-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="65d05-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="65d05-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="65d05-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-114">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="65d05-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-115">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="65d05-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-116">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="65d05-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-117">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="65d05-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-118">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="65d05-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-119"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="65d05-119">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="65d05-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="65d05-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-122">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="65d05-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="65d05-123">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="65d05-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="65d05-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="65d05-124">Requirements</span></span>



| <span data-ttu-id="65d05-125">需求</span><span class="sxs-lookup"><span data-stu-id="65d05-125">Requirement</span></span> | <span data-ttu-id="65d05-126">值</span><span class="sxs-lookup"><span data-stu-id="65d05-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d05-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65d05-127">Minimum supported client</span></span><br/> | <span data-ttu-id="65d05-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65d05-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="65d05-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65d05-129">Minimum supported server</span></span><br/> | <span data-ttu-id="65d05-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65d05-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65d05-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="65d05-131">Namespace</span></span><br/>                | <span data-ttu-id="65d05-132">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="65d05-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="65d05-133">MOF</span><span class="sxs-lookup"><span data-stu-id="65d05-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65d05-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="65d05-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="65d05-135">DLL</span><span class="sxs-lookup"><span data-stu-id="65d05-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65d05-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65d05-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="65d05-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65d05-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d05-138">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="65d05-138">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




