---
description: SetShareInfo&\# 8194;WMI 類別方法會設定共用資源的參數。
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Win32_Share 類別的 SetShareInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191039"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a><span data-ttu-id="74531-103">Win32 共用類別的 SetShareInfo 方法 \_</span><span class="sxs-lookup"><span data-stu-id="74531-103">SetShareInfo method of the Win32\_Share class</span></span>

<span data-ttu-id="74531-104">**SetShareInfo** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會設定共用資源的參數。</span><span class="sxs-lookup"><span data-stu-id="74531-104">The **SetShareInfo** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the parameters of a shared resource.</span></span>

<span data-ttu-id="74531-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="74531-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="74531-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="74531-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="74531-107">語法</span><span class="sxs-lookup"><span data-stu-id="74531-107">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="74531-108">參數</span><span class="sxs-lookup"><span data-stu-id="74531-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74531-109">*MaximumAllowed* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="74531-109">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="74531-110">允許同時使用此資源的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="74531-110">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

<span data-ttu-id="74531-111">範例：10。</span><span class="sxs-lookup"><span data-stu-id="74531-111">Example: 10.</span></span> <span data-ttu-id="74531-112">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="74531-112">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="74531-113">*描述* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="74531-113">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="74531-114">描述所共用資源的選擇性批註。</span><span class="sxs-lookup"><span data-stu-id="74531-114">Optional comment to describe the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="74531-115">*存取* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="74531-115">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="74531-116">使用者層級許可權的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="74531-116">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="74531-117">安全描述項包含資源的許可權、擁有者和存取功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="74531-117">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="74531-118">如需詳細資訊，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)。</span><span class="sxs-lookup"><span data-stu-id="74531-118">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74531-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="74531-119">Return value</span></span>

<span data-ttu-id="74531-120">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="74531-120">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="74531-121">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="74531-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74531-122">**拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="74531-122">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="74531-123">**未知的失敗** (8) </span><span class="sxs-lookup"><span data-stu-id="74531-123">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="74531-124">**不正確名稱** (9) </span><span class="sxs-lookup"><span data-stu-id="74531-124">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="74531-125">**層級** (10) 無效</span><span class="sxs-lookup"><span data-stu-id="74531-125">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="74531-126">**不正確參數** (21) </span><span class="sxs-lookup"><span data-stu-id="74531-126">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="74531-127">**重複的共用** (22) </span><span class="sxs-lookup"><span data-stu-id="74531-127">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="74531-128">重新 **導向路徑** (23) </span><span class="sxs-lookup"><span data-stu-id="74531-128">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="74531-129">**未知的裝置或目錄** (24) </span><span class="sxs-lookup"><span data-stu-id="74531-129">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="74531-130">**找不到網路名稱** (25) </span><span class="sxs-lookup"><span data-stu-id="74531-130">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="74531-131">**其他** (26 4294967295) </span><span class="sxs-lookup"><span data-stu-id="74531-131">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="74531-132">備註</span><span class="sxs-lookup"><span data-stu-id="74531-132">Remarks</span></span>

<span data-ttu-id="74531-133">**SetShareInfo** 方法是動態物件方法，會用於這個類別的出現位置。</span><span class="sxs-lookup"><span data-stu-id="74531-133">**SetShareInfo** method is a dynamic object method and is used on an occurrence of this class.</span></span>

<span data-ttu-id="74531-134">只有 Administrators 或 Account Operators 本機群組的成員，或是具有通訊、列印或伺服器操作員群組成員資格的成員，才能夠成功執行 **SetShareInfo**。</span><span class="sxs-lookup"><span data-stu-id="74531-134">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **SetShareInfo**.</span></span> <span data-ttu-id="74531-135">列印操作員只能設定印表機佇列。</span><span class="sxs-lookup"><span data-stu-id="74531-135">The print operator can only set printer queues.</span></span> <span data-ttu-id="74531-136">通訊運算子只能設定通訊裝置佇列。</span><span class="sxs-lookup"><span data-stu-id="74531-136">The Communication operator can only set communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="74531-137">範例</span><span class="sxs-lookup"><span data-stu-id="74531-137">Examples</span></span>

<span data-ttu-id="74531-138">下列 PowerShell 範例會更新 **newShare** 共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="74531-138">The following PowerShell sample updates the name of the **newShare** share.</span></span>


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



## <a name="requirements"></a><span data-ttu-id="74531-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="74531-139">Requirements</span></span>



| <span data-ttu-id="74531-140">需求</span><span class="sxs-lookup"><span data-stu-id="74531-140">Requirement</span></span> | <span data-ttu-id="74531-141">值</span><span class="sxs-lookup"><span data-stu-id="74531-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74531-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74531-142">Minimum supported client</span></span><br/> | <span data-ttu-id="74531-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74531-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74531-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74531-144">Minimum supported server</span></span><br/> | <span data-ttu-id="74531-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74531-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74531-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="74531-146">Namespace</span></span><br/>                | <span data-ttu-id="74531-147">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74531-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="74531-148">MOF</span><span class="sxs-lookup"><span data-stu-id="74531-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74531-149"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="74531-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="74531-150">DLL</span><span class="sxs-lookup"><span data-stu-id="74531-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74531-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74531-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74531-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74531-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="74531-153">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74531-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="74531-154">**Win32 \_ 共用**</span><span class="sxs-lookup"><span data-stu-id="74531-154">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

