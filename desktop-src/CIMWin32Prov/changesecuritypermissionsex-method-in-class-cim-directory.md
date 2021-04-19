---
description: 變更物件路徑中指定之邏輯目錄專案檔的安全性許可權 (這個方法是 ChangeSecurityPermissions 方法的擴充版本，並且繼承自 CIM \_ LogicalFile) 。
ms.assetid: 5c1f66ba-9aa1-47ca-8fcf-7663782544cd
ms.tgt_platform: multiple
title: CIM_Directory 類別的 ChangeSecurityPermissionsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2d8ddf4c6ffdbd016db1e8c08d89f2dd6476ccf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973577"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_directory-class"></a><span data-ttu-id="ae995-103">CIM 目錄類別的 ChangeSecurityPermissionsEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ae995-103">ChangeSecurityPermissionsEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="ae995-104">**ChangeSecurityPermissionsEx** 方法會變更物件路徑中所指定之邏輯目錄專案檔的安全性許可權 (此方法是 [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md)方法的擴充版本，並且繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ae995-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md)).</span></span> <span data-ttu-id="ae995-105">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，以變更目錄所包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="ae995-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae995-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="ae995-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ae995-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="ae995-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ae995-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="ae995-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ae995-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="ae995-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae995-110">語法</span><span class="sxs-lookup"><span data-stu-id="ae995-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="ae995-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae995-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae995-112">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae995-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae995-113">指定安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="ae995-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="ae995-114">[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構中的 **Null** ACL 會授與無限制的存取權。</span><span class="sxs-lookup"><span data-stu-id="ae995-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="ae995-115">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae995-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae995-116">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="ae995-116">Security privilege to modify.</span></span> <span data-ttu-id="ae995-117">例如，若要變更擁有者和 DACL 安全性，請使用</span><span class="sxs-lookup"><span data-stu-id="ae995-117">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="ae995-118">或</span><span class="sxs-lookup"><span data-stu-id="ae995-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="ae995-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="ae995-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ae995-120">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="ae995-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="ae995-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="ae995-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ae995-122">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="ae995-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="ae995-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="ae995-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ae995-124">變更邏輯檔案的 ACL。</span><span class="sxs-lookup"><span data-stu-id="ae995-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="ae995-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="ae995-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ae995-126">變更邏輯檔案的系統 ACL。</span><span class="sxs-lookup"><span data-stu-id="ae995-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ae995-127">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ae995-127">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae995-128">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae995-128">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="ae995-129">如果方法成功，這個參數的值會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="ae995-129">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ae995-130">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ae995-130">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ae995-131">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ae995-131">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="ae995-132">一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ae995-132">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="ae995-133">如果參數值為 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="ae995-133">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="ae995-134">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ae995-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ae995-135">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ 目錄**](cim-directory.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="ae995-135">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="ae995-136">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="ae995-136">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae995-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae995-137">Return value</span></span>

<span data-ttu-id="ae995-138">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="ae995-138">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="ae995-139">0</span><span class="sxs-lookup"><span data-stu-id="ae995-139">0</span></span>

<span data-ttu-id="ae995-140">成功。</span><span class="sxs-lookup"><span data-stu-id="ae995-140">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-141">2</span><span class="sxs-lookup"><span data-stu-id="ae995-141">2</span></span>

<span data-ttu-id="ae995-142">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="ae995-142">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-143">8</span><span class="sxs-lookup"><span data-stu-id="ae995-143">8</span></span>

<span data-ttu-id="ae995-144">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="ae995-144">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-145">9</span><span class="sxs-lookup"><span data-stu-id="ae995-145">9</span></span>

<span data-ttu-id="ae995-146">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="ae995-146">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-147">10</span><span class="sxs-lookup"><span data-stu-id="ae995-147">10</span></span>

<span data-ttu-id="ae995-148">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="ae995-148">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-149">11</span><span class="sxs-lookup"><span data-stu-id="ae995-149">11</span></span>

<span data-ttu-id="ae995-150">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="ae995-150">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-151">12</span><span class="sxs-lookup"><span data-stu-id="ae995-151">12</span></span>

<span data-ttu-id="ae995-152">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="ae995-152">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-153">13</span><span class="sxs-lookup"><span data-stu-id="ae995-153">13</span></span>

<span data-ttu-id="ae995-154">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="ae995-154">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-155">14</span><span class="sxs-lookup"><span data-stu-id="ae995-155">14</span></span>

<span data-ttu-id="ae995-156">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="ae995-156">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-157">15</span><span class="sxs-lookup"><span data-stu-id="ae995-157">15</span></span>

<span data-ttu-id="ae995-158">共用違規。</span><span class="sxs-lookup"><span data-stu-id="ae995-158">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-159">16</span><span class="sxs-lookup"><span data-stu-id="ae995-159">16</span></span>

<span data-ttu-id="ae995-160">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="ae995-160">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-161">17</span><span class="sxs-lookup"><span data-stu-id="ae995-161">17</span></span>

<span data-ttu-id="ae995-162">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="ae995-162">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae995-163">21</span><span class="sxs-lookup"><span data-stu-id="ae995-163">21</span></span>

<span data-ttu-id="ae995-164">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="ae995-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae995-165">備註</span><span class="sxs-lookup"><span data-stu-id="ae995-165">Remarks</span></span>

<span data-ttu-id="ae995-166">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="ae995-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ae995-167">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="ae995-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ae995-168">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="ae995-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ae995-169">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ae995-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae995-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae995-170">Requirements</span></span>



| <span data-ttu-id="ae995-171">需求</span><span class="sxs-lookup"><span data-stu-id="ae995-171">Requirement</span></span> | <span data-ttu-id="ae995-172">值</span><span class="sxs-lookup"><span data-stu-id="ae995-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae995-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae995-173">Minimum supported client</span></span><br/> | <span data-ttu-id="ae995-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae995-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae995-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae995-175">Minimum supported server</span></span><br/> | <span data-ttu-id="ae995-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae995-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae995-177">命名空間</span><span class="sxs-lookup"><span data-stu-id="ae995-177">Namespace</span></span><br/>                | <span data-ttu-id="ae995-178">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ae995-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae995-179">MOF</span><span class="sxs-lookup"><span data-stu-id="ae995-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae995-180"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae995-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae995-181">DLL</span><span class="sxs-lookup"><span data-stu-id="ae995-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae995-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae995-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae995-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae995-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae995-184">CIM \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="ae995-184">CIM\_Directory</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="ae995-185">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="ae995-185">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

