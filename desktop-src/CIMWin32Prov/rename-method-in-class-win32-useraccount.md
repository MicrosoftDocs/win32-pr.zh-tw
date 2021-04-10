---
description: 重新命名使用者帳戶名稱。
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Win32_UserAccount 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111248"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a><span data-ttu-id="c4264-103">Win32 UserAccount 類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="c4264-103">Rename method of the Win32\_UserAccount class</span></span>

<span data-ttu-id="c4264-104">**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會重新命名使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c4264-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a user account name.</span></span>

<span data-ttu-id="c4264-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="c4264-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c4264-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="c4264-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4264-107">語法</span><span class="sxs-lookup"><span data-stu-id="c4264-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="c4264-108">參數</span><span class="sxs-lookup"><span data-stu-id="c4264-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4264-109">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4264-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4264-110">新的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c4264-110">New account name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4264-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4264-111">Return value</span></span>

<span data-ttu-id="c4264-112">傳回下列清單所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c4264-112">Returns one of the values listed in the following list.</span></span> <span data-ttu-id="c4264-113">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="c4264-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c4264-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="c4264-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c4264-115">「成功」</span><span class="sxs-lookup"><span data-stu-id="c4264-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-116">0</span><span class="sxs-lookup"><span data-stu-id="c4264-116">0</span></span>

<span data-ttu-id="c4264-117">成功。</span><span class="sxs-lookup"><span data-stu-id="c4264-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c4264-118">**找不到實例**</span><span class="sxs-lookup"><span data-stu-id="c4264-118">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-119">1</span><span class="sxs-lookup"><span data-stu-id="c4264-119">1</span></span>

<span data-ttu-id="c4264-120">找不到實例。</span><span class="sxs-lookup"><span data-stu-id="c4264-120">Instance not found.</span></span>

</dd> <dt>

<span data-ttu-id="c4264-121">**需要的實例**</span><span class="sxs-lookup"><span data-stu-id="c4264-121">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-122">2</span><span class="sxs-lookup"><span data-stu-id="c4264-122">2</span></span>

<span data-ttu-id="c4264-123">需要實例。</span><span class="sxs-lookup"><span data-stu-id="c4264-123">Instance required.</span></span>

</dd> <dt>

<span data-ttu-id="c4264-124">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="c4264-124">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-125">3</span><span class="sxs-lookup"><span data-stu-id="c4264-125">3</span></span>

<span data-ttu-id="c4264-126">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="c4264-126">Invalid parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c4264-127">**找不到使用者**</span><span class="sxs-lookup"><span data-stu-id="c4264-127">**User not found**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-128">4</span><span class="sxs-lookup"><span data-stu-id="c4264-128">4</span></span>

<span data-ttu-id="c4264-129">找不到使用者。</span><span class="sxs-lookup"><span data-stu-id="c4264-129">User not found.</span></span>

</dd> <dt>

<span data-ttu-id="c4264-130">**找不到網域**</span><span class="sxs-lookup"><span data-stu-id="c4264-130">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-131">5</span><span class="sxs-lookup"><span data-stu-id="c4264-131">5</span></span>

<span data-ttu-id="c4264-132">找不到網域。</span><span class="sxs-lookup"><span data-stu-id="c4264-132">Domain not found.</span></span>

</dd> <dt>

<span data-ttu-id="c4264-133">**只允許在網域的主域控制站上執行操作**</span><span class="sxs-lookup"><span data-stu-id="c4264-133">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-134">6</span><span class="sxs-lookup"><span data-stu-id="c4264-134">6</span></span>

<span data-ttu-id="c4264-135">只允許在網域的主域控制站上執行操作。</span><span class="sxs-lookup"><span data-stu-id="c4264-135">Operation is allowed only on the primary domain controller of the domain.</span></span>

</dd> <dt>

<span data-ttu-id="c4264-136">**最後一個系統管理帳戶上不允許操作。**</span><span class="sxs-lookup"><span data-stu-id="c4264-136">**Operation is not allowed on the last administrative account.**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-137">7</span><span class="sxs-lookup"><span data-stu-id="c4264-137">7</span></span>

</dd> <dt>

<span data-ttu-id="c4264-138">**在指定的特殊群組上不允許操作;user、admin、local 或 guest。**</span><span class="sxs-lookup"><span data-stu-id="c4264-138">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-139">8</span><span class="sxs-lookup"><span data-stu-id="c4264-139">8</span></span>

<span data-ttu-id="c4264-140">在指定的特殊群組上不允許操作： user、admin、local 或 guest。</span><span class="sxs-lookup"><span data-stu-id="c4264-140">Operation is not allowed on specified special groups: user, admin, local, or guest.</span></span>

</dd> <dt>

<span data-ttu-id="c4264-141">**其他 API 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c4264-141">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-142">9</span><span class="sxs-lookup"><span data-stu-id="c4264-142">9</span></span>

<span data-ttu-id="c4264-143">其他 API 錯誤。</span><span class="sxs-lookup"><span data-stu-id="c4264-143">Other API error.</span></span>

</dd> <dt>

<span data-ttu-id="c4264-144">**內部錯誤**</span><span class="sxs-lookup"><span data-stu-id="c4264-144">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="c4264-145">10</span><span class="sxs-lookup"><span data-stu-id="c4264-145">10</span></span>

<span data-ttu-id="c4264-146">內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="c4264-146">Internal error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4264-147">備註</span><span class="sxs-lookup"><span data-stu-id="c4264-147">Remarks</span></span>

<span data-ttu-id="c4264-148">這項功能會實作為一種方法，為新名稱提供不同的內容，而此名稱與要修改之實例相關聯之名稱的索引鍵屬性值可區別。</span><span class="sxs-lookup"><span data-stu-id="c4264-148">This functionality is implemented as a method to provide a separate context for the new name that is distinguishable from the key property value for Name that is associated with the instance to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4264-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4264-149">Requirements</span></span>



| <span data-ttu-id="c4264-150">需求</span><span class="sxs-lookup"><span data-stu-id="c4264-150">Requirement</span></span> | <span data-ttu-id="c4264-151">值</span><span class="sxs-lookup"><span data-stu-id="c4264-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4264-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4264-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c4264-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4264-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4264-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4264-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c4264-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4264-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4264-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="c4264-156">Namespace</span></span><br/>                | <span data-ttu-id="c4264-157">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c4264-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c4264-158">MOF</span><span class="sxs-lookup"><span data-stu-id="c4264-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4264-159"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4264-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4264-160">DLL</span><span class="sxs-lookup"><span data-stu-id="c4264-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4264-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4264-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4264-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4264-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4264-163">**Win32 \_ UserAccount**</span><span class="sxs-lookup"><span data-stu-id="c4264-163">**Win32\_UserAccount**</span></span>](win32-useraccount.md)
</dt> <dt>

<span data-ttu-id="c4264-164">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4264-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

