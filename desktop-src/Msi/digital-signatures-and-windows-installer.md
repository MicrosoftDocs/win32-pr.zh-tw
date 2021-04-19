---
description: Windows Installer 可以使用數位簽章來偵測損毀的資源。
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: 數位簽章和 Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d41dee15da938c586bf061d216d9003586a799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988919"
---
# <a name="digital-signatures-and-windows-installer"></a><span data-ttu-id="6134a-103">數位簽章和 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6134a-103">Digital Signatures and Windows Installer</span></span>

<span data-ttu-id="6134a-104">Windows Installer 可以使用數位簽章來偵測損毀的資源。</span><span class="sxs-lookup"><span data-stu-id="6134a-104">The Windows Installer can use digital signatures to detect corrupted resources.</span></span> <span data-ttu-id="6134a-105">簽署者憑證可以與要由封裝安裝之外部資源的簽署者憑證進行比較。</span><span class="sxs-lookup"><span data-stu-id="6134a-105">A signer certificate may be compared to the signer certificate of an external resource to be installed by the package.</span></span> <span data-ttu-id="6134a-106">如需有關使用數位簽章、數位憑證和 [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)的詳細資訊，請參閱 Microsoft WINDOWS 軟體開發套件 (SDK) 的 [安全性](https://msdn.microsoft.com/library/cc527452.aspx) 一節。</span><span class="sxs-lookup"><span data-stu-id="6134a-106">For more information regarding the use of digital signatures, digital certificates, and [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), see the [Security](https://msdn.microsoft.com/library/cc527452.aspx) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="6134a-107">使用 Windows Installer，數位簽章可與 Windows Installer 套件、轉換、修補程式、合併模組和外部封包檔一起使用。</span><span class="sxs-lookup"><span data-stu-id="6134a-107">With Windows Installer, digital signatures can be used with Windows Installer packages, transforms, patches, merge modules, and external cabinet files.</span></span> <span data-ttu-id="6134a-108">Windows Installer 已與 Microsoft Windows XP 上的軟體限制原則整合。</span><span class="sxs-lookup"><span data-stu-id="6134a-108">Windows Installer is integrated with Software Restriction Policy on Microsoft Windows XP.</span></span> <span data-ttu-id="6134a-109">您可以建立原則，以根據不同的準則（包括特定的簽署者憑證或發行者）來允許或防止安裝。</span><span class="sxs-lookup"><span data-stu-id="6134a-109">Policies can be created to allow or prevent installations based upon different criteria, including a particular signer certificate or publisher.</span></span> <span data-ttu-id="6134a-110">Windows Installer 可以在安裝 CryptoAPI 2.0 版的所有平臺上執行外部封包檔的簽章驗證。</span><span class="sxs-lookup"><span data-stu-id="6134a-110">The Windows Installer can perform signature validation of external cabinet files on all platforms where CryptoAPI version 2.0 is installed.</span></span>

<span data-ttu-id="6134a-111">請注意，Windows Installer SDK 所提供的範例 Setup.exe 啟動程式會在起始安裝之前，對 Windows Installer 套件執行簽章檢查。</span><span class="sxs-lookup"><span data-stu-id="6134a-111">Note that the sample Setup.exe bootstrap provided with the Windows Installer SDK performs a signature check on a Windows Installer package prior to initiating the installation.</span></span>

<span data-ttu-id="6134a-112">執行 [系統管理安裝](administrative-installation.md) 會移除套件中的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="6134a-112">Performing an [administrative installation](administrative-installation.md) removes the digital signature from the package.</span></span> <span data-ttu-id="6134a-113">系統管理安裝會修改安裝套件，以新增 AdminProperties 資料流程，這會使原始數位簽章失效。</span><span class="sxs-lookup"><span data-stu-id="6134a-113">An administrative installation modifies the installation package in order to add the AdminProperties stream, which would invalidate the original digital signature.</span></span> <span data-ttu-id="6134a-114">系統管理員可以重新簽署封裝。</span><span class="sxs-lookup"><span data-stu-id="6134a-114">An administrator can resign the package.</span></span>

<span data-ttu-id="6134a-115">將修補程式套用至系統管理安裝也會從套件中移除數位簽章。</span><span class="sxs-lookup"><span data-stu-id="6134a-115">Applying a patch to an administrative installation also removes the digital signature from the package.</span></span> <span data-ttu-id="6134a-116">原因是這些變更會保存在系統管理安裝的修補安裝套件中。</span><span class="sxs-lookup"><span data-stu-id="6134a-116">The reason is because the changes persist in the patched installation package of the administrative installation.</span></span> <span data-ttu-id="6134a-117">系統管理員可以重新簽署封裝。</span><span class="sxs-lookup"><span data-stu-id="6134a-117">An administrator can resign the package.</span></span>

<span data-ttu-id="6134a-118">從 Windows Installer 版本3.0 開始， [ (UAC) 修補的使用者帳戶控制](user-account-control--uac--patching.md) 可讓非系統管理員使用者修補個別電腦內容中安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6134a-118">Starting with Windows Installer version 3.0, [User Account Control (UAC) Patching](user-account-control--uac--patching.md) enables non-administrator users to patch applications installed in the per-machine context.</span></span> <span data-ttu-id="6134a-119">UAC 修補的啟用方式是在 [MsiPatchCertificate](msipatchcertificate-table.md) 資料表中提供簽署者憑證，並使用相同的憑證簽署修補程式。</span><span class="sxs-lookup"><span data-stu-id="6134a-119">UAC patching is enabled by providing a signer certificate in the [MsiPatchCertificate](msipatchcertificate-table.md) table and signing patches with the same certificate.</span></span>

<span data-ttu-id="6134a-120">如需詳細資訊，請參閱 [數位簽章和外部封包](digital-signatures-and-external-cabinet-files.md)檔、 [Windows Installer 和軟體限制原則](windows-installer-and-software-restriction-policy.md)、 [撰寫完整驗證的已簽署安裝](authoring-a-fully-verified-signed-installation.md)，以及 [以 URL 為基礎的 Windows Installer 安裝範例](a-url-based-windows-installer-installation-example.md)。</span><span class="sxs-lookup"><span data-stu-id="6134a-120">For more information, see [Digital Signatures and External Cabinet Files](digital-signatures-and-external-cabinet-files.md), [Windows Installer and Software Restriction Policy](windows-installer-and-software-restriction-policy.md), [Authoring a Fully Verified Signed Installation](authoring-a-fully-verified-signed-installation.md), and [A URL based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span>

 

 
