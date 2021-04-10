---
title: 'IADsSecurityDescriptor 屬性方法 (Iads .h) '
description: IADsSecurityDescriptor 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- IADsSecurityDescriptor 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5c07213a2d2a3a1b64621dbc40f707b0900703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094447"
---
# <a name="iadssecuritydescriptor-property-methods"></a><span data-ttu-id="aba50-105">IADsSecurityDescriptor 屬性方法</span><span class="sxs-lookup"><span data-stu-id="aba50-105">IADsSecurityDescriptor Property Methods</span></span>

<span data-ttu-id="aba50-106">[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="aba50-106">The property methods of the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="aba50-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="aba50-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="aba50-108">屬性</span><span class="sxs-lookup"><span data-stu-id="aba50-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="aba50-109">**控制**</span><span class="sxs-lookup"><span data-stu-id="aba50-109">**Control**</span></span>
<span data-ttu-id="aba50-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-111">符合安全描述項意義的旗標。</span><span class="sxs-lookup"><span data-stu-id="aba50-111">Flags that qualify the meaning of the security descriptor.</span></span> <span data-ttu-id="aba50-112">值取自 Win32 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control) 結構。</span><span class="sxs-lookup"><span data-stu-id="aba50-112">Values are taken from the Win32 [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) structure.</span></span>

<dt>

<span data-ttu-id="aba50-113">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-114">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="aba50-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aba50-115">**DaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="aba50-115">**DaclDefaulted**</span></span>
<span data-ttu-id="aba50-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-117">BOOL 類型的旗標，指出 DACL 是否衍生自預設的機制，而不是由安全描述項的原始提供者明確提供。</span><span class="sxs-lookup"><span data-stu-id="aba50-117">A flag of the BOOL type that indicates if the DACL is derived from a default mechanism, rather than being provided explicitly by the original provider of the security descriptor.</span></span> <span data-ttu-id="aba50-118">例如，如果物件的建立者未指定 DACL，則物件會從建立者的存取權杖接收預設的 DACL。</span><span class="sxs-lookup"><span data-stu-id="aba50-118">For example, if an object's creator does not specify a DACL, the object receives the default DACL from the creator's access token.</span></span> <span data-ttu-id="aba50-119">此旗標可能會影響對 ACE 繼承而言，系統處理 DACL 的方式。</span><span class="sxs-lookup"><span data-stu-id="aba50-119">This flag can affect how the system treats the DACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="aba50-120">如果 \_ 未設定 SE DACL 出現旗標，系統會忽略此旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="aba50-120">The system ignores this flag if the SE\_DACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="aba50-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-122">腳本資料類型： **VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="aba50-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aba50-123">**Objdescriptor.discretionaryacl**</span><span class="sxs-lookup"><span data-stu-id="aba50-123">**DiscretionaryAcl**</span></span>
<span data-ttu-id="aba50-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-125">任意存取控制清單 (DACL) ，可指定授與指定使用者和群組之物件的存取類型。</span><span class="sxs-lookup"><span data-stu-id="aba50-125">Discretionary access-control list (DACL) that specifies the types of access granted to the object for specified users and groups.</span></span> <span data-ttu-id="aba50-126">如需 Dacl 的詳細資訊，請參閱 [Null dacl 和空白的 dacl](/windows/desktop/AD/null-dacls-and-empty-dacls)。</span><span class="sxs-lookup"><span data-stu-id="aba50-126">For more information about DACLs, see [Null DACLs and Empty DACLs](/windows/desktop/AD/null-dacls-and-empty-dacls).</span></span>

<dt>

<span data-ttu-id="aba50-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-128">腳本資料類型： **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="aba50-128">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aba50-129">**群組**</span><span class="sxs-lookup"><span data-stu-id="aba50-129">**Group**</span></span>
<span data-ttu-id="aba50-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-131">擁有者的安全識別碼所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="aba50-131">Group to which the owner's security ID belongs.</span></span>

<dt>

<span data-ttu-id="aba50-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-133">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="aba50-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aba50-134">**GroupDefaulted**</span><span class="sxs-lookup"><span data-stu-id="aba50-134">**GroupDefaulted**</span></span>
<span data-ttu-id="aba50-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-136">BOOL 類型的旗標，這個旗標會指出群組資料是否衍生自預設的機制，而不是由安全描述項的原始提供者明確提供。</span><span class="sxs-lookup"><span data-stu-id="aba50-136">A flag of the BOOL type that indicates if the group data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="aba50-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-138">腳本資料類型： **VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="aba50-138">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aba50-139">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="aba50-139">**Owner**</span></span>
<span data-ttu-id="aba50-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-141">物件擁有者。</span><span class="sxs-lookup"><span data-stu-id="aba50-141">Object owner.</span></span>

