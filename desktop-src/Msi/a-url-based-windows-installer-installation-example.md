---
description: 此範例說明如何建立 Windows Installer 套件的 URL 型安裝。
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: 以 URL 為基礎的 Windows Installer 安裝範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a210eb1b93202930309223b49c737aa85b1812
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "107001475"
---
# <a name="a-url-based-windows-installer-installation-example"></a><span data-ttu-id="6cf9f-103">以 URL 為基礎的 Windows Installer 安裝範例</span><span class="sxs-lookup"><span data-stu-id="6cf9f-103">A URL-Based Windows Installer Installation Example</span></span>

<span data-ttu-id="6cf9f-104">此範例說明如何建立 Windows Installer 套件的 URL 型安裝。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-104">This example illustrates how to create a URL-based installation of a Windows Installer package.</span></span> <span data-ttu-id="6cf9f-105">如需保護安裝和使用數位憑證的詳細資訊，請參閱 [撰寫安全安裝](guidelines-for-authoring-secure-installations.md) 和 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)的指導方針。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-105">For more information about securing installations and using digital certificates see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="6cf9f-106">若要重現此範例，您需要 [SignTool](../seccrypto/signtool.md) 公用程式。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-106">To reproduce this sample you need the [SignTool](../seccrypto/signtool.md) utility.</span></span> <span data-ttu-id="6cf9f-107">如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 中的 [CryptoAPI 工具參考](../seccrypto/cryptoapi-tools-reference.md) 。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-107">For details, see the [CryptoAPI Tools Reference](../seccrypto/cryptoapi-tools-reference.md) in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6cf9f-108">您也需要[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)的[Msistuff.exe](msistuff-exe.md)和 Setup.exe 公用程式。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-108">You also need [Msistuff.exe](msistuff-exe.md) and Setup.exe utilities from the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="6cf9f-109">如需詳細資訊，請參閱 [網際網路下載](internet-download-bootstrapping.md)啟動載入。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-109">For more information, see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

<span data-ttu-id="6cf9f-110">此範例具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="6cf9f-110">The example has the following specifications:</span></span>

-   <span data-ttu-id="6cf9f-111">當使用者造訪您的網站並按一下 [>mysetup.bat 安裝] 連結時，會顯示從該位置儲存或執行的選項。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-111">When users visit your website and click the "MySetup Installation" link, they are presented with the option to save or run from that location.</span></span> <span data-ttu-id="6cf9f-112">如果使用者選取從該位置執行，Setup.exe 會在其電腦上升級 Windows Installer 的版本（如有必要），在安裝程式套件上驗證數位簽章，並在其電腦上安裝套件。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-112">If the user selects to run from that location, the Setup.exe upgrades the version of Windows Installer on their computer, if necessary, verifies the digital signature on the installer package, and installs the package on their computer.</span></span>
-   <span data-ttu-id="6cf9f-113">有一個 Mycert.cer 的數位憑證，Mycert.cer. pvk 提供了私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-113">There is a digital certificate, Mycert.cer, provided with a private key, Mycert.pvk.</span></span>
-   <span data-ttu-id="6cf9f-114">客戶會造訪以安裝套件之假設網站的 URL 為 HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-114">The URL of the hypothetical website a customer would visit to install the package is https:\//www.blueyonderairlines.com/Products/MySetup/mysetup.html.</span></span>
-   <span data-ttu-id="6cf9f-115">Web 服務器版面配置如下所示。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-115">The web server layout is as follows.</span></span> 

    | <span data-ttu-id="6cf9f-116">URL</span><span class="sxs-lookup"><span data-stu-id="6cf9f-116">URL</span></span>                                                               | <span data-ttu-id="6cf9f-117">檔案</span><span class="sxs-lookup"><span data-stu-id="6cf9f-117">File</span></span>        | <span data-ttu-id="6cf9f-118">描述</span><span class="sxs-lookup"><span data-stu-id="6cf9f-118">Description</span></span>                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | <span data-ttu-id="6cf9f-119">HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/</span><span class="sxs-lookup"><span data-stu-id="6cf9f-119">https:\//www.blueyonderairlines.com/Products/MySetup/</span></span>               | <span data-ttu-id="6cf9f-120">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="6cf9f-120">Setup.exe</span></span>   | <span data-ttu-id="6cf9f-121">Setup.exe 啟動載入器。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-121">Setup.exe bootstrapper.</span></span>                        |
    | <span data-ttu-id="6cf9f-122">HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/</span><span class="sxs-lookup"><span data-stu-id="6cf9f-122">https:\//www.blueyonderairlines.com/Products/MySetup/</span></span>               | <span data-ttu-id="6cf9f-123">MySetup.msi</span><span class="sxs-lookup"><span data-stu-id="6cf9f-123">MySetup.msi</span></span> | <span data-ttu-id="6cf9f-124">安裝套件</span><span class="sxs-lookup"><span data-stu-id="6cf9f-124">Installation package</span></span>                           |
    | <span data-ttu-id="6cf9f-125">HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/</span><span class="sxs-lookup"><span data-stu-id="6cf9f-125">https:\//www.blueyonderairlines.com/Products/MySetup/</span></span>               | <span data-ttu-id="6cf9f-126">Cab1.cab</span><span class="sxs-lookup"><span data-stu-id="6cf9f-126">Cab1.cab</span></span>    | <span data-ttu-id="6cf9f-127">來源檔案封包 \# 1</span><span class="sxs-lookup"><span data-stu-id="6cf9f-127">Source file cabinet \#1</span></span>                        |
    | <span data-ttu-id="6cf9f-128">HTTPs： \/ /www.blueyonderairlines.com/Products/MySetup/</span><span class="sxs-lookup"><span data-stu-id="6cf9f-128">https:\//www.blueyonderairlines.com/Products/MySetup/</span></span>               | <span data-ttu-id="6cf9f-129">Cab2.cab</span><span class="sxs-lookup"><span data-stu-id="6cf9f-129">Cab2.cab</span></span>    | <span data-ttu-id="6cf9f-130">來源檔案封包 \# 2</span><span class="sxs-lookup"><span data-stu-id="6cf9f-130">Source file cabinet \#2</span></span>                        |
    | <span data-ttu-id="6cf9f-131">HTTPs： \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Ansi</span><span class="sxs-lookup"><span data-stu-id="6cf9f-131">https:\//www.blueyonderairlines.com/Products/Common/InstMsi/Ansi</span></span>    | <span data-ttu-id="6cf9f-132">Instmsi.exe</span><span class="sxs-lookup"><span data-stu-id="6cf9f-132">Instmsi.exe</span></span> | <span data-ttu-id="6cf9f-133">ANSI Windows Installer 2.0 可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-133">ANSI Windows Installer 2.0 redistributable.</span></span>    |
    | <span data-ttu-id="6cf9f-134">HTTPs： \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Unicode</span><span class="sxs-lookup"><span data-stu-id="6cf9f-134">https:\//www.blueyonderairlines.com/Products/Common/InstMsi/Unicode</span></span> | <span data-ttu-id="6cf9f-135">Instmsi.exe</span><span class="sxs-lookup"><span data-stu-id="6cf9f-135">Instmsi.exe</span></span> | <span data-ttu-id="6cf9f-136">Unicode Windows Installer 2.0 可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="6cf9f-136">Unicode Windows Installer 2.0 redistributable.</span></span> |

    

     

[<span data-ttu-id="6cf9f-137">繼續</span><span class="sxs-lookup"><span data-stu-id="6cf9f-137">Continue</span></span>](configuring-the-setup-exe-resources.md)

 

 
