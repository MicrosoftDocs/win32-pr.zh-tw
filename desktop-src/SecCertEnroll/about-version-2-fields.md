---
description: X.509 版本 2 憑證包含版本 1 中定義的基本欄位，並新增下列欄位。
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: 第2版欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191117"
---
# <a name="version-2-fields"></a><span data-ttu-id="31357-103">第2版欄位</span><span class="sxs-lookup"><span data-stu-id="31357-103">Version 2 Fields</span></span>

<span data-ttu-id="31357-104">X.509 版本 2 憑證包含版本 1 中定義的基本欄位，並新增下列欄位。</span><span class="sxs-lookup"><span data-stu-id="31357-104">An X.509 version 2 certificate contains the basic fields defined in version 1 and adds the following fields.</span></span>

## <a name="issuer-unique-identifier"></a><span data-ttu-id="31357-105">簽發者唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="31357-105">Issuer Unique Identifier</span></span>

<span data-ttu-id="31357-106">包含唯一識別碼，可以在一段時間後，當其他實體重複使用 CA 時，清楚識別該 CA 的 X.500 名稱。</span><span class="sxs-lookup"><span data-stu-id="31357-106">Contains a unique value that can be used to make the X.500 name of the CA unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a><span data-ttu-id="31357-107">主體唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="31357-107">Subject Unique Identifier</span></span>

<span data-ttu-id="31357-108">包含唯一識別碼，可以在一段時間後，當其他實體重複使用憑證主體時，清楚識別該憑證主體的 X.500 名稱。</span><span class="sxs-lookup"><span data-stu-id="31357-108">Contains a unique value that can be used to make the X.500 name of the certificate subject unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a><span data-ttu-id="31357-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="31357-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31357-110">基本欄位</span><span class="sxs-lookup"><span data-stu-id="31357-110">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="31357-111">第3版擴充功能</span><span class="sxs-lookup"><span data-stu-id="31357-111">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="31357-112">X.509 公開金鑰憑證</span><span class="sxs-lookup"><span data-stu-id="31357-112">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



