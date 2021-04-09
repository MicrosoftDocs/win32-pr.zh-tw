---
description: 憑證服務支援使用 x.509 中所定義的憑證，ISO/IEC 9594-8 (也是 ISO/IEC) 。
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: 憑證內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848913"
---
# <a name="certificate-properties"></a><span data-ttu-id="c0748-103">憑證內容</span><span class="sxs-lookup"><span data-stu-id="c0748-103">Certificate Properties</span></span>

<span data-ttu-id="c0748-104">憑證服務支援使用 [*x.509*](../secgloss/x-gly.md) 中所定義的憑證，ISO/IEC 9594-8 (也是 ISO/IEC) 。</span><span class="sxs-lookup"><span data-stu-id="c0748-104">Certificate Services supports the use of certificates as defined in the ITU-T recommendation [*X.509*](../secgloss/x-gly.md) (also, ISO/IEC 9594-8).</span></span> <span data-ttu-id="c0748-105">以下是標準 x.509 憑證中包含的屬性。</span><span class="sxs-lookup"><span data-stu-id="c0748-105">The following are properties that are contained in a standard X.509 certificate.</span></span>



| <span data-ttu-id="c0748-106">欄位</span><span class="sxs-lookup"><span data-stu-id="c0748-106">Field</span></span>                                       | <span data-ttu-id="c0748-107">描述</span><span class="sxs-lookup"><span data-stu-id="c0748-107">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0748-108">版本</span><span class="sxs-lookup"><span data-stu-id="c0748-108">Version</span></span>                                     | <span data-ttu-id="c0748-109">憑證格式的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c0748-109">Version number of the certificate format.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="c0748-110">序號</span><span class="sxs-lookup"><span data-stu-id="c0748-110">Serial Number</span></span>                               | <span data-ttu-id="c0748-111">憑證的序號。</span><span class="sxs-lookup"><span data-stu-id="c0748-111">Serial number of the certificate.</span></span> <span data-ttu-id="c0748-112">此號碼是由簽發者所指派，在簽發的憑證的簽發者清單中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c0748-112">This number is assigned by the issuer and is unique within the issuer's list of issued certificates.</span></span>                                                                          |
| <span data-ttu-id="c0748-113">演算法識別碼和參數</span><span class="sxs-lookup"><span data-stu-id="c0748-113">Algorithm Identifier and Parameters</span></span>         | <span data-ttu-id="c0748-114">簽章演算法和簽發者使用的任何參數。</span><span class="sxs-lookup"><span data-stu-id="c0748-114">Signature algorithm and any parameters used by the issuer.</span></span>                                                                                                                                                      |
| <span data-ttu-id="c0748-115">Issuer</span><span class="sxs-lookup"><span data-stu-id="c0748-115">Issuer</span></span>                                      | <span data-ttu-id="c0748-116">簽發憑證的 [*憑證授權單位*](../secgloss/c-gly.md) 單位名稱。</span><span class="sxs-lookup"><span data-stu-id="c0748-116">Name of the [*certification authority*](../secgloss/c-gly.md) which issued the certificate.</span></span>                                               |
| <span data-ttu-id="c0748-117">在 (日期之前) </span><span class="sxs-lookup"><span data-stu-id="c0748-117">Not Before (Date)</span></span>                           | <span data-ttu-id="c0748-118">此日期之前的憑證無效。</span><span class="sxs-lookup"><span data-stu-id="c0748-118">Certificate not valid before this date.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="c0748-119"> (日期之後不) </span><span class="sxs-lookup"><span data-stu-id="c0748-119">Not After (Date)</span></span>                            | <span data-ttu-id="c0748-120">此日期之後的憑證無效。</span><span class="sxs-lookup"><span data-stu-id="c0748-120">Certificate not valid after this date.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="c0748-121">主體名稱</span><span class="sxs-lookup"><span data-stu-id="c0748-121">Subject Name</span></span>                                | <span data-ttu-id="c0748-122">憑證簽發者或實體的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0748-122">Name of the person or entity to whom the certificate is being issued.</span></span> <span data-ttu-id="c0748-123">此欄位也可以包含憑證收件者的組織、組織單位、位置、州/省和國家/地區。</span><span class="sxs-lookup"><span data-stu-id="c0748-123">This field can also include the certificate recipient's organization, organization unit, locality, state or province, and country/region.</span></span> |
| <span data-ttu-id="c0748-124">主體公開金鑰演算法和參數</span><span class="sxs-lookup"><span data-stu-id="c0748-124">Subject Public Key Algorithm and Parameters</span></span> | <span data-ttu-id="c0748-125">用於主體 [*公開金鑰*](../secgloss/p-gly.md)的演算法和任何參數。</span><span class="sxs-lookup"><span data-stu-id="c0748-125">The algorithm and any parameters used for the subject's [*public key*](../secgloss/p-gly.md).</span></span>                                                                       |
| <span data-ttu-id="c0748-126">主體公開金鑰</span><span class="sxs-lookup"><span data-stu-id="c0748-126">Subject Public Key</span></span>                          | <span data-ttu-id="c0748-127">實際的公開金鑰 (位字串) 。</span><span class="sxs-lookup"><span data-stu-id="c0748-127">The actual public key (a bit string).</span></span>                                                                                                                                                                           |
| <span data-ttu-id="c0748-128">簽名</span><span class="sxs-lookup"><span data-stu-id="c0748-128">Signature</span></span>                                   | <span data-ttu-id="c0748-129">簽發者所提供的簽章。</span><span class="sxs-lookup"><span data-stu-id="c0748-129">Signature as provided by the issuer.</span></span>                                                                                                                                                                            |



 

