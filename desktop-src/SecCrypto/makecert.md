---
description: 建立由測試根目錄金鑰或其他指定的金鑰簽署的 x.509 憑證，以將您的名稱系結至金鑰組的公開部分。 憑證會儲存至檔案、系統憑證存放區或兩者。
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991753"
---
# <a name="makecert"></a><span data-ttu-id="d0d4b-104">MakeCert</span><span class="sxs-lookup"><span data-stu-id="d0d4b-104">MakeCert</span></span>

> [!Note]  
> <span data-ttu-id="d0d4b-105">MakeCert 已被取代。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-105">MakeCert is deprecated.</span></span> <span data-ttu-id="d0d4b-106">若要建立自我簽署憑證，請使用 Powershell Cmdlet [New-new-selfsignedcertificate](/powershell/module/pkiclient/new-selfsignedcertificate)。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-106">To create self-signed certificates, use the Powershell Cmdlet [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span></span>

 

<span data-ttu-id="d0d4b-107">MakeCert 工具會建立由測試根目錄金鑰或其他指定的機碼簽署的 [*x.509*](../secgloss/x-gly.md) 憑證，以將您的名稱系結至金鑰組的公開部分。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-107">The MakeCert tool creates an [*X.509*](../secgloss/x-gly.md) certificate, signed by the test root key or other specified key, that binds your name to the public part of the key pair.</span></span> <span data-ttu-id="d0d4b-108">憑證會儲存至檔案、系統憑證存放區或兩者。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-108">The certificate is saved to a file, a system certificate store, or both.</span></span> <span data-ttu-id="d0d4b-109">此工具會安裝在 \\ Microsoft Windows 軟體開發套件 (SDK) 安裝路徑的 Bin 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-109">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="d0d4b-110">MakeCert 工具會使用下列命令語法：</span><span class="sxs-lookup"><span data-stu-id="d0d4b-110">The MakeCert tool uses the following command syntax:</span></span>

<span data-ttu-id="d0d4b-111">**MakeCert** \[*BasicOptions* \|*ExtendedOptions* \]*OutputFile*</span><span class="sxs-lookup"><span data-stu-id="d0d4b-111">**MakeCert** \[*BasicOptions*\|*ExtendedOptions*\] *OutputFile*</span></span>

<span data-ttu-id="d0d4b-112">*OutputFile* 是將寫入憑證的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-112">*OutputFile* is the name of the file where the certificate will be written.</span></span> <span data-ttu-id="d0d4b-113">如果憑證不是寫入檔案，您可以省略 *OutputFile* 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-113">You can omit *OutputFile* if the certificate is not to be written to a file.</span></span>

## <a name="options"></a><span data-ttu-id="d0d4b-114">選項</span><span class="sxs-lookup"><span data-stu-id="d0d4b-114">Options</span></span>

<span data-ttu-id="d0d4b-115">MakeCert 包含基本和擴充的選項。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-115">MakeCert includes basic and extended options.</span></span> <span data-ttu-id="d0d4b-116">基本選項是最常用來建立憑證的選項。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-116">Basic options are those most commonly used to create a certificate.</span></span> <span data-ttu-id="d0d4b-117">擴充選項則提供更多彈性。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-117">Extended options provide more flexibility.</span></span>

<span data-ttu-id="d0d4b-118">MakeCert 的選項也可以分為三個功能群組：</span><span class="sxs-lookup"><span data-stu-id="d0d4b-118">The options for MakeCert are also divided into three functional groups:</span></span>

-   <span data-ttu-id="d0d4b-119">僅限憑證存放區技術專用的基本選項。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-119">Basic options specific to certificate store technology only.</span></span>
-   <span data-ttu-id="d0d4b-120">僅限 SPC 檔案和私密金鑰技術專用的擴充選項。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-120">Extended options specific to SPC-file and private key technology only.</span></span>
-   <span data-ttu-id="d0d4b-121">適用于 SPC 檔案、私密金鑰和憑證存放區技術的擴充選項。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-121">Extended options applicable to SPC-file, private key, and certificate store technology.</span></span>

<span data-ttu-id="d0d4b-122">下表中提供的選項只可用於 Internet Explorer 4.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-122">Options given in the following tables can be used only with Internet Explorer 4.0 or later.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0d4b-123">基本選項</span><span class="sxs-lookup"><span data-stu-id="d0d4b-123">Basic option</span></span></th>
<th><span data-ttu-id="d0d4b-124">Description</span><span class="sxs-lookup"><span data-stu-id="d0d4b-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d0d4b-125"><strong>-a</strong> <strong></strong><em>演算法</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-125"><strong>-a</strong> <strong></strong> <em>Algorithm</em></span></span></td>
<td><span data-ttu-id="d0d4b-126"><a href="/windows/desktop/SecGloss/h-gly"><em>雜湊</em></a> 演算法。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> algorithm.</span></span> <span data-ttu-id="d0d4b-127">必須設定為 <strong>sha-1</strong> 或 <strong>MD5</strong> (預設) 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-127">Must be set to either <strong>SHA-1</strong> or <strong>MD5</strong> (default).</span></span> <span data-ttu-id="d0d4b-128">如需 MD5 的詳細資訊，請參閱 <a href="/windows/desktop/SecGloss/m-gly"><em>md5</em></a>。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-128">For information about MD5, see <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-129"><strong>-b</strong> <strong></strong><em>DateStart</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span></span></td>
<td><span data-ttu-id="d0d4b-130">憑證首次生效的日期。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-130">Date the certificate first becomes valid.</span></span> <span data-ttu-id="d0d4b-131">預設值為建立憑證的時間。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-131">The default is when the certificate is created.</span></span> <span data-ttu-id="d0d4b-132"><em>DateStart</em>的格式為 mm/dd/yyyy。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-132">The format of <em>DateStart</em> is mm/dd/yyyy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-133"><strong>-cy</strong> <strong></strong><em>CertificateTypes</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span></span></td>
<td><span data-ttu-id="d0d4b-134">憑證類型。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-134">Certificate type.</span></span> <span data-ttu-id="d0d4b-135"><em>CertificateTypes</em> <strong>可用於終端</strong>實體或<a href="/windows/desktop/SecGloss/c-gly"><em>憑證授權單位</em></a>單位的<strong>授權</strong>單位。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-135"><em>CertificateTypes</em> can be <strong>end</strong> for end-entity, or <strong>authority</strong> for <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-136"><strong>-e</strong> <strong></strong><em>DateEnd</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span></span></td>
<td><span data-ttu-id="d0d4b-137">有效期間結束的日期。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-137">Date when the validity period ends.</span></span> <span data-ttu-id="d0d4b-138">預設值為2039年。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-138">The default is the year 2039.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-139"><strong>-eku</strong> <strong></strong><em>OID1</em><strong>、</strong> <em>OID2</em> .。。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> …</span></span></td>
<td><span data-ttu-id="d0d4b-140">將一或多個以逗號分隔、 <a href="/windows/desktop/SecGloss/e-gly"><em>增強金鑰使用</em></a>方法 <a href="/windows/desktop/SecGloss/o-gly"><em>物件識別碼</em></a> 的清單插入憑證 (oid) 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-140">Inserts a list of one or more comma-separated, <a href="/windows/desktop/SecGloss/e-gly"><em>enhanced key usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>object identifiers</em></a> (OIDs) into the certificate.</span></span> <span data-ttu-id="d0d4b-141">例如， <strong>-eku 1.3.6.1.5.5.7.3.2</strong> 會插入用戶端驗證 OID。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-141">For example, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserts the client authentication OID.</span></span> <span data-ttu-id="d0d4b-142">如需允許 Oid 的定義，請參閱 CryptoAPI 2.0 中的 Wincrypt .h 檔案。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-142">For definitions of allowable OIDs, see the Wincrypt.h file in CryptoAPI 2.0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-143"><strong>-h</strong> <strong></strong><em>NumChildren</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span></span></td>
<td><span data-ttu-id="d0d4b-144">此憑證下的樹狀結構最大高度。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-144">Maximum height of the tree below this certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-145"><strong>-l</strong> <strong></strong><em>PolicyLink</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span></span></td>
<td><span data-ttu-id="d0d4b-146">與 SPC 機構原則資訊的連結 (例如，URL) 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-146">Link to SPC agency policy information (for example, a URL).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-147"><strong>-m</strong> <strong></strong><em>nMonths</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span></span></td>
<td><span data-ttu-id="d0d4b-148">有效期間的持續時間。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-148">Duration of the validity period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-149"><strong>-n</strong> <strong>&quot;</strong><em>名稱</em><strong>&quot;</strong></span><span class="sxs-lookup"><span data-stu-id="d0d4b-149"><strong>-n</strong> <strong>&quot;</strong><em>Name</em><strong>&quot;</strong></span></span></td>
<td><span data-ttu-id="d0d4b-150">發行者憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-150">Name for the publisher's certificate.</span></span> <span data-ttu-id="d0d4b-151">這個名稱必須符合 <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> 標準。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-151">This name must conform to the <a href="/windows/desktop/SecGloss/x-gly"><em>X.500</em></a> standard.</span></span> <span data-ttu-id="d0d4b-152">最簡單的方法是使用 &quot; CN =<em>MyName</em> &quot; 格式。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-152">The simplest method is to use the &quot;CN=<em>MyName</em>&quot; format.</span></span> <span data-ttu-id="d0d4b-153">例如： <strong>-n &quot; CN = Test &quot; </strong>。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-153">For example: <strong>-n &quot;CN=Test&quot;</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-154"><strong>-nscp</strong></span><span class="sxs-lookup"><span data-stu-id="d0d4b-154"><strong>-nscp</strong></span></span></td>
<td><span data-ttu-id="d0d4b-155">應包含 Netscape 用戶端驗證延伸模組。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-155">The Netscape client authentication extension should be included.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-156"><strong>-pe</strong></span><span class="sxs-lookup"><span data-stu-id="d0d4b-156"><strong>-pe</strong></span></span></td>
<td><span data-ttu-id="d0d4b-157">將私密金鑰標記為可匯出。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-157">Marks the private key as exportable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-158"><strong>-r</strong></span><span class="sxs-lookup"><span data-stu-id="d0d4b-158"><strong>-r</strong></span></span></td>
<td><span data-ttu-id="d0d4b-159">建立自我簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-159">Creates a self-signed certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-160"><strong>-sc</strong> <strong></strong><em>SubjectCertFile</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span></span></td>
<td><span data-ttu-id="d0d4b-161">包含要使用之現有主體公開金鑰的憑證檔案名。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-161">Certificate file name with the existing subject public key to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-162"><strong>-sk</strong> <strong></strong><em>SubjectKey</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span></span></td>
<td><span data-ttu-id="d0d4b-163">保存 <a href="/windows/desktop/SecGloss/p-gly"><em>私密金鑰</em></a>之主體金鑰容器的位置。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-163">Location of the subject's key container which holds the <a href="/windows/desktop/SecGloss/p-gly"><em>private key</em></a>.</span></span> <span data-ttu-id="d0d4b-164">如果金鑰容器不存在，便會建立一個。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-164">If a key container does not exist, one is created.</span></span> <span data-ttu-id="d0d4b-165">如果不使用 <strong>-sk</strong> 或 <strong>-sv</strong> 選項，預設會建立預設的金鑰容器並使用。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-165">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-166"><strong>-天空</strong> <strong></strong><em>SubjectKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span></span></td>
<td><span data-ttu-id="d0d4b-167">主體的金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-167">Subject's key specification.</span></span> <span data-ttu-id="d0d4b-168"><em>SubjectKeySpec</em> 必須是三個可能值的其中一個：</span><span class="sxs-lookup"><span data-stu-id="d0d4b-168"><em>SubjectKeySpec</em> must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="d0d4b-169">簽章 (AT_SIGNATURE 機<strong>碼</strong>規格) </span><span class="sxs-lookup"><span data-stu-id="d0d4b-169"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="d0d4b-170"><strong>Exchange</strong> (AT_KEYEXCHANGE 金鑰規格) </span><span class="sxs-lookup"><span data-stu-id="d0d4b-170"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="d0d4b-171">整數，例如<strong>3</strong> 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-171">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="d0d4b-172">如需詳細資訊，請參閱此表格後面的附注。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-172">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-173"><strong>-sp</strong> <strong></strong><em>SubjectProviderName</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span></span></td>
<td><span data-ttu-id="d0d4b-174">Subject 的 CryptoAPI 提供者。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-174">CryptoAPI provider for subject.</span></span> <span data-ttu-id="d0d4b-175">預設值是使用者的提供者。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-175">The default is the user's provider.</span></span> <span data-ttu-id="d0d4b-176">如需 CryptoAPI 提供者的詳細資訊，請參閱 CryptoAPI 2.0 檔。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-176">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-177"><strong>-sr</strong> <strong></strong><em>SubjectCertStoreLocation</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span></span></td>
<td><span data-ttu-id="d0d4b-178">主體憑證存放區的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-178">Registry location of the subject's certificate store.</span></span> <span data-ttu-id="d0d4b-179"><em>SubjectCertStoreLocation</em> 必須是 <strong>LocalMachine</strong> (登錄機碼 HKEY_LOCAL_MACHINE) 或 <strong>CurrentUser</strong> (登錄機碼 HKEY_CURRENT_USER) 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-179"><em>SubjectCertStoreLocation</em> must be either <strong>LocalMachine</strong> (registry key HKEY_LOCAL_MACHINE) or <strong>CurrentUser</strong> (registry key HKEY_CURRENT_USER).</span></span> <span data-ttu-id="d0d4b-180">預設值為<strong>CurrentUser</strong> 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-180"><strong>CurrentUser</strong> is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-181"><strong>-ss</strong> <strong></strong><em>SubjectCertStoreName</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span></span></td>
<td><span data-ttu-id="d0d4b-182">將儲存所產生之憑證的主體憑證存放區名稱。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-182">Name of the subject's certificate store where the generated certificate will be stored.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-183"><strong>-sv</strong> <strong></strong><em>SubjectKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span></span></td>
<td><span data-ttu-id="d0d4b-184">主體 pvk 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-184">Name of the subject's .pvk file.</span></span> <span data-ttu-id="d0d4b-185">如果不使用 <strong>-sk</strong> 或 <strong>-sv</strong> 選項，預設會建立預設的金鑰容器並使用。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-185">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-186"><strong>-sy</strong> <strong></strong><em>nSubjectProviderType</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span></span></td>
<td><span data-ttu-id="d0d4b-187">Subject 的 CryptoAPI 提供者類型。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-187">CryptoAPI provider type for subject.</span></span> <span data-ttu-id="d0d4b-188">預設值為 <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-188">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="d0d4b-189">如需 CryptoAPI 提供者類型的詳細資訊，請參閱 CryptoAPI 2.0 檔。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-189">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-190"><strong>-#</strong><strong></strong> <em>SerialNumber</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-190"><strong>-#</strong> <strong></strong> <em>SerialNumber</em></span></span></td>
<td><span data-ttu-id="d0d4b-191">憑證的序號。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-191">Serial number of the certificate.</span></span> <span data-ttu-id="d0d4b-192">最大值為 2 ^ 31。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-192">The maximum value is 2^31.</span></span> <span data-ttu-id="d0d4b-193">預設值是工具所產生的值，這個值保證是唯一的。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-193">The default is a value generated by the tool that is guaranteed to be unique.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-194"><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-194"><strong>-$</strong> <strong></strong> <em>CertificateAuthority</em></span></span></td>
<td><span data-ttu-id="d0d4b-195"><a href="/windows/desktop/SecGloss/c-gly"><em>憑證授權單位</em></a>單位的類型。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-195">Type of <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span> <span data-ttu-id="d0d4b-196"><em>CertificateAuthority</em> 必須設定為 <strong>商業 (，才能讓商務軟體</strong> 發行者) 或個別軟體發行者) 使用憑證的 <strong>個別</strong> (。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-196"><em>CertificateAuthority</em> must be set to either <strong>commercial</strong> (for certificates to be used by commercial software publishers) or <strong>individual</strong> (for certificates to be used by individual software publishers).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-197"><strong>-?</strong></span><span class="sxs-lookup"><span data-stu-id="d0d4b-197"><strong>-?</strong></span></span></td>
<td><span data-ttu-id="d0d4b-198">顯示基本選項。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-198">Displays the basic options.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-199"><strong>-!</strong></span><span class="sxs-lookup"><span data-stu-id="d0d4b-199"><strong>-!</strong></span></span></td>
<td><span data-ttu-id="d0d4b-200">顯示擴充的選項。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-200">Displays the extended options.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="d0d4b-201">如果 Internet Explorer 4.0 版或更新版本中使用 **-天空** 金鑰規格選項，則規格必須符合 [*私密金鑰*](../secgloss/p-gly.md) 檔案或私密金鑰 [*容器*](../secgloss/k-gly.md)所指出的金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-201">If the **-sky** key specification option is used in Internet Explorer version 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="d0d4b-202">如果未使用金鑰規格選項，將會使用私密金鑰檔案或私密金鑰容器所指出的金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-202">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="d0d4b-203">如果金鑰容器中有一個以上的金鑰規格，MakeCert 會先嘗試使用 AT \_ SIGNATURE key 規格。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-203">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="d0d4b-204">如果失敗，MakeCert 會嘗試在 KEYEXCHANGE 中使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-204">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="d0d4b-205">因為大部分的使用者都有 AT \_ SIGNATURE key 或 at \_ KEYEXCHANGE 索引鍵，所以在大部分情況下都不需要使用此選項。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-205">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="d0d4b-206">下列選項僅適用于 (SPC) 檔和私密金鑰技術的 [*軟體發行者憑證*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-206">The following options are only for [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) files and private key technology.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0d4b-207">SPC 和私用金鑰選項</span><span class="sxs-lookup"><span data-stu-id="d0d4b-207">SPC and private key option</span></span></th>
<th><span data-ttu-id="d0d4b-208">Description</span><span class="sxs-lookup"><span data-stu-id="d0d4b-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d0d4b-209"><strong>-ic</strong> <strong></strong><em>IssuerCertFile</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span></span></td>
<td><span data-ttu-id="d0d4b-210">簽發者憑證的位置。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-210">Location of the issuer's certificate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-211"><strong>-ik</strong> <strong></strong><em>IssuerKey</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span></span></td>
<td><span data-ttu-id="d0d4b-212">簽發者金鑰容器的位置。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-212">Location of the issuer's key container.</span></span> <span data-ttu-id="d0d4b-213">預設值為測試根目錄金鑰。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-213">The default is the test root key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-214"><strong>-iky</strong> <strong></strong><em>IssuerKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span></span></td>
<td><span data-ttu-id="d0d4b-215">簽發者的金鑰規格，其必須是三個可能值的其中一個：</span><span class="sxs-lookup"><span data-stu-id="d0d4b-215">Issuer's key specification, which must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="d0d4b-216">簽章 (AT_SIGNATURE 機<strong>碼</strong>規格) </span><span class="sxs-lookup"><span data-stu-id="d0d4b-216"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="d0d4b-217"><strong>Exchange</strong> (AT_KEYEXCHANGE 金鑰規格) </span><span class="sxs-lookup"><span data-stu-id="d0d4b-217"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="d0d4b-218">整數，例如<strong>3</strong> 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-218">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="d0d4b-219">如需詳細資訊，請參閱此表格後面的附注。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-219">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-220"><strong>-ip</strong> <strong></strong><em>IssuerProviderName</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span></span></td>
<td><span data-ttu-id="d0d4b-221">簽發者的 CryptoAPI 提供者。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-221">CryptoAPI provider for issuer.</span></span> <span data-ttu-id="d0d4b-222">預設值是使用者的提供者。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-222">The default is the user's provider.</span></span> <span data-ttu-id="d0d4b-223">如需 CryptoAPI 提供者的詳細資訊，請參閱 CryptoAPI 2.0 檔。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-223">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0d4b-224"><strong>-iv</strong> <strong></strong><em>IssuerKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span></span></td>
<td><span data-ttu-id="d0d4b-225">簽發者的私密金鑰檔案。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-225">Issuer's private key file.</span></span> <span data-ttu-id="d0d4b-226">預設值是測試根目錄。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-226">The default is the test root.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0d4b-227"><strong>-iy</strong> <strong></strong><em>nIssuerProviderType</em></span><span class="sxs-lookup"><span data-stu-id="d0d4b-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span></span></td>
<td><span data-ttu-id="d0d4b-228">簽發者的 CryptoAPI 提供者類型。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-228">CryptoAPI provider type for issuer.</span></span> <span data-ttu-id="d0d4b-229">預設值為 <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-229">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="d0d4b-230">如需 CryptoAPI 提供者類型的詳細資訊，請參閱 CryptoAPI 2.0 檔。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-230">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="d0d4b-231">如果 Internet Explorer 4.0 或更新版本中使用 **-iky** 金鑰規格選項，則規格必須符合 [*私密金鑰*](../secgloss/p-gly.md) 檔案或私密金鑰 [*容器*](../secgloss/k-gly.md)所指出的金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-231">If the **-iky** key specification option is used in Internet Explorer 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="d0d4b-232">如果未使用金鑰規格選項，將會使用私密金鑰檔案或私密金鑰容器所指出的金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-232">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="d0d4b-233">如果金鑰容器中有一個以上的金鑰規格，MakeCert 會先嘗試使用 AT \_ SIGNATURE key 規格。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-233">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="d0d4b-234">如果失敗，MakeCert 會嘗試在 KEYEXCHANGE 中使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-234">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="d0d4b-235">因為大部分的使用者都有 AT \_ SIGNATURE key 或 at \_ KEYEXCHANGE 索引鍵，所以在大部分情況下都不需要使用此選項。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-235">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="d0d4b-236">下列選項僅適用于 [*憑證存放區*](../secgloss/c-gly.md) 技術。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-236">The following options are for [*certificate store*](../secgloss/c-gly.md) technology only.</span></span>



| <span data-ttu-id="d0d4b-237">憑證存放區選項</span><span class="sxs-lookup"><span data-stu-id="d0d4b-237">Certificate store option</span></span>          | <span data-ttu-id="d0d4b-238">Description</span><span class="sxs-lookup"><span data-stu-id="d0d4b-238">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0d4b-239">**-ic** *IssuerCertFile*</span><span class="sxs-lookup"><span data-stu-id="d0d4b-239">**-ic** *IssuerCertFile*</span></span>          | <span data-ttu-id="d0d4b-240">包含簽發者憑證的檔案。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-240">File that contains the issuer's certificate.</span></span> <span data-ttu-id="d0d4b-241">MakeCert 會在憑證存放區中搜尋完全相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-241">MakeCert will search in the certificate store for a certificate with an exact match.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="d0d4b-242">**-in** *IssuerNameString*</span><span class="sxs-lookup"><span data-stu-id="d0d4b-242">**-in** *IssuerNameString*</span></span>        | <span data-ttu-id="d0d4b-243">簽發者憑證的一般名稱。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-243">Common name of the issuer's certificate.</span></span> <span data-ttu-id="d0d4b-244">MakeCert 會在憑證存放區中搜尋一般名稱包含 *IssuerNameString* 的憑證。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-244">MakeCert will search in the certificate store for a certificate whose common name includes *IssuerNameString*.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="d0d4b-245">**-ir** *IssuerCertStoreLocation*</span><span class="sxs-lookup"><span data-stu-id="d0d4b-245">**-ir** *IssuerCertStoreLocation*</span></span> | <span data-ttu-id="d0d4b-246">簽發者憑證存放區的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-246">Registry location of the issuer's certificate store.</span></span> <span data-ttu-id="d0d4b-247">*IssuerCertStoreLocation* 必須是 **LocalMachine** (登錄機碼 HKEY \_ 本機 \_ 電腦) 或 **CurrentUser** (登錄機碼 HKEY \_ 目前 \_ 的使用者) 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-247">*IssuerCertStoreLocation* must be either **LocalMachine** (registry key HKEY\_LOCAL\_MACHINE) or **CurrentUser** (registry key HKEY\_CURRENT\_USER).</span></span> <span data-ttu-id="d0d4b-248">預設值為 **CurrentUser** 。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-248">**CurrentUser** is the default.</span></span>                                                                                                |
| <span data-ttu-id="d0d4b-249">**-是** *IssuerCertStoreName*</span><span class="sxs-lookup"><span data-stu-id="d0d4b-249">**-is** *IssuerCertStoreName*</span></span>     | <span data-ttu-id="d0d4b-250">簽發者的憑證存放區，其中包含簽發者的憑證及其相關聯的私密金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-250">Issuer's certificate store that includes the issuer's certificate and its associated private key information.</span></span> <span data-ttu-id="d0d4b-251">如果存放區中有一個以上的憑證，則使用者必須使用 **-ic** 或 **-in** 選項來唯一識別它。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-251">If there is more than one certificate in the store, the user must uniquely identify it by using the **-ic** or **-in** option.</span></span> <span data-ttu-id="d0d4b-252">如果憑證存放區中的憑證無法唯一識別，MakeCert 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="d0d4b-252">If the certificate in the certificate store is not uniquely identified, MakeCert will fail.</span></span> |



 

 

 
