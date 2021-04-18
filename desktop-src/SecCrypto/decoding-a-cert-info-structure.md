---
description: 指定憑證之後，解碼憑證 BLOB 的第一個步驟就是呼叫 CertCreateCertificateCoNtext，將編碼憑證的指標傳遞 (BLOB) 。
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: 解碼 CERT_INFO 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7178c9a5bcfc95a8e2945a6e381f0c2c29cf3b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558535"
---
# <a name="decoding-a-cert_info-structure"></a><span data-ttu-id="6be37-103">解碼 CERT \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="6be37-103">Decoding a CERT\_INFO Structure</span></span>

<span data-ttu-id="6be37-104">指定憑證之後，解碼憑證 [*BLOB*](../secgloss/b-gly.md) 的第一個步驟就是呼叫 [**CertCreateCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)，將編碼憑證的指標傳遞 (*BLOB*) 。</span><span class="sxs-lookup"><span data-stu-id="6be37-104">Given a certificate, the first step in decoding the certificate [*BLOB*](../secgloss/b-gly.md) is to call [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), passing it a pointer to the encoded certificate (*BLOB*).</span></span> <span data-ttu-id="6be37-105">呼叫此函式時，它會建立重複的編碼憑證、建立類型 [**cert \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的結構，並建立 [**cert \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)類型的結構。</span><span class="sxs-lookup"><span data-stu-id="6be37-105">When this function is called, it creates a duplicate of the encoded certificate, creates a structure of type [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context), and creates a structure of type [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info).</span></span> <span data-ttu-id="6be37-106">如下圖所示， [*憑證內容*](../secgloss/c-gly.md) 包含原始憑證 *BLOB*、類型為 **cert \_ CoNtext** 的 c 結構，以及 **cert \_ 資訊** 類型的 c 結構。</span><span class="sxs-lookup"><span data-stu-id="6be37-106">As shown in the following illustration, a [*certificate context*](../secgloss/c-gly.md) includes the original certificate *BLOB*, a C structure of type **CERT\_CONTEXT**, and a C structure of type **CERT\_INFO**.</span></span> <span data-ttu-id="6be37-107">憑證 **\_ 內容** 結構的其中一個成員會指向 **cert \_ 資訊** 結構，而另一個成員會指向編碼的憑證 BLOB。</span><span class="sxs-lookup"><span data-stu-id="6be37-107">One of the members of the **CERT\_CONTEXT** structure points to the **CERT\_INFO** structure and another to the encoded certificate BLOB.</span></span>

![憑證內容](images/certcntx.png)

<span data-ttu-id="6be37-109">編碼的物件 (資料成員) 一律會提供做為 [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) 函數的輸入，而輸出則是 C 結構，可能或可能沒有編碼的成員，這取決於您的進程有多遠。</span><span class="sxs-lookup"><span data-stu-id="6be37-109">The encoded object (data member) is always provided as the input to the [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) function, and the output is a C structure that may or may not have encoded members, depending on how far into the process you are.</span></span>

<span data-ttu-id="6be37-110">另外還有另一個需要解碼的成員，也就是 **延伸** 成員。</span><span class="sxs-lookup"><span data-stu-id="6be37-110">There is one other member that requires some decoding, and that is the **Extension** member.</span></span> <span data-ttu-id="6be37-111">雖然它未編碼于 [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 層級，但它確實包含一些編碼資訊。</span><span class="sxs-lookup"><span data-stu-id="6be37-111">Although it is not encoded at the [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) level, it does contain some encoded information.</span></span> <span data-ttu-id="6be37-112">若要解碼這項資訊，請繼續進行，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="6be37-112">To decode this information, proceed as shown in the following illustration.</span></span>

![解碼資訊](images/xtension.png)

<span data-ttu-id="6be37-114">在 [**cert \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 結構中，成員 **rgExtension** 是憑證 [**\_ 延伸**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) 結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="6be37-114">In the [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) structure, member **rgExtension** is a pointer to an array of [**CERT\_EXTENSION**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) structures.</span></span> <span data-ttu-id="6be37-115">每個憑證 **\_ 延伸** 結構都有以編碼形式提供的 **值** 成員，需要進行解碼。</span><span class="sxs-lookup"><span data-stu-id="6be37-115">Each **CERT\_EXTENSION** structure has a **Value** member that is in encoded form and needs to be decoded.</span></span> <span data-ttu-id="6be37-116">**值** 成員會傳遞至 [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)函式，然後函式的輸出取決於 **pszObjId** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="6be37-116">The **Value** member is passed to the [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) function, and then the output from the function depends on the value of the **pszObjId** member.</span></span> <span data-ttu-id="6be37-117">請注意，在此圖中，會產生兩個不同的結構，其中一個類型 [**cert \_ 基本 \_ 條件約束 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) 和類型 [**cert \_ 授權單位 \_ 金鑰 \_ 識別碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info)，視 **pszObjId** 的值而定。</span><span class="sxs-lookup"><span data-stu-id="6be37-117">Notice that in the illustration, two different structures are produced, one of type [**CERT\_BASIC\_CONSTRAINTS\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) and one of type [**CERT\_AUTHORITY\_KEY\_ID\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info), depending on the value of **pszObjId**.</span></span>

 

 
