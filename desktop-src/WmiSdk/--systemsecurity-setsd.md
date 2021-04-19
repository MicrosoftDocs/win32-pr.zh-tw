---
description: 為使用者所連接的命名空間設定安全描述項。 這個方法需要二進位位元組陣列格式的安全描述項。 如果您要撰寫腳本，請使用 SetSecurityDescriptor 方法。
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 SetSD 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979192"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="c5134-105">\_ \_ SystemSecurity 類別的 SetSD 方法</span><span class="sxs-lookup"><span data-stu-id="c5134-105">SetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="c5134-106">**SetSD** 方法會設定使用者所連接之命名空間的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="c5134-106">The **SetSD** method sets the security descriptor for the namespace to which a user is connected.</span></span> <span data-ttu-id="c5134-107">這個方法需要二進位位元組陣列格式的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="c5134-107">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="c5134-108">如果您要撰寫腳本，請使用 [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c5134-108">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span> <span data-ttu-id="c5134-109">如需詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="c5134-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="c5134-110">如果您是使用 c + + 進行程式設計，您可以使用 [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)來操作二進位安全描述項，以及 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)的轉換方法。</span><span class="sxs-lookup"><span data-stu-id="c5134-110">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="c5134-111">使用者必須擁有「 **寫入 \_ DAC** 」許可權，而且根據預設，系統管理員具有該許可權。</span><span class="sxs-lookup"><span data-stu-id="c5134-111">A user must have the **WRITE\_DAC** permission, and by default, an administrator has that permission.</span></span> <span data-ttu-id="c5134-112">安全描述項中唯一使用的部分是 noninherited 存取控制專案， (ACE) 在任意存取控制清單 (DACL) 中。</span><span class="sxs-lookup"><span data-stu-id="c5134-112">The only part of the security descriptor that is used is the noninherited access control entry (ACE) in the discretionary access control list (DACL).</span></span> <span data-ttu-id="c5134-113">藉由設定 Ace 中的 **容器 \_ 繼承** 旗標，安全描述項會影響子命名空間。</span><span class="sxs-lookup"><span data-stu-id="c5134-113">By setting the **CONTAINER\_INHERIT** flag in the ACEs, the security descriptor affects child namespaces.</span></span> <span data-ttu-id="c5134-114">允許和拒絕 Ace 都是允許的。</span><span class="sxs-lookup"><span data-stu-id="c5134-114">Both allow and deny ACEs are permitted.</span></span>

