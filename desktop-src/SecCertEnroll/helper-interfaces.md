---
description: 憑證註冊 API 支援下列一般使用介面。
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Helper 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a0c6948e9b0fe09aee0b983d230f53bc8e76b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975859"
---
# <a name="helper-interfaces"></a><span data-ttu-id="2ec6c-103">Helper 介面</span><span class="sxs-lookup"><span data-stu-id="2ec6c-103">Helper Interfaces</span></span>

<span data-ttu-id="2ec6c-104">憑證註冊 API 支援下列一般使用介面。</span><span class="sxs-lookup"><span data-stu-id="2ec6c-104">The following general use interfaces are supported by the Certificate Enrollment API.</span></span>



| <span data-ttu-id="2ec6c-105">介面</span><span class="sxs-lookup"><span data-stu-id="2ec6c-105">Interface</span></span>                                                                    | <span data-ttu-id="2ec6c-106">描述</span><span class="sxs-lookup"><span data-stu-id="2ec6c-106">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ec6c-107">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="2ec6c-107">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | <span data-ttu-id="2ec6c-108">從位元組陣列建立 Unicode 編碼的字串、從 Unicode 編碼的字串建立位元組陣列，並修改套用至字串的 Unicode 編碼類型。</span><span class="sxs-lookup"><span data-stu-id="2ec6c-108">Creates a Unicode-encoded string from a byte array, creates a byte array from a Unicode-encoded string, and modifies the type of Unicode encoding applied to a string.</span></span> |
| [<span data-ttu-id="2ec6c-109">**ICertificateAttestationChallenge**</span><span class="sxs-lookup"><span data-stu-id="2ec6c-109">**ICertificateAttestationChallenge**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | <span data-ttu-id="2ec6c-110">支援憑證證明挑戰。</span><span class="sxs-lookup"><span data-stu-id="2ec6c-110">Supports certificate attestation challenges.</span></span>                                                                                                                           |
| [<span data-ttu-id="2ec6c-111">**IObjectId**</span><span class="sxs-lookup"><span data-stu-id="2ec6c-111">**IObjectId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | <span data-ttu-id="2ec6c-112">表示物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ec6c-112">Represents an object identifier.</span></span>                                                                                                                                       |
| [<span data-ttu-id="2ec6c-113">**IObjectIds**</span><span class="sxs-lookup"><span data-stu-id="2ec6c-113">**IObjectIds**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | <span data-ttu-id="2ec6c-114">管理 [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="2ec6c-114">Manages a collection of [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) objects.</span></span>                                                                                                        |
| [<span data-ttu-id="2ec6c-115">**IX500DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="2ec6c-115">**IX500DistinguishedName**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | <span data-ttu-id="2ec6c-116">表示 x.500 辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="2ec6c-116">Represents an X.500 distinguished name.</span></span>                                                                                                                                |
| [<span data-ttu-id="2ec6c-117">**IX509EndorsementKey**</span><span class="sxs-lookup"><span data-stu-id="2ec6c-117">**IX509EndorsementKey**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | <span data-ttu-id="2ec6c-118">X.509 簽署金鑰介面</span><span class="sxs-lookup"><span data-stu-id="2ec6c-118">X.509 Endorsement Key Interface</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="2ec6c-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ec6c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ec6c-120">CertEnroll 介面</span><span class="sxs-lookup"><span data-stu-id="2ec6c-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



