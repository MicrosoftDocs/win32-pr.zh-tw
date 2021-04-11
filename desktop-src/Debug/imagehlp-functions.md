---
description: 以下是 Imagehlp.dll 函數。
ms.assetid: 926f412e-25ba-4f9c-a118-b5a1bc723379
title: Imagehlp.dll 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e921707474f68e288f67e84dda9e361922bca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936411"
---
# <a name="imagehlp-functions"></a><span data-ttu-id="79989-103">Imagehlp.dll 函式</span><span class="sxs-lookup"><span data-stu-id="79989-103">ImageHlp Functions</span></span>

<span data-ttu-id="79989-104">以下是 Imagehlp.dll 函數。</span><span class="sxs-lookup"><span data-stu-id="79989-104">The following are the ImageHlp functions.</span></span>

## <a name="image-access"></a><span data-ttu-id="79989-105">影像存取</span><span class="sxs-lookup"><span data-stu-id="79989-105">Image Access</span></span>

<span data-ttu-id="79989-106">影像存取功能可存取可執行映射中的資料。</span><span class="sxs-lookup"><span data-stu-id="79989-106">The image access functions access the data in an executable image.</span></span> <span data-ttu-id="79989-107">這些函式可提供映射基底的高階存取，以及對影像資料最常見部分的非常特定存取。</span><span class="sxs-lookup"><span data-stu-id="79989-107">The functions provide high-level access to the base of images and very specific access to the most common parts of an image's data.</span></span>

<dl>

[<span data-ttu-id="79989-108">**GetImageConfigInformation**</span><span class="sxs-lookup"><span data-stu-id="79989-108">**GetImageConfigInformation**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageconfiginformation)  
[<span data-ttu-id="79989-109">**GetImageUnusedHeaderBytes**</span><span class="sxs-lookup"><span data-stu-id="79989-109">**GetImageUnusedHeaderBytes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageunusedheaderbytes)  
[<span data-ttu-id="79989-110">**ImageLoad**</span><span class="sxs-lookup"><span data-stu-id="79989-110">**ImageLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageload)  
[<span data-ttu-id="79989-111">**ImageUnload**</span><span class="sxs-lookup"><span data-stu-id="79989-111">**ImageUnload**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageunload)  
[<span data-ttu-id="79989-112">**MapAndLoad**</span><span class="sxs-lookup"><span data-stu-id="79989-112">**MapAndLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapandload)  
[<span data-ttu-id="79989-113">**SetImageConfigInformation**</span><span class="sxs-lookup"><span data-stu-id="79989-113">**SetImageConfigInformation**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-setimageconfiginformation)  
[<span data-ttu-id="79989-114">**UnMapAndLoad**</span><span class="sxs-lookup"><span data-stu-id="79989-114">**UnMapAndLoad**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-unmapandload)  
</dl>

## <a name="image-integrity"></a><span data-ttu-id="79989-115">映射完整性</span><span class="sxs-lookup"><span data-stu-id="79989-115">Image Integrity</span></span>

<span data-ttu-id="79989-116">映射完整性函式會管理影像檔案中的一組憑證。</span><span class="sxs-lookup"><span data-stu-id="79989-116">The image integrity functions manage the set of certificates in an image file.</span></span>

<dl>

[<span data-ttu-id="79989-117">**DigestFunction**</span><span class="sxs-lookup"><span data-stu-id="79989-117">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)  
[<span data-ttu-id="79989-118">**ImageAddCertificate**</span><span class="sxs-lookup"><span data-stu-id="79989-118">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)  
[<span data-ttu-id="79989-119">**ImageEnumerateCertificates**</span><span class="sxs-lookup"><span data-stu-id="79989-119">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)  
[<span data-ttu-id="79989-120">**ImageGetCertificateData**</span><span class="sxs-lookup"><span data-stu-id="79989-120">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)  
[<span data-ttu-id="79989-121">**ImageGetCertificateHeader**</span><span class="sxs-lookup"><span data-stu-id="79989-121">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)  
[<span data-ttu-id="79989-122">**ImageGetDigestStream**</span><span class="sxs-lookup"><span data-stu-id="79989-122">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)  
[<span data-ttu-id="79989-123">**ImageRemoveCertificate**</span><span class="sxs-lookup"><span data-stu-id="79989-123">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)  
</dl>

## <a name="image-modification"></a><span data-ttu-id="79989-124">影像修改</span><span class="sxs-lookup"><span data-stu-id="79989-124">Image Modification</span></span>

<span data-ttu-id="79989-125">影像修改函式可讓您變更可執行檔映射。</span><span class="sxs-lookup"><span data-stu-id="79989-125">The image modification functions allow you to change the executable image.</span></span>

<dl>

[<span data-ttu-id="79989-126">**BindImage**</span><span class="sxs-lookup"><span data-stu-id="79989-126">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)  
[<span data-ttu-id="79989-127">**BindImageEx**</span><span class="sxs-lookup"><span data-stu-id="79989-127">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)  
[<span data-ttu-id="79989-128">**CheckSumMappedFile**</span><span class="sxs-lookup"><span data-stu-id="79989-128">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)  
[<span data-ttu-id="79989-129">**MapFileAndCheckSum**</span><span class="sxs-lookup"><span data-stu-id="79989-129">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)  
[<span data-ttu-id="79989-130">**ReBaseImage**</span><span class="sxs-lookup"><span data-stu-id="79989-130">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)  
[<span data-ttu-id="79989-131">**ReBaseImage64**</span><span class="sxs-lookup"><span data-stu-id="79989-131">**ReBaseImage64**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage64)  
[<span data-ttu-id="79989-132">**SplitSymbols**</span><span class="sxs-lookup"><span data-stu-id="79989-132">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)  
[<span data-ttu-id="79989-133">**StatusRoutine**</span><span class="sxs-lookup"><span data-stu-id="79989-133">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)  
[<span data-ttu-id="79989-134">**TouchFileTimes**</span><span class="sxs-lookup"><span data-stu-id="79989-134">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)  
[<span data-ttu-id="79989-135">**UpdateDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="79989-135">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)  
[<span data-ttu-id="79989-136">**UpdateDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="79989-136">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)  
</dl>

 

 



