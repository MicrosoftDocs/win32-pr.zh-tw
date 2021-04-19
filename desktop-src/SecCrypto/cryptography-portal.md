---
description: 使用加密技術來加密公開金鑰、加密演算法、RSA 加密及數位憑證。
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: 密碼編譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970791"
---
# <a name="cryptography"></a><span data-ttu-id="81179-103">密碼編譯</span><span class="sxs-lookup"><span data-stu-id="81179-103">Cryptography</span></span>

## <a name="purpose"></a><span data-ttu-id="81179-104">目的</span><span class="sxs-lookup"><span data-stu-id="81179-104">Purpose</span></span>

<span data-ttu-id="81179-105">密碼編譯是使用程式碼來轉換資料，如此一來，只有特定的收件者才能夠使用金鑰來讀取它。</span><span class="sxs-lookup"><span data-stu-id="81179-105">Cryptography is the use of codes to convert data so that only a specific recipient will be able to read it, using a key.</span></span>

<span data-ttu-id="81179-106">Microsoft 密碼編譯技術包括 CryptoAPI、密碼編譯服務提供者 (CSP) 、CryptoAPI 工具、CAPICOM、WinTrust、發行和管理憑證，以及開發可自訂的公開金鑰基礎結構。</span><span class="sxs-lookup"><span data-stu-id="81179-106">Microsoft cryptographic technologies include CryptoAPI, Cryptographic Service Providers (CSP), CryptoAPI Tools, CAPICOM, WinTrust, issuing and managing certificates, and developing customizable public key infrastructures.</span></span> <span data-ttu-id="81179-107">此外也會說明憑證和智慧卡註冊、憑證管理和自訂模組開發。</span><span class="sxs-lookup"><span data-stu-id="81179-107">Certificate and smart card enrollment, certificate management, and custom module development are also described.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="81179-108">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="81179-108">Developer audience</span></span>

<span data-ttu-id="81179-109">CryptoAPI 適用于 Windows 應用程式的開發人員，可讓使用者在安全的環境中建立及交換檔和其他資料，尤其是透過非安全的媒體（例如網際網路）。</span><span class="sxs-lookup"><span data-stu-id="81179-109">CryptoAPI is intended for use by developers of Windows-based applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="81179-110">開發人員應該熟悉 C 和 c + + 程式設計語言和 Windows 程式設計環境。</span><span class="sxs-lookup"><span data-stu-id="81179-110">Developers should be familiar with the C and C++ programming languages and the Windows programming environment.</span></span> <span data-ttu-id="81179-111">雖然並非必要，但建議您瞭解密碼編譯或安全性相關的主題。</span><span class="sxs-lookup"><span data-stu-id="81179-111">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="81179-112">CAPICOM 是僅限32位的元件，適用于使用 Visual Basic Scripting Edition (VBScript) 程式設計語言或 c + + 程式設計語言來建立應用程式的開發人員。</span><span class="sxs-lookup"><span data-stu-id="81179-112">CAPICOM is a 32-bit only component that is intended for use by developers who are creating applications using Visual Basic Scripting Edition (VBScript) programming language or the C++ programming language.</span></span> <span data-ttu-id="81179-113">您可以在 Run-Time 需求所指定的作業系統中使用 CAPICOM。</span><span class="sxs-lookup"><span data-stu-id="81179-113">CAPICOM is available for use in the operating systems specified in Run-Time Requirements.</span></span> <span data-ttu-id="81179-114">針對未來的開發，建議您使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="81179-114">For future development, we recommend that you use the .NET Framework to implement security features.</span></span> <span data-ttu-id="81179-115">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。</span><span class="sxs-lookup"><span data-stu-id="81179-115">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="81179-116">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="81179-116">Run-time requirements</span></span>

<span data-ttu-id="81179-117">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="81179-117">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="81179-118">下列作業系統和版本支援 CAPICOM 2.1.0.2：</span><span class="sxs-lookup"><span data-stu-id="81179-118">CAPICOM 2.1.0.2 is supported on the following operating systems and versions:</span></span>

-   <span data-ttu-id="81179-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="81179-119">Windows Server 2003</span></span>
-   <span data-ttu-id="81179-120">Windows XP</span><span class="sxs-lookup"><span data-stu-id="81179-120">Windows XP</span></span>

<span data-ttu-id="81179-121">您可以從可從 [PLATFORM SDK](https://www.microsoft.com/download/details.aspx?id=25281)可轉散發套件下載的可轉散發檔案取得 capicom： capicom。</span><span class="sxs-lookup"><span data-stu-id="81179-121">CAPICOM is available as a redistributable file that can be downloaded from [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span></span>

<span data-ttu-id="81179-122">憑證服務需要下列作業系統版本：</span><span class="sxs-lookup"><span data-stu-id="81179-122">Certificate Services requires the following versions of these operating systems:</span></span>

-   <span data-ttu-id="81179-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81179-123">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="81179-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81179-124">Windows Server 2008</span></span>
-   <span data-ttu-id="81179-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="81179-125">Windows Server 2003</span></span>

## <a name="in-this-section"></a><span data-ttu-id="81179-126">本節內容</span><span class="sxs-lookup"><span data-stu-id="81179-126">In this section</span></span>



| <span data-ttu-id="81179-127">主題</span><span class="sxs-lookup"><span data-stu-id="81179-127">Topic</span></span>                                                           | <span data-ttu-id="81179-128">描述</span><span class="sxs-lookup"><span data-stu-id="81179-128">Description</span></span>                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81179-129">關於密碼編譯</span><span class="sxs-lookup"><span data-stu-id="81179-129">About Cryptography</span></span>](about-cryptography.md)<br/>         | <span data-ttu-id="81179-130">重要的密碼編譯概念，以及 Microsoft 加密技術的高階觀點。</span><span class="sxs-lookup"><span data-stu-id="81179-130">Key cryptography concepts and a high-level view of Microsoft cryptography technologies.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="81179-131">使用加密</span><span class="sxs-lookup"><span data-stu-id="81179-131">Using Cryptography</span></span>](using-cryptography.md)<br/>         | <span data-ttu-id="81179-132">使用 CryptoAPI 函式和 CAPICOM 物件的 C 和 Visual Basic 程式的密碼編譯器、程式和擴充的範例。</span><span class="sxs-lookup"><span data-stu-id="81179-132">Cryptography processes, procedures, and extended samples of C and Visual Basic programs using CryptoAPI functions and CAPICOM objects.</span></span><br/>                                                                            |
| [<span data-ttu-id="81179-133">密碼編譯參考</span><span class="sxs-lookup"><span data-stu-id="81179-133">Cryptography Reference</span></span>](cryptography-reference.md)<br/> | <span data-ttu-id="81179-134">Microsoft 加密函式、介面、物件、結構和其他程式設計項目的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="81179-134">Detailed descriptions of the Microsoft cryptography functions, interfaces, objects, structures, and other programming elements.</span></span> <span data-ttu-id="81179-135">包含使用數位憑證的 API 參考描述。</span><span class="sxs-lookup"><span data-stu-id="81179-135">Includes reference descriptions of the API for working with digital certificates.</span></span><br/> |



 

 

 




