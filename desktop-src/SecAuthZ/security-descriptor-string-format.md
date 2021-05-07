---
description: 安全描述項字串格式是在安全描述項中儲存或傳輸資訊的文字格式。
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: 安全描述項字串格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7fd6e9e2387deee63b5046086ed167a29fa54b
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644200"
---
# <a name="security-descriptor-string-format"></a><span data-ttu-id="2810f-103">安全描述項字串格式</span><span class="sxs-lookup"><span data-stu-id="2810f-103">Security Descriptor String Format</span></span>

<span data-ttu-id="2810f-104">**安全描述項字串格式** 是在安全描述項中儲存或傳輸資訊的文字格式。</span><span class="sxs-lookup"><span data-stu-id="2810f-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="2810f-105">[**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)函數會使用此格式。</span><span class="sxs-lookup"><span data-stu-id="2810f-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="2810f-106">格式是以 **null** 終止的字串，其標記會指出安全描述項的四個主要元件：擁有者 (O： ) 、主要群組 (G： ) 、DACL (D： ) 和 SACL (S： ) 。</span><span class="sxs-lookup"><span data-stu-id="2810f-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="2810f-107"> (Ace) 和條件式 Ace 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)具有不同的格式。</span><span class="sxs-lookup"><span data-stu-id="2810f-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="2810f-108">針對 Ace，請參閱 [Ace 字串](ace-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="2810f-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="2810f-109">針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。</span><span class="sxs-lookup"><span data-stu-id="2810f-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="2810f-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>擁有者 \_ sid</span><span class="sxs-lookup"><span data-stu-id="2810f-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="2810f-111">識別物件擁有者的 [SID 字串](sid-strings.md) 。</span><span class="sxs-lookup"><span data-stu-id="2810f-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="2810f-112"><span id="group_sid"></span><span id="GROUP_SID"></span>群組 \_ sid</span><span class="sxs-lookup"><span data-stu-id="2810f-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="2810f-113">識別物件主要群組的 SID 字串。</span><span class="sxs-lookup"><span data-stu-id="2810f-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="2810f-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="2810f-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="2810f-115">適用于 DACL 的安全描述項控制旗標。</span><span class="sxs-lookup"><span data-stu-id="2810f-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="2810f-116">如需這些控制項旗標的說明，請參閱 [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="2810f-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="2810f-117">Dacl \_ 旗標字串可以是零或多個下列字串的串連。</span><span class="sxs-lookup"><span data-stu-id="2810f-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="2810f-118">控制</span><span class="sxs-lookup"><span data-stu-id="2810f-118">Control</span></span>               | <span data-ttu-id="2810f-119">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="2810f-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="2810f-120">意義</span><span class="sxs-lookup"><span data-stu-id="2810f-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="2810f-121">曲線</span><span class="sxs-lookup"><span data-stu-id="2810f-121">"P"</span></span>                   | <span data-ttu-id="2810f-122">SDDL \_ 受保護</span><span class="sxs-lookup"><span data-stu-id="2810f-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="2810f-123">\_已設定「SE DACL \_ 保護」旗標。</span><span class="sxs-lookup"><span data-stu-id="2810f-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="2810f-124">款</span><span class="sxs-lookup"><span data-stu-id="2810f-124">"AR"</span></span>                  | <span data-ttu-id="2810f-125">SDDL \_ 自動 \_ 繼承 \_ 需求</span><span class="sxs-lookup"><span data-stu-id="2810f-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="2810f-126">\_ \_ 已設定 SE DACL AUTO \_ INHERIT 要求旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2810f-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="2810f-127">AI</span><span class="sxs-lookup"><span data-stu-id="2810f-127">"AI"</span></span>                  | <span data-ttu-id="2810f-128">SDDL \_ 自動 \_ 繼承</span><span class="sxs-lookup"><span data-stu-id="2810f-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="2810f-129">\_已設定「SE DACL \_ 自動 \_ 繼承」旗標。</span><span class="sxs-lookup"><span data-stu-id="2810f-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="2810f-130">「沒有 \_ 訪問 \_ 控制」</span><span class="sxs-lookup"><span data-stu-id="2810f-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="2810f-131">SDDL \_ Null \_ ACL</span><span class="sxs-lookup"><span data-stu-id="2810f-131">SDDL\_NULL\_ACL</span></span>          | <span data-ttu-id="2810f-132">ACL 為 null。</span><span class="sxs-lookup"><span data-stu-id="2810f-132">The ACL is null.</span></span> <span data-ttu-id="2810f-133">**Windows server 2008、Windows Vista 和 Windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="2810f-133">**Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2810f-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="2810f-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="2810f-135">適用于 SACL 的安全描述項控制旗標。</span><span class="sxs-lookup"><span data-stu-id="2810f-135">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="2810f-136">Sacl \_ 旗標字串會使用與 dacl 旗標字串相同的控制項位字串 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2810f-136">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="2810f-137"><span id="string_ace"></span><span id="STRING_ACE"></span>字串 \_ ace</span><span class="sxs-lookup"><span data-stu-id="2810f-137"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="2810f-138">描述安全描述項 DACL 或 SACL 中之 ACE 的字串。</span><span class="sxs-lookup"><span data-stu-id="2810f-138">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="2810f-139">如需 ACE 字串格式的描述，請參閱 [ace 字串](ace-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="2810f-139">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="2810f-140">每個 ACE 字串都會以括弧括住 ( () ) 。</span><span class="sxs-lookup"><span data-stu-id="2810f-140">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="2810f-141">您可以從安全描述項字串省略不必要的元件。</span><span class="sxs-lookup"><span data-stu-id="2810f-141">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="2810f-142">例如，如果 \_ \_ 輸入安全描述項中未設定「SE DACL」旗標， [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 不會在輸出字串中包含 D：元件。</span><span class="sxs-lookup"><span data-stu-id="2810f-142">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="2810f-143">您也可以使用 [**安全性 \_ 資訊**](security-information.md) 位旗標，來指出要包含在安全描述項字串中的元件。</span><span class="sxs-lookup"><span data-stu-id="2810f-143">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="2810f-144">安全描述項字串格式不支援 **Null** acl。</span><span class="sxs-lookup"><span data-stu-id="2810f-144">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="2810f-145">為了表示空的 ACL，安全描述項字串包含 D：或 S： token，沒有其他字串資訊。</span><span class="sxs-lookup"><span data-stu-id="2810f-145">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="2810f-146">安全描述項字串會以不同的方式儲存 [**安全描述項控制項**](security-descriptor-control.md) 位。</span><span class="sxs-lookup"><span data-stu-id="2810f-146">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="2810f-147">出現「SE \_ DACL」 \_ 或「se SACL」 \_ \_ 存在位的方式，是以字串中的 D：或 S： token 存在的方式表示。</span><span class="sxs-lookup"><span data-stu-id="2810f-147">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="2810f-148">適用于 DACL 或 SACL 的其他位會儲存在 dacl \_ 旗標和 sacl \_ 旗標中。</span><span class="sxs-lookup"><span data-stu-id="2810f-148">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="2810f-149">「SE \_ 擁有者」 \_ 預設、「se \_ 群組 \_ 預設」、「se DACL 預設」 \_ 和「 \_ se \_ SACL \_ 預設位」都不會儲存在安全描述項字串中。</span><span class="sxs-lookup"><span data-stu-id="2810f-149">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="2810f-150">SE \_ 本身的 \_ 相對位不會儲存在字串中，但 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 一律會在輸出安全描述項中設定此位。</span><span class="sxs-lookup"><span data-stu-id="2810f-150">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="2810f-151">下列範例顯示安全描述項字串以及相關聯安全描述項中的資訊。</span><span class="sxs-lookup"><span data-stu-id="2810f-151">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="2810f-152">字串1：</span><span class="sxs-lookup"><span data-stu-id="2810f-152">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="2810f-153">安全描述項1：</span><span class="sxs-lookup"><span data-stu-id="2810f-153">Security Descriptor 1:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0004
        SE_DACL_PRESENT
    Owner: (S-1-5-32-548)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x02
    Size:     0x001c
    AceCount: 0x0001
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x100e003f
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            GENERIC_ALL
                            Others(0x0000003f)
        Ace Sid      : (S-1-0-0)
SACL
    Not present
```



<span data-ttu-id="2810f-154">字串2：</span><span class="sxs-lookup"><span data-stu-id="2810f-154">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="2810f-155">安全描述項2：</span><span class="sxs-lookup"><span data-stu-id="2810f-155">Security Descriptor 2:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0014
        SE_DACL_PRESENT
        SE_SACL_PRESENT
    Owner: (S-1-5-21-397955417-626881126-188441444-512)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x04
    Size:     0x0104
    AceCount: 0x0007
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-18)
    Ace[01]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0024
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-21-397955417-626881126-188441444-512)
    Ace[02]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_USER
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[03]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_GROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[04]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_LOCALGROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[05]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_PRINT_QUEUE
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-550)
    Ace[06]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x00020014
                            READ_CONTROL
                            Others(0x00000014)
        Ace Sid:       (S-1-5-11)
    SACL
        Revision: 0x02
        Size:     0x001c
        AceCount: 0x0001
        Ace[00]
            AceType:       0x02 (SYSTEM_AUDIT_ACE_TYPE)
            AceSize:       0x0014
            InheritFlags:  0xc0
                SUCCESSFUL_ACCESS_ACE_FLAG
                FAILED_ACCESS_ACE_FLAG
            Access Mask:    0x000d002b
                                DELETE
                                WRITE_DAC
                                WRITE_OWNER
                                Others(0x0000002b)
            Ace Sid:       (S-1-1-0)
```



## <a name="related-topics"></a><span data-ttu-id="2810f-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="2810f-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2810f-157">ACE 字串</span><span class="sxs-lookup"><span data-stu-id="2810f-157">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="2810f-158">條件式 Ace 的安全描述項定義語言</span><span class="sxs-lookup"><span data-stu-id="2810f-158">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
