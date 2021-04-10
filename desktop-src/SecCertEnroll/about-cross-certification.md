---
description: 「交叉認證」可讓一個公開金鑰基礎結構中的實體 (PKI) ，以信任另一個 PKI 中的實體。
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: 交叉認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193904"
---
# <a name="cross-certification"></a><span data-ttu-id="a9922-103">交叉認證</span><span class="sxs-lookup"><span data-stu-id="a9922-103">Cross Certification</span></span>

<span data-ttu-id="a9922-104">「交叉認證」可讓一個公開金鑰基礎結構中的實體 (PKI) ，以信任另一個 PKI 中的實體。</span><span class="sxs-lookup"><span data-stu-id="a9922-104">Cross certification enables entities in one public key infrastructure (PKI) to trust entities in another PKI.</span></span> <span data-ttu-id="a9922-105">在每個 PKI 的憑證授權單位單位 (CAs) 之間，此相互信任關係通常受到交叉憑證協定的支援。</span><span class="sxs-lookup"><span data-stu-id="a9922-105">This mutual trust relationship is typically supported by a cross-certification agreement between the certification authorities (CAs) in each PKI.</span></span> <span data-ttu-id="a9922-106">合約會建立各方的責任和責任。</span><span class="sxs-lookup"><span data-stu-id="a9922-106">The agreement establishes the responsibilities and liability of each party.</span></span>

<span data-ttu-id="a9922-107">兩個 ca 之間的相互信任關係需要每個 CA 對另一個 CA 發出憑證，以建立雙向的關聯性。</span><span class="sxs-lookup"><span data-stu-id="a9922-107">A mutual trust relationship between two CAs requires that each CA issue a certificate to the other to establish the relationship in both directions.</span></span> <span data-ttu-id="a9922-108">因為不同的 Pki 可能是憑證階層，所以信任的路徑不是階層 (任何治理 CAs 都不屬於其他) 。</span><span class="sxs-lookup"><span data-stu-id="a9922-108">The path of trust is not hierarchal (neither of the governing CAs is subordinate to the other) although the separate PKIs may be certificate hierarchies.</span></span> <span data-ttu-id="a9922-109">在兩個 Ca 建立並指定信任條款和互相發行的憑證之後，個別 Pki 內的實體可以與憑證中指定的原則互動。</span><span class="sxs-lookup"><span data-stu-id="a9922-109">After two CAs have established and specified the terms of trust and issued certificates to each other, entities within the separate PKIs can interact subject to the policies specified in the certificates.</span></span>

![交叉認證圖表](images/cross-certification.png)

## <a name="related-topics"></a><span data-ttu-id="a9922-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9922-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9922-112">信任模型</span><span class="sxs-lookup"><span data-stu-id="a9922-112">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



