---
description: PKCS 10 憑證要求的 [主旨] 欄位 \# 包含要求憑證之實體的分辨名稱。
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Subject Names
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 226c294e75477a3960cd0ad824a98b3556c34322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989482"
---
# <a name="subject-names"></a><span data-ttu-id="310e6-103">Subject Names</span><span class="sxs-lookup"><span data-stu-id="310e6-103">Subject Names</span></span>

<span data-ttu-id="310e6-104">PKCS 10 憑證要求的 [主旨 **] 欄位** \# 包含要求憑證之實體的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="310e6-104">The **subject** field of a PKCS \#10 certificate request contains the distinguished name of the entity requesting the certificate.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

<span data-ttu-id="310e6-105">辨別名稱是由一系列 (RDNs) 的相對辨別名稱所組成。</span><span class="sxs-lookup"><span data-stu-id="310e6-105">The distinguished name consists of a sequence of relative distinguished names (RDNs).</span></span> <span data-ttu-id="310e6-106">每個 RDN 都包含一組屬性，而每個屬性都是由物件識別碼和值所組成。</span><span class="sxs-lookup"><span data-stu-id="310e6-106">Each RDN consists of a set of attributes, and each attribute consists of an object identifier and a value.</span></span> <span data-ttu-id="310e6-107">值的資料類型是由 **DirectoryString** 結構所識別。</span><span class="sxs-lookup"><span data-stu-id="310e6-107">The data type of the value is identified by the **DirectoryString** structure.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="310e6-108">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="310e6-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="310e6-109">建立主體名稱</span><span class="sxs-lookup"><span data-stu-id="310e6-109">Creating a Subject Name</span></span>](creating-a-subject-name.md)
-   [<span data-ttu-id="310e6-110">編碼主體名稱</span><span class="sxs-lookup"><span data-stu-id="310e6-110">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)

## <a name="related-topics"></a><span data-ttu-id="310e6-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="310e6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="310e6-112">要求</span><span class="sxs-lookup"><span data-stu-id="310e6-112">Requests</span></span>](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
