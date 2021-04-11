---
description: 變更物件路徑中指定之裝置檔案的安全性許可權 (這個方法是) 的延伸版本 ChangeSecurityPermissions 方法。
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: CIM_DeviceFile 類別的 ChangeSecurityPermissionsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f2c7261844542f6414052517432c2e8ff3f1194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110973"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="0d2b1-103">CIM DeviceFile 類別的 ChangeSecurityPermissionsEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0d2b1-103">ChangeSecurityPermissionsEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="0d2b1-104">**ChangeSecurityPermissionsEx** 方法會變更物件路徑中所指定之裝置檔案的安全性許可權， (這個方法是 [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md)方法的擴充版本) 。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the device file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) method).</span></span> <span data-ttu-id="0d2b1-105">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，變更目錄所包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-105">If the logical file is a directory, then this method acts recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="0d2b1-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d2b1-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0d2b1-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0d2b1-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0d2b1-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d2b1-111">語法</span><span class="sxs-lookup"><span data-stu-id="0d2b1-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0d2b1-112">參數</span><span class="sxs-lookup"><span data-stu-id="0d2b1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d2b1-113">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d2b1-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2b1-114">指定安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="0d2b1-115">[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構中的 **Null** ACL 會授與無限制的存取權。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-115">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="0d2b1-116">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d2b1-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2b1-117">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-117">Security privilege to modify.</span></span> <span data-ttu-id="0d2b1-118">例如，若要變更擁有者和 DACL 安全性，請使用</span><span class="sxs-lookup"><span data-stu-id="0d2b1-118">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="0d2b1-119">或</span><span class="sxs-lookup"><span data-stu-id="0d2b1-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="0d2b1-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="0d2b1-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0d2b1-121">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="0d2b1-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="0d2b1-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0d2b1-123">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="0d2b1-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="0d2b1-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0d2b1-125">變更邏輯檔案的 ACL。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="0d2b1-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="0d2b1-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0d2b1-127">變更邏輯檔案的系統 ACL。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0d2b1-128">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0d2b1-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2b1-129">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="0d2b1-130">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0d2b1-131">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0d2b1-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2b1-132">要做為這個方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-132">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="0d2b1-133">一般而言， *StartFileName* 參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0d2b1-134">如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="0d2b1-135">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0d2b1-135">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2b1-136">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ DeviceFile**](cim-devicefile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-136">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="0d2b1-137">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-137">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d2b1-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d2b1-138">Return value</span></span>

<span data-ttu-id="0d2b1-139">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-139">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-140">0</span><span class="sxs-lookup"><span data-stu-id="0d2b1-140">0</span></span>

<span data-ttu-id="0d2b1-141">成功。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-141">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-142">2</span><span class="sxs-lookup"><span data-stu-id="0d2b1-142">2</span></span>

<span data-ttu-id="0d2b1-143">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-143">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-144">8</span><span class="sxs-lookup"><span data-stu-id="0d2b1-144">8</span></span>

<span data-ttu-id="0d2b1-145">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-145">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-146">9</span><span class="sxs-lookup"><span data-stu-id="0d2b1-146">9</span></span>

<span data-ttu-id="0d2b1-147">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-147">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-148">10</span><span class="sxs-lookup"><span data-stu-id="0d2b1-148">10</span></span>

<span data-ttu-id="0d2b1-149">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-149">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-150">11</span><span class="sxs-lookup"><span data-stu-id="0d2b1-150">11</span></span>

<span data-ttu-id="0d2b1-151">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-151">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-152">12</span><span class="sxs-lookup"><span data-stu-id="0d2b1-152">12</span></span>

<span data-ttu-id="0d2b1-153">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-153">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-154">13</span><span class="sxs-lookup"><span data-stu-id="0d2b1-154">13</span></span>

<span data-ttu-id="0d2b1-155">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-155">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-156">14</span><span class="sxs-lookup"><span data-stu-id="0d2b1-156">14</span></span>

<span data-ttu-id="0d2b1-157">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-157">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-158">15</span><span class="sxs-lookup"><span data-stu-id="0d2b1-158">15</span></span>

<span data-ttu-id="0d2b1-159">共用違規。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-159">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-160">16</span><span class="sxs-lookup"><span data-stu-id="0d2b1-160">16</span></span>

<span data-ttu-id="0d2b1-161">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-161">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-162">17</span><span class="sxs-lookup"><span data-stu-id="0d2b1-162">17</span></span>

<span data-ttu-id="0d2b1-163">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-163">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d2b1-164">21</span><span class="sxs-lookup"><span data-stu-id="0d2b1-164">21</span></span>

<span data-ttu-id="0d2b1-165">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-165">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d2b1-166">備註</span><span class="sxs-lookup"><span data-stu-id="0d2b1-166">Remarks</span></span>

<span data-ttu-id="0d2b1-167">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-167">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0d2b1-168">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-168">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0d2b1-169">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0d2b1-170">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0d2b1-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d2b1-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d2b1-171">Requirements</span></span>



| <span data-ttu-id="0d2b1-172">需求</span><span class="sxs-lookup"><span data-stu-id="0d2b1-172">Requirement</span></span> | <span data-ttu-id="0d2b1-173">值</span><span class="sxs-lookup"><span data-stu-id="0d2b1-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2b1-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d2b1-174">Minimum supported client</span></span><br/> | <span data-ttu-id="0d2b1-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d2b1-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d2b1-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d2b1-176">Minimum supported server</span></span><br/> | <span data-ttu-id="0d2b1-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d2b1-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d2b1-178">命名空間</span><span class="sxs-lookup"><span data-stu-id="0d2b1-178">Namespace</span></span><br/>                | <span data-ttu-id="0d2b1-179">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d2b1-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d2b1-180">MOF</span><span class="sxs-lookup"><span data-stu-id="0d2b1-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d2b1-181"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d2b1-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d2b1-182">DLL</span><span class="sxs-lookup"><span data-stu-id="0d2b1-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d2b1-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d2b1-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d2b1-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d2b1-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d2b1-185">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="0d2b1-185">CIM\_DeviceFile</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="0d2b1-186">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="0d2b1-186">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

