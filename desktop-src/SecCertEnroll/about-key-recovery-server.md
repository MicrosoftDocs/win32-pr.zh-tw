---
description: 您可以設定 (CA) 的 Microsoft 憑證授權單位單位，以封存和復原與憑證要求中所提交之公開金鑰相關聯的私密金鑰。
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: 金鑰修復伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e9fd60b7ee6596b98953d382978be64695c035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849246"
---
# <a name="key-recovery-server"></a><span data-ttu-id="7f06c-103">金鑰修復伺服器</span><span class="sxs-lookup"><span data-stu-id="7f06c-103">Key Recovery Server</span></span>

<span data-ttu-id="7f06c-104">您可以設定 (CA) 的 Microsoft 憑證授權單位單位，以封存和復原與憑證要求中所提交之公開金鑰相關聯的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-104">A Microsoft certification authority (CA) can be configured to archive and recover the private key associated with the public key submitted in the certificate request.</span></span> <span data-ttu-id="7f06c-105">如果遺失金鑰，復原會很有用。</span><span class="sxs-lookup"><span data-stu-id="7f06c-105">Recovery is useful if a key is lost.</span></span> <span data-ttu-id="7f06c-106">依預設，只可封存加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-106">By default, only encryption keys can be archived.</span></span> <span data-ttu-id="7f06c-107">不需要封存僅供簽署的金鑰，因為如果遺失私用簽署金鑰，則只需要公開金鑰來驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="7f06c-107">It is not necessary to archive keys intended only for signing because only the public key is needed to verify a signature if the private signing key is lost.</span></span>

<span data-ttu-id="7f06c-108">若要封存金鑰，必須將 CA 設定為向 (KRA) 憑證發出金鑰復原代理，並至少已發出一個憑證。</span><span class="sxs-lookup"><span data-stu-id="7f06c-108">To archive a key, the CA must be configured to issue key recovery agent (KRA) certificates and to have already issued at least one.</span></span> <span data-ttu-id="7f06c-109">金鑰復原代理是組織授權的系統管理員，可將私密金鑰解密。</span><span class="sxs-lookup"><span data-stu-id="7f06c-109">A key recovery agent is an administrator authorized by an organization to decrypt private keys.</span></span> <span data-ttu-id="7f06c-110">為了增強安全性，建議您將金鑰復原代理和憑證管理員角色指派給不同的個人、允許憑證管理員抓取但不解密封存金鑰，以及允許金鑰復原代理程式解密金鑰，但無法取出金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-110">To enhance security, we recommend that the key recovery agent and the certificate manager roles be assigned to different individuals, that the certificate manager be permitted to retrieve but not decrypt archived keys, and that the key recovery agent be permitted to decrypt keys but not retrieve them.</span></span>

## <a name="key-archival"></a><span data-ttu-id="7f06c-111">金鑰保存</span><span class="sxs-lookup"><span data-stu-id="7f06c-111">Key Archival</span></span>

<span data-ttu-id="7f06c-112">用戶端通常會使用範本來要求憑證。</span><span class="sxs-lookup"><span data-stu-id="7f06c-112">A client typically requests a certificate by using a template.</span></span> <span data-ttu-id="7f06c-113">如果範本需要封存私密金鑰，則下列步驟是由用戶端和 CA 執行：</span><span class="sxs-lookup"><span data-stu-id="7f06c-113">If the template requires that the private key be archived, the following steps are performed by the client and the CA:</span></span>

