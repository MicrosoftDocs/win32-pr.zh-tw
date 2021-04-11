---
description: Microsoft Windows HTTP Services (WinHTTP) 憑證設定工具 &\# 0034; WinHttpCertCfg.exe&\# 0034;，可讓系統管理員在任何憑證存放區中安裝和設定用戶端憑證，該憑證存放區可由網際網路伺服器 Web 應用程式管理員 (IWAM) 帳戶存取。 此工具也可讓您不需要對帳戶（例如 IWAM 帳戶）採取任何特殊動作，就能在使用 Active Server Pages (ASP) 時取得憑證的存取權。
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe，憑證設定工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4250cd717b9f611f4f23f17c93069760c283c97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113136"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a><span data-ttu-id="74c12-104">WinHttpCertCfg.exe，憑證設定工具</span><span class="sxs-lookup"><span data-stu-id="74c12-104">WinHttpCertCfg.exe, a Certificate Configuration Tool</span></span>

<span data-ttu-id="74c12-105">[Microsoft WINDOWS HTTP Services (WinHTTP)](about-winhttp.md)憑證設定工具 "WinHttpCertCfg.exe"，可讓系統管理員在任何憑證存放區中安裝和設定用戶端憑證，該 [*憑證存放區*](glossary.md)可由網際網路伺服器 Web 應用程式管理員 (IWAM) 帳戶存取。</span><span class="sxs-lookup"><span data-stu-id="74c12-105">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) certificate configuration tool, "WinHttpCertCfg.exe", enables administrators to install and configure client certificates in any [*certificate store*](glossary.md) that can be accessed by the Internet Server Web Application Manager (IWAM) account.</span></span> <span data-ttu-id="74c12-106">此工具也可讓您不需要對帳戶（例如 IWAM 帳戶）採取任何特殊動作，就能在使用 Active Server Pages (ASP) 時取得憑證的存取權。</span><span class="sxs-lookup"><span data-stu-id="74c12-106">The tool also eliminates the need to do anything special to accounts such as the IWAM account to gain access to certificates when using Active Server Pages (ASP).</span></span>

<span data-ttu-id="74c12-107">Microsoft Management Console (MMC) 可讓系統管理員將用戶端憑證匯入本機電腦。</span><span class="sxs-lookup"><span data-stu-id="74c12-107">The Microsoft Management Console (MMC) enables administrators to import client certificates to a local computer.</span></span> <span data-ttu-id="74c12-108">不過，匯入憑證並不會自動授與其他帳戶私密金鑰的存取權。</span><span class="sxs-lookup"><span data-stu-id="74c12-108">However, importing a certificate does not automatically grant access to the private key for other accounts.</span></span> <span data-ttu-id="74c12-109">此私密金鑰是用戶端憑證驗證的必要項。</span><span class="sxs-lookup"><span data-stu-id="74c12-109">This private key is required for client certificate authentication.</span></span> <span data-ttu-id="74c12-110">Microsoft Windows HTTP Services (WinHTTP) 憑證設定工具可在必要時，將存取權授與其他帳戶，例如 IWAM 帳戶。</span><span class="sxs-lookup"><span data-stu-id="74c12-110">The Microsoft Windows HTTP Services (WinHTTP) certificate configuration tool provides the ability to grant access to additional accounts, such as the IWAM account, when required.</span></span>

