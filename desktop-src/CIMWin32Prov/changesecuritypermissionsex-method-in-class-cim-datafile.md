---
description: 變更物件路徑中指定之邏輯資料檔案的安全性許可權 (這個方法是) 的 ChangeSecurityPermissions 方法擴充版本。
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 ChangeSecurityPermissionsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c97f9b17fd148a0686a96fb46f77694a2b78b21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510610"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a><span data-ttu-id="93774-103">CIM \_ 資料檔案類別的 ChangeSecurityPermissionsEx 方法</span><span class="sxs-lookup"><span data-stu-id="93774-103">ChangeSecurityPermissionsEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="93774-104">**ChangeSecurityPermissionsEx** 方法會變更物件路徑中所指定之邏輯資料檔案的安全性許可權 (這個方法是 [**) 的擴充**](changesecuritypermissions-method-in-class-cim-datafile.md)版本。</span><span class="sxs-lookup"><span data-stu-id="93774-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical data file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) method).</span></span> <span data-ttu-id="93774-105">如果邏輯檔案實際上是目錄，則這個方法會以遞迴方式運作，變更目錄包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="93774-105">If the logical file is actually a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93774-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="93774-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="93774-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="93774-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="93774-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="93774-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="93774-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="93774-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="93774-110">語法</span><span class="sxs-lookup"><span data-stu-id="93774-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="93774-111">參數</span><span class="sxs-lookup"><span data-stu-id="93774-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93774-112">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93774-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93774-113">指定安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="93774-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="93774-114">[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構中的 **Null** ACL 會授與無限制的存取權。</span><span class="sxs-lookup"><span data-stu-id="93774-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="93774-115">如需無限制存取含意的詳細資訊，請參閱 [建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="93774-115">For more information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="93774-116">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93774-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93774-117">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="93774-117">Security privilege to modify.</span></span> <span data-ttu-id="93774-118">例如，若要變更擁有者和 DACL 安全性，請使用：</span><span class="sxs-lookup"><span data-stu-id="93774-118">For example, to change the owner and DACL security, use:</span></span>

<span data-ttu-id="93774-119">`Option = 1 + 4` 或 `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span><span class="sxs-lookup"><span data-stu-id="93774-119">`Option = 1 + 4` or `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span></span>

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="93774-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="93774-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="93774-121">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="93774-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="93774-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="93774-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="93774-123">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="93774-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="93774-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="93774-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93774-125">變更邏輯檔案的 ACL。</span><span class="sxs-lookup"><span data-stu-id="93774-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="93774-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="93774-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="93774-127">變更邏輯檔案的系統 ACL。</span><span class="sxs-lookup"><span data-stu-id="93774-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="93774-128">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93774-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93774-129">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="93774-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="93774-130">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="93774-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="93774-131">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="93774-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93774-132">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="93774-132">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="93774-133">一般而言， *StartFileName* 參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="93774-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="93774-134">如果這個參數是 **null**，則會在 **ExecMethod** 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="93774-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="93774-135">如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="93774-135">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="93774-136">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="93774-136">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93774-137">若 **為 True**，則此方法也會以遞迴方式套用至 [**CIM \_ 資料檔案**](cim-datafile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="93774-137">If **True**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="93774-138">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="93774-138">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93774-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="93774-139">Return value</span></span>

<span data-ttu-id="93774-140">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="93774-140">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="93774-141">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="93774-141">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="93774-142">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="93774-142">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="93774-143">「成功」</span><span class="sxs-lookup"><span data-stu-id="93774-143">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="93774-144">0</span><span class="sxs-lookup"><span data-stu-id="93774-144">0</span></span>

<span data-ttu-id="93774-145">成功。</span><span class="sxs-lookup"><span data-stu-id="93774-145">Success.</span></span>

</dd> <dt>

<span data-ttu-id="93774-146">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="93774-146">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="93774-147">2</span><span class="sxs-lookup"><span data-stu-id="93774-147">2</span></span>

<span data-ttu-id="93774-148">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="93774-148">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="93774-149">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="93774-149">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="93774-150">8</span><span class="sxs-lookup"><span data-stu-id="93774-150">8</span></span>

<span data-ttu-id="93774-151">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="93774-151">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="93774-152">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="93774-152">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="93774-153">9</span><span class="sxs-lookup"><span data-stu-id="93774-153">9</span></span>

<span data-ttu-id="93774-154">指定的物件名稱無效。</span><span class="sxs-lookup"><span data-stu-id="93774-154">Object name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="93774-155">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="93774-155">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="93774-156">10</span><span class="sxs-lookup"><span data-stu-id="93774-156">10</span></span>

<span data-ttu-id="93774-157">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="93774-157">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="93774-158">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="93774-158">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="93774-159">11</span><span class="sxs-lookup"><span data-stu-id="93774-159">11</span></span>

<span data-ttu-id="93774-160">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="93774-160">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="93774-161">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="93774-161">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="93774-162">12</span><span class="sxs-lookup"><span data-stu-id="93774-162">12</span></span>

<span data-ttu-id="93774-163">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="93774-163">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="93774-164">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="93774-164">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="93774-165">13</span><span class="sxs-lookup"><span data-stu-id="93774-165">13</span></span>

<span data-ttu-id="93774-166">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="93774-166">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="93774-167">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="93774-167">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="93774-168">14</span><span class="sxs-lookup"><span data-stu-id="93774-168">14</span></span>

<span data-ttu-id="93774-169">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="93774-169">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="93774-170">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="93774-170">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="93774-171">15</span><span class="sxs-lookup"><span data-stu-id="93774-171">15</span></span>

<span data-ttu-id="93774-172">共用違規。</span><span class="sxs-lookup"><span data-stu-id="93774-172">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="93774-173">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="93774-173">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="93774-174">16</span><span class="sxs-lookup"><span data-stu-id="93774-174">16</span></span>

<span data-ttu-id="93774-175">起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="93774-175">The start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="93774-176">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="93774-176">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="93774-177">17</span><span class="sxs-lookup"><span data-stu-id="93774-177">17</span></span>

<span data-ttu-id="93774-178">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="93774-178">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="93774-179">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="93774-179">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="93774-180">21</span><span class="sxs-lookup"><span data-stu-id="93774-180">21</span></span>

<span data-ttu-id="93774-181">參數無效。</span><span class="sxs-lookup"><span data-stu-id="93774-181">A parameter is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93774-182">備註</span><span class="sxs-lookup"><span data-stu-id="93774-182">Remarks</span></span>

<span data-ttu-id="93774-183">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **CHANGESECURITYPERMISSIONSEX** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="93774-183">The **ChangeSecurityPermissionsEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="93774-184">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="93774-184">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="93774-185">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="93774-185">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="93774-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="93774-186">Requirements</span></span>



| <span data-ttu-id="93774-187">需求</span><span class="sxs-lookup"><span data-stu-id="93774-187">Requirement</span></span> | <span data-ttu-id="93774-188">值</span><span class="sxs-lookup"><span data-stu-id="93774-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93774-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93774-189">Minimum supported client</span></span><br/> | <span data-ttu-id="93774-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93774-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93774-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93774-191">Minimum supported server</span></span><br/> | <span data-ttu-id="93774-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93774-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93774-193">命名空間</span><span class="sxs-lookup"><span data-stu-id="93774-193">Namespace</span></span><br/>                | <span data-ttu-id="93774-194">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="93774-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93774-195">MOF</span><span class="sxs-lookup"><span data-stu-id="93774-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93774-196"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="93774-196"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93774-197">DLL</span><span class="sxs-lookup"><span data-stu-id="93774-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93774-198"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93774-198"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93774-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93774-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93774-200">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="93774-200">**CIM\_DataFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="93774-201">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="93774-201">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="93774-202">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="93774-202">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="93774-203">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="93774-203">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