> [!Note]  
> <span data-ttu-id="c5134-115">因為 DACL 中允許使用 deny 和 allow Ace，所以 Ace 的順序很重要。</span><span class="sxs-lookup"><span data-stu-id="c5134-115">Because deny and allow ACEs are both permitted in a DACL, the order of ACEs is important.</span></span> <span data-ttu-id="c5134-116">如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。</span><span class="sxs-lookup"><span data-stu-id="c5134-116">For more information, see [Ordering of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c5134-117">語法</span><span class="sxs-lookup"><span data-stu-id="c5134-117">Syntax</span></span>


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="c5134-118">參數</span><span class="sxs-lookup"><span data-stu-id="c5134-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5134-119">*SD* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5134-119">*SD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5134-120">組成安全描述項的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="c5134-120">Byte array that makes up the security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5134-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5134-121">Return value</span></span>

<span data-ttu-id="c5134-122">傳回 **HRESULT** ，指出方法呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="c5134-122">Returns an **HRESULT** that indicates the status of a method call.</span></span> <span data-ttu-id="c5134-123">針對編寫腳本和 Visual Basic 應用程式，可以從 OutParameters 取得結果 [ReturnValue](parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="c5134-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="c5134-124">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="c5134-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="c5134-125">下列清單列出對 **SetSD** 很重要的傳回值。</span><span class="sxs-lookup"><span data-stu-id="c5134-125">The following list lists the return values that are significant to **SetSD**.</span></span>

<dl> <dt>

<span data-ttu-id="c5134-126">**S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="c5134-126">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="c5134-127">已成功執行方法。</span><span class="sxs-lookup"><span data-stu-id="c5134-127">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="c5134-128">**WBEM \_ E \_ \_ 拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="c5134-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="c5134-129">呼叫端沒有足夠的許可權可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c5134-129">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="c5134-130">**\_ \_ \_ 已停用 WBEM E 方法**</span><span class="sxs-lookup"><span data-stu-id="c5134-130">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="c5134-131">嘗試在不支援的作業系統上執行此方法。</span><span class="sxs-lookup"><span data-stu-id="c5134-131">Attempted to run this method on OS that does not support it.</span></span>

</dd> <dt>

<span data-ttu-id="c5134-132">**WBEM \_ E \_ 不正確 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="c5134-132">**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="c5134-133">SD 不會通過基本有效性測試。</span><span class="sxs-lookup"><span data-stu-id="c5134-133">SD does not pass basic validity tests.</span></span>

</dd> <dt>

<span data-ttu-id="c5134-134">**WBEM \_ E \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="c5134-134">**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="c5134-135">SD 因為下列其中一項而無效：</span><span class="sxs-lookup"><span data-stu-id="c5134-135">SD is not valid due to one of the following:</span></span>

-   <span data-ttu-id="c5134-136">遺漏 DACL。</span><span class="sxs-lookup"><span data-stu-id="c5134-136">DACL is missing.</span></span>
-   <span data-ttu-id="c5134-137">DACL 無效。</span><span class="sxs-lookup"><span data-stu-id="c5134-137">DACL is not valid.</span></span>
-   <span data-ttu-id="c5134-138">ACE 已設定 **wbem \_ FULL \_ write \_ rep** 旗標，且未設定 **wbem \_ 部分 \_ 寫入 \_ 代表** 或 **wbem \_ 寫入 \_ 提供者** 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5134-138">ACE has the **WBEM\_FULL\_WRITE\_REP** flag set, and the **WBEM\_PARTIAL\_WRITE\_REP** or **WBEM\_WRITE\_PROVIDER** flag is not set.</span></span>
-   <span data-ttu-id="c5134-139">ACE 具有 **\_ 僅限繼承 \_ ace** 旗標的設定，而不含 **CONTAINER \_ INHERIT \_ ace** 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5134-139">ACE has the **INHERIT\_ONLY\_ACE** flag set without the **CONTAINER\_INHERIT\_ACE** flag.</span></span>
-   <span data-ttu-id="c5134-140">ACE 有未知的存取位集。</span><span class="sxs-lookup"><span data-stu-id="c5134-140">ACE has an unknown access bit set.</span></span>
-   <span data-ttu-id="c5134-141">ACE 的旗標設定不在資料表中。</span><span class="sxs-lookup"><span data-stu-id="c5134-141">ACE has a flag set that is not in the table.</span></span>
-   <span data-ttu-id="c5134-142">ACE 的型別不在資料表中。</span><span class="sxs-lookup"><span data-stu-id="c5134-142">ACE has a type that is not in the table.</span></span>
-   <span data-ttu-id="c5134-143">SD 缺少擁有者和群組。</span><span class="sxs-lookup"><span data-stu-id="c5134-143">The owner and group are missing from the SD.</span></span>

<span data-ttu-id="c5134-144">如需存取控制專案 (ACE) 旗標的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="c5134-144">For more information about the access control entry (ACE) flags, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5134-145">備註</span><span class="sxs-lookup"><span data-stu-id="c5134-145">Remarks</span></span>

<span data-ttu-id="c5134-146">如需以程式設計方式或手動方式修改命名空間安全性的詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md)。</span><span class="sxs-lookup"><span data-stu-id="c5134-146">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c5134-147">範例</span><span class="sxs-lookup"><span data-stu-id="c5134-147">Examples</span></span>

<span data-ttu-id="c5134-148">下列腳本示範如何使用 **SetSD** 來設定根命名空間的命名空間安全描述項，並將其變更為 *strSD* 中顯示的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="c5134-148">The following script shows how to use **SetSD** to set the namespace security descriptor for the root namespace and change it to the byte array shown in *strSD*.</span></span>


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



<span data-ttu-id="c5134-149">下列 c # 程式碼範例會使用 AccessControl 來列舉、插入和移除 RawSecurityDescriptor. Objdescriptor.discretionaryacl 中的新 CommonAce 物件，然後再將它轉換回位元組陣列，以透過 SetSD 加以儲存。</span><span class="sxs-lookup"><span data-stu-id="c5134-149">The following C# code sample uses the System.Security.AccessControl.RawSecurityDescriptor to enumerate, insert and remove new CommonAce objects in RawSecurityDescriptor.DiscretionaryAcl and then convert it back to an byte array to save it via SetSD.</span></span> <span data-ttu-id="c5134-150">您可以使用 NTAccount 和轉譯來取出 SecurityIdentifier。</span><span class="sxs-lookup"><span data-stu-id="c5134-150">An SecurityIdentifier can be retrieved by using NTAccount and Translate.</span></span>


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a><span data-ttu-id="c5134-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5134-151">Requirements</span></span>



| <span data-ttu-id="c5134-152">需求</span><span class="sxs-lookup"><span data-stu-id="c5134-152">Requirement</span></span> | <span data-ttu-id="c5134-153">值</span><span class="sxs-lookup"><span data-stu-id="c5134-153">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c5134-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5134-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c5134-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5134-155">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c5134-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5134-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c5134-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5134-157">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c5134-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="c5134-158">Namespace</span></span><br/>                | <span data-ttu-id="c5134-159">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="c5134-159">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c5134-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5134-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5134-161">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="c5134-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c5134-162">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="c5134-162">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="c5134-163">**\_\_SystemSecurity::GetSD**</span><span class="sxs-lookup"><span data-stu-id="c5134-163">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="c5134-164">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="c5134-164">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="c5134-165">**Win32 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="c5134-165">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="c5134-166">**Win32 \_ SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c5134-166">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="c5134-167">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="c5134-167">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

