---
description: 使用 CAPICOM 物件的應用程式必須使用 CAPICOM.dll 建立。 CAPICOM.dll 也必須存在，並且在執行時間註冊以使用 CAPICOM 物件。
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: 準備開始使用 CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6fc1ad0dbfe3d4f8c4dae3286eb3ffa5e1ae03d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988930"
---
# <a name="getting-ready-to-use-capicom"></a><span data-ttu-id="5e5c9-104">準備開始使用 CAPICOM</span><span class="sxs-lookup"><span data-stu-id="5e5c9-104">Getting Ready to Use CAPICOM</span></span>

<span data-ttu-id="5e5c9-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5e5c9-106">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="5e5c9-107">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="5e5c9-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="5e5c9-108">使用 CAPICOM 物件的應用程式必須使用 CAPICOM.dll 建立。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-108">Applications that use CAPICOM objects must be created by using CAPICOM.dll.</span></span> <span data-ttu-id="5e5c9-109">CAPICOM.dll 也必須存在，並且在執行時間註冊以使用 CAPICOM 物件。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-109">CAPICOM.dll must also be present and registered at run time to use CAPICOM objects.</span></span> <span data-ttu-id="5e5c9-110">CAPICOM.dll 應新增至 Visual Basic 專案參考，才能使用 CAPICOM 物件。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-110">CAPICOM.dll should be added to Visual Basic projects references to use CAPICOM objects.</span></span>

