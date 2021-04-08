---
description: CryptXML 可讓開發人員藉由註冊整個系統的密碼編譯延伸模組 DLL，擴充原生支援的密碼編譯演算法。
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: XML 數位簽章密碼編譯延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "103853212"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a><span data-ttu-id="d45fd-103">XML 數位簽章密碼編譯延伸模組</span><span class="sxs-lookup"><span data-stu-id="d45fd-103">XML Digital Signature Cryptographic Extensions</span></span>

<span data-ttu-id="d45fd-104">CryptXML 可讓開發人員藉由註冊整個系統的密碼編譯延伸模組 DLL，擴充原生支援的密碼編譯演算法。</span><span class="sxs-lookup"><span data-stu-id="d45fd-104">CryptXML allows developers to extend natively supported cryptographic algorithms by registering a system wide cryptographic extension DLL.</span></span> <span data-ttu-id="d45fd-105">擴充 Dll 會擴充 **SignatureMethod** 和 **DigestMethod** XML 元素所支援的演算法。</span><span class="sxs-lookup"><span data-stu-id="d45fd-105">Extension DLLs extend the algorithms supported by **SignatureMethod** and **DigestMethod** XML elements.</span></span> <span data-ttu-id="d45fd-106">延伸模組 Dll 可支援將其他參數編碼成 XML 數位簽章的演算法。</span><span class="sxs-lookup"><span data-stu-id="d45fd-106">Extension DLLs can support algorithms that encode additional parameters into the XML digital signature.</span></span>

