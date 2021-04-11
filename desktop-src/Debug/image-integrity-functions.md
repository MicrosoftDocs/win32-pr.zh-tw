---
description: 映射完整性函式會管理影像檔案中的一組憑證。
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: 映射完整性函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025898"
---
# <a name="image-integrity-functions"></a><span data-ttu-id="2b9b0-103">映射完整性函式</span><span class="sxs-lookup"><span data-stu-id="2b9b0-103">Image Integrity Functions</span></span>

<span data-ttu-id="2b9b0-104">映射完整性函式會管理影像檔案中的一組憑證。</span><span class="sxs-lookup"><span data-stu-id="2b9b0-104">The image integrity functions manage the set of certificates in an image file.</span></span> <span data-ttu-id="2b9b0-105">系統會提供常式來新增、移除和查詢憑證。</span><span class="sxs-lookup"><span data-stu-id="2b9b0-105">Routines are provided to add, remove, and query certificates.</span></span> <span data-ttu-id="2b9b0-106">另外還有一個函式，可用來取得計算影像檔案摘要所需的影像檔位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="2b9b0-106">There is also a function available for obtaining the byte stream of an image file required to calculate a message digest of the image file.</span></span> <span data-ttu-id="2b9b0-107">這是建立簽章憑證的必要項。</span><span class="sxs-lookup"><span data-stu-id="2b9b0-107">This is needed to create signature certificates.</span></span>

<span data-ttu-id="2b9b0-108">檔案中的每個憑證都有一個索引，可在移除憑證時變更。</span><span class="sxs-lookup"><span data-stu-id="2b9b0-108">Every certificate in a file has an index which can change as certificates are removed.</span></span> <span data-ttu-id="2b9b0-109">新憑證一律會新增至現有憑證清單的「結尾」。</span><span class="sxs-lookup"><span data-stu-id="2b9b0-109">New certificates will always be added "at the end" of the list of existing certificates.</span></span> <span data-ttu-id="2b9b0-110">也就是說，它們的指派索引大於目前使用中的任何索引。</span><span class="sxs-lookup"><span data-stu-id="2b9b0-110">That is, they will be assigned indices that are greater than any index currently in use.</span></span> <span data-ttu-id="2b9b0-111">一般情況下，應用程式不應假設指定的憑證具有與其上次參考時相同的索引。</span><span class="sxs-lookup"><span data-stu-id="2b9b0-111">In general, an application should not assume that a given certificate has the same index it had the last time it was referenced.</span></span>

-   [<span data-ttu-id="2b9b0-112">**DigestFunction**</span><span class="sxs-lookup"><span data-stu-id="2b9b0-112">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [<span data-ttu-id="2b9b0-113">**ImageAddCertificate**</span><span class="sxs-lookup"><span data-stu-id="2b9b0-113">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [<span data-ttu-id="2b9b0-114">**ImageEnumerateCertificates**</span><span class="sxs-lookup"><span data-stu-id="2b9b0-114">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [<span data-ttu-id="2b9b0-115">**ImageGetCertificateData**</span><span class="sxs-lookup"><span data-stu-id="2b9b0-115">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [<span data-ttu-id="2b9b0-116">**ImageGetCertificateHeader**</span><span class="sxs-lookup"><span data-stu-id="2b9b0-116">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [<span data-ttu-id="2b9b0-117">**ImageGetDigestStream**</span><span class="sxs-lookup"><span data-stu-id="2b9b0-117">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [<span data-ttu-id="2b9b0-118">**ImageRemoveCertificate**</span><span class="sxs-lookup"><span data-stu-id="2b9b0-118">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



