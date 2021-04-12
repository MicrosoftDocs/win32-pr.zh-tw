---
description: 使用 CryptoAPI 編碼和解碼憑證內容。
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: 編碼和解碼憑證內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4168d15ad8db5d4711a18f2042106e7d6d46010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191690"
---
# <a name="encoding-and-decoding-a-certificate-context"></a><span data-ttu-id="f327f-103">編碼和解碼憑證內容</span><span class="sxs-lookup"><span data-stu-id="f327f-103">Encoding and Decoding a Certificate Context</span></span>

<span data-ttu-id="f327f-104">[*CryptoAPI*](../secgloss/c-gly.md) 支援 [*憑證*](../secgloss/c-gly.md)的編碼和解碼。</span><span class="sxs-lookup"><span data-stu-id="f327f-104">[*CryptoAPI*](../secgloss/c-gly.md) supports the encoding and decoding of [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="f327f-105">CryptoAPI 包含廣泛、彈性的函式和 C 結構系統，可讓您以各種方式進行編碼和解碼。</span><span class="sxs-lookup"><span data-stu-id="f327f-105">CryptoAPI includes an extensive, flexible system of functions and C structures that allow encoding and decoding in various ways.</span></span> <span data-ttu-id="f327f-106">CryptoAPI 支援標準的 [*x.509*](../secgloss/x-gly.md) 憑證結構和標準 [*抽象語法標記法 (一)*](../secgloss/a-gly.md) (asn.1) 編碼，以提供與其他系統之間的互通性。</span><span class="sxs-lookup"><span data-stu-id="f327f-106">CryptoAPI supports standard [*X.509*](../secgloss/x-gly.md) certificate structure and standard [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1) encoding to provide interoperability with other systems.</span></span>

<span data-ttu-id="f327f-107">如需編碼資料的總覽，請參閱 [編碼和解碼的資料](encoded-and-decoded-data.md)。</span><span class="sxs-lookup"><span data-stu-id="f327f-107">For an overview of encoded data, see [Encoded and Decoded Data](encoded-and-decoded-data.md).</span></span>

## <a name="certificate-contexts"></a><span data-ttu-id="f327f-108">憑證內容</span><span class="sxs-lookup"><span data-stu-id="f327f-108">Certificate Contexts</span></span>

<span data-ttu-id="f327f-109">[*憑證內容*](../secgloss/c-gly.md)（ [**CERT \_ coNtext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)）是包含編碼成員的 C 結構、[*憑證存放區*](../secgloss/c-gly.md)的控制碼、原始編碼 [*憑證 BLOB*](../secgloss/c-gly.md)的指標，以及 [**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)C 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f327f-109">A [*certificate context*](../secgloss/c-gly.md), [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context), is a C structure that contains an encoded member, a handle to a [*certificate store*](../secgloss/c-gly.md), a pointer to the original encoded [*certificate BLOB*](../secgloss/c-gly.md), and a pointer to a [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) C structure.</span></span>

<span data-ttu-id="f327f-110">[**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)結構是憑證的核心。</span><span class="sxs-lookup"><span data-stu-id="f327f-110">The [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) structure is the heart of the certificate.</span></span> <span data-ttu-id="f327f-111">它包含以直接形式與編碼形式的憑證中的所有基本資訊。</span><span class="sxs-lookup"><span data-stu-id="f327f-111">It contains, in direct form and in encoded form, all the basic information in the certificate.</span></span> <span data-ttu-id="f327f-112">下圖顯示 **CERT \_ 資訊** 結構，其中所有編碼的成員都顯示為陰影。</span><span class="sxs-lookup"><span data-stu-id="f327f-112">The following illustration shows the **CERT\_INFO** structure with all of its encoded members shown as shaded.</span></span>

![cert \- 資訊結構](images/certinf2.png)

<span data-ttu-id="f327f-114">**IssuerUniqueID** 和 **SubjectUniqueID** 成員是 [*x.509*](../secgloss/x-gly.md)第2版憑證的一部分，但很少使用。</span><span class="sxs-lookup"><span data-stu-id="f327f-114">The **IssuerUniqueID** and **SubjectUniqueID** members are part of the [*X.509*](../secgloss/x-gly.md) version 2 certificate implementation but are seldom used.</span></span> <span data-ttu-id="f327f-115">第3版中的憑證擴充取代這些成員的功能。</span><span class="sxs-lookup"><span data-stu-id="f327f-115">Certificate extensions in version 3 replace the functionality of these members.</span></span>

<span data-ttu-id="f327f-116">如果編碼 (所包含的資訊已加上陰影) 成員 **簽發者** 和 **主體** ，則必須將這些成員解碼。</span><span class="sxs-lookup"><span data-stu-id="f327f-116">If the information contained in the encoded (shaded) members **Issuer** and **Subject** is needed, those members must be decoded.</span></span> <span data-ttu-id="f327f-117">使用 [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) 來解碼這些成員。</span><span class="sxs-lookup"><span data-stu-id="f327f-117">Use [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) to decode these members.</span></span> <span data-ttu-id="f327f-118">下圖顯示解碼其中一個成員的流程。</span><span class="sxs-lookup"><span data-stu-id="f327f-118">The following illustration shows the process of decoding one of these members.</span></span>

![使用 cryptdecodeobject 解碼](images/infoflow.png)

<span data-ttu-id="f327f-120">在說明的案例中， [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) 函數會建立 [**憑證 \_ 名稱 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) 結構、 [**cert \_ rdn**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) 結構的陣列、憑證 [**\_ rdn \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) 結構的對應陣列，以及包含名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="f327f-120">In the illustrated case, the [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) function creates a [**CERT\_NAME\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) structure, an array of [**CERT\_RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) structures, a corresponding array of [**CERT\_RDN\_ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) structures, and a string that contains the name.</span></span> <span data-ttu-id="f327f-121">**CERT \_ RDN \_ ATTR** 結構的成員會決定字串的內容。</span><span class="sxs-lookup"><span data-stu-id="f327f-121">Members of the **CERT\_RDN\_ATTR** structure determine the contents of the string.</span></span> <span data-ttu-id="f327f-122">例如，如果 **pszObjId** 成員是2.5.4.3，字串就會包含一般名稱。</span><span class="sxs-lookup"><span data-stu-id="f327f-122">For example, if the **pszObjId** member is 2.5.4.3, the string contains a common name.</span></span> <span data-ttu-id="f327f-123">如果是2.5.4.10，則字串會包含組織名稱。</span><span class="sxs-lookup"><span data-stu-id="f327f-123">If it is 2.5.4.10, the string would contain an organization name.</span></span> <span data-ttu-id="f327f-124">如需 (Oid) 的 [*物件識別碼*](../secgloss/o-gly.md) 清單，請參閱 **CERT \_ RDN \_ ATTR**。</span><span class="sxs-lookup"><span data-stu-id="f327f-124">For a list of these [*object identifiers*](../secgloss/o-gly.md) (OIDs), see **CERT\_RDN\_ATTR**.</span></span>

<span data-ttu-id="f327f-125">**DwValueType** 成員包含有關字串類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="f327f-125">The **dwValueType** member contains information about the type of string.</span></span> <span data-ttu-id="f327f-126">如果它是 CERT \_ RDN \_ 可列印 \_ 字串，則值成員會包含位元組寬度、以零結束的字元字串。</span><span class="sxs-lookup"><span data-stu-id="f327f-126">If it is CERT\_RDN\_PRINTABLE\_STRING, the value member contains a byte-width, zero-terminated character string.</span></span> <span data-ttu-id="f327f-127">如果它是 CERT \_ RDN \_ UNICODE \_ 字串，則字串會是雙寬度 (文字大小) 字元字串。</span><span class="sxs-lookup"><span data-stu-id="f327f-127">If it is CERT\_RDN\_UNICODE\_STRING, the string is a double-width (word-sized) character string.</span></span>

<span data-ttu-id="f327f-128">如需編碼和解碼憑證的詳細程式，請參閱 [編碼憑證 \_ 資訊結構](encoding-a-cert-info-structure.md) 和 [解碼 cert \_ 資訊結構](decoding-a-cert-info-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="f327f-128">For a detailed process for encoding and decoding certificates, see [Encoding a CERT\_INFO Structure](encoding-a-cert-info-structure.md) and [Decoding a CERT\_INFO Structure](decoding-a-cert-info-structure.md).</span></span>

 

 
