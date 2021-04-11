---
description: 變更物件路徑中所指定之邏輯資料檔案的安全性許可權。
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 ChangeSecurityPermissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111005"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a><span data-ttu-id="e3014-103">CIM \_ 資料檔案類別的 ChangeSecurityPermissions 方法</span><span class="sxs-lookup"><span data-stu-id="e3014-103">ChangeSecurityPermissions method of the CIM\_DataFile class</span></span>

<span data-ttu-id="e3014-104">**ChangeSecurityPermissions** 方法會變更物件路徑中所指定之邏輯資料檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="e3014-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical data file specified in the object path.</span></span> <span data-ttu-id="e3014-105">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，以變更目錄所包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="e3014-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="e3014-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="e3014-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3014-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e3014-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e3014-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e3014-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e3014-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="e3014-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e3014-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="e3014-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3014-111">語法</span><span class="sxs-lookup"><span data-stu-id="e3014-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="e3014-112">參數</span><span class="sxs-lookup"><span data-stu-id="e3014-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3014-113">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3014-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3014-114">指定安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="e3014-114">Specifies the security information.</span></span>

> [!Note]  
> <span data-ttu-id="e3014-115">在 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構中 (ACL) 的 **Null** 存取控制清單會授與無限制的存取權。</span><span class="sxs-lookup"><span data-stu-id="e3014-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="e3014-116">如需無限制存取之含意的詳細資訊，請參閱 [建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="e3014-116">For information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="e3014-117">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3014-117">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3014-118">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="e3014-118">Security privilege to modify.</span></span> <span data-ttu-id="e3014-119">例如，若要變更擁有者和 DACL 安全性，請使用：</span><span class="sxs-lookup"><span data-stu-id="e3014-119">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="e3014-120">或</span><span class="sxs-lookup"><span data-stu-id="e3014-120">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="e3014-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="e3014-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e3014-122">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="e3014-122">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="e3014-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="e3014-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e3014-124">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="e3014-124">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="e3014-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="e3014-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e3014-126">變更邏輯檔案的 ACL。</span><span class="sxs-lookup"><span data-stu-id="e3014-126">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="e3014-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="e3014-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e3014-128">變更邏輯檔案的系統 ACL。</span><span class="sxs-lookup"><span data-stu-id="e3014-128">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3014-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3014-129">Return value</span></span>

<span data-ttu-id="e3014-130">在成功時傳回0的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3014-130">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="e3014-131">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="e3014-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e3014-132">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="e3014-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e3014-133">「成功」</span><span class="sxs-lookup"><span data-stu-id="e3014-133">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-134">0</span><span class="sxs-lookup"><span data-stu-id="e3014-134">0</span></span>

<span data-ttu-id="e3014-135">成功。</span><span class="sxs-lookup"><span data-stu-id="e3014-135">Success.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-136">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="e3014-136">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-137">2</span><span class="sxs-lookup"><span data-stu-id="e3014-137">2</span></span>

<span data-ttu-id="e3014-138">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="e3014-138">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-139">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="e3014-139">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-140">8</span><span class="sxs-lookup"><span data-stu-id="e3014-140">8</span></span>

<span data-ttu-id="e3014-141">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="e3014-141">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-142">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="e3014-142">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-143">9</span><span class="sxs-lookup"><span data-stu-id="e3014-143">9</span></span>

<span data-ttu-id="e3014-144">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="e3014-144">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-145">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="e3014-145">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-146">10</span><span class="sxs-lookup"><span data-stu-id="e3014-146">10</span></span>

<span data-ttu-id="e3014-147">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="e3014-147">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-148">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="e3014-148">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-149">11</span><span class="sxs-lookup"><span data-stu-id="e3014-149">11</span></span>

</dd> <dt>

<span data-ttu-id="e3014-150">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="e3014-150">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-151">12</span><span class="sxs-lookup"><span data-stu-id="e3014-151">12</span></span>

<span data-ttu-id="e3014-152">平臺不是以 Windows NT 為基礎。</span><span class="sxs-lookup"><span data-stu-id="e3014-152">Platform not Windows NT-based.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-153">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="e3014-153">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-154">13</span><span class="sxs-lookup"><span data-stu-id="e3014-154">13</span></span>

<span data-ttu-id="e3014-155">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="e3014-155">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-156">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="e3014-156">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-157">14</span><span class="sxs-lookup"><span data-stu-id="e3014-157">14</span></span>

<span data-ttu-id="e3014-158">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="e3014-158">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-159">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="e3014-159">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-160">15</span><span class="sxs-lookup"><span data-stu-id="e3014-160">15</span></span>

<span data-ttu-id="e3014-161">共用違規。</span><span class="sxs-lookup"><span data-stu-id="e3014-161">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-162">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="e3014-162">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-163">16</span><span class="sxs-lookup"><span data-stu-id="e3014-163">16</span></span>

<span data-ttu-id="e3014-164">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="e3014-164">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-165">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="e3014-165">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-166">17</span><span class="sxs-lookup"><span data-stu-id="e3014-166">17</span></span>

<span data-ttu-id="e3014-167">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="e3014-167">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="e3014-168">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="e3014-168">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e3014-169">21</span><span class="sxs-lookup"><span data-stu-id="e3014-169">21</span></span>

<span data-ttu-id="e3014-170">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="e3014-170">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3014-171">備註</span><span class="sxs-lookup"><span data-stu-id="e3014-171">Remarks</span></span>

<span data-ttu-id="e3014-172">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **CHANGESECURITYPERMISSIONS** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="e3014-172">The **ChangeSecurityPermissions** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="e3014-173">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e3014-173">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e3014-174">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e3014-174">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3014-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3014-175">Requirements</span></span>



| <span data-ttu-id="e3014-176">需求</span><span class="sxs-lookup"><span data-stu-id="e3014-176">Requirement</span></span> | <span data-ttu-id="e3014-177">值</span><span class="sxs-lookup"><span data-stu-id="e3014-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3014-178">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3014-178">Minimum supported client</span></span><br/> | <span data-ttu-id="e3014-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3014-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3014-180">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3014-180">Minimum supported server</span></span><br/> | <span data-ttu-id="e3014-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3014-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3014-182">命名空間</span><span class="sxs-lookup"><span data-stu-id="e3014-182">Namespace</span></span><br/>                | <span data-ttu-id="e3014-183">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e3014-183">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e3014-184">MOF</span><span class="sxs-lookup"><span data-stu-id="e3014-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3014-185"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3014-185"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3014-186">DLL</span><span class="sxs-lookup"><span data-stu-id="e3014-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3014-187"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3014-187"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3014-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3014-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3014-189">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="e3014-189">**CIM\_DataFile**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="e3014-190">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="e3014-190">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="e3014-191">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="e3014-191">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="e3014-192">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="e3014-192">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

