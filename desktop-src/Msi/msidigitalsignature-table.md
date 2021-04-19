---
description: MsiDigitalSignature 資料表包含安裝資料庫中每個數位簽署物件的簽章資訊。
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: MsiDigitalSignature 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971738"
---
# <a name="msidigitalsignature-table"></a><span data-ttu-id="95548-103">MsiDigitalSignature 資料表</span><span class="sxs-lookup"><span data-stu-id="95548-103">MsiDigitalSignature Table</span></span>

<span data-ttu-id="95548-104">MsiDigitalSignature 資料表包含安裝資料庫中每個數位簽署物件的簽章資訊。</span><span class="sxs-lookup"><span data-stu-id="95548-104">The MsiDigitalSignature table contains the signature information for every digitally signed object in the installation database.</span></span>

<span data-ttu-id="95548-105">從 Windows Installer 版本2.0 開始，可以使用 MsiDigitalSignature 和 [MsiDigitalCertificate](msidigitalcertificate-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="95548-105">The MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="95548-106">Windows Installer 版本可以使用數位簽章來偵測損毀的資源。</span><span class="sxs-lookup"><span data-stu-id="95548-106">Windows Installer version can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="95548-107">Windows Installer 2.0 只能驗證外部封包的數位簽章，而且只會使用 MsiDigitalSignature 和 [MsiDigitalCertificate](msidigitalcertificate-table.md) 資料表。</span><span class="sxs-lookup"><span data-stu-id="95548-107">Windows Installer 2.0 can only verify the digital signatures of external cabinets, and only by the use of the MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="95548-108">從 Windows Installer 3.0 開始，Windows Installer 可以使用 [MsiPatchCertificate](msipatchcertificate-table.md) 和 MsiDigitalCertificate 資料表來確認修補程式 () .msp 檔案的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="95548-108">Beginning with Windows Installer 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="95548-109">如需詳細資訊，請參閱撰寫安全安裝和[使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md)[的指導方針](guidelines-for-authoring-secure-installations.md)。</span><span class="sxs-lookup"><span data-stu-id="95548-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="95548-110">MsiDigitalSignature 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="95548-110">The MsiDigitalSignature table has the following columns.</span></span>



| <span data-ttu-id="95548-111">Column</span><span class="sxs-lookup"><span data-stu-id="95548-111">Column</span></span>               | <span data-ttu-id="95548-112">類型</span><span class="sxs-lookup"><span data-stu-id="95548-112">Type</span></span>                         | <span data-ttu-id="95548-113">答案</span><span class="sxs-lookup"><span data-stu-id="95548-113">Key</span></span> | <span data-ttu-id="95548-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="95548-114">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="95548-115">資料表</span><span class="sxs-lookup"><span data-stu-id="95548-115">Table</span></span>                | [<span data-ttu-id="95548-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="95548-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="95548-117">Y</span><span class="sxs-lookup"><span data-stu-id="95548-117">Y</span></span>   | <span data-ttu-id="95548-118">N</span><span class="sxs-lookup"><span data-stu-id="95548-118">N</span></span>        |
| <span data-ttu-id="95548-119">SignObject</span><span class="sxs-lookup"><span data-stu-id="95548-119">SignObject</span></span>           | [<span data-ttu-id="95548-120">Text</span><span class="sxs-lookup"><span data-stu-id="95548-120">Text</span></span>](text.md)             | <span data-ttu-id="95548-121">Y</span><span class="sxs-lookup"><span data-stu-id="95548-121">Y</span></span>   | <span data-ttu-id="95548-122">N</span><span class="sxs-lookup"><span data-stu-id="95548-122">N</span></span>        |
| <span data-ttu-id="95548-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="95548-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="95548-124">識別碼</span><span class="sxs-lookup"><span data-stu-id="95548-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="95548-125">N</span><span class="sxs-lookup"><span data-stu-id="95548-125">N</span></span>   | <span data-ttu-id="95548-126">N</span><span class="sxs-lookup"><span data-stu-id="95548-126">N</span></span>        |
| <span data-ttu-id="95548-127">雜湊</span><span class="sxs-lookup"><span data-stu-id="95548-127">Hash</span></span>                 | [<span data-ttu-id="95548-128">二進位</span><span class="sxs-lookup"><span data-stu-id="95548-128">Binary</span></span>](binary.md)         | <span data-ttu-id="95548-129">N</span><span class="sxs-lookup"><span data-stu-id="95548-129">N</span></span>   | <span data-ttu-id="95548-130">Y</span><span class="sxs-lookup"><span data-stu-id="95548-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="95548-131">資料行</span><span class="sxs-lookup"><span data-stu-id="95548-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="95548-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>表</span><span class="sxs-lookup"><span data-stu-id="95548-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="95548-133">使用 Windows Installer 版本2.0 時，此欄位中的專案必須是 [媒體資料表](media-table.md)的「媒體」。</span><span class="sxs-lookup"><span data-stu-id="95548-133">With the Windows Installer version 2.0, the entry in this field must be "Media" for the [Media table](media-table.md).</span></span> <span data-ttu-id="95548-134">安裝程式只會驗證外部封包媒體專案的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="95548-134">The installer only verifies the digital signatures on external cabinet media entries.</span></span> <span data-ttu-id="95548-135">此資料行和 SignObject 資料行會一起指定經過數位簽署的資源。</span><span class="sxs-lookup"><span data-stu-id="95548-135">This column and the SignObject column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="95548-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span><span class="sxs-lookup"><span data-stu-id="95548-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span></span>
</dt> <dd>

<span data-ttu-id="95548-137">資料表資料行所指定之資料表主鍵的外鍵。</span><span class="sxs-lookup"><span data-stu-id="95548-137">A foreign key into the primary key of the table specified by the Table column.</span></span> <span data-ttu-id="95548-138">此資料行和資料表資料行會一起指定經過數位簽署的資源。</span><span class="sxs-lookup"><span data-stu-id="95548-138">This column and the Table column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="95548-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="95548-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span></span>
</dt> <dd>

<span data-ttu-id="95548-140">[MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="95548-140">A foreign key into the [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="95548-141">這會識別檔案上必須存在的憑證，才能讓相關聯的動作成功。</span><span class="sxs-lookup"><span data-stu-id="95548-141">This identifies the certificate that must exist on the file for the associated action to succeed.</span></span> <span data-ttu-id="95548-142">資源 (或物件) 一律需要符合 MsiDigitalCertificate 資料表中的這個憑證。</span><span class="sxs-lookup"><span data-stu-id="95548-142">The resource (or object) is always required to match this certificate in the MsiDigitalCertificate table.</span></span>

</dd> <dt>

<span data-ttu-id="95548-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>散 列</span><span class="sxs-lookup"><span data-stu-id="95548-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash</span></span>
</dt> <dd>

<span data-ttu-id="95548-144">在此欄位中，輸入資源 (或物件) 的參考雜湊，以針對資源 (或在執行時間取得的物件) 的實際雜湊進行檢查。</span><span class="sxs-lookup"><span data-stu-id="95548-144">In this field enter the reference hash of the resource (or object) that is to be checked against the actual hash of the resource (or object) obtained at run-time.</span></span> <span data-ttu-id="95548-145">如果只有憑證需要驗證，則雜湊欄位可能是 null。</span><span class="sxs-lookup"><span data-stu-id="95548-145">If only the certificate needs to be verified, the Hash field may be null.</span></span> <span data-ttu-id="95548-146">請注意，雜湊的格式取決於資源 (類型或簽署的物件) 。</span><span class="sxs-lookup"><span data-stu-id="95548-146">Note that the format of the hash depends on the type of the resource (or object) being signed.</span></span>

<span data-ttu-id="95548-147">雜湊資料行包含雜湊的二進位標記法。</span><span class="sxs-lookup"><span data-stu-id="95548-147">The Hash column contains the binary representation of the hash.</span></span> <span data-ttu-id="95548-148">實際的內容是 [**CRYPT \_ 雜湊 \_ Blob**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob)結構的 **>pbdata** 成員，這是 **CRYPTOAPI \_ blob** 結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="95548-148">The actual content is the **pbData** member of the [**CRYPT\_HASH\_BLOB**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure, which is part of the **CRYPTOAPI\_BLOB** structure.</span></span> <span data-ttu-id="95548-149">這可透過呼叫 [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) 或 [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)來取得。</span><span class="sxs-lookup"><span data-stu-id="95548-149">This may be obtained by calling [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) or [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="95548-150">驗證</span><span class="sxs-lookup"><span data-stu-id="95548-150">Validation</span></span>

<dl>

[<span data-ttu-id="95548-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="95548-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="95548-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="95548-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="95548-153">ICE29</span><span class="sxs-lookup"><span data-stu-id="95548-153">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="95548-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="95548-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="95548-155">ICE66</span><span class="sxs-lookup"><span data-stu-id="95548-155">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="95548-156">ICE81</span><span class="sxs-lookup"><span data-stu-id="95548-156">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="95548-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="95548-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95548-158">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="95548-158">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="95548-159">MsiDigitalCertificate 資料表</span><span class="sxs-lookup"><span data-stu-id="95548-159">MsiDigitalCertificate table</span></span>](msidigitalcertificate-table.md)
</dt> <dt>

[<span data-ttu-id="95548-160">數位簽章和 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="95548-160">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