1.  <span data-ttu-id="7f06c-114">用戶端會抓取並驗證 CA exchange 憑證，以判斷它是否已由用來簽署 CA 簽署憑證的相同金鑰簽署。</span><span class="sxs-lookup"><span data-stu-id="7f06c-114">The client retrieves and validates the CA exchange certificate to determine whether it has been signed by the same key that was used to sign the CA signing certificate.</span></span> <span data-ttu-id="7f06c-115">這可確保唯一可解密私密金鑰的 CA 是要求憑證的 CA。</span><span class="sxs-lookup"><span data-stu-id="7f06c-115">This ensures that the only CA that can decrypt the private key is the CA from which a certificate is being requested.</span></span>
2.  <span data-ttu-id="7f06c-116">CA exchange 憑證中的公開金鑰是用來加密與憑證要求相關聯的私密金鑰，並將要求傳送至 CA。</span><span class="sxs-lookup"><span data-stu-id="7f06c-116">The public key in the CA exchange certificate is used to encrypt the private key associated with the certificate request, and the request is sent to the CA.</span></span>
3.  <span data-ttu-id="7f06c-117">CA 會使用與其 exchange 憑證相關聯的私密金鑰來解密用戶端所傳送的私密金鑰，並確認要求中的公開金鑰和私密金鑰相關聯。</span><span class="sxs-lookup"><span data-stu-id="7f06c-117">The CA uses the private key associated with its exchange certificate to decrypt the private key sent by the client and verifies that the public and private keys in the request are related.</span></span>
4.  <span data-ttu-id="7f06c-118">CA 會使用 KRA 憑證中的公開金鑰來加密私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-118">The CA encrypts the private key by using the public key in the KRA certificate.</span></span> <span data-ttu-id="7f06c-119">如果 CA 已發出多個 KRA 憑證，它會使用每個可用的公開金鑰來加密私密金鑰一次，讓任何授權的金鑰復原代理程式都可以復原金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-119">If the CA has issued multiple KRA certificates, it encrypts the private key once with each available public key so that any authorized key recovery agent can recover a key.</span></span> <span data-ttu-id="7f06c-120">加密的私密金鑰會儲存在憑證資料庫中。</span><span class="sxs-lookup"><span data-stu-id="7f06c-120">The encrypted private keys are stored in the certificate database.</span></span>
5.  <span data-ttu-id="7f06c-121">CA 會釋放私密金鑰的所有參考，並安全地釋出所有包含金鑰的記憶體和零。</span><span class="sxs-lookup"><span data-stu-id="7f06c-121">The CA releases all references to the private key and securely frees and zeros all memory that contained the key.</span></span> <span data-ttu-id="7f06c-122">這可確保 CA 無法再以純文字格式存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-122">This ensures that the CA has no further access to the key in clear text format.</span></span>

> [!Note]  
> <span data-ttu-id="7f06c-123">只有 CMC 要求才能用於金鑰保存。</span><span class="sxs-lookup"><span data-stu-id="7f06c-123">Only a CMC request can be used for key archival.</span></span> <span data-ttu-id="7f06c-124">CMC 要求會以 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="7f06c-124">CMC requests are represented by the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) interface.</span></span>

 

## <a name="key-recovery"></a><span data-ttu-id="7f06c-125">金鑰復原</span><span class="sxs-lookup"><span data-stu-id="7f06c-125">Key Recovery</span></span>

<span data-ttu-id="7f06c-126">Active Directory 憑證服務或憑證註冊 API 不直接支援金鑰復原。</span><span class="sxs-lookup"><span data-stu-id="7f06c-126">Key recovery is not directly supported by Active Directory Certificate Services or the Certificate Enrollment API.</span></span> <span data-ttu-id="7f06c-127">不過，Microsoft 會提供下列應用程式來協助處理：</span><span class="sxs-lookup"><span data-stu-id="7f06c-127">Microsoft does, however, provide the following applications to help with the process:</span></span>

