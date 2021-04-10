---
description: 支援數位簽章和資料加密。 它被視為一般用途密碼編譯服務提供者 (CSP) 。
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027178"
---
# <a name="prov_rsa_aes"></a><span data-ttu-id="62fa2-104">>PROV \_ RSA \_ AES</span><span class="sxs-lookup"><span data-stu-id="62fa2-104">PROV\_RSA\_AES</span></span>

<span data-ttu-id="62fa2-105">>PROV \_ RSA \_ AES 提供者類型支援 [數位簽章](digital-signatures.md) 和資料加密。</span><span class="sxs-lookup"><span data-stu-id="62fa2-105">The PROV\_RSA\_AES provider type supports both [digital signatures](digital-signatures.md) and data encryption.</span></span> <span data-ttu-id="62fa2-106">它被視為一般用途 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 。</span><span class="sxs-lookup"><span data-stu-id="62fa2-106">It is considered a general purpose [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="62fa2-107">RSA [*公開金鑰演算法*](../secgloss/p-gly.md) 可用於所有的 [*公開金鑰*](../secgloss/p-gly.md) 作業。</span><span class="sxs-lookup"><span data-stu-id="62fa2-107">The RSA [*public key algorithm*](../secgloss/p-gly.md) is used for all [*public key*](../secgloss/p-gly.md) operations.</span></span>

## <a name="algorithms-supported"></a><span data-ttu-id="62fa2-108">支援的演算法</span><span class="sxs-lookup"><span data-stu-id="62fa2-108">Algorithms Supported</span></span>

<span data-ttu-id="62fa2-109">如需這些演算法的說明，請參閱詞彙。</span><span class="sxs-lookup"><span data-stu-id="62fa2-109">For descriptions of each of these algorithms, see the glossary.</span></span>



| <span data-ttu-id="62fa2-110">目的</span><span class="sxs-lookup"><span data-stu-id="62fa2-110">Purpose</span></span>      | <span data-ttu-id="62fa2-111">支援的演算法</span><span class="sxs-lookup"><span data-stu-id="62fa2-111">Supported algorithms</span></span>                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62fa2-112">金鑰交換</span><span class="sxs-lookup"><span data-stu-id="62fa2-112">Key Exchange</span></span> | [<span data-ttu-id="62fa2-113">*RSA*</span><span class="sxs-lookup"><span data-stu-id="62fa2-113">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="62fa2-114">簽名</span><span class="sxs-lookup"><span data-stu-id="62fa2-114">Signature</span></span>    | [<span data-ttu-id="62fa2-115">*RSA*</span><span class="sxs-lookup"><span data-stu-id="62fa2-115">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="62fa2-116">加密</span><span class="sxs-lookup"><span data-stu-id="62fa2-116">Encryption</span></span>   | [<span data-ttu-id="62fa2-117">*RC2*</span><span class="sxs-lookup"><span data-stu-id="62fa2-117">*RC2*</span></span>](../secgloss/r-gly.md)<br/> [<span data-ttu-id="62fa2-118">*RC4*</span><span class="sxs-lookup"><span data-stu-id="62fa2-118">*RC4*</span></span>](../secgloss/r-gly.md)<br/> <span data-ttu-id="62fa2-119">[*進階加密標準*](../secgloss/a-gly.md) (AES) </span><span class="sxs-lookup"><span data-stu-id="62fa2-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span></span> <br/>                                                       |
| <span data-ttu-id="62fa2-120">雜湊</span><span class="sxs-lookup"><span data-stu-id="62fa2-120">Hashing</span></span>      | [<span data-ttu-id="62fa2-121">*MD2*</span><span class="sxs-lookup"><span data-stu-id="62fa2-121">*MD2*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="62fa2-122">*MD4*</span><span class="sxs-lookup"><span data-stu-id="62fa2-122">*MD4*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="62fa2-123">*MD5*</span><span class="sxs-lookup"><span data-stu-id="62fa2-123">*MD5*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="62fa2-124">*SHA-1*</span><span class="sxs-lookup"><span data-stu-id="62fa2-124">*SHA-1*</span></span>](../secgloss/s-gly.md)<br/> <span data-ttu-id="62fa2-125">SHA-1 (256 SHA-1、SHA-384 和 SHA-512) </span><span class="sxs-lookup"><span data-stu-id="62fa2-125">SHA-2 (SHA-256, SHA-384, and SHA-512)</span></span><br/> |



 

## <a name="related-documentation"></a><span data-ttu-id="62fa2-126">相關文件</span><span class="sxs-lookup"><span data-stu-id="62fa2-126">Related Documentation</span></span>

<span data-ttu-id="62fa2-127">此提供者類型是由 Microsoft 和 RSA 資料安全性所定義。</span><span class="sxs-lookup"><span data-stu-id="62fa2-127">This provider type is defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="62fa2-128">本檔將在下列檔中說明：</span><span class="sxs-lookup"><span data-stu-id="62fa2-128">It is described in the following documents:</span></span>

-   <span data-ttu-id="62fa2-129">*Microsoft 密碼編譯服務提供者程式設計人員指南*，microsoft，1996。</span><span class="sxs-lookup"><span data-stu-id="62fa2-129">*Microsoft Cryptographic Service Provider Programmer's Guide*, Microsoft, 1996.</span></span>
-   <span data-ttu-id="62fa2-130">RSA 實驗室，公開金鑰加密標準，RSA 資料安全性，1993年11月。</span><span class="sxs-lookup"><span data-stu-id="62fa2-130">RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.</span></span>

> [!Note]  
> <span data-ttu-id="62fa2-131">這些資源可能無法在某些語言及國家/地區中使用。</span><span class="sxs-lookup"><span data-stu-id="62fa2-131">These resources may not be available in some languages and countries or regions.</span></span>

 

 

 
