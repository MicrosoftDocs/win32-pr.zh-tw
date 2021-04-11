---
description: Microsoft 增強型密碼編譯提供者提供的應用程式安全性比 Microsoft 基礎密碼編譯提供者目前提供的安全性更強。 更高的金鑰長度可為使用者提供機密資料的更多保護。
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: 金鑰長度比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852896"
---
# <a name="key-length-comparison"></a><span data-ttu-id="d8e24-104">金鑰長度比較</span><span class="sxs-lookup"><span data-stu-id="d8e24-104">Key Length Comparison</span></span>

<span data-ttu-id="d8e24-105">Microsoft 增強型密碼編譯提供者提供的應用程式安全性比 Microsoft 基礎密碼編譯提供者目前提供的安全性更強。</span><span class="sxs-lookup"><span data-stu-id="d8e24-105">The Microsoft Enhanced Cryptographic Provider provides an application with stronger security than currently available with the Microsoft Base Cryptographic Provider.</span></span> <span data-ttu-id="d8e24-106">更高的金鑰長度可為使用者提供機密資料的更多保護。</span><span class="sxs-lookup"><span data-stu-id="d8e24-106">Greater key length gives users more protection for sensitive data.</span></span>

<span data-ttu-id="d8e24-107">下表列出基底提供者所支援的預設 [*金鑰長度*](../secgloss/k-gly.md) ，以及標準演算法的增強型提供者。</span><span class="sxs-lookup"><span data-stu-id="d8e24-107">The following table lists the default [*key lengths*](../secgloss/k-gly.md) supported by the Base Provider and the Enhanced Provider for standard algorithms.</span></span>



| <span data-ttu-id="d8e24-108">演算法</span><span class="sxs-lookup"><span data-stu-id="d8e24-108">Algorithm</span></span>                                                                                | <span data-ttu-id="d8e24-109">基底提供者</span><span class="sxs-lookup"><span data-stu-id="d8e24-109">Base Provider</span></span> | <span data-ttu-id="d8e24-110">強大且增強的提供者</span><span class="sxs-lookup"><span data-stu-id="d8e24-110">Strong and Enhanced Providers</span></span> |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| <span data-ttu-id="d8e24-111">RSA 金鑰交換</span><span class="sxs-lookup"><span data-stu-id="d8e24-111">RSA Key Exchange</span></span>                                                                         | <span data-ttu-id="d8e24-112">512位</span><span class="sxs-lookup"><span data-stu-id="d8e24-112">512-bit</span></span>       | <span data-ttu-id="d8e24-113">1024位</span><span class="sxs-lookup"><span data-stu-id="d8e24-113">1,024-bit</span></span>                     |
| <span data-ttu-id="d8e24-114">RSA 簽章</span><span class="sxs-lookup"><span data-stu-id="d8e24-114">RSA Signature</span></span>                                                                            | <span data-ttu-id="d8e24-115">512位</span><span class="sxs-lookup"><span data-stu-id="d8e24-115">512-bit</span></span>       | <span data-ttu-id="d8e24-116">1024位</span><span class="sxs-lookup"><span data-stu-id="d8e24-116">1,024-bit</span></span>                     |
| <span data-ttu-id="d8e24-117">RC2</span><span class="sxs-lookup"><span data-stu-id="d8e24-117">RC2</span></span>                                                                                      | <span data-ttu-id="d8e24-118">40位</span><span class="sxs-lookup"><span data-stu-id="d8e24-118">40-bit</span></span>        | <span data-ttu-id="d8e24-119">128位</span><span class="sxs-lookup"><span data-stu-id="d8e24-119">128-bit</span></span>                       |
| <span data-ttu-id="d8e24-120">RC4</span><span class="sxs-lookup"><span data-stu-id="d8e24-120">RC4</span></span>                                                                                      | <span data-ttu-id="d8e24-121">40位</span><span class="sxs-lookup"><span data-stu-id="d8e24-121">40-bit</span></span>        | <span data-ttu-id="d8e24-122">128位</span><span class="sxs-lookup"><span data-stu-id="d8e24-122">128-bit</span></span>                       |
| <span data-ttu-id="d8e24-123">DES</span><span class="sxs-lookup"><span data-stu-id="d8e24-123">DES</span></span>                                                                                      | <span data-ttu-id="d8e24-124">不支援</span><span class="sxs-lookup"><span data-stu-id="d8e24-124">Not supported</span></span> | <span data-ttu-id="d8e24-125">56位</span><span class="sxs-lookup"><span data-stu-id="d8e24-125">56-bit</span></span>                        |
| <span data-ttu-id="d8e24-126">[*三重 DES*](../secgloss/t-gly.md) (2-金鑰) </span><span class="sxs-lookup"><span data-stu-id="d8e24-126">[*Triple DES*](../secgloss/t-gly.md) (2-key)</span></span> | <span data-ttu-id="d8e24-127">不支援</span><span class="sxs-lookup"><span data-stu-id="d8e24-127">Not supported</span></span> | <span data-ttu-id="d8e24-128">112位</span><span class="sxs-lookup"><span data-stu-id="d8e24-128">112-bit</span></span>                       |
| <span data-ttu-id="d8e24-129">三重 DES (3-金鑰) </span><span class="sxs-lookup"><span data-stu-id="d8e24-129">Triple DES (3-key)</span></span>                                                                       | <span data-ttu-id="d8e24-130">不支援</span><span class="sxs-lookup"><span data-stu-id="d8e24-130">Not supported</span></span> | <span data-ttu-id="d8e24-131">168位</span><span class="sxs-lookup"><span data-stu-id="d8e24-131">168-bit</span></span>                       |



 

<span data-ttu-id="d8e24-132">增強型提供者支援 [*des*](../secgloss/d-gly.md)和 [*三重 des*](../secgloss/t-gly.md)演算法。</span><span class="sxs-lookup"><span data-stu-id="d8e24-132">[*DES*](../secgloss/d-gly.md) and [*Triple DES*](../secgloss/t-gly.md) algorithms are supported in the Enhanced Provider.</span></span>

<span data-ttu-id="d8e24-133">增強型提供者與使用較舊版本 CryptoAPI 散發的基底提供者回溯相容，但有下列例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d8e24-133">The Enhanced Provider is backward-compatible with the Base Provider distributed with earlier versions of CryptoAPI with the following exception.</span></span> <span data-ttu-id="d8e24-134">基底提供者和增強型提供者都只能產生預設金鑰長度的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="d8e24-134">Both the base provider and the Enhanced Provider can only generate session keys of default key length.</span></span> <span data-ttu-id="d8e24-135">基底提供者的工作階段金鑰預設長度為40位。</span><span class="sxs-lookup"><span data-stu-id="d8e24-135">The default length of session keys for the Base Provider is 40 bits.</span></span> <span data-ttu-id="d8e24-136">增強型提供者的預設金鑰長度是128位。</span><span class="sxs-lookup"><span data-stu-id="d8e24-136">The default key length for the Enhanced Provider is 128 bits.</span></span> <span data-ttu-id="d8e24-137">增強型提供者無法建立具有基底提供者相容金鑰長度的金鑰。</span><span class="sxs-lookup"><span data-stu-id="d8e24-137">The Enhanced Provider cannot create keys with Base Provider-compatible key lengths.</span></span> <span data-ttu-id="d8e24-138">不過，增強型提供者可以匯入任何大小的金鑰長度，最多可達128位。</span><span class="sxs-lookup"><span data-stu-id="d8e24-138">However, the Enhanced Provider can import key lengths of any size, up to 128 bits.</span></span>

 

 
