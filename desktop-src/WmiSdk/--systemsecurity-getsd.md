---
description: 取得使用者所連接之命名空間的安全描述項。 這個方法會以二進位位元組陣列格式傳回安全描述項。 如果您要撰寫腳本，請使用 GetSecurityDescriptor 方法。
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 GetSD 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987573"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="7c133-105">\_ \_ SystemSecurity 類別的 GetSD 方法</span><span class="sxs-lookup"><span data-stu-id="7c133-105">GetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="7c133-106">**GetSD** 方法會取得使用者所連接之命名空間的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="7c133-106">The **GetSD** method gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="7c133-107">這個方法會以二進位位元組陣列格式傳回安全描述項。</span><span class="sxs-lookup"><span data-stu-id="7c133-107">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="7c133-108">如果您要撰寫腳本，請使用 [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7c133-108">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span> <span data-ttu-id="7c133-109">如需詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="7c133-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="7c133-110">使用者必須擁有「 **讀取 \_ 控制** 」許可權。</span><span class="sxs-lookup"><span data-stu-id="7c133-110">The user must have the **READ\_CONTROL** permission.</span></span> <span data-ttu-id="7c133-111">依預設，系統管理員擁有該許可權。</span><span class="sxs-lookup"><span data-stu-id="7c133-111">By default, administrators have that permission.</span></span> <span data-ttu-id="7c133-112">實際使用之安全描述項的唯一部分是 (DACL) 的任意存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="7c133-112">The only part of the security descriptor that is actually used is the discretionary access control list (DACL).</span></span> <span data-ttu-id="7c133-113">DACL 可以包含繼承的和非繼承的 Ace。</span><span class="sxs-lookup"><span data-stu-id="7c133-113">The DACL can contain both inherited and non-inherited ACEs.</span></span> <span data-ttu-id="7c133-114">拒絕和允許 Ace 都是允許的。</span><span class="sxs-lookup"><span data-stu-id="7c133-114">Both deny and allow ACEs are permitted.</span></span>

<span data-ttu-id="7c133-115">如果您是使用 c + + 進行程式設計，您可以使用 [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)來操作二進位安全描述項，以及 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)的轉換方法。</span><span class="sxs-lookup"><span data-stu-id="7c133-115">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c133-116">語法</span><span class="sxs-lookup"><span data-stu-id="7c133-116">Syntax</span></span>


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="7c133-117">參數</span><span class="sxs-lookup"><span data-stu-id="7c133-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c133-118">*SD* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7c133-118">*SD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c133-119">二進位位元組陣列格式的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="7c133-119">Security descriptor in binary byte array format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c133-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c133-120">Return value</span></span>

<span data-ttu-id="7c133-121">這個方法會傳回 **HRESULT** ，指出方法呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="7c133-121">This method returns an **HRESULT** indicating the status of the method call.</span></span> <span data-ttu-id="7c133-122">下列清單列出對 **GetSD** 而言很重要的傳回值。</span><span class="sxs-lookup"><span data-stu-id="7c133-122">The following list lists the return values that are of significance to **GetSD**.</span></span> <span data-ttu-id="7c133-123">針對編寫腳本和 Visual Basic 應用程式，可以從 OutParameters 取得結果 [ReturnValue](parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="7c133-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="7c133-124">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="7c133-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="7c133-125">**S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="7c133-125">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="7c133-126">已成功執行方法。</span><span class="sxs-lookup"><span data-stu-id="7c133-126">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="7c133-127">**WBEM \_ E \_ \_ 拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="7c133-127">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="7c133-128">呼叫端沒有足夠的許可權可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7c133-128">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="7c133-129">**\_ \_ \_ 已停用 WBEM E 方法**</span><span class="sxs-lookup"><span data-stu-id="7c133-129">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="7c133-130">嘗試在不支援的系統上執行這個方法。</span><span class="sxs-lookup"><span data-stu-id="7c133-130">Attempted to run this method on an unsupported system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c133-131">備註</span><span class="sxs-lookup"><span data-stu-id="7c133-131">Remarks</span></span>

<span data-ttu-id="7c133-132">如需以程式設計方式或手動方式修改命名空間安全性的詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7c133-132">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7c133-133">範例</span><span class="sxs-lookup"><span data-stu-id="7c133-133">Examples</span></span>

<span data-ttu-id="7c133-134">下列腳本會示範如何使用 **GetSD** 來取得根 Cimv2 命名空間的目前安全描述項 \\ ，並將其變更為 **DisplaySD** 中顯示的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="7c133-134">The following script shows you how to use **GetSD** to obtain the current security descriptor for the Root\\Cimv2 namespace and change it to the byte array shown in **DisplaySD**.</span></span>


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a><span data-ttu-id="7c133-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c133-135">Requirements</span></span>



| <span data-ttu-id="7c133-136">需求</span><span class="sxs-lookup"><span data-stu-id="7c133-136">Requirement</span></span> | <span data-ttu-id="7c133-137">值</span><span class="sxs-lookup"><span data-stu-id="7c133-137">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7c133-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c133-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7c133-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c133-139">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7c133-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c133-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7c133-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c133-141">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7c133-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="7c133-142">Namespace</span></span><br/>                | <span data-ttu-id="7c133-143">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="7c133-143">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7c133-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c133-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c133-145">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="7c133-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="7c133-146">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="7c133-146">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="7c133-147">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="7c133-147">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="7c133-148">**Win32 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="7c133-148">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="7c133-149">**\_\_SystemSecurity::SetSD**</span><span class="sxs-lookup"><span data-stu-id="7c133-149">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="7c133-150">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="7c133-150">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="7c133-151">**Win32 \_ SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7c133-151">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="7c133-152">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="7c133-152">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