-   [<span data-ttu-id="74c12-111">使用憑證設定工具</span><span class="sxs-lookup"><span data-stu-id="74c12-111">Using the Certificate Configuration Tool</span></span>](#using-the-certificate-configuration-tool)
-   [<span data-ttu-id="74c12-112">範例</span><span class="sxs-lookup"><span data-stu-id="74c12-112">Examples</span></span>](#examples)

## <a name="using-the-certificate-configuration-tool"></a><span data-ttu-id="74c12-113">使用憑證設定工具</span><span class="sxs-lookup"><span data-stu-id="74c12-113">Using the Certificate Configuration Tool</span></span>

<span data-ttu-id="74c12-114">您可以從 [Windows Server 2003 資源套件工具](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) 網站下載 WinHTTP 憑證設定工具（WinHttpCertCfg.exe）。</span><span class="sxs-lookup"><span data-stu-id="74c12-114">The WinHTTP certificate configuration tool, WinHttpCertCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="74c12-115">下列範例程式碼顯示要搭配此工具使用的有效命令列參數。</span><span class="sxs-lookup"><span data-stu-id="74c12-115">The following example code shows the valid command line parameters to use with this tool.</span></span>

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

<span data-ttu-id="74c12-116">下表列出設定工具的參數。</span><span class="sxs-lookup"><span data-stu-id="74c12-116">The following table lists parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74c12-117">參數</span><span class="sxs-lookup"><span data-stu-id="74c12-117">Parameter</span></span></th>
<th><span data-ttu-id="74c12-118">Description</span><span class="sxs-lookup"><span data-stu-id="74c12-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74c12-119">-?</span><span class="sxs-lookup"><span data-stu-id="74c12-119">-?</span></span></td>
<td><span data-ttu-id="74c12-120">顯示語法資料。</span><span class="sxs-lookup"><span data-stu-id="74c12-120">Displays syntax data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c12-121">-i</span><span class="sxs-lookup"><span data-stu-id="74c12-121">-i</span></span></td>
<td><span data-ttu-id="74c12-122">指定要從個人資訊交換匯入憑證 (PFX) 檔。</span><span class="sxs-lookup"><span data-stu-id="74c12-122">Specifies that the certificate is to be imported from a Personal Information Exchange (PFX) file.</span></span> <span data-ttu-id="74c12-123">此參數後面必須接著檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="74c12-123">This parameter must be followed by the name of the file.</span></span> <span data-ttu-id="74c12-124">當指定這個參數時， &quot; &quot; &quot; 也必須指定-a 和-c &quot; 。</span><span class="sxs-lookup"><span data-stu-id="74c12-124">When this parameter is specified, &quot;-a&quot; and &quot;-c&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c12-125">-g</span><span class="sxs-lookup"><span data-stu-id="74c12-125">-g</span></span></td>
<td><span data-ttu-id="74c12-126">指定授與私密金鑰的存取權。</span><span class="sxs-lookup"><span data-stu-id="74c12-126">Specifies that access is granted to a private key.</span></span> <span data-ttu-id="74c12-127">當指定這個參數時， &quot; &quot; &quot; 也必須指定-a、-c &quot; 和 &quot; -s &quot; 。</span><span class="sxs-lookup"><span data-stu-id="74c12-127">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c12-128">-r</span><span class="sxs-lookup"><span data-stu-id="74c12-128">-r</span></span></td>
<td><span data-ttu-id="74c12-129">指定移除私密金鑰的存取權。</span><span class="sxs-lookup"><span data-stu-id="74c12-129">Specifies that access is removed for a private key.</span></span> <span data-ttu-id="74c12-130">當指定這個參數時， &quot; &quot; &quot; 也必須指定-a、-c &quot; 和 &quot; -s &quot; 。</span><span class="sxs-lookup"><span data-stu-id="74c12-130">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c12-131">-l</span><span class="sxs-lookup"><span data-stu-id="74c12-131">-l</span></span></td>
<td><span data-ttu-id="74c12-132">指定列出具有私密金鑰存取權的帳戶。</span><span class="sxs-lookup"><span data-stu-id="74c12-132">Specifies that accounts with access to a private key are listed.</span></span> <span data-ttu-id="74c12-133">當指定這個參數時， &quot; &quot; &quot; 也必須指定-c 和-s &quot; 。</span><span class="sxs-lookup"><span data-stu-id="74c12-133">When this parameter is specified, &quot;-c&quot; and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c12-134">-a</span><span class="sxs-lookup"><span data-stu-id="74c12-134">-a</span></span></td>
<td><span data-ttu-id="74c12-135">指定要設定之電腦上的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="74c12-135">Specifies the user account on the machine being configured.</span></span> <span data-ttu-id="74c12-136">這可以是本機電腦或網域帳戶，例如 &quot; IWAM_TESTMACHINE &quot; 、 &quot; TESTUSER &quot; 或 &quot; TESTDOMAIN\DOMAINUSER &quot; 。</span><span class="sxs-lookup"><span data-stu-id="74c12-136">This could be a local machine or domain account, such as &quot;IWAM_TESTMACHINE&quot;, &quot;TESTUSER&quot;, or &quot;TESTDOMAIN\DOMAINUSER&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c12-137">-c</span><span class="sxs-lookup"><span data-stu-id="74c12-137">-c</span></span></td>
<td><span data-ttu-id="74c12-138">指定 <a href="glossary.md"><em>憑證存放區</em></a>的位置和名稱。</span><span class="sxs-lookup"><span data-stu-id="74c12-138">Specifies the location and name of the <a href="glossary.md"><em>certificate store</em></a>.</span></span> <span data-ttu-id="74c12-139">使用 &quot; LOCAL_MACHINE &quot; 或 &quot; CURRENT_USER &quot; 指定要用於位置的登錄分支。</span><span class="sxs-lookup"><span data-stu-id="74c12-139">Use &quot;LOCAL_MACHINE&quot; or &quot;CURRENT_USER&quot; to designate which registry branch to use for the location.</span></span> <span data-ttu-id="74c12-140"><em>憑證存放區</em>可以是電腦上安裝的任何一個。</span><span class="sxs-lookup"><span data-stu-id="74c12-140">The <em>certificate store</em> can be any installed on the machine.</span></span> <span data-ttu-id="74c12-141">一般名稱範例包括 &quot; MY &quot; 、 &quot; Root &quot; 和 &quot; TrustedPeople &quot; 。</span><span class="sxs-lookup"><span data-stu-id="74c12-141">Typical name examples are &quot;MY&quot;, &quot;Root&quot;, and &quot;TrustedPeople&quot;.</span></span> <span data-ttu-id="74c12-142"><em>憑證存放區</em>的位置和名稱會以反斜線分隔，例如 &quot; LOCAL_MACHINE \root &quot; 。</span><span class="sxs-lookup"><span data-stu-id="74c12-142">The location and name of the <em>certificate store</em> are separated with a backward slash, for example, &quot;LOCAL_MACHINE\Root&quot;.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="74c12-143">雖然您 &quot; &quot; 可以使用這個參數來指定登錄的 CURRENT_USER 分支，但延伸私密金鑰的存取主要是用於安裝在本機電腦 <a href="glossary.md"><em>憑證存放區</em></a> 中的憑證，可供多位使用者存取。</span><span class="sxs-lookup"><span data-stu-id="74c12-143">Although the &quot;CURRENT_USER&quot; branch of the registry can be specified with this parameter, extending access to private keys is primarily intended for certificates installed in a local computer <a href="glossary.md"><em>certificate store</em></a> that can be accessed by multiple users.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c12-144">-S</span><span class="sxs-lookup"><span data-stu-id="74c12-144">-s</span></span></td>
<td><span data-ttu-id="74c12-145">指定不區分大小寫的搜尋字串，以尋找包含此子字串的主體名稱的第一個列舉憑證。</span><span class="sxs-lookup"><span data-stu-id="74c12-145">Specifies a case-insensitive search string for finding the first enumerated certificate with a subject name that contains this substring.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c12-146">-p</span><span class="sxs-lookup"><span data-stu-id="74c12-146">-p</span></span></td>
<td><span data-ttu-id="74c12-147">指定用來匯入憑證和私密金鑰的密碼。</span><span class="sxs-lookup"><span data-stu-id="74c12-147">Specifies a password that is used to import the certificate and the private key.</span></span> <span data-ttu-id="74c12-148">這只會與匯入選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="74c12-148">This is only used with the import option.</span></span></td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> <span data-ttu-id="74c12-149">使用者必須有足夠的許可權才能使用此工具，這需要使用者是系統管理員，以及安裝用戶端憑證的相同使用者（如果有安裝的話）。</span><span class="sxs-lookup"><span data-stu-id="74c12-149">The user must have sufficient privileges to use this tool, which requires the user to be an administrator and the same user who installed the client certificate, if installed.</span></span>
>
> <span data-ttu-id="74c12-150">「WinHttpCertCfg.exe」工具不適用於設定儲存在檔案系統（例如 FAT32）中的憑證，這種方法不支援 (ACL) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="74c12-150">The "WinHttpCertCfg.exe" tool is not useful to configure certificates stored in a file system such as FAT32, which does not support access control lists (ACL).</span></span>

## <a name="examples"></a><span data-ttu-id="74c12-151">範例</span><span class="sxs-lookup"><span data-stu-id="74c12-151">Examples</span></span>

<span data-ttu-id="74c12-152">下列範例顯示可使用設定工具的一些方式。</span><span class="sxs-lookup"><span data-stu-id="74c12-152">The following examples show some of the ways in which the configuration tool can be used.</span></span>

1.  <span data-ttu-id="74c12-153">此命令會列出在登錄本機電腦分支的「根」 [*憑證存放區*](glossary.md) 中，可存取 "MyCertificate" 憑證之私密金鑰的帳戶 \_ 。</span><span class="sxs-lookup"><span data-stu-id="74c12-153">This command lists accounts that have access to the private key for the "MyCertificate" certificate in the "Root" [*certificate store*](glossary.md) of the LOCAL\_MACHINE branch of the registry.</span></span>

    <span data-ttu-id="74c12-154">**winHTTPcertcfg.exe-l-c 本機 \_ 電腦 \\ 根目錄-s MyCertificate**</span><span class="sxs-lookup"><span data-stu-id="74c12-154">**winhttpcertcfg -l -c LOCAL\_MACHINE\\Root -s MyCertificate**</span></span>

2.  <span data-ttu-id="74c12-155">此命令會在 TESTUSER 帳戶的 "My" [*憑證存放區*](glossary.md) 中，授與 "MyCertificate" 憑證私密金鑰的存取權。</span><span class="sxs-lookup"><span data-stu-id="74c12-155">This command grants access to the private key of the "MyCertificate" certificate in the "My" [*certificate store*](glossary.md) for the TESTUSER account.</span></span>

    <span data-ttu-id="74c12-156">**winHTTPcertcfg.exe-g-c 本機 \_ 電腦 \\ My-s MyCertificate-a TESTUSER**</span><span class="sxs-lookup"><span data-stu-id="74c12-156">**winhttpcertcfg -g -c LOCAL\_MACHINE\\My -s MyCertificate -a TESTUSER**</span></span>

3.  <span data-ttu-id="74c12-157">此命令會從 PFX 檔案匯入憑證和私密金鑰，並將私密金鑰存取權延伸至另一個帳戶。</span><span class="sxs-lookup"><span data-stu-id="74c12-157">This command imports a certificate and private key from a PFX file and extends private key access to another account.</span></span>

    <span data-ttu-id="74c12-158">**winHTTPcertcfg.exe-i PFXFile-c LOCAL \_ MACHINE \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**</span><span class="sxs-lookup"><span data-stu-id="74c12-158">**winhttpcertcfg -i PFXFile -c LOCAL\_MACHINE\\My -a IWAM\_TESTMACHINE -p PFXPassword**</span></span>

4.  <span data-ttu-id="74c12-159">此命令會針對 \_ 具有指定憑證的 IWAM TESTMACHINE 帳戶拒絕存取私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="74c12-159">This command denies access to the private key for the IWAM\_TESTMACHINE account with the specified certificate.</span></span>

    <span data-ttu-id="74c12-160">**winHTTPcertcfg.exe-r-c 本機 \_ 電腦 \\ 根目錄-s MYCERTIFICATE-IWAM \_ TESTMACHINE**</span><span class="sxs-lookup"><span data-stu-id="74c12-160">**winhttpcertcfg -r -c LOCAL\_MACHINE\\Root -s MyCertificate -a IWAM\_TESTMACHINE**</span></span>

 

 




