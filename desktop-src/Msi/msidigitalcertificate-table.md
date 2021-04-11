---
description: MsiDigitalCertificate 資料表會以二進位資料流程格式儲存憑證，並將每個憑證與主鍵產生關聯。
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: MsiDigitalCertificate 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4765dee433cfab989e79c7ef4663d8939381ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692384"
---
# <a name="msidigitalcertificate-table"></a><span data-ttu-id="84ff7-103">MsiDigitalCertificate 資料表</span><span class="sxs-lookup"><span data-stu-id="84ff7-103">MsiDigitalCertificate Table</span></span>

<span data-ttu-id="84ff7-104">MsiDigitalCertificate 資料表會以二進位資料流程格式儲存憑證，並將每個憑證與主鍵產生關聯。</span><span class="sxs-lookup"><span data-stu-id="84ff7-104">The MsiDigitalCertificate table stores certificates in binary stream format and associates each certificate with a primary key.</span></span> <span data-ttu-id="84ff7-105">主要金鑰是用來在多個數位簽署的物件之間共用憑證。</span><span class="sxs-lookup"><span data-stu-id="84ff7-105">The primary key is used to share certificates among multiple digitally signed objects.</span></span> <span data-ttu-id="84ff7-106">數位憑證是提供驗證身分識別方法的認證。</span><span class="sxs-lookup"><span data-stu-id="84ff7-106">A digital certificate is a credential that provides a means to verify identity.</span></span> <span data-ttu-id="84ff7-107">如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 的[密碼](../seccrypto/cryptography-portal.md)編譯一節中的[數位憑證](../seccrypto/digital-certificates.md)。</span><span class="sxs-lookup"><span data-stu-id="84ff7-107">For more information, see [Digital Certificates](../seccrypto/digital-certificates.md) in the [Cryptography](../seccrypto/cryptography-portal.md) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="84ff7-108">從 Windows Installer 版本2.0 開始，可以使用 [MsiDigitalSignature](msidigitalsignature-table.md) 和 MsiDigitalCertificate 資料表。</span><span class="sxs-lookup"><span data-stu-id="84ff7-108">The [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="84ff7-109">Windows Installer 可以使用數位簽章作為偵測損毀資源的途徑。</span><span class="sxs-lookup"><span data-stu-id="84ff7-109">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="84ff7-110">Windows Installer 版本2.0 只能驗證外部封包的數位簽章，而且只會使用 [MsiDigitalSignature](msidigitalsignature-table.md) 和 MsiDigitalCertificate 資料表。</span><span class="sxs-lookup"><span data-stu-id="84ff7-110">Windows Installer version 2.0 can only verify the digital signatures of external cabinets, and only by the use of the [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables.</span></span>

<span data-ttu-id="84ff7-111">從 Windows Installer 版本3.0 開始，Windows Installer 可以使用 [MsiPatchCertificate](msipatchcertificate-table.md) 和 MsiDigitalCertificate 資料表來確認修補程式 () .msp 檔案的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="84ff7-111">Beginning with Windows Installer version 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="84ff7-112">如需詳細資訊，請參閱撰寫安全安裝和[使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md)[的指導方針](guidelines-for-authoring-secure-installations.md)。</span><span class="sxs-lookup"><span data-stu-id="84ff7-112">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="84ff7-113">MsiDigitalCertificate 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="84ff7-113">The MsiDigitalCertificate table has the following columns.</span></span>



| <span data-ttu-id="84ff7-114">Column</span><span class="sxs-lookup"><span data-stu-id="84ff7-114">Column</span></span>             | <span data-ttu-id="84ff7-115">類型</span><span class="sxs-lookup"><span data-stu-id="84ff7-115">Type</span></span>                         | <span data-ttu-id="84ff7-116">答案</span><span class="sxs-lookup"><span data-stu-id="84ff7-116">Key</span></span> | <span data-ttu-id="84ff7-117">Nullable</span><span class="sxs-lookup"><span data-stu-id="84ff7-117">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="84ff7-118">DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="84ff7-118">DigitalCertificate</span></span> | [<span data-ttu-id="84ff7-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="84ff7-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="84ff7-120">Y</span><span class="sxs-lookup"><span data-stu-id="84ff7-120">Y</span></span>   | <span data-ttu-id="84ff7-121">N</span><span class="sxs-lookup"><span data-stu-id="84ff7-121">N</span></span>        |
| <span data-ttu-id="84ff7-122">CertData</span><span class="sxs-lookup"><span data-stu-id="84ff7-122">CertData</span></span>           | [<span data-ttu-id="84ff7-123">二進位</span><span class="sxs-lookup"><span data-stu-id="84ff7-123">Binary</span></span>](binary.md)         | <span data-ttu-id="84ff7-124">N</span><span class="sxs-lookup"><span data-stu-id="84ff7-124">N</span></span>   | <span data-ttu-id="84ff7-125">N</span><span class="sxs-lookup"><span data-stu-id="84ff7-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="84ff7-126">資料行</span><span class="sxs-lookup"><span data-stu-id="84ff7-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="84ff7-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="84ff7-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="84ff7-128">識別數位簽章證書。</span><span class="sxs-lookup"><span data-stu-id="84ff7-128">Identifies the digital signature certificate.</span></span> <span data-ttu-id="84ff7-129">資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="84ff7-129">Primary key of table.</span></span>

</dd> <dt>

<span data-ttu-id="84ff7-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span><span class="sxs-lookup"><span data-stu-id="84ff7-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span></span>
</dt> <dd>

<span data-ttu-id="84ff7-131">數位憑證的二進位標記法。</span><span class="sxs-lookup"><span data-stu-id="84ff7-131">The binary representation of the digital certificate.</span></span> <span data-ttu-id="84ff7-132">CertData 資料行包含憑證內容的編碼位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="84ff7-132">The CertData column contains the encoded byte array of a certificate context.</span></span> <span data-ttu-id="84ff7-133">這是 [**CERT \_ 內容**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)結構的 **pbCertEncoded** 成員。</span><span class="sxs-lookup"><span data-stu-id="84ff7-133">This is the **pbCertEncoded** member of the [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="84ff7-134">您可以藉由呼叫 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)、 [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)或匯入 .cer 檔案來取得憑證內容。</span><span class="sxs-lookup"><span data-stu-id="84ff7-134">The certificate context can be obtained by calling [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), or by importing a .cer file.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="84ff7-135">驗證</span><span class="sxs-lookup"><span data-stu-id="84ff7-135">Validation</span></span>

<dl>

[<span data-ttu-id="84ff7-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="84ff7-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="84ff7-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="84ff7-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="84ff7-138">ICE29</span><span class="sxs-lookup"><span data-stu-id="84ff7-138">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="84ff7-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="84ff7-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="84ff7-140">ICE66</span><span class="sxs-lookup"><span data-stu-id="84ff7-140">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="84ff7-141">ICE81</span><span class="sxs-lookup"><span data-stu-id="84ff7-141">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="84ff7-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="84ff7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84ff7-143">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="84ff7-143">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="84ff7-144">MsiDigitalSignature 資料表</span><span class="sxs-lookup"><span data-stu-id="84ff7-144">MsiDigitalSignature table</span></span>](msidigitalsignature-table.md)
</dt> <dt>

[<span data-ttu-id="84ff7-145">數位簽章和 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="84ff7-145">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