-   <span data-ttu-id="7f06c-128">Certutil.exe 是命令列程式，可用來取出 CA 設定資訊、驗證憑證、金鑰組和憑證鏈，以及備份和還原金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-128">Certutil.exe is a command line program that can be used to retrieve CA configuration information, verify certificates, key pairs, and certificate chains, and back up and restore keys.</span></span> <span data-ttu-id="7f06c-129">它包含在從 Windows Server 2003 開始的伺服器作業系統中。</span><span class="sxs-lookup"><span data-stu-id="7f06c-129">It is included in server operating systems beginning with Windows Server 2003.</span></span>
-   <span data-ttu-id="7f06c-130">Krecover.exe 是以對話方塊為基礎的程式，可進行金鑰修復。</span><span class="sxs-lookup"><span data-stu-id="7f06c-130">Krecover.exe is a dialog box–based program that enables key recovery.</span></span> <span data-ttu-id="7f06c-131">它隨附于從 Windows Server 2003 開始的資源套件。</span><span class="sxs-lookup"><span data-stu-id="7f06c-131">It is included with the Resource Kit beginning with Windows Server 2003.</span></span>

<span data-ttu-id="7f06c-132">您可以執行下列步驟來復原私密金鑰：</span><span class="sxs-lookup"><span data-stu-id="7f06c-132">The following steps are performed to recover a private key:</span></span>

1.  <span data-ttu-id="7f06c-133">憑證管理員會使用憑證、要求者或使用者的名稱，找出憑證資料庫中金鑰復原的潛在候選項目。</span><span class="sxs-lookup"><span data-stu-id="7f06c-133">The certificate manager locates potential candidates for key recovery in the certificate database by using the name of the certificate, requester, or user.</span></span> <span data-ttu-id="7f06c-134">**Certutil** **-getkey** 命令可用於此用途。</span><span class="sxs-lookup"><span data-stu-id="7f06c-134">The **Certutil** **-getkey** command can be used for this purpose.</span></span>
2.  <span data-ttu-id="7f06c-135">一旦憑證管理員有憑證清單之後，就會再次呼叫 **-getkey** 命令，並使用特定的憑證序號或 thumb 列印來取出 PKCS \# 7 檔案，其中包含在使用 kra 公開金鑰進行封存期間加密的 KRA 憑證、使用者憑證鏈，以及私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-135">Once the certificate manager has a list of certificates, the **-getkey** command is called again with a specific certificate serial number or thumb print to retrieve a PKCS \#7 file that contains the KRA certificate, user certificate chain, and the private key that was encrypted during archival by using the KRA public key.</span></span>
3.  <span data-ttu-id="7f06c-136">憑證管理員會將進程的控制權傳遞給金鑰復原代理程式，其私密金鑰符合 KRA 憑證中包含的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-136">The certificate manager passes control of the process to the key recovery agent whose private key matches the public key contained in the KRA certificate.</span></span>
4.  <span data-ttu-id="7f06c-137">Key recovery agent 會 \# 使用 KRA 私密金鑰來解密 PKCS 7 檔案中所傳回的封存私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-137">The key recovery agent decrypts the archived private key returned in the PKCS \#7 file by using the KRA private key.</span></span> <span data-ttu-id="7f06c-138">這可以藉由使用 **Certutil** **-recoverkey** 命令來完成，此命令會將金鑰放在受密碼保護的 PKCS 12 檔案中 \# 。</span><span class="sxs-lookup"><span data-stu-id="7f06c-138">This can be done by using the **Certutil** **-recoverkey** command which places the key in a password-protected PKCS \#12 file.</span></span> <span data-ttu-id="7f06c-139">用戶端必須透過安全的頻外機制提供密碼。</span><span class="sxs-lookup"><span data-stu-id="7f06c-139">The client must be given the password through a secure out-of-band mechanism.</span></span>
5.  <span data-ttu-id="7f06c-140">用戶端會匯入 PKCS \# 12 檔案並使用密碼來取得金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f06c-140">The client imports the PKCS \#12 file and uses the password to retrieve the key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f06c-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f06c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f06c-142">PKI 元素</span><span class="sxs-lookup"><span data-stu-id="7f06c-142">PKI Elements</span></span>](about-pki-components.md)
</dt> </dl>

 

 



