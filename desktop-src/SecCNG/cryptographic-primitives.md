---
description: CNG API 提供一組執行基本密碼編譯作業的函式，例如建立雜湊或加密和解密資料。 如需這些函式的詳細資訊，請參閱 CNG 密碼編譯基本函數。
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: 密碼編譯基本類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0f390b36bc500bf80b5b2ef0065651cf99f5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510884"
---
# <a name="cryptographic-primitives"></a><span data-ttu-id="3a059-104">密碼編譯基本類型</span><span class="sxs-lookup"><span data-stu-id="3a059-104">Cryptographic Primitives</span></span>

<span data-ttu-id="3a059-105">CNG API 提供一組執行基本密碼編譯作業的函式，例如建立雜湊或加密和解密資料。</span><span class="sxs-lookup"><span data-stu-id="3a059-105">The CNG API provides a set of functions that perform basic cryptographic operations such as creating hashes or encrypting and decrypting data.</span></span> <span data-ttu-id="3a059-106">如需這些函式的詳細資訊，請參閱 [CNG 密碼編譯基本函數](cng-cryptographic-primitive-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="3a059-106">For more information about these functions, see [CNG Cryptographic Primitive Functions](cng-cryptographic-primitive-functions.md).</span></span>

<span data-ttu-id="3a059-107">CNG 實行了許多密碼編譯演算法。</span><span class="sxs-lookup"><span data-stu-id="3a059-107">CNG implements numerous cryptographic algorithms.</span></span> <span data-ttu-id="3a059-108">演算法的每個演算法或類別都會公開自己的基本 API。</span><span class="sxs-lookup"><span data-stu-id="3a059-108">Each algorithm or class of algorithms exposes its own primitive API.</span></span> <span data-ttu-id="3a059-109">您可以同時安裝指定演算法的多個實值;不過，在任何指定的時間，都只會有一個預設的實作為預設值。</span><span class="sxs-lookup"><span data-stu-id="3a059-109">Multiple implementations of a given algorithm can be installed at the same time; however, only one implementation will be the default at any given time.</span></span>

<span data-ttu-id="3a059-110">CNG 中的每個演算法類別都是由基本路由器表示。</span><span class="sxs-lookup"><span data-stu-id="3a059-110">Each algorithm class in CNG is represented by a primitive router.</span></span> <span data-ttu-id="3a059-111">使用 CNG 基本函式的應用程式會在使用者模式中 Bcrypt.dll 連結到路由器二進位檔案，或在呼叫函式之前 Ksecdd.sys 在核心模式中。</span><span class="sxs-lookup"><span data-stu-id="3a059-111">Applications using the CNG primitive functions will link to the router binary file Bcrypt.dll in user mode, or Ksecdd.sys in kernel mode before calling the functions.</span></span> <span data-ttu-id="3a059-112">各種路由器常式都會管理所有的演算法基本專案。</span><span class="sxs-lookup"><span data-stu-id="3a059-112">Various router routines manage all of the algorithm primitives.</span></span> <span data-ttu-id="3a059-113">這些路由器會追蹤系統上所安裝的每個演算法執行，並將每個函式呼叫路由至適當的基本提供者模組。</span><span class="sxs-lookup"><span data-stu-id="3a059-113">These routers track each algorithm implementation installed on the system and route each function call to the appropriate primitive provider module.</span></span>

<span data-ttu-id="3a059-114">CNG 提供下列演算法類別的基本類型。</span><span class="sxs-lookup"><span data-stu-id="3a059-114">CNG provides primitives for the following classes of algorithms.</span></span>



| <span data-ttu-id="3a059-115">演算法類別</span><span class="sxs-lookup"><span data-stu-id="3a059-115">Algorithm class</span></span>                                                                                                                                                  | <span data-ttu-id="3a059-116">Description</span><span class="sxs-lookup"><span data-stu-id="3a059-116">Description</span></span>                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a059-117"><span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>亂數產生器</span><span class="sxs-lookup"><span data-stu-id="3a059-117"><span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Random number generator</span></span><br/> | <span data-ttu-id="3a059-118">可插入的亂數字產生 (RNG) 。</span><span class="sxs-lookup"><span data-stu-id="3a059-118">Pluggable random number generation (RNG).</span></span><br/>                                                         |
| <span data-ttu-id="3a059-119"><span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>散 列</span><span class="sxs-lookup"><span data-stu-id="3a059-119"><span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hashing</span></span><br/>                                                                 | <span data-ttu-id="3a059-120">用於雜湊的演算法，例如 SHA1 和 SHA2。</span><span class="sxs-lookup"><span data-stu-id="3a059-120">Algorithms used for hashing, such as SHA1 and SHA2.</span></span><br/>                                               |
| <span data-ttu-id="3a059-121"><span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>對稱式加密</span><span class="sxs-lookup"><span data-stu-id="3a059-121"><span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Symmetric encryption</span></span><br/>             | <span data-ttu-id="3a059-122">用於對稱式加密的演算法，例如 AES、3DES 和 RC4。</span><span class="sxs-lookup"><span data-stu-id="3a059-122">Algorithms used for symmetric encryption, such as AES, 3DES, and RC4.</span></span><br/>                             |
| <span data-ttu-id="3a059-123"><span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>非對稱式加密</span><span class="sxs-lookup"><span data-stu-id="3a059-123"><span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Asymmetric encryption</span></span><br/>         | <span data-ttu-id="3a059-124">非對稱 (公開金鑰) 支援加密的演算法，例如 RSA。</span><span class="sxs-lookup"><span data-stu-id="3a059-124">Asymmetric (public key) algorithms that support encryption, such as RSA.</span></span><br/>                          |
| <span data-ttu-id="3a059-125"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>簽名</span><span class="sxs-lookup"><span data-stu-id="3a059-125"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span><br/>                                                         | <span data-ttu-id="3a059-126">簽署演算法，例如 DSA 和 ECDSA。</span><span class="sxs-lookup"><span data-stu-id="3a059-126">Signature algorithms such as DSA and ECDSA.</span></span> <span data-ttu-id="3a059-127">此類別也可以搭配 RSA 使用。</span><span class="sxs-lookup"><span data-stu-id="3a059-127">This class can also be used with RSA.</span></span><br/>                 |
| <span data-ttu-id="3a059-128"><span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>秘密合約</span><span class="sxs-lookup"><span data-stu-id="3a059-128"><span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Secret agreement</span></span><br/>                             | <span data-ttu-id="3a059-129">秘密協定演算法，例如 Diffie-Hellman (DH) 和橢圓曲線 Diffie-Hellman (ECDH) 。</span><span class="sxs-lookup"><span data-stu-id="3a059-129">Secret agreement algorithms such as Diffie-Hellman (DH) and elliptic curve Diffie-Hellman (ECDH).</span></span><br/> |



 

<span data-ttu-id="3a059-130">下圖顯示 CNG 密碼編譯基本專案的設計和功能。</span><span class="sxs-lookup"><span data-stu-id="3a059-130">The following illustration shows the design and function of the CNG cryptographic primitives.</span></span>

![cng 密碼編譯基本專案的設計和功能](images/ssdk-cng1c.png)

<span data-ttu-id="3a059-132">標頭檔 Bcrypt 會將 **MS \_ 基本 \_ 提供者** 常數定義為 "Microsoft 基本提供者"。</span><span class="sxs-lookup"><span data-stu-id="3a059-132">The header file Bcrypt.h defines the **MS\_PRIMITIVE\_PROVIDER** constant as "Microsoft Primitive Provider".</span></span> <span data-ttu-id="3a059-133">若要使用 Microsoft 基本提供者，請將此值傳遞給 [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)。</span><span class="sxs-lookup"><span data-stu-id="3a059-133">To use the Microsoft Primitive Provider, pass this value to [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).</span></span>

 

 




