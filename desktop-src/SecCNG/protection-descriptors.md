---
description: 保護描述項規則字串包含一或多個保護裝置的連續清單。
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: 保護描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11814df2af5bd9abee4260f4aadab5bb74c77a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192300"
---
# <a name="protection-descriptors"></a><span data-ttu-id="b5ee2-103">保護描述項</span><span class="sxs-lookup"><span data-stu-id="b5ee2-103">Protection Descriptors</span></span>

<span data-ttu-id="b5ee2-104">保護描述項規則字串包含一或多個保護裝置的連續清單。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-104">A protection descriptor rule string contains a sequential list of one or more protectors.</span></span> <span data-ttu-id="b5ee2-105">至少必須有一個保護裝置。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-105">There must be at least one protector.</span></span> <span data-ttu-id="b5ee2-106">如果有一個以上的保護裝置，則必須以 **和** 或 **或** 分隔字串。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-106">If there is more than one, the protectors must be separated in the string by **AND** or **OR**.</span></span> <span data-ttu-id="b5ee2-107">這些值必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-107">These values must be capitalized.</span></span> <span data-ttu-id="b5ee2-108">下列語法顯示保護描述項的字串格式。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-108">The following syntax shows the string format of a protection descriptor.</span></span>


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



<span data-ttu-id="b5ee2-109">目前可以針對下列類型的授權定義保護描述項：</span><span class="sxs-lookup"><span data-stu-id="b5ee2-109">Protection descriptors can currently be defined for the following types of authorization:</span></span>

-   <span data-ttu-id="b5ee2-110">Active Directory 樹系中的群組。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-110">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="b5ee2-111">一組 web 認證。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-111">A set of web credentials.</span></span>
-   <span data-ttu-id="b5ee2-112">使用者憑證存放區中的憑證。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-112">A certificate in the user's certificate store.</span></span>

<span data-ttu-id="b5ee2-113">Active Directory 群組的保護描述項規則字串的範例包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="b5ee2-113">Examples of protection descriptor rule strings for an Active Directory group include the following:</span></span>

-   <span data-ttu-id="b5ee2-114">"SID = S-1-5-21-4392301 和 SID = S-1-5-21-3101812"</span><span class="sxs-lookup"><span data-stu-id="b5ee2-114">"SID=S-1-5-21-4392301 AND SID=S-1-5-21-3101812"</span></span>
-   <span data-ttu-id="b5ee2-115">"SDDL = O:S-1-5-5-0-290724G： SYD： (A;;CCDC;;;S-1-5-5-0-290724)  (A;;DC;;;WD) 」</span><span class="sxs-lookup"><span data-stu-id="b5ee2-115">"SDDL=O:S-1-5-5-0-290724G:SYD:(A;;CCDC;;;S-1-5-5-0-290724)(A;;DC;;;WD)"</span></span>
-   <span data-ttu-id="b5ee2-116">"LOCAL = user"</span><span class="sxs-lookup"><span data-stu-id="b5ee2-116">"LOCAL=user"</span></span>
-   <span data-ttu-id="b5ee2-117">"LOCAL = machine"</span><span class="sxs-lookup"><span data-stu-id="b5ee2-117">"LOCAL=machine"</span></span>

<span data-ttu-id="b5ee2-118">一組 web 認證的保護描述項規則字串的範例包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="b5ee2-118">Examples of protection descriptor rule strings for a set of web credentials include the following:</span></span>

-   <span data-ttu-id="b5ee2-119">"WEBCREDENTIALS = MyPasswordName"</span><span class="sxs-lookup"><span data-stu-id="b5ee2-119">"WEBCREDENTIALS=MyPasswordName"</span></span>
-   <span data-ttu-id="b5ee2-120">"WEBCREDENTIALS = MyPasswordName，myweb .com"</span><span class="sxs-lookup"><span data-stu-id="b5ee2-120">"WEBCREDENTIALS=MyPasswordName,myweb.com"</span></span>

<span data-ttu-id="b5ee2-121">憑證的保護描述項規則字串範例包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="b5ee2-121">Examples of protection descriptor rule strings for a certificate include the following:</span></span>

-   <span data-ttu-id="b5ee2-122">「憑證 = HashID： \_ \_ 憑證的 sha1 雜湊」 \_</span><span class="sxs-lookup"><span data-stu-id="b5ee2-122">"CERTIFICATE=HashID:sha1\_hash\_of\_certificate"</span></span>
-   <span data-ttu-id="b5ee2-123">"CERTIFICATE = CertBlob： base64String"</span><span class="sxs-lookup"><span data-stu-id="b5ee2-123">"CERTIFICATE=CertBlob:base64String"</span></span>

<span data-ttu-id="b5ee2-124">您指定的保護描述項會自動決定要使用的金鑰保護提供者。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-124">The protection descriptor you specify automatically determines which key protection provider is used.</span></span> <span data-ttu-id="b5ee2-125">如需詳細資訊，請參閱 [保護提供者](protection-providers.md)。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-125">For more information, see [Protection Providers](protection-providers.md).</span></span>

<span data-ttu-id="b5ee2-126">請注意，等號 (=) 的左邊必須是 **SID**、 **SDDL**、 **LOCAL**、 **WEBCREDENTIALS** 或 **CERTIFICATE**。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-126">Note that the left side of the equals sign (=) must be **SID**, **SDDL**, **LOCAL**, **WEBCREDENTIALS**, or **CERTIFICATE**.</span></span> <span data-ttu-id="b5ee2-127">這些值不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-127">These values are not case sensitive.</span></span>

<span data-ttu-id="b5ee2-128">當您呼叫 [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) 函式時，您必須指定規則字串 (或與規則字串相關聯的顯示名稱) 。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-128">You must specify a rule string (or a display name associated with a rule string) when you call the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function.</span></span> <span data-ttu-id="b5ee2-129">或者，因為保護描述項規則字串有點麻煩，所以您可以使用 [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) 函式，將顯示名稱與規則字串建立關聯，並註冊這兩者。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-129">Alternatively, because protection descriptor rule strings are somewhat cumbersome to use and remember, you can associate a display name with the rule string and register both by using the [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) function.</span></span> <span data-ttu-id="b5ee2-130">然後，您可以使用 **NCryptCreateProtectionDescriptor** 中的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b5ee2-130">Then you can use the display name in **NCryptCreateProtectionDescriptor**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5ee2-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5ee2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5ee2-132">CNG DPAPI</span><span class="sxs-lookup"><span data-stu-id="b5ee2-132">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="b5ee2-133">保護提供者</span><span class="sxs-lookup"><span data-stu-id="b5ee2-133">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