<span data-ttu-id="d45fd-107">所有延伸模組 Dll 都必須支援 [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) 函式，此函式會傳回 [**CRYPT \_ XML 密碼編譯 \_ \_ 介面**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d45fd-107">All extensions DLLs must support the [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) function, which returns a pointer to a [**CRYPT\_XML\_CRYPTOGRAPHIC\_INTERFACE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) structure.</span></span> <span data-ttu-id="d45fd-108">此結構提供函式指標來執行密碼編譯延伸模組函式。</span><span class="sxs-lookup"><span data-stu-id="d45fd-108">This structure provides function pointers to implemented cryptographic extension functions.</span></span> <span data-ttu-id="d45fd-109">支援的函式取決於支援的密碼編譯演算法類型，以及演算法是否必須將參數編碼為 XML 數位簽章。</span><span class="sxs-lookup"><span data-stu-id="d45fd-109">The functions supported depend on the type of cryptographic algorithm supported and whether the algorithm must encode parameters into the XML digital signature.</span></span>

<span data-ttu-id="d45fd-110">密碼編譯延伸模組函式包含下列函式指標：</span><span class="sxs-lookup"><span data-stu-id="d45fd-110">Cryptographic extensions functions include the following function pointers:</span></span>

<dl> <dt>

<span data-ttu-id="d45fd-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>必要函數</span><span class="sxs-lookup"><span data-stu-id="d45fd-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Required functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="d45fd-112">**CryptXmlDllGetInterface**</span><span class="sxs-lookup"><span data-stu-id="d45fd-112">**CryptXmlDllGetInterface**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [<span data-ttu-id="d45fd-113">**CryptXmlDllGetAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="d45fd-113">**CryptXmlDllGetAlgorithmInfo**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span data-ttu-id="d45fd-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest 方法函數</span><span class="sxs-lookup"><span data-stu-id="d45fd-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest Method functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="d45fd-115">**CryptXmlDllCloseDigest**</span><span class="sxs-lookup"><span data-stu-id="d45fd-115">**CryptXmlDllCloseDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [<span data-ttu-id="d45fd-116">**CryptXmlDllCreateDigest**</span><span class="sxs-lookup"><span data-stu-id="d45fd-116">**CryptXmlDllCreateDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [<span data-ttu-id="d45fd-117">**CryptXmlDllDigestData**</span><span class="sxs-lookup"><span data-stu-id="d45fd-117">**CryptXmlDllDigestData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [<span data-ttu-id="d45fd-118">**CryptXmlDllFinalizeDigest**</span><span class="sxs-lookup"><span data-stu-id="d45fd-118">**CryptXmlDllFinalizeDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span data-ttu-id="d45fd-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature 方法函數</span><span class="sxs-lookup"><span data-stu-id="d45fd-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature Method Functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="d45fd-120">**CryptXmlDllSignData**</span><span class="sxs-lookup"><span data-stu-id="d45fd-120">**CryptXmlDllSignData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [<span data-ttu-id="d45fd-121">**CryptXmlDllVerifySignature**</span><span class="sxs-lookup"><span data-stu-id="d45fd-121">**CryptXmlDllVerifySignature**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [<span data-ttu-id="d45fd-122">**CryptXmlDllCreateKey**</span><span class="sxs-lookup"><span data-stu-id="d45fd-122">**CryptXmlDllCreateKey**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [<span data-ttu-id="d45fd-123">**CryptXmlDllEncodeKeyValue**</span><span class="sxs-lookup"><span data-stu-id="d45fd-123">**CryptXmlDllEncodeKeyValue**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span data-ttu-id="d45fd-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>針對具有預設編碼參數的演算法</span><span class="sxs-lookup"><span data-stu-id="d45fd-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>For algorithms with default encoded parameters</span></span>
</dt> <dd>

-   [<span data-ttu-id="d45fd-125">**CryptXmlDllEncodeAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="d45fd-125">**CryptXmlDllEncodeAlgorithm**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

<span data-ttu-id="d45fd-126">密碼編譯延伸模組 Dll 是以全系統為基礎進行註冊。</span><span class="sxs-lookup"><span data-stu-id="d45fd-126">Cryptographic extension DLLs are registered on a system-wide basis.</span></span> <span data-ttu-id="d45fd-127">需要系統管理員許可權才能註冊密碼編譯延伸模組 DLL。</span><span class="sxs-lookup"><span data-stu-id="d45fd-127">Administrator privileges are required to register a cryptographic extension DLL.</span></span>

<span data-ttu-id="d45fd-128">所有 CryptXML 的密碼編譯延伸模組都是由 **SignatureMethod** 或 **DigestMethod** 元素的演算法屬性欄位中設定的 URI 值所註冊。</span><span class="sxs-lookup"><span data-stu-id="d45fd-128">All CryptXML cryptographic extensions are registered by the URI value set in the **SignatureMethod** or the algorithm attribute field of the **DigestMethod** element.</span></span>

<span data-ttu-id="d45fd-129">擴充 Dll 的登錄路徑如下所示：</span><span class="sxs-lookup"><span data-stu-id="d45fd-129">The registry paths for the extension DLLs are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="d45fd-130"><span id="32-bit"></span><span id="32-BIT"></span>bit.msi</span><span class="sxs-lookup"><span data-stu-id="d45fd-130"><span id="32-bit"></span><span id="32-BIT"></span>32-bit</span></span>
</dt> <dd>

<span data-ttu-id="d45fd-131">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **加密** \\ **CryptXML** \\ **URI** \\ *{uri}*</span><span class="sxs-lookup"><span data-stu-id="d45fd-131">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> <dt>

<span data-ttu-id="d45fd-132"><span id="64-bit"></span><span id="64-BIT"></span>64 bit.msi</span><span class="sxs-lookup"><span data-stu-id="d45fd-132"><span id="64-bit"></span><span id="64-BIT"></span>64-bit</span></span>
</dt> <dd>

<span data-ttu-id="d45fd-133">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **加密** \\ **CryptXML** \\ **URI** \\ *{uri}*</span><span class="sxs-lookup"><span data-stu-id="d45fd-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

<span data-ttu-id="d45fd-134">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **WOW6432NODE** \\ **Microsoft** \\ **加密** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="d45fd-134">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**WOW6432NODE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> </dl>

<span data-ttu-id="d45fd-135">每個金鑰都包含下列設定。</span><span class="sxs-lookup"><span data-stu-id="d45fd-135">Each key contains the following settings.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d45fd-136">名稱</span><span class="sxs-lookup"><span data-stu-id="d45fd-136">Name</span></span></th>
<th><span data-ttu-id="d45fd-137">類型</span><span class="sxs-lookup"><span data-stu-id="d45fd-137">Type</span></span></th>
<th><span data-ttu-id="d45fd-138">資料</span><span class="sxs-lookup"><span data-stu-id="d45fd-138">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d45fd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d45fd-139">DLL</span></span><br/></td>
<td><span data-ttu-id="d45fd-140">可擴充的字串</span><span class="sxs-lookup"><span data-stu-id="d45fd-140">Expandable string</span></span><br/></td>
<td><span data-ttu-id="d45fd-141">必要。</span><span class="sxs-lookup"><span data-stu-id="d45fd-141">Required.</span></span><br/><span data-ttu-id="d45fd-142">XML 密碼編譯提供者 DLL 的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="d45fd-142">The absolute path to the XML Cryptographic Provider DLL.</span></span>
<blockquote>
<p><span data-ttu-id="d45fd-143"><b>注意： </b>建議您在只能由具有系統管理許可權的應用程式寫入的目錄中，使用密碼編譯延伸模組 Dll。</span><span class="sxs-lookup"><span data-stu-id="d45fd-143"><b>Note: </b>We recommend that cryptographic extension DLLs be located in directories that can only be written to by applications with administrative privilege.</span></span></p>
<p><span data-ttu-id="d45fd-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> 用來載入密碼編譯延伸模組 DLL。</span><span class="sxs-lookup"><span data-stu-id="d45fd-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> is used to load the cryptographic extension DLL.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d45fd-145">名稱</span><span class="sxs-lookup"><span data-stu-id="d45fd-145">Name</span></span><br/></td>
<td><span data-ttu-id="d45fd-146"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d45fd-146"><strong>String</strong></span></span></td>
<td><span data-ttu-id="d45fd-147">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d45fd-147">Optional.</span></span><br/> <span data-ttu-id="d45fd-148">與此 URI 相關聯的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d45fd-148">The display name associated with this URI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d45fd-149">GroupId</span><span class="sxs-lookup"><span data-stu-id="d45fd-149">GroupId</span></span><br/></td>
<td><span data-ttu-id="d45fd-150"><strong>Dword</strong></span><span class="sxs-lookup"><span data-stu-id="d45fd-150"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="d45fd-151">必要。</span><span class="sxs-lookup"><span data-stu-id="d45fd-151">Required.</span></span><br/> <span data-ttu-id="d45fd-152">與此密碼編譯演算法相關聯的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="d45fd-152">The group identifier associated with this cryptographic algorithm.</span></span> <span data-ttu-id="d45fd-153">可能的值包括下列各項：<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1</span><span class="sxs-lookup"><span data-stu-id="d45fd-153">Possible values include the following:<strong>CRYPT_XML_GROUP_ID_HASH</strong>\<strong></strong> = 1</span></span><br/><span data-ttu-id="d45fd-154"><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong>= 2</span><span class="sxs-lookup"><span data-stu-id="d45fd-154"><strong>CRYPT_XML_GROUP_ID_SIGN</strong>\<strong></strong> = 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d45fd-155">CNGAlgid</span><span class="sxs-lookup"><span data-stu-id="d45fd-155">CNGAlgid</span></span><br/></td>
<td><span data-ttu-id="d45fd-156"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d45fd-156"><strong>String</strong></span></span></td>
<td><span data-ttu-id="d45fd-157">必要。</span><span class="sxs-lookup"><span data-stu-id="d45fd-157">Required.</span></span><br/> <span data-ttu-id="d45fd-158">要傳遞給 BCrypt 或 NCrypt 函數的 CNG 演算法名稱。</span><span class="sxs-lookup"><span data-stu-id="d45fd-158">The CNG algorithm name to be passed to BCrypt or NCrypt functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d45fd-159">CNGExtraAlgid</span><span class="sxs-lookup"><span data-stu-id="d45fd-159">CNGExtraAlgid</span></span><br/></td>
<td><span data-ttu-id="d45fd-160"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d45fd-160"><strong>String</strong></span></span></td>
<td><span data-ttu-id="d45fd-161">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d45fd-161">Optional.</span></span><br/> <span data-ttu-id="d45fd-162">額外的演算法字串，而非 CNGAlgid 成員中的字串，可以傳遞給 CNG 函數。</span><span class="sxs-lookup"><span data-stu-id="d45fd-162">An extra algorithm string, other than the string in the CNGAlgid member, that can be passed to the CNG functions.</span></span><br/> <span data-ttu-id="d45fd-163">針對 (CRYPT_XML_GROUP_ID_SIGN) 的簽章演算法，此成員是要傳遞至 CNG 函數的公開金鑰演算法字串。</span><span class="sxs-lookup"><span data-stu-id="d45fd-163">For the signature algorithms (CRYPT_XML_GROUP_ID_SIGN), this member is the public key algorithm string to pass to the CNG functions.</span></span><br/> <span data-ttu-id="d45fd-164">如果是 GroupId 的其他值，請將<strong>pwszCNGExtraAlgid</strong>成員設為空字串： L &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="d45fd-164">For the other values of GroupId, set the <strong>pwszCNGExtraAlgid</strong> member to the empty string, L&quot;&quot;.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d45fd-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="d45fd-165">Related topics</span></span>

<dl> <span data-ttu-id="d45fd-166"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d45fd-166"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="d45fd-167">XML 數位簽章密碼編譯演算法</span><span class="sxs-lookup"><span data-stu-id="d45fd-167">XML Digital Signature Cryptographic Algorithms</span></span>](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
