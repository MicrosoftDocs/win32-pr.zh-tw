---
description: 允許變更組名。
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Win32_Group 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970705"
---
# <a name="rename-method-of-the-win32_group-class"></a><span data-ttu-id="27c00-103">Win32 群組類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="27c00-103">Rename method of the Win32\_Group class</span></span>

<span data-ttu-id="27c00-104">**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法允許變更組名。</span><span class="sxs-lookup"><span data-stu-id="27c00-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows the group name to be changed.</span></span>

<span data-ttu-id="27c00-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="27c00-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="27c00-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="27c00-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="27c00-107">語法</span><span class="sxs-lookup"><span data-stu-id="27c00-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="27c00-108">參數</span><span class="sxs-lookup"><span data-stu-id="27c00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c00-109">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27c00-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c00-110">此類別的 **domain** 屬性所指定之網域上的 Windows 使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="27c00-110">Name of the Windows user account on the domain specified by the **Domain** property of this class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c00-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="27c00-111">Return value</span></span>

<span data-ttu-id="27c00-112">**重新命名** 方法可以傳回下列清單所列的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="27c00-112">The **Rename** method can return the error codes listed in the following list.</span></span> <span data-ttu-id="27c00-113">針對未列出的整數值，請參閱 [WMI 傳回 \_ 碼](/windows/desktop/WmiSdk/wmi-return-codes)。</span><span class="sxs-lookup"><span data-stu-id="27c00-113">For integer values other than those listed, refer to [WMI\_Return Codes](/windows/desktop/WmiSdk/wmi-return-codes).</span></span>

<dl> <dt>

<span data-ttu-id="27c00-114">「成功」</span><span class="sxs-lookup"><span data-stu-id="27c00-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-115">0</span><span class="sxs-lookup"><span data-stu-id="27c00-115">0</span></span>

<span data-ttu-id="27c00-116">成功。</span><span class="sxs-lookup"><span data-stu-id="27c00-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="27c00-117">**找不到實例**</span><span class="sxs-lookup"><span data-stu-id="27c00-117">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-118">1</span><span class="sxs-lookup"><span data-stu-id="27c00-118">1</span></span>

</dd> <dt>

<span data-ttu-id="27c00-119">**需要的實例**</span><span class="sxs-lookup"><span data-stu-id="27c00-119">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-120">2</span><span class="sxs-lookup"><span data-stu-id="27c00-120">2</span></span>

</dd> <dt>

<span data-ttu-id="27c00-121">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="27c00-121">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-122">3</span><span class="sxs-lookup"><span data-stu-id="27c00-122">3</span></span>

</dd> <dt>

<span data-ttu-id="27c00-123">**找不到群組**</span><span class="sxs-lookup"><span data-stu-id="27c00-123">**Group not found**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-124">4</span><span class="sxs-lookup"><span data-stu-id="27c00-124">4</span></span>

</dd> <dt>

<span data-ttu-id="27c00-125">**找不到網域**</span><span class="sxs-lookup"><span data-stu-id="27c00-125">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-126">5</span><span class="sxs-lookup"><span data-stu-id="27c00-126">5</span></span>

</dd> <dt>

<span data-ttu-id="27c00-127">**只允許在網域的主域控制站上執行操作**</span><span class="sxs-lookup"><span data-stu-id="27c00-127">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-128">6</span><span class="sxs-lookup"><span data-stu-id="27c00-128">6</span></span>

</dd> <dt>

<span data-ttu-id="27c00-129">**在指定的特殊群組上不允許操作;user、admin、local 或 guest。**</span><span class="sxs-lookup"><span data-stu-id="27c00-129">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-130">7</span><span class="sxs-lookup"><span data-stu-id="27c00-130">7</span></span>

</dd> <dt>

<span data-ttu-id="27c00-131">**其他 API 錯誤**</span><span class="sxs-lookup"><span data-stu-id="27c00-131">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-132">8</span><span class="sxs-lookup"><span data-stu-id="27c00-132">8</span></span>

</dd> <dt>

<span data-ttu-id="27c00-133">**內部錯誤**</span><span class="sxs-lookup"><span data-stu-id="27c00-133">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="27c00-134">9</span><span class="sxs-lookup"><span data-stu-id="27c00-134">9</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27c00-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="27c00-135">Requirements</span></span>



| <span data-ttu-id="27c00-136">需求</span><span class="sxs-lookup"><span data-stu-id="27c00-136">Requirement</span></span> | <span data-ttu-id="27c00-137">值</span><span class="sxs-lookup"><span data-stu-id="27c00-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27c00-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27c00-138">Minimum supported client</span></span><br/> | <span data-ttu-id="27c00-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27c00-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27c00-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27c00-140">Minimum supported server</span></span><br/> | <span data-ttu-id="27c00-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27c00-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27c00-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="27c00-142">Namespace</span></span><br/>                | <span data-ttu-id="27c00-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="27c00-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27c00-144">MOF</span><span class="sxs-lookup"><span data-stu-id="27c00-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27c00-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="27c00-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27c00-146">DLL</span><span class="sxs-lookup"><span data-stu-id="27c00-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27c00-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27c00-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c00-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27c00-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="27c00-149">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="27c00-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="27c00-150">**Win32 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="27c00-150">**Win32\_Group**</span></span>](win32-group.md)
</dt> <dt>

[<span data-ttu-id="27c00-151">**Win32 \_ LogicalFileSecuritySetting**</span><span class="sxs-lookup"><span data-stu-id="27c00-151">**Win32\_LogicalFileSecuritySetting**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