<dt>

<span data-ttu-id="aba50-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-143">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="aba50-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aba50-144">**OwnerDefaulted**</span><span class="sxs-lookup"><span data-stu-id="aba50-144">**OwnerDefaulted**</span></span>
<span data-ttu-id="aba50-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-146">BOOL 類型的旗標，表示擁有者資料是衍生自預設的機制，而不是由安全描述項的原始提供者明確提供。</span><span class="sxs-lookup"><span data-stu-id="aba50-146">A flag of the BOOL type that indicates that the owner data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="aba50-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-148">腳本資料類型： **VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="aba50-148">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aba50-149">**修訂**</span><span class="sxs-lookup"><span data-stu-id="aba50-149">**Revision**</span></span>
<span data-ttu-id="aba50-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-151">安全描述項的修訂層級。</span><span class="sxs-lookup"><span data-stu-id="aba50-151">Revision level of the security descriptor.</span></span> <span data-ttu-id="aba50-152">此值取自 Win32 [**ACL \_ 修訂 \_ 資訊**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) 結構。</span><span class="sxs-lookup"><span data-stu-id="aba50-152">This value is taken from the Win32 [**ACL\_REVISION\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) structure.</span></span> <span data-ttu-id="aba50-153">ACL 中的所有 Ace 都必須位於相同的修訂層級。</span><span class="sxs-lookup"><span data-stu-id="aba50-153">All ACEs in an ACL must be at the same revision level.</span></span>

<dt>

<span data-ttu-id="aba50-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-155">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="aba50-155">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aba50-156">**SaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="aba50-156">**SaclDefaulted**</span></span>
<span data-ttu-id="aba50-157"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-157"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-158">BOOL 類型的旗標，表示 SACL 衍生自預設的機制，而不是由安全描述項的原始提供者明確提供。</span><span class="sxs-lookup"><span data-stu-id="aba50-158">A flag of the BOOL type that indicates that the SACL is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span> <span data-ttu-id="aba50-159">此旗標可能會影響系統處理 SACL 的方式（相對於 ACE 繼承）。</span><span class="sxs-lookup"><span data-stu-id="aba50-159">This flag can affect how the system handles the SACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="aba50-160">如果 \_ 未設定 SE SACL 出現旗標，系統會忽略此旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="aba50-160">The system ignores this flag if the SE\_SACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="aba50-161">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-162">腳本資料類型： **VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="aba50-162">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="aba50-163">**SystemAcl**</span><span class="sxs-lookup"><span data-stu-id="aba50-163">**SystemAcl**</span></span>
<span data-ttu-id="aba50-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="aba50-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="aba50-165">用來產生物件之審核記錄的系統存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="aba50-165">System access-control list used to generate audit records for the object.</span></span>

<dt>

<span data-ttu-id="aba50-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aba50-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="aba50-167">腳本資料類型： **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="aba50-167">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="aba50-168">範例</span><span class="sxs-lookup"><span data-stu-id="aba50-168">Examples</span></span>

<span data-ttu-id="aba50-169">下列程式碼範例顯示如何列舉現有的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="aba50-169">The following code example shows how to enumerate an existing security descriptor.</span></span>


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a><span data-ttu-id="aba50-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="aba50-170">Requirements</span></span>



| <span data-ttu-id="aba50-171">需求</span><span class="sxs-lookup"><span data-stu-id="aba50-171">Requirement</span></span> | <span data-ttu-id="aba50-172">值</span><span class="sxs-lookup"><span data-stu-id="aba50-172">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba50-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aba50-173">Minimum supported client</span></span><br/> | <span data-ttu-id="aba50-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aba50-174">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="aba50-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aba50-175">Minimum supported server</span></span><br/> | <span data-ttu-id="aba50-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aba50-176">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="aba50-177">標頭</span><span class="sxs-lookup"><span data-stu-id="aba50-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="aba50-178"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="aba50-178"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="aba50-179">DLL</span><span class="sxs-lookup"><span data-stu-id="aba50-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aba50-180"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aba50-180"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="aba50-181">IID</span><span class="sxs-lookup"><span data-stu-id="aba50-181">IID</span></span><br/>                      | <span data-ttu-id="aba50-182">IID \_ IADsSecurityDescriptor 定義為 B8C787CA-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="aba50-182">IID\_IADsSecurityDescriptor is defined as B8C787CA-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aba50-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aba50-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba50-184">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="aba50-184">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="aba50-185">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="aba50-185">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="aba50-186">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="aba50-186">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

