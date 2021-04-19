---
description: CryptXML 提供一組低層級的 Api，可讓應用程式建立及驗證信封、封套和卸離的簽章。 您可以使用 CryptXML 來建立及驗證儲存在 signature 物件元素中的內容，包括資訊清單。
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: XML 數位簽章 API 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989437"
---
# <a name="xml-digital-signature-api-functionality"></a><span data-ttu-id="961d1-104">XML 數位簽章 API 功能</span><span class="sxs-lookup"><span data-stu-id="961d1-104">XML Digital Signature API Functionality</span></span>

<span data-ttu-id="961d1-105">CryptXML 提供一組低層級的 Api，可讓應用程式建立及驗證信封、封套和卸離的簽章。</span><span class="sxs-lookup"><span data-stu-id="961d1-105">CryptXML provides a low level set of APIs that allow applications to create and verify enveloped, enveloping, and detached signatures.</span></span> <span data-ttu-id="961d1-106">您可以使用 CryptXML 來建立及驗證儲存在 signature 物件元素中的內容，包括資訊清單。</span><span class="sxs-lookup"><span data-stu-id="961d1-106">You can use CryptXML to create and verify content stored in signature object elements, including manifests.</span></span> <span data-ttu-id="961d1-107">公開/私用、共用金鑰或 [*x.509*](../secgloss/x-gly.md) 憑證或憑證鏈可以用來簽署和驗證 XML [*數位簽章*](../secgloss/d-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="961d1-107">A public/private, shared key, or an [*X.509*](../secgloss/x-gly.md) certificate or certificate chain can be used to sign and verify the XML [*digital signature*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="961d1-108">使用 CryptXML 來驗證外部參考的應用程式 (以檔內容以外的外部檔或檔案為目標的參考，) 必須解析外部 Uri 並取出要子集的資料。</span><span class="sxs-lookup"><span data-stu-id="961d1-108">Applications that use CryptXML to verify external references (references that target an external document or file outside of the document context) must resolve the external URIs and retrieve the data to be digested.</span></span>

<span data-ttu-id="961d1-109">如需 CryptXML 所支援的密碼編譯演算法的詳細資訊，請參閱 [XML 數位簽章密碼編譯演算法](xml-digital-signature-cryptographic-algorithms.md)。</span><span class="sxs-lookup"><span data-stu-id="961d1-109">For information about the cryptographic algorithms supported by CryptXML, see [XML Digital Signature Cryptographic Algorithms](xml-digital-signature-cryptographic-algorithms.md).</span></span>

<span data-ttu-id="961d1-110">CryptXML 可支援具有下列識別碼的標準化演算法。</span><span class="sxs-lookup"><span data-stu-id="961d1-110">CryptXML provides support for the canonicalization algorithms with the following identifiers.</span></span>



| <span data-ttu-id="961d1-111">常數</span><span class="sxs-lookup"><span data-stu-id="961d1-111">Constant</span></span>                                              | <span data-ttu-id="961d1-112">URI 值</span><span class="sxs-lookup"><span data-stu-id="961d1-112">URI value</span></span>                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="961d1-113">wszURI \_ 標準化 \_ C14N</span><span class="sxs-lookup"><span data-stu-id="961d1-113">wszURI\_CANONICALIZATION\_C14N</span></span><br/>             | <span data-ttu-id="961d1-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span><span class="sxs-lookup"><span data-stu-id="961d1-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span></span><br/>               |
| <span data-ttu-id="961d1-115">wszURI \_ 標準化 \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="961d1-115">wszURI\_CANONICALIZATION\_C14NC</span></span><br/>            | <span data-ttu-id="961d1-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="961d1-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span></span><br/> |
| <span data-ttu-id="961d1-117">wszURI \_ 標準化 \_ EXSLUSIVE \_ C14N</span><span class="sxs-lookup"><span data-stu-id="961d1-117">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14N</span></span><br/>  | <span data-ttu-id="961d1-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span><span class="sxs-lookup"><span data-stu-id="961d1-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span></span><br/>                      |
| <span data-ttu-id="961d1-119">wszURI \_ 標準化 \_ EXSLUSIVE \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="961d1-119">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14NC</span></span><br/> | <span data-ttu-id="961d1-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="961d1-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span></span><br/>          |



 

<span data-ttu-id="961d1-121">CryptXML 提供封裝簽章轉換的支援。</span><span class="sxs-lookup"><span data-stu-id="961d1-121">CryptXML provides support for the enveloped signature transform.</span></span>



| <span data-ttu-id="961d1-122">常數</span><span class="sxs-lookup"><span data-stu-id="961d1-122">Constant</span></span>                                       | <span data-ttu-id="961d1-123">URI 值</span><span class="sxs-lookup"><span data-stu-id="961d1-123">URI value</span></span>                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="961d1-124">wszURI \_ XMLNS \_ 轉換的 \_ 封包</span><span class="sxs-lookup"><span data-stu-id="961d1-124">wszURI\_XMLNS\_TRANSFORM\_ENVELOPED</span></span><br/> | <span data-ttu-id="961d1-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span><span class="sxs-lookup"><span data-stu-id="961d1-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span></span><br/> |



 

<span data-ttu-id="961d1-126">根據預設，CryptXML 不支援 XPath 或 XSLT 轉換。</span><span class="sxs-lookup"><span data-stu-id="961d1-126">By default, CryptXML does not support XPath or XSLT transforms.</span></span> <span data-ttu-id="961d1-127">如有必要，應用程式可以在 CryptXML 上執行這些轉換。</span><span class="sxs-lookup"><span data-stu-id="961d1-127">If required, applications can implement these transforms on top of CryptXML.</span></span>

 

 
