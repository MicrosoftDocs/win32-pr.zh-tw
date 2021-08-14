---
description: 保護描述項規則字串包含一或多個保護裝置的連續清單。
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: 保護描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e99d4ec8de08ad2f657d2b3ac1992ce6e399ede277f8fde3e12f0732571b01a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907250"
---
# <a name="protection-descriptors"></a>保護描述項

保護描述項規則字串包含一或多個保護裝置的連續清單。 至少必須有一個保護裝置。 如果有一個以上的保護裝置，則必須以 **和** 或 **或** 分隔字串。 這些值必須為大寫。 下列語法顯示保護描述項的字串格式。


```C++
Descriptor = [ Protector-or
              *( OR-separator Protector-or ) ]

    Protector-or = Protector-and
              *( AND-separator Protector-and )

    OR-separator = "OR"
    AND-separator = "AND"

    Protector-and = providerName EQUALS providerAttributes

    providerName = descr

    providerAttribute = string | hexstring

      ; The following characters are to be escaped when they appear
      ; in the value to be encoded: ESC, one of <escaped>, leading
      ; SHARP or SPACE, trailing SPACE, and NULL.
      string =   [ ( leadchar / pair ) [ *( stringchar / pair )
         ( trailchar / pair ) ] ]

      leadchar = LUTF1 / UTFMB
      LUTF1 = %x01-1F / %x21 / %x24-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      trailchar  = TUTF1 / UTFMB
      TUTF1 = %x01-1F / %x21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      stringchar = SUTF1 / UTFMB
      SUTF1 = %x01-21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      pair = ESC ( ESC / special / hexpair )
      special = escaped / SPACE / SHARP / EQUALS
      escaped = DQUOTE / PLUS / COMMA / SEMI / LANGLE / RANGLE
      hexstring = SHARP 1*hexpair
      hexpair = HEX HEX

      descr   = leadkeychar *keychar
      leadkeychar = ALPHA
      keychar = ALPHA / DIGIT / HYPHEN
      number  = DIGIT / ( LDIGIT 1*DIGIT )

      ALPHA   = %x41-5A / %x61-7A   ; "A"-"Z" / "a"-"z"
      DIGIT   = %x30 / LDIGIT       ; "0"-"9"
      LDIGIT  = %x31-39             ; "1"-"9"
      HEX     = DIGIT / %x41-46 / %x61-66 ; "0"-"9" / "A"-"F" / "a"-"f"

      NULL    = %x00 ; null (0)
      SPACE   = %x20 ; space (" ")
      DQUOTE  = %x22 ; quote (""")
      SHARP   = %x23 ; octothorpe (or sharp sign) ("#")
      DOLLAR  = %x24 ; dollar sign ("$")
      SQUOTE  = %x27 ; single quote ("'")
      LPAREN  = %x28 ; left paren ("(")
      RPAREN  = %x29 ; right paren (")")
      PLUS    = %x2B ; plus sign ("+")
      COMMA   = %x2C ; comma (",")
      HYPHEN  = %x2D ; hyphen ("-")
      DOT     = %x2E ; period (".")
      SEMI    = %x3B ; semicolon (";")
      LANGLE  = %x3C ; left angle bracket ("<")
      EQUALS  = %x3D ; equals sign ("=")
      RANGLE  = %x3E ; right angle bracket (">")
      ESC     = %x5C ; backslash ("\")
      USCORE  = %x5F ; underscore ("_")
      LCURLY  = %x7B ; left curly brace "{"
      RCURLY  = %x7D ; right curly brace "}"

      ; Any UTF-8 [RFC3629] encoded Unicode [Unicode] character
      UTF8    = UTF1 / UTFMB
      UTFMB   = UTF2 / UTF3 / UTF4
      UTF0    = %x80-BF
      UTF1    = %x00-7F
      UTF2    = %xC2-DF UTF0
      UTF3    = %xE0 %xA0-BF UTF0 / %xE1-EC 2(UTF0) /
                %xED %x80-9F UTF0 / %xEE-EF 2(UTF0)
      UTF4    = %xF0 %x90-BF 2(UTF0) / %xF1-F3 3(UTF0) /
                %xF4 %x80-8F 2(UTF0)

      OCTET   = %x00-FF ; Any octet (8-bit data unit)
```



目前可以針對下列類型的授權定義保護描述項：

-   Active Directory 樹系中的群組。
-   一組 web 認證。
-   使用者憑證存放區中的憑證。

Active Directory 群組的保護描述項規則字串的範例包括下列各項：

-   "SID = S-1-5-21-4392301 和 SID = S-1-5-21-3101812"
-   "SDDL = O:S-1-5-5-0-290724G： SYD： (A;;CCDC;;;S-1-5-5-0-290724)  (A;;DC;;;WD) 」
-   "LOCAL = user"
-   "LOCAL = machine"

一組 web 認證的保護描述項規則字串的範例包括下列各項：

-   "WEBCREDENTIALS = MyPasswordName"
-   "WEBCREDENTIALS = MyPasswordName，myweb .com"

憑證的保護描述項規則字串範例包括下列各項：

-   「憑證 = HashID： \_ \_ 憑證的 sha1 雜湊」 \_
-   "CERTIFICATE = CertBlob： base64String"

您指定的保護描述項會自動決定要使用的金鑰保護提供者。 如需詳細資訊，請參閱 [保護提供者](protection-providers.md)。

請注意，等號 (=) 的左邊必須是 **SID**、 **SDDL**、 **LOCAL**、 **WEBCREDENTIALS** 或 **CERTIFICATE**。 這些值不會區分大小寫。

當您呼叫 [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) 函式時，您必須指定規則字串 (或與規則字串相關聯的顯示名稱) 。 或者，因為保護描述項規則字串有點麻煩，所以您可以使用 [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) 函式，將顯示名稱與規則字串建立關聯，並註冊這兩者。 然後，您可以使用 **NCryptCreateProtectionDescriptor** 中的顯示名稱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[保護提供者](protection-providers.md)
</dt> </dl>

 

 



