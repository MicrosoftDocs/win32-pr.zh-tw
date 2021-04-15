---
description: 變更物件路徑中指定之邏輯裝置檔案的安全性許可權。
ms.assetid: 4b3e1a0e-3c9e-45bb-8c7b-cbbc8f9d1265
ms.tgt_platform: multiple
title: CIM_DeviceFile 類別的 ChangeSecurityPermissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a772c17695a537e4a9a8518bf05b052c0417f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468365"
---
# <a name="changesecuritypermissions-method-of-the-cim_devicefile-class"></a><span data-ttu-id="8fbe1-103">CIM DeviceFile 類別的 ChangeSecurityPermissions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8fbe1-103">ChangeSecurityPermissions method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="8fbe1-104">**ChangeSecurityPermissions** 方法會變更物件路徑中指定之邏輯裝置檔案的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical device file specified in the object path.</span></span> <span data-ttu-id="8fbe1-105">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，以變更目錄所包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="8fbe1-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fbe1-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8fbe1-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8fbe1-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8fbe1-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbe1-111">語法</span><span class="sxs-lookup"><span data-stu-id="8fbe1-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="8fbe1-112">參數</span><span class="sxs-lookup"><span data-stu-id="8fbe1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fbe1-113">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fbe1-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-114">指定安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="8fbe1-115">在 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構中 (ACL) 的 **Null** 存取控制清單會授與無限制的存取權。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="8fbe1-116">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fbe1-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-117">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-117">Security privilege to modify.</span></span> <span data-ttu-id="8fbe1-118">例如，若要變更擁有者和 DACL 安全性，請使用：</span><span class="sxs-lookup"><span data-stu-id="8fbe1-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="8fbe1-119">或</span><span class="sxs-lookup"><span data-stu-id="8fbe1-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="8fbe1-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="8fbe1-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8fbe1-121">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="8fbe1-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="8fbe1-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8fbe1-123">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="8fbe1-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="8fbe1-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8fbe1-125">變更邏輯檔案的 ACL。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="8fbe1-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="8fbe1-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8fbe1-127">變更邏輯檔案的系統 ACL。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fbe1-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fbe1-128">Return value</span></span>

<span data-ttu-id="8fbe1-129">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8fbe1-130">「成功」</span><span class="sxs-lookup"><span data-stu-id="8fbe1-130">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-131">0</span><span class="sxs-lookup"><span data-stu-id="8fbe1-131">0</span></span>

<span data-ttu-id="8fbe1-132">成功。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-132">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-133">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-134">2</span><span class="sxs-lookup"><span data-stu-id="8fbe1-134">2</span></span>

<span data-ttu-id="8fbe1-135">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-135">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-136">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-136">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-137">8</span><span class="sxs-lookup"><span data-stu-id="8fbe1-137">8</span></span>

<span data-ttu-id="8fbe1-138">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-138">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-139">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-139">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-140">9</span><span class="sxs-lookup"><span data-stu-id="8fbe1-140">9</span></span>

<span data-ttu-id="8fbe1-141">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-141">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-142">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-142">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-143">10</span><span class="sxs-lookup"><span data-stu-id="8fbe1-143">10</span></span>

<span data-ttu-id="8fbe1-144">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-144">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-145">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-145">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-146">11</span><span class="sxs-lookup"><span data-stu-id="8fbe1-146">11</span></span>

<span data-ttu-id="8fbe1-147">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-147">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-148">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-148">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-149">12</span><span class="sxs-lookup"><span data-stu-id="8fbe1-149">12</span></span>

<span data-ttu-id="8fbe1-150">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-150">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-151">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-151">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-152">13</span><span class="sxs-lookup"><span data-stu-id="8fbe1-152">13</span></span>

<span data-ttu-id="8fbe1-153">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-153">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-154">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-154">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-155">14</span><span class="sxs-lookup"><span data-stu-id="8fbe1-155">14</span></span>

<span data-ttu-id="8fbe1-156">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-156">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-157">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-157">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-158">15</span><span class="sxs-lookup"><span data-stu-id="8fbe1-158">15</span></span>

<span data-ttu-id="8fbe1-159">共用違規。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-159">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-160">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-160">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-161">16</span><span class="sxs-lookup"><span data-stu-id="8fbe1-161">16</span></span>

<span data-ttu-id="8fbe1-162">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-162">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-163">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-163">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-164">17</span><span class="sxs-lookup"><span data-stu-id="8fbe1-164">17</span></span>

<span data-ttu-id="8fbe1-165">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-165">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="8fbe1-166">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-166">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8fbe1-167">21</span><span class="sxs-lookup"><span data-stu-id="8fbe1-167">21</span></span>

<span data-ttu-id="8fbe1-168">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-168">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fbe1-169">備註</span><span class="sxs-lookup"><span data-stu-id="8fbe1-169">Remarks</span></span>

<span data-ttu-id="8fbe1-170">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-170">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8fbe1-171">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-171">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8fbe1-172">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-172">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8fbe1-173">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8fbe1-173">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fbe1-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fbe1-174">Requirements</span></span>



| <span data-ttu-id="8fbe1-175">需求</span><span class="sxs-lookup"><span data-stu-id="8fbe1-175">Requirement</span></span> | <span data-ttu-id="8fbe1-176">值</span><span class="sxs-lookup"><span data-stu-id="8fbe1-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbe1-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fbe1-177">Minimum supported client</span></span><br/> | <span data-ttu-id="8fbe1-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fbe1-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fbe1-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fbe1-179">Minimum supported server</span></span><br/> | <span data-ttu-id="8fbe1-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fbe1-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fbe1-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="8fbe1-181">Namespace</span></span><br/>                | <span data-ttu-id="8fbe1-182">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8fbe1-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8fbe1-183">MOF</span><span class="sxs-lookup"><span data-stu-id="8fbe1-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fbe1-184"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fbe1-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fbe1-185">DLL</span><span class="sxs-lookup"><span data-stu-id="8fbe1-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fbe1-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fbe1-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fbe1-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fbe1-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbe1-188">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-188">**CIM\_DeviceFile**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="8fbe1-189">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-189">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

