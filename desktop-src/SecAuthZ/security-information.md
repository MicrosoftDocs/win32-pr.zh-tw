---
description: 識別要設定或查詢的物件相關安全性資訊。
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: 'SECURITY_INFORMATION (Winnt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaad4b9f61a20b26397081433b88782dcbc33f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191564"
---
# <a name="security_information"></a><span data-ttu-id="58631-103">安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-103">SECURITY\_INFORMATION</span></span>

<span data-ttu-id="58631-104">[ **安全性 \_ 資訊** ] 資料類型會識別要設定或查詢的物件相關安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="58631-104">The **SECURITY\_INFORMATION** data type identifies the object-related security information being set or queried.</span></span> <span data-ttu-id="58631-105">此安全性資訊包括：</span><span class="sxs-lookup"><span data-stu-id="58631-105">This security information includes:</span></span>

-   <span data-ttu-id="58631-106">物件的擁有者</span><span class="sxs-lookup"><span data-stu-id="58631-106">The owner of an object</span></span>
-   <span data-ttu-id="58631-107">物件的主要群組</span><span class="sxs-lookup"><span data-stu-id="58631-107">The primary group of an object</span></span>
-   <span data-ttu-id="58631-108">物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) </span><span class="sxs-lookup"><span data-stu-id="58631-108">The [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of an object</span></span>
-   <span data-ttu-id="58631-109">[*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (物件的 SACL) </span><span class="sxs-lookup"><span data-stu-id="58631-109">The [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL) of an object</span></span>


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a><span data-ttu-id="58631-110">備註</span><span class="sxs-lookup"><span data-stu-id="58631-110">Remarks</span></span>

<span data-ttu-id="58631-111">某些 **安全性 \_ 資訊** 成員僅適用于 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) 函數。</span><span class="sxs-lookup"><span data-stu-id="58631-111">Some **SECURITY\_INFORMATION** members work only with the [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) function.</span></span> <span data-ttu-id="58631-112">這些成員不會在其他安全性函數（例如 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) 或 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)）所傳回的結構中傳回。</span><span class="sxs-lookup"><span data-stu-id="58631-112">These members are not returned in the structure returned by other security functions such as [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) or [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="58631-113">安全性資訊的每個專案都是由位旗標所指定。</span><span class="sxs-lookup"><span data-stu-id="58631-113">Each item of security information is designated by a bit flag.</span></span> <span data-ttu-id="58631-114">每個位旗標可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="58631-114">Each bit flag can be one of the following values.</span></span> <span data-ttu-id="58631-115">如需詳細資訊，請參閱 [**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) 和 [**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask) 函數。</span><span class="sxs-lookup"><span data-stu-id="58631-115">For more information, see the [**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) and [**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask) functions.</span></span>



| <span data-ttu-id="58631-116">需要查詢/設定的值/許可權</span><span class="sxs-lookup"><span data-stu-id="58631-116">Value/rights required to query/set</span></span>                                                                                                                                                                                                     | <span data-ttu-id="58631-117">意義</span><span class="sxs-lookup"><span data-stu-id="58631-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58631-118">屬性 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-118">ATTRIBUTE\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-119">需要查詢的許可權： **讀取 \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="58631-119">Right required to query: **READ\_CONTROL**</span></span><br/> <span data-ttu-id="58631-120">需要設定的許可權： **寫入 \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="58631-120">Right required to set: **WRITE\_DAC**</span></span><br/>                                                                                     | <span data-ttu-id="58631-121">所參考之物件的資源屬性。</span><span class="sxs-lookup"><span data-stu-id="58631-121">The resource properties of the object being referenced.</span></span> <span data-ttu-id="58631-122">資源屬性會儲存在安全描述項的 SACL 中的系統 \_ 資源 \_ 屬性 \_ ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="58631-122">The resource properties are stored in SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE types in the SACL of the security descriptor.</span></span><br/> <span data-ttu-id="58631-123">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 無法使用這個位旗標。</span><span class="sxs-lookup"><span data-stu-id="58631-123">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This bit flag is not available.</span></span><br/> <br/>                 |
| <span data-ttu-id="58631-124">備份 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-124">BACKUP\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-125">需要查詢的許可權： **讀取 \_ 控制** 和 **存取 \_ 系統 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="58631-125">Right required to query: **READ\_CONTROL** and **ACCESS\_SYSTEM\_SECURITY**</span></span><br/> <span data-ttu-id="58631-126">需要設定的許可權： **寫入 \_ DAC** 和 **寫入 \_ 擁有** 者和 **存取 \_ 系統 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="58631-126">Right required to set: **WRITE\_DAC** and **WRITE\_OWNER** and **ACCESS\_SYSTEM\_SECURITY**</span></span><br/> | <span data-ttu-id="58631-127">安全描述項的所有部分。</span><span class="sxs-lookup"><span data-stu-id="58631-127">All parts of the security descriptor.</span></span> <span data-ttu-id="58631-128">這適用于需要保留整個安全描述項的備份和還原軟體。</span><span class="sxs-lookup"><span data-stu-id="58631-128">This is useful for backup and restore software that needs to preserve the entire security descriptor.</span></span><br/> <span data-ttu-id="58631-129">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 無法使用這個位旗標。</span><span class="sxs-lookup"><span data-stu-id="58631-129">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This bit flag is not available.</span></span><br/> <br/>                                                  |
| <span data-ttu-id="58631-130">DACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-130">DACL\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-131">需要查詢的許可權： **讀取 \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="58631-131">Right required to query: **READ\_CONTROL**</span></span><br/> <span data-ttu-id="58631-132">需要設定的許可權： **寫入 \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="58631-132">Right required to set: **WRITE\_DAC**</span></span><br/>                                                                                          | <span data-ttu-id="58631-133">正在參考物件的 DACL。</span><span class="sxs-lookup"><span data-stu-id="58631-133">The DACL of the object is being referenced.</span></span><br/>                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="58631-134">群組 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-134">GROUP\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-135">需要查詢的許可權： **讀取 \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="58631-135">Right required to query: **READ\_CONTROL**</span></span><br/> <span data-ttu-id="58631-136">需要設定的許可權：**寫入 \_ 擁有** 者</span><span class="sxs-lookup"><span data-stu-id="58631-136">Right required to set: **WRITE\_OWNER**</span></span> <br/>                                                                                      | <span data-ttu-id="58631-137">正在參考物件的主要群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="58631-137">The primary group identifier of the object is being referenced.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="58631-138">標籤 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-138">LABEL\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-139">需要查詢的許可權： **讀取 \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="58631-139">Right required to query: **READ\_CONTROL**</span></span><br/> <span data-ttu-id="58631-140">需要設定的許可權：**寫入 \_ 擁有** 者</span><span class="sxs-lookup"><span data-stu-id="58631-140">Right required to set: **WRITE\_OWNER**</span></span> <br/>                                                                                      | <span data-ttu-id="58631-141">正在參考強制完整性標籤。</span><span class="sxs-lookup"><span data-stu-id="58631-141">The mandatory integrity label is being referenced.</span></span><br/> <span data-ttu-id="58631-142">強制完整性標籤是物件的 SACL 中的 ACE。</span><span class="sxs-lookup"><span data-stu-id="58631-142">The mandatory integrity label is an ACE in the SACL of the object.</span></span><br/> <span data-ttu-id="58631-143">**Windows Server 2003 和 WINDOWS XP：** 無法使用這個位旗標。</span><span class="sxs-lookup"><span data-stu-id="58631-143">**Windows Server 2003 and Windows XP:** This bit flag is not available.</span></span><br/> <br/>                                                                                                                                    |
| <span data-ttu-id="58631-144">擁有者 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-144">OWNER\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-145">需要查詢的許可權： **讀取 \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="58631-145">Right required to query: **READ\_CONTROL**</span></span><br/> <span data-ttu-id="58631-146">需要設定的許可權：**寫入 \_ 擁有** 者</span><span class="sxs-lookup"><span data-stu-id="58631-146">Right required to set: **WRITE\_OWNER**</span></span> <br/>                                                                                      | <span data-ttu-id="58631-147">正在參考物件的擁有者識別碼。</span><span class="sxs-lookup"><span data-stu-id="58631-147">The owner identifier of the object is being referenced.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="58631-148">受保護的 \_ DACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-148">PROTECTED\_DACL\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-149">需要查詢的許可權：無法使用</span><span class="sxs-lookup"><span data-stu-id="58631-149">Right required to query: Not available</span></span><br/> <span data-ttu-id="58631-150">需要設定的許可權： **寫入 \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="58631-150">Right required to set: **WRITE\_DAC**</span></span><br/>                                                                                   | <span data-ttu-id="58631-151">DACL 無法 (Ace) 繼承 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 。</span><span class="sxs-lookup"><span data-stu-id="58631-151">The DACL cannot inherit [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs).</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="58631-152">受保護的 \_ SACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-152">PROTECTED\_SACL\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-153">需要查詢的許可權：無法使用</span><span class="sxs-lookup"><span data-stu-id="58631-153">Right required to query: Not available</span></span><br/> <span data-ttu-id="58631-154">需要設定的許可權： **存取 \_ 系統 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="58631-154">Right required to set: **ACCESS\_SYSTEM\_SECURITY**</span></span><br/>                                                                     | <span data-ttu-id="58631-155">SACL 無法繼承 Ace。</span><span class="sxs-lookup"><span data-stu-id="58631-155">The SACL cannot inherit ACEs.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="58631-156">SACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-156">SACL\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-157">需要查詢的許可權： **存取 \_ 系統 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="58631-157">Right required to query: **ACCESS\_SYSTEM\_SECURITY**</span></span><br/> <span data-ttu-id="58631-158">需要設定的許可權： **存取 \_ 系統 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="58631-158">Right required to set: **ACCESS\_SYSTEM\_SECURITY**</span></span><br/>                                                                 | <span data-ttu-id="58631-159">正在參考物件的 SACL。</span><span class="sxs-lookup"><span data-stu-id="58631-159">The SACL of the object is being referenced.</span></span><br/>                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="58631-160">領域 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-160">SCOPE\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-161">需要查詢的許可權： **讀取 \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="58631-161">Right required to query: **READ\_CONTROL**</span></span><br/> <span data-ttu-id="58631-162">需要設定的許可權： **存取 \_ 系統 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="58631-162">Right required to set: **ACCESS\_SYSTEM\_SECURITY**</span></span><br/>                                                                           | <span data-ttu-id="58631-163">集中存取原則 (端點適用于所參考物件的) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="58631-163">The Central Access Policy (CAP) identifier applicable on the object that is being referenced.</span></span> <span data-ttu-id="58631-164">每個 CAP 識別碼都會儲存在 \_ SD 的 SACL 中的系統範圍原則識別碼 \_ \_ \_ ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="58631-164">Each CAP identifier is stored in a SYSTEM\_SCOPED\_POLICY\_ID\_ACE type in the SACL of the SD.</span></span><br/> <span data-ttu-id="58631-165">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 無法使用這個位旗標。</span><span class="sxs-lookup"><span data-stu-id="58631-165">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This bit flag is not available.</span></span><br/> <br/> |
| <span data-ttu-id="58631-166">未受保護的 \_ DACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-166">UNPROTECTED\_DACL\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-167">需要查詢的許可權：無法使用</span><span class="sxs-lookup"><span data-stu-id="58631-167">Right required to query: Not available</span></span><br/> <span data-ttu-id="58631-168">需要設定的許可權： **寫入 \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="58631-168">Right required to set: **WRITE\_DAC**</span></span><br/>                                                                                 | <span data-ttu-id="58631-169">DACL 繼承自父物件的 Ace。</span><span class="sxs-lookup"><span data-stu-id="58631-169">The DACL inherits ACEs from the parent object.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="58631-170">未受保護的 \_ SACL \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="58631-170">UNPROTECTED\_SACL\_SECURITY\_INFORMATION</span></span><br/> <span data-ttu-id="58631-171">需要查詢的許可權：無法使用</span><span class="sxs-lookup"><span data-stu-id="58631-171">Right required to query: Not available</span></span><br/> <span data-ttu-id="58631-172">需要設定的許可權： **存取 \_ 系統 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="58631-172">Right required to set: **ACCESS\_SYSTEM\_SECURITY**</span></span><br/>                                                                   | <span data-ttu-id="58631-173">SACL 會從父物件繼承 Ace。</span><span class="sxs-lookup"><span data-stu-id="58631-173">The SACL inherits ACEs from the parent object.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="58631-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="58631-174">Requirements</span></span>



| <span data-ttu-id="58631-175">需求</span><span class="sxs-lookup"><span data-stu-id="58631-175">Requirement</span></span> | <span data-ttu-id="58631-176">值</span><span class="sxs-lookup"><span data-stu-id="58631-176">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58631-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58631-177">Minimum supported client</span></span><br/> | <span data-ttu-id="58631-178">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58631-178">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="58631-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58631-179">Minimum supported server</span></span><br/> | <span data-ttu-id="58631-180">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58631-180">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="58631-181">標頭</span><span class="sxs-lookup"><span data-stu-id="58631-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="58631-182"><dt>Winnt (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="58631-182"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58631-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58631-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58631-184">存取控制</span><span class="sxs-lookup"><span data-stu-id="58631-184">Access Control</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="58631-185">基本存取控制結構</span><span class="sxs-lookup"><span data-stu-id="58631-185">Basic Access Control Structures</span></span>](authorization-structures.md)
</dt> <dt>

[<span data-ttu-id="58631-186">**ConvertSecurityDescriptorToStringSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="58631-186">**ConvertSecurityDescriptorToStringSecurityDescriptor**</span></span>](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
</dt> <dt>

[<span data-ttu-id="58631-187">**ConvertStringSecurityDescriptorToSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="58631-187">**ConvertStringSecurityDescriptorToSecurityDescriptor**</span></span>](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)
</dt> <dt>

[<span data-ttu-id="58631-188">**GetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="58631-188">**GetFileSecurity**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[<span data-ttu-id="58631-189">**GetKernelObjectSecurity**</span><span class="sxs-lookup"><span data-stu-id="58631-189">**GetKernelObjectSecurity**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)
</dt> <dt>

[<span data-ttu-id="58631-190">**GetNamedSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="58631-190">**GetNamedSecurityInfo**</span></span>](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)
</dt> <dt>

[<span data-ttu-id="58631-191">**GetPrivateObjectSecurity**</span><span class="sxs-lookup"><span data-stu-id="58631-191">**GetPrivateObjectSecurity**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)
</dt> <dt>

[<span data-ttu-id="58631-192">**GetSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="58631-192">**GetSecurityInfo**</span></span>](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)
</dt> <dt>

[<span data-ttu-id="58631-193">**GetUserObjectSecurity**</span><span class="sxs-lookup"><span data-stu-id="58631-193">**GetUserObjectSecurity**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity)
</dt> <dt>

[<span data-ttu-id="58631-194">**QuerySecurityAccessMask**</span><span class="sxs-lookup"><span data-stu-id="58631-194">**QuerySecurityAccessMask**</span></span>](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)
</dt> <dt>

[<span data-ttu-id="58631-195">**SetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="58631-195">**SetFileSecurity**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya)
</dt> <dt>

[<span data-ttu-id="58631-196">**SetKernelObjectSecurity**</span><span class="sxs-lookup"><span data-stu-id="58631-196">**SetKernelObjectSecurity**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)
</dt> <dt>

[<span data-ttu-id="58631-197">**SetNamedSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="58631-197">**SetNamedSecurityInfo**</span></span>](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)
</dt> <dt>

[<span data-ttu-id="58631-198">**SetPrivateObjectSecurity**</span><span class="sxs-lookup"><span data-stu-id="58631-198">**SetPrivateObjectSecurity**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)
</dt> <dt>

[<span data-ttu-id="58631-199">**SetSecurityAccessMask**</span><span class="sxs-lookup"><span data-stu-id="58631-199">**SetSecurityAccessMask**</span></span>](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask)
</dt> <dt>

[<span data-ttu-id="58631-200">**SetSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="58631-200">**SetSecurityInfo**</span></span>](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[<span data-ttu-id="58631-201">**SetUserObjectSecurity**</span><span class="sxs-lookup"><span data-stu-id="58631-201">**SetUserObjectSecurity**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity)
</dt> <dt>

[<span data-ttu-id="58631-202">**TreeResetNamedSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="58631-202">**TreeResetNamedSecurityInfo**</span></span>](/windows/desktop/api/Aclapi/nf-aclapi-treeresetnamedsecurityinfoa)
</dt> <dt>

[<span data-ttu-id="58631-203">**TreeSetNamedSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="58631-203">**TreeSetNamedSecurityInfo**</span></span>](/windows/desktop/api/Aclapi/nf-aclapi-treesetnamedsecurityinfoa)
</dt> </dl>

 

