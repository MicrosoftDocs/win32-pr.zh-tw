---
description: 安全描述項字串格式是在安全描述項中儲存或傳輸資訊的文字格式。
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: 安全描述項字串格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5182de796ee8d3c61f079d3704ab29ad552457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848236"
---
# <a name="security-descriptor-string-format"></a>安全描述項字串格式

**安全描述項字串格式** 是在安全描述項中儲存或傳輸資訊的文字格式。 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)函數會使用此格式。

格式是以 **null** 終止的字串，其標記會指出安全描述項的四個主要元件：擁有者 (O： ) 、主要群組 (G： ) 、DACL (D： ) 和 SACL (S： ) 。

> [!Note]  
>  (Ace) 和條件式 Ace 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)具有不同的格式。 針對 Ace，請參閱 [Ace 字串](ace-strings.md)。 針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span id="owner_sid"></span><span id="OWNER_SID"></span>擁有者 \_ sid
</dt> <dd>

識別物件擁有者的 [SID 字串](sid-strings.md) 。

</dd> <dt>

<span id="group_sid"></span><span id="GROUP_SID"></span>群組 \_ sid
</dt> <dd>

識別物件主要群組的 SID 字串。

</dd> <dt>

<span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl \_ 旗標
</dt> <dd>

適用于 DACL 的安全描述項控制旗標。 如需這些控制項旗標的說明，請參閱 [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) 函數。 Dacl \_ 旗標字串可以是零或多個下列字串的串連。



| 控制               | Sddl 中的常數       | 意義                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| 曲線                   | SDDL \_ 受保護          | \_已設定「SE DACL \_ 保護」旗標。          |
| 款                  | SDDL \_ 自動 \_ 繼承 \_ 需求 | \_ \_ 已設定 SE DACL AUTO \_ INHERIT 要求旗標 \_ 。 |
| AI                  | SDDL \_ 自動 \_ 繼承    | \_已設定「SE DACL \_ 自動 \_ 繼承」旗標。    |
| 「沒有 \_ 訪問 \_ 控制」 | SSDL \_ Null \_ ACL          | ACL 為 null。                              |



 

</dd> <dt>

<span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl \_ 旗標
</dt> <dd>

適用于 SACL 的安全描述項控制旗標。 Sacl \_ 旗標字串會使用與 dacl 旗標字串相同的控制項位字串 \_ 。

</dd> <dt>

<span id="string_ace"></span><span id="STRING_ACE"></span>字串 \_ ace
</dt> <dd>

描述安全描述項 DACL 或 SACL 中之 ACE 的字串。 如需 ACE 字串格式的描述，請參閱 [ace 字串](ace-strings.md)。 每個 ACE 字串都會以括弧括住 ( () ) 。

</dd> </dl>

您可以從安全描述項字串省略不必要的元件。 例如，如果 \_ \_ 輸入安全描述項中未設定「SE DACL」旗標， [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 不會在輸出字串中包含 D：元件。 您也可以使用 [**安全性 \_ 資訊**](security-information.md) 位旗標，來指出要包含在安全描述項字串中的元件。

安全描述項字串格式不支援 **Null** acl。

為了表示空的 ACL，安全描述項字串包含 D：或 S： token，沒有其他字串資訊。

安全描述項字串會以不同的方式儲存 [**安全描述項控制項**](security-descriptor-control.md) 位。 出現「SE \_ DACL」 \_ 或「se SACL」 \_ \_ 存在位的方式，是以字串中的 D：或 S： token 存在的方式表示。 適用于 DACL 或 SACL 的其他位會儲存在 dacl \_ 旗標和 sacl \_ 旗標中。 「SE \_ 擁有者」 \_ 預設、「se \_ 群組 \_ 預設」、「se DACL 預設」 \_ 和「 \_ se \_ SACL \_ 預設位」都不會儲存在安全描述項字串中。 SE \_ 本身的 \_ 相對位不會儲存在字串中，但 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 一律會在輸出安全描述項中設定此位。

下列範例顯示安全描述項字串以及相關聯安全描述項中的資訊。

字串1：


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



安全描述項1：


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



字串2：


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



安全描述項2：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ACE 字串](ace-strings.md)
</dt> <dt>

[條件式 Ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
