---
description: 變更物件路徑中指定之邏輯檔案的安全性許可權。
ms.assetid: a3caa717-ad37-4e4f-9f4e-f37aed382fa4
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 ChangeSecurityPermissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 929e05047af203d8e2344afa8175228e3bd969fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972344"
---
# <a name="changesecuritypermissions-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="1b3e4-103">CIM LogicalFile 類別的 ChangeSecurityPermissions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1b3e4-103">ChangeSecurityPermissions method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="1b3e4-104">**ChangeSecurityPermissions** 方法會變更物件路徑中所指定之邏輯檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="1b3e4-105">如果邏輯檔案是目錄，則 **ChangeSecurityPermissions** 將會以遞迴方式運作，變更目錄包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-105">If the logical file is a directory, then **ChangeSecurityPermissions** will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b3e4-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1b3e4-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1b3e4-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1b3e4-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b3e4-110">語法</span><span class="sxs-lookup"><span data-stu-id="1b3e4-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="1b3e4-111">參數</span><span class="sxs-lookup"><span data-stu-id="1b3e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b3e4-112">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b3e4-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-113">指定安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="1b3e4-114">在 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)中 (ACL) 的 **Null** 存取控制清單會授與無限制的存取權。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-114">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b3e4-115">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b3e4-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-116">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-116">Security privilege to modify.</span></span> <span data-ttu-id="1b3e4-117">例如，若要變更擁有者和 DACL 安全性，請使用：</span><span class="sxs-lookup"><span data-stu-id="1b3e4-117">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="1b3e4-118">或</span><span class="sxs-lookup"><span data-stu-id="1b3e4-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="1b3e4-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="1b3e4-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1b3e4-120">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="1b3e4-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="1b3e4-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1b3e4-122">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="1b3e4-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**變更 \_Dacl \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="1b3e4-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1b3e4-124">變更邏輯檔案的 ACL。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="1b3e4-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**變更 \_Sacl \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="1b3e4-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1b3e4-126">變更邏輯檔案的系統 ACL。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b3e4-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b3e4-127">Return value</span></span>

<span data-ttu-id="1b3e4-128">在成功時傳回0的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-128">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1b3e4-129">「成功」</span><span class="sxs-lookup"><span data-stu-id="1b3e4-129">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-130">0</span><span class="sxs-lookup"><span data-stu-id="1b3e4-130">0</span></span>

<span data-ttu-id="1b3e4-131">成功。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-131">Success.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-132">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-133">2</span><span class="sxs-lookup"><span data-stu-id="1b3e4-133">2</span></span>

<span data-ttu-id="1b3e4-134">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-134">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-135">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-135">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-136">8</span><span class="sxs-lookup"><span data-stu-id="1b3e4-136">8</span></span>

<span data-ttu-id="1b3e4-137">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-137">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-138">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-138">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-139">9</span><span class="sxs-lookup"><span data-stu-id="1b3e4-139">9</span></span>

<span data-ttu-id="1b3e4-140">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-140">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-141">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-141">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-142">10</span><span class="sxs-lookup"><span data-stu-id="1b3e4-142">10</span></span>

<span data-ttu-id="1b3e4-143">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-143">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-144">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-144">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-145">11</span><span class="sxs-lookup"><span data-stu-id="1b3e4-145">11</span></span>

<span data-ttu-id="1b3e4-146">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-146">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-147">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-147">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-148">12</span><span class="sxs-lookup"><span data-stu-id="1b3e4-148">12</span></span>

<span data-ttu-id="1b3e4-149">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-149">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-150">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-150">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-151">13</span><span class="sxs-lookup"><span data-stu-id="1b3e4-151">13</span></span>

<span data-ttu-id="1b3e4-152">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-152">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-153">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-153">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-154">14</span><span class="sxs-lookup"><span data-stu-id="1b3e4-154">14</span></span>

<span data-ttu-id="1b3e4-155">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-155">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-156">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-156">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-157">15</span><span class="sxs-lookup"><span data-stu-id="1b3e4-157">15</span></span>

<span data-ttu-id="1b3e4-158">共用違規。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-158">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-159">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-159">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-160">16</span><span class="sxs-lookup"><span data-stu-id="1b3e4-160">16</span></span>

<span data-ttu-id="1b3e4-161">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-161">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-162">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-162">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-163">17</span><span class="sxs-lookup"><span data-stu-id="1b3e4-163">17</span></span>

<span data-ttu-id="1b3e4-164">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-164">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="1b3e4-165">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-165">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1b3e4-166">21</span><span class="sxs-lookup"><span data-stu-id="1b3e4-166">21</span></span>

<span data-ttu-id="1b3e4-167">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-167">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b3e4-168">備註</span><span class="sxs-lookup"><span data-stu-id="1b3e4-168">Remarks</span></span>

<span data-ttu-id="1b3e4-169">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-169">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1b3e4-170">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-170">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1b3e4-171">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1b3e4-172">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1b3e4-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b3e4-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b3e4-173">Requirements</span></span>



| <span data-ttu-id="1b3e4-174">需求</span><span class="sxs-lookup"><span data-stu-id="1b3e4-174">Requirement</span></span> | <span data-ttu-id="1b3e4-175">值</span><span class="sxs-lookup"><span data-stu-id="1b3e4-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b3e4-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b3e4-176">Minimum supported client</span></span><br/> | <span data-ttu-id="1b3e4-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b3e4-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b3e4-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b3e4-178">Minimum supported server</span></span><br/> | <span data-ttu-id="1b3e4-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b3e4-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b3e4-180">命名空間</span><span class="sxs-lookup"><span data-stu-id="1b3e4-180">Namespace</span></span><br/>                | <span data-ttu-id="1b3e4-181">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1b3e4-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b3e4-182">MOF</span><span class="sxs-lookup"><span data-stu-id="1b3e4-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b3e4-183"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b3e4-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b3e4-184">DLL</span><span class="sxs-lookup"><span data-stu-id="1b3e4-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b3e4-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b3e4-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b3e4-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b3e4-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b3e4-187">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-187">**CIM\_LogicalFile**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="1b3e4-188">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="1b3e4-188">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