<span data-ttu-id="5e5c9-111">您可以從可從 [PLATFORM SDK](https://www.microsoft.com/download/details.aspx?id=25281)可轉散發套件下載的可轉散發檔案取得 capicom： capicom。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-111">CAPICOM is available as a redistributable file that can be downloaded from [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span></span> <span data-ttu-id="5e5c9-112">如需有關 CAPICOM 版本的詳細資訊，請參閱 [Capicom 版本](capicom-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-112">For information about CAPICOM versions, see [CAPICOM Versions](capicom-versions.md).</span></span>

<span data-ttu-id="5e5c9-113">**註冊 CAPICOM.dll**</span><span class="sxs-lookup"><span data-stu-id="5e5c9-113">**To register CAPICOM.dll**</span></span>

-   <span data-ttu-id="5e5c9-114">在命令提示字元中，將目錄變更為儲存 CAPICOM.dll 的目錄，然後輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="5e5c9-114">At a command prompt, change the directory to the directory where CAPICOM.dll is stored, and then enter the following command:</span></span>

    <span data-ttu-id="5e5c9-115">**regsvr32 CAPICOM.dll**</span><span class="sxs-lookup"><span data-stu-id="5e5c9-115">**regsvr32 CAPICOM.dll**</span></span>

## <a name="example-code-limitations"></a><span data-ttu-id="5e5c9-116">範例程式碼限制</span><span class="sxs-lookup"><span data-stu-id="5e5c9-116">Example Code Limitations</span></span>

<span data-ttu-id="5e5c9-117">為了提供更簡潔、更容易閱讀的程式碼，在這些範例中，不一定會遵循良好程式設計實務的原則。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-117">To provide more concise, more readable code, principles of good programming practice are not always followed in these examples.</span></span> <span data-ttu-id="5e5c9-118">特別是，只會顯示有限的錯誤回應。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-118">In particular, only limited error responses are shown.</span></span> <span data-ttu-id="5e5c9-119">使用中的應用程式應該一律檢查傳回的錯誤碼，並在發生錯誤時執行適當的動作。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-119">Working applications should always check returned error codes and perform appropriate actions when an error is encountered.</span></span>

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a><span data-ttu-id="5e5c9-120">在 CAPICOM 中所需的金鑰容器、金鑰和憑證</span><span class="sxs-lookup"><span data-stu-id="5e5c9-120">Necessary Key Containers, Keys, and Certificates in CAPICOM</span></span>

<span data-ttu-id="5e5c9-121">雖然任何使用者都可以在任何電腦上執行具有 CAPICOM 物件的某些作業，但使用 CAPICOM 物件建立 [*數位簽章*](../secgloss/d-gly.md) 以及抓取封包訊息的純文字內容是以憑證為基礎的作業。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-121">While some operations with CAPICOM objects can be done on any computer by any user, creating [*digital signatures*](../secgloss/d-gly.md) and retrieving the plaintext content of an enveloped message using CAPICOM objects are certificate-based operations.</span></span> <span data-ttu-id="5e5c9-122">建立數位簽章的使用者，以及抓取封包訊息之加密內容的使用者，都必須具有具有可用相關私密金鑰的數位憑證。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-122">The user who creates a digital signature and the user who retrieves the encrypted contents of an enveloped message must have a digital certificate with an available associated private key.</span></span> <span data-ttu-id="5e5c9-123">如果沒有具有相關私密金鑰的憑證，密碼編譯作業將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-123">If a certificate with an associated private key is not present, the cryptographic operation will fail.</span></span> <span data-ttu-id="5e5c9-124">當應用程式正在執行時，CAPICOM 應用程式的使用者必須確保它們具有適當的憑證和可用的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-124">Users of CAPICOM applications must ensure that they have the appropriate certificate and available private key when the applications are running.</span></span>

<span data-ttu-id="5e5c9-125">下列各節中的一些範例會執行需要可用 [*公開/私密金鑰*](../secgloss/p-gly.md) 組的作業，以加密和解密檔案、訊息和簽章。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-125">Some examples in the following sections perform operations that require an available [*public/private key pair*](../secgloss/p-gly.md) for encrypting and decrypting files, messages, and signatures.</span></span> <span data-ttu-id="5e5c9-126">其中許多程式會在執行時間進行編譯和執行，但不會有適當的 [*金鑰容器*](../secgloss/k-gly.md)、金鑰、憑證存放區和 [*憑證*](../secgloss/c-gly.md) 存在於這些存放區中。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-126">Many of these programs will compile and run but fail at run time without the existence of proper [*key containers*](../secgloss/k-gly.md), keys, certificate stores, and [*certificates*](../secgloss/c-gly.md) in those stores.</span></span>

<span data-ttu-id="5e5c9-127">**建立自我簽署憑證**</span><span class="sxs-lookup"><span data-stu-id="5e5c9-127">**To create a self-signed certificate**</span></span>

1.  <span data-ttu-id="5e5c9-128">安裝簽署工具。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-128">Install the signing tools.</span></span> <span data-ttu-id="5e5c9-129">這些會安裝為 Microsoft Windows 軟體開發套件 (SDK) 、平臺軟體發展工具組 (SDK) 或 .NET Framework SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-129">These are installed as part of the Microsoft Windows Software Development Kit (SDK), the Platform Software Development Kit (SDK), or the .NET Framework SDK.</span></span>
2.  <span data-ttu-id="5e5c9-130">下載 Makecert.exe 之後，請在命令提示字元中執行下列命令、將使用者名稱 *取代為使用者* 名稱、 *OrganizationName* 的組織名稱，以及用於公司 *名稱的公司名稱：*</span><span class="sxs-lookup"><span data-stu-id="5e5c9-130">After Makecert.exe is downloaded, run the following command at a command prompt, substituting a user name for *UserName*, an organization name for *OrganizationName*, and a company name for *CompanyName*:</span></span>

    <span data-ttu-id="5e5c9-131">**makecert-r-n "cn =**_UserName_*_，ou =_*_OrganizationName_*_，o =_*_公司名稱_*_"-ss my_*</span><span class="sxs-lookup"><span data-stu-id="5e5c9-131">**makecert -r -n "cn=**_UserName_*_, ou=_*_OrganizationName_*_, o=_*_CompanyName_*_" -ss my_*</span></span>

3.  <span data-ttu-id="5e5c9-132">您可以將憑證放在目前使用者的 [我的存放區] 中。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-132">The certificate can be placed in the My store of the current user.</span></span> <span data-ttu-id="5e5c9-133">將建立的憑證匯入至根存放區，使其成為受信任的憑證。</span><span class="sxs-lookup"><span data-stu-id="5e5c9-133">Import the certificate created into the root store so that it is trusted.</span></span>

 

 
