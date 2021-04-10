---
description: 變更物件路徑中所指定邏輯目錄專案檔的安全性許可權。
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: CIM_Directory 類別的 ChangeSecurityPermissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bf767dc45907a90354b2c00fb30c6b31ce6d09a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688991"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="236a7-103">CIM 目錄類別的 ChangeSecurityPermissions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="236a7-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="236a7-104">**ChangeSecurityPermissions** 方法會變更物件路徑中所指定邏輯目錄專案檔的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="236a7-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="236a7-105">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，以變更目錄所包含的所有檔案和子目錄的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="236a7-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="236a7-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="236a7-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="236a7-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="236a7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="236a7-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="236a7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="236a7-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="236a7-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="236a7-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="236a7-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="236a7-111">語法</span><span class="sxs-lookup"><span data-stu-id="236a7-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="236a7-112">參數</span><span class="sxs-lookup"><span data-stu-id="236a7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="236a7-113">*SecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="236a7-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="236a7-114">指定安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="236a7-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="236a7-115">在 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)結構中 (ACL) 的 **Null** 存取控制清單會授與無限制的存取權。</span><span class="sxs-lookup"><span data-stu-id="236a7-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="236a7-116">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="236a7-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="236a7-117">要修改的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="236a7-117">Security privilege to modify.</span></span> <span data-ttu-id="236a7-118">例如，若要變更擁有者和 DACL 安全性，請使用：</span><span class="sxs-lookup"><span data-stu-id="236a7-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="236a7-119">或</span><span class="sxs-lookup"><span data-stu-id="236a7-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="236a7-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**變更 \_擁有者 \_ 安全性 \_ 資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="236a7-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="236a7-121">變更邏輯檔案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="236a7-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="236a7-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**變更 \_將 \_ 安全性 \_ 資訊群組** (2) </span><span class="sxs-lookup"><span data-stu-id="236a7-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="236a7-123">變更邏輯檔案的群組。</span><span class="sxs-lookup"><span data-stu-id="236a7-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="236a7-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**變更 \_DACL \_ 安全性 \_ 資訊** (4) </span><span class="sxs-lookup"><span data-stu-id="236a7-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="236a7-125">變更邏輯檔案的 ACL。</span><span class="sxs-lookup"><span data-stu-id="236a7-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="236a7-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**變更 \_SACL \_ 安全性 \_ 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="236a7-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="236a7-127">變更邏輯檔案的系統 ACL。</span><span class="sxs-lookup"><span data-stu-id="236a7-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="236a7-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="236a7-128">Return value</span></span>

<span data-ttu-id="236a7-129">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="236a7-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="236a7-130">0</span><span class="sxs-lookup"><span data-stu-id="236a7-130">0</span></span>

<span data-ttu-id="236a7-131">成功。</span><span class="sxs-lookup"><span data-stu-id="236a7-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-132">2</span><span class="sxs-lookup"><span data-stu-id="236a7-132">2</span></span>

<span data-ttu-id="236a7-133">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="236a7-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-134">8</span><span class="sxs-lookup"><span data-stu-id="236a7-134">8</span></span>

<span data-ttu-id="236a7-135">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="236a7-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-136">9</span><span class="sxs-lookup"><span data-stu-id="236a7-136">9</span></span>

<span data-ttu-id="236a7-137">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="236a7-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-138">10</span><span class="sxs-lookup"><span data-stu-id="236a7-138">10</span></span>

<span data-ttu-id="236a7-139">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="236a7-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-140">11</span><span class="sxs-lookup"><span data-stu-id="236a7-140">11</span></span>

<span data-ttu-id="236a7-141">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="236a7-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-142">12</span><span class="sxs-lookup"><span data-stu-id="236a7-142">12</span></span>

<span data-ttu-id="236a7-143">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="236a7-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-144">13</span><span class="sxs-lookup"><span data-stu-id="236a7-144">13</span></span>

<span data-ttu-id="236a7-145">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="236a7-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-146">14</span><span class="sxs-lookup"><span data-stu-id="236a7-146">14</span></span>

<span data-ttu-id="236a7-147">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="236a7-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-148">15</span><span class="sxs-lookup"><span data-stu-id="236a7-148">15</span></span>

<span data-ttu-id="236a7-149">共用違規。</span><span class="sxs-lookup"><span data-stu-id="236a7-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-150">16</span><span class="sxs-lookup"><span data-stu-id="236a7-150">16</span></span>

<span data-ttu-id="236a7-151">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="236a7-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-152">17</span><span class="sxs-lookup"><span data-stu-id="236a7-152">17</span></span>

<span data-ttu-id="236a7-153">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="236a7-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="236a7-154">21</span><span class="sxs-lookup"><span data-stu-id="236a7-154">21</span></span>

<span data-ttu-id="236a7-155">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="236a7-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="236a7-156">備註</span><span class="sxs-lookup"><span data-stu-id="236a7-156">Remarks</span></span>

<span data-ttu-id="236a7-157">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="236a7-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="236a7-158">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="236a7-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="236a7-159">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="236a7-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="236a7-160">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="236a7-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="236a7-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="236a7-161">Requirements</span></span>



| <span data-ttu-id="236a7-162">需求</span><span class="sxs-lookup"><span data-stu-id="236a7-162">Requirement</span></span> | <span data-ttu-id="236a7-163">值</span><span class="sxs-lookup"><span data-stu-id="236a7-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="236a7-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="236a7-164">Minimum supported client</span></span><br/> | <span data-ttu-id="236a7-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="236a7-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="236a7-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="236a7-166">Minimum supported server</span></span><br/> | <span data-ttu-id="236a7-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="236a7-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="236a7-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="236a7-168">Namespace</span></span><br/>                | <span data-ttu-id="236a7-169">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="236a7-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="236a7-170">MOF</span><span class="sxs-lookup"><span data-stu-id="236a7-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="236a7-171"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="236a7-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="236a7-172">DLL</span><span class="sxs-lookup"><span data-stu-id="236a7-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="236a7-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="236a7-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="236a7-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="236a7-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="236a7-175">CIM \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="236a7-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="236a7-176">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="236a7-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

