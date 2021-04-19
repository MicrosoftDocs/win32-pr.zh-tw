---
description: X.509 標準憑證包含版本、序號、演算法識別碼、簽發者名稱、有效的日期範圍、主體名稱、演算法和主體公開金鑰資訊，以及選擇性的簽發者唯一識別碼、主體唯一識別碼和延伸模組。
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: 憑證和 CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325086ab0dd46ace85745ca292bcab9bcd5324e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974604"
---
# <a name="certificates-and-cryptoapi"></a><span data-ttu-id="f6a15-103">憑證和 CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="f6a15-103">Certificates and CryptoAPI</span></span>

<span data-ttu-id="f6a15-104">[*CryptoAPI*](../secgloss/c-gly.md) 支援使用在 [IETF RFC 3280](https://www.ietf.org/rfc/rfc3280.txt)中定義的 x.509 憑證。</span><span class="sxs-lookup"><span data-stu-id="f6a15-104">[*CryptoAPI*](../secgloss/c-gly.md) supports using X.509 certificates as defined in [IETF RFC 3280](https://www.ietf.org/rfc/rfc3280.txt).</span></span> <span data-ttu-id="f6a15-105">本檔假設您使用的是 x.509 或可比較的 [*數位憑證*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="f6a15-105">This documentation assumes the use of an X.509 or comparable [*digital certificate*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="f6a15-106">X.509 標準憑證包含下列資訊。</span><span class="sxs-lookup"><span data-stu-id="f6a15-106">An X.509 standard certificate contains the following information.</span></span>



| <span data-ttu-id="f6a15-107">欄位</span><span class="sxs-lookup"><span data-stu-id="f6a15-107">Field</span></span>                | <span data-ttu-id="f6a15-108">描述</span><span class="sxs-lookup"><span data-stu-id="f6a15-108">Description</span></span>                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a15-109">版本</span><span class="sxs-lookup"><span data-stu-id="f6a15-109">Version</span></span>              | <span data-ttu-id="f6a15-110">憑證的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="f6a15-110">Version number of the certificate.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="f6a15-111">序號</span><span class="sxs-lookup"><span data-stu-id="f6a15-111">Serial Number</span></span>        | <span data-ttu-id="f6a15-112">憑證的序號。</span><span class="sxs-lookup"><span data-stu-id="f6a15-112">Serial number of the certificate.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="f6a15-113">演算法識別碼</span><span class="sxs-lookup"><span data-stu-id="f6a15-113">Algorithm Identifier</span></span> | <span data-ttu-id="f6a15-114">憑證簽署者使用的簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="f6a15-114">Signature algorithm used by the certificate signer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="f6a15-115">簽發者名稱</span><span class="sxs-lookup"><span data-stu-id="f6a15-115">Issuer Name</span></span>          | <span data-ttu-id="f6a15-116">憑證簽發者的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6a15-116">Name of the issuer of the certificate.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="f6a15-117">生效時間</span><span class="sxs-lookup"><span data-stu-id="f6a15-117">Not Before</span></span>           | <span data-ttu-id="f6a15-118">憑證無效之前的日期。</span><span class="sxs-lookup"><span data-stu-id="f6a15-118">Date before which the certificate is not valid.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="f6a15-119">不晚於</span><span class="sxs-lookup"><span data-stu-id="f6a15-119">Not After</span></span>            | <span data-ttu-id="f6a15-120">憑證不正確日期。</span><span class="sxs-lookup"><span data-stu-id="f6a15-120">Date after which the certificate is not valid.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="f6a15-121">主體名稱</span><span class="sxs-lookup"><span data-stu-id="f6a15-121">Subject Name</span></span>         | <span data-ttu-id="f6a15-122">憑證簽發者或實體的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6a15-122">Name of the person or entity to whom the certificate is being issued.</span></span>                                                                                                                                                      |
| <span data-ttu-id="f6a15-123">演算法</span><span class="sxs-lookup"><span data-stu-id="f6a15-123">Algorithm</span></span>            | <span data-ttu-id="f6a15-124">公開金鑰所使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="f6a15-124">Algorithm used for the public key.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="f6a15-125">主體公開金鑰</span><span class="sxs-lookup"><span data-stu-id="f6a15-125">Subject Public Key</span></span>   | <span data-ttu-id="f6a15-126">實際公開金鑰 (位字串) 。</span><span class="sxs-lookup"><span data-stu-id="f6a15-126">Actual public key (a bit string).</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="f6a15-127">簽發者唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="f6a15-127">Issuer Unique ID</span></span>     | <span data-ttu-id="f6a15-128">選擇性欄位。</span><span class="sxs-lookup"><span data-stu-id="f6a15-128">Optional Field.</span></span> <span data-ttu-id="f6a15-129">如果有的話，version 必須是第2版。</span><span class="sxs-lookup"><span data-stu-id="f6a15-129">If present, version must be version 2.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="f6a15-130">主體唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="f6a15-130">Subject Unique ID</span></span>    | <span data-ttu-id="f6a15-131">選擇性欄位。</span><span class="sxs-lookup"><span data-stu-id="f6a15-131">Optional Field.</span></span> <span data-ttu-id="f6a15-132">如果有的話，version 必須是第2版。</span><span class="sxs-lookup"><span data-stu-id="f6a15-132">If present, version must be version 2.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="f6a15-133">延伸模組</span><span class="sxs-lookup"><span data-stu-id="f6a15-133">Extensions</span></span>           | <span data-ttu-id="f6a15-134">選擇性欄位。</span><span class="sxs-lookup"><span data-stu-id="f6a15-134">Optional field.</span></span> <span data-ttu-id="f6a15-135">代表簽發者可能想要新增至憑證的其他資料，例如電子郵件地址或授權，以頒發證書。</span><span class="sxs-lookup"><span data-stu-id="f6a15-135">Represents additional data that an issuer can want to add to a certificate, such as email address or authorization to issue certificates.</span></span> <span data-ttu-id="f6a15-136">如果有擴充功能，版本必須是第3版。</span><span class="sxs-lookup"><span data-stu-id="f6a15-136">If extensions are present, version must be version 3.</span></span><br/> |



 

 

 
