---
title: 金鑰和金鑰識別碼
description: 金鑰和金鑰識別碼
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- 數位版權管理 (DRM) ，金鑰
- DRM (數位版權管理) 、金鑰
- 數位版權管理 (DRM) ，小孩
- DRM (數位版權管理) ，小孩
- '金鑰識別碼 (小孩) '
- '小孩 (金鑰識別碼) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967820"
---
# <a name="key-and-key-id"></a><span data-ttu-id="5d2a8-110">金鑰和金鑰識別碼</span><span class="sxs-lookup"><span data-stu-id="5d2a8-110">Key and Key ID</span></span>

<span data-ttu-id="5d2a8-111">當您封裝檔案時，您會使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="5d2a8-111">When you package a file, you use a key.</span></span> <span data-ttu-id="5d2a8-112">金鑰是用於保護內容的加密演算法中所使用的一段資料。</span><span class="sxs-lookup"><span data-stu-id="5d2a8-112">A key is a piece of data used in the encryption algorithms that protect the content.</span></span> <span data-ttu-id="5d2a8-113">每個金鑰都有兩個部分：授權金鑰植入和金鑰識別碼， (通常縮寫為小孩) 。</span><span class="sxs-lookup"><span data-stu-id="5d2a8-113">There are two parts to each key: a license key seed and a key ID (often abbreviated as KID).</span></span> <span data-ttu-id="5d2a8-114">金鑰識別碼是公用的，而且會儲存在檔案標頭中，以識別解密檔案所需的金鑰。</span><span class="sxs-lookup"><span data-stu-id="5d2a8-114">The key ID is public, and is stored in the file header as a way to identify the key required to decrypt the file.</span></span> <span data-ttu-id="5d2a8-115">授權金鑰種子是內容封裝程式和授權簽發者必須共用的秘密值。</span><span class="sxs-lookup"><span data-stu-id="5d2a8-115">The license key seed is a secret value that must be shared by the content packager and the license issuer.</span></span>

<span data-ttu-id="5d2a8-116">金鑰識別碼會從授權的觀點來識別受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="5d2a8-116">A key ID identifies protected content from the perspective of the license.</span></span> <span data-ttu-id="5d2a8-117">雖然您可以將相同的金鑰識別碼用於多個檔案，但建議您一律針對每個受保護的內容使用唯一的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d2a8-117">Although you can use the same key ID for multiple files, it is recommended that you always use a unique key ID for each piece of protected content.</span></span>

<span data-ttu-id="5d2a8-118">本檔中所述的許多方法都使用金鑰識別碼字串來選取授權。</span><span class="sxs-lookup"><span data-stu-id="5d2a8-118">Many of the methods described in this documentation use key ID strings to select licenses.</span></span> <span data-ttu-id="5d2a8-119">這些字串包含以 base64 編碼的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d2a8-119">These strings contain the key ID encoded in base64.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d2a8-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d2a8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d2a8-121">**概念**</span><span class="sxs-lookup"><span data-stu-id="5d2a8-121">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