<span data-ttu-id="c0748-130">根據憑證的 [*x.509*](../secgloss/x-gly.md) 版本而定，憑證可以包含下列專案。</span><span class="sxs-lookup"><span data-stu-id="c0748-130">A certificate can contain the following items, depending on the [*X.509*](../secgloss/x-gly.md) version of the certificate.</span></span>



| <span data-ttu-id="c0748-131">選擇性欄位</span><span class="sxs-lookup"><span data-stu-id="c0748-131">Optional field</span></span>    | <span data-ttu-id="c0748-132">Description</span><span class="sxs-lookup"><span data-stu-id="c0748-132">Description</span></span>                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0748-133">簽發者唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="c0748-133">Issuer Unique ID</span></span>  | <span data-ttu-id="c0748-134">用來讓簽發者名稱明確地用於多個實體。</span><span class="sxs-lookup"><span data-stu-id="c0748-134">Used to make the issuer name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="c0748-135">僅存在於 [*x.509*](../secgloss/x-gly.md) 2.0 或更新版本中。</span><span class="sxs-lookup"><span data-stu-id="c0748-135">Present only in versions [*X.509*](../secgloss/x-gly.md) 2.0 or later.</span></span><br/> |
| <span data-ttu-id="c0748-136">主體唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="c0748-136">Subject unique ID</span></span> | <span data-ttu-id="c0748-137">用來將主體名稱明確地用於一個以上的實體。</span><span class="sxs-lookup"><span data-stu-id="c0748-137">Used to make the subject name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="c0748-138">只存在於 x.509 2.0 或更新版本中。</span><span class="sxs-lookup"><span data-stu-id="c0748-138">Present only in X.509 2.0 or later.</span></span><br/>                                                                     |
| <span data-ttu-id="c0748-139">延伸模組</span><span class="sxs-lookup"><span data-stu-id="c0748-139">Extensions</span></span>        | <span data-ttu-id="c0748-140">用於指定任何所需的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="c0748-140">For specifying any desired custom properties.</span></span> <span data-ttu-id="c0748-141">憑證中可以包含任意數目的延伸模組欄位。</span><span class="sxs-lookup"><span data-stu-id="c0748-141">Any number of extension fields can be included in the certificate.</span></span> <span data-ttu-id="c0748-142">只存在於3.0 版的 x.509 中。</span><span class="sxs-lookup"><span data-stu-id="c0748-142">Present only in version X.509 3.0.</span></span><br/>                                            |



 

> [!Note]  
> <span data-ttu-id="c0748-143">Microsoft 憑證服務會發出 x.509 第3版憑證。</span><span class="sxs-lookup"><span data-stu-id="c0748-143">Microsoft Certificate Services issues X.509 version 3 certificates.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c0748-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0748-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0748-145">名稱屬性</span><span class="sxs-lookup"><span data-stu-id="c0748-145">Name Properties</span></span>](name-properties.md)
</dt> </dl>

 

 
