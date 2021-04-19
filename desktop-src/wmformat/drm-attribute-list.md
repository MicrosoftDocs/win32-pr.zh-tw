---
title: DRM 屬性清單
description: DRM 屬性清單
ms.assetid: 222ef91c-b776-4de8-b1ad-88c2beca05aa
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- '屬性，數位版權管理 (DRM) '
- 數位版權管理 (DRM) ，屬性
- DRM (數位版權管理) ，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3beccc33a48f57015040f06c140a55f5f9691daa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966826"
---
# <a name="drm-attribute-list"></a><span data-ttu-id="21fb2-109">DRM 屬性清單</span><span class="sxs-lookup"><span data-stu-id="21fb2-109">DRM Attribute List</span></span>

<span data-ttu-id="21fb2-110">為了方便起見，下表列出所有 DRM 相關的檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="21fb2-110">For convenience, the following table lists all the DRM-related file attributes.</span></span> <span data-ttu-id="21fb2-111"> (這些屬性也會列在 [ [屬性清單](attribute-list.md)] 下所有屬性的資料表中。 ) </span><span class="sxs-lookup"><span data-stu-id="21fb2-111">(These attributes are also listed in the table of all attributes under [Attribute List](attribute-list.md).)</span></span>

<span data-ttu-id="21fb2-112">應用程式可以在寫入 DRM 檔案時設定這些值，而且可以在讀取時取得這些值。</span><span class="sxs-lookup"><span data-stu-id="21fb2-112">Applications can set these values when writing DRM files and can retrieve them when reading.</span></span>



| <span data-ttu-id="21fb2-113">DRM 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="21fb2-113">DRM file attribute</span></span>                                                                   | <span data-ttu-id="21fb2-114">全域識別碼</span><span class="sxs-lookup"><span data-stu-id="21fb2-114">Global identifier</span></span>                             | <span data-ttu-id="21fb2-115">資料類型</span><span class="sxs-lookup"><span data-stu-id="21fb2-115">Data type</span></span>             |
|--------------------------------------------------------------------------------------|-----------------------------------------------|-----------------------|
| [<span data-ttu-id="21fb2-116">**DRM \_ ContentID**</span><span class="sxs-lookup"><span data-stu-id="21fb2-116">**DRM\_ContentID**</span></span>](drm-contentid.md)                                              | <span data-ttu-id="21fb2-117">g \_ wszWMDRM \_ ContentID</span><span class="sxs-lookup"><span data-stu-id="21fb2-117">g\_wszWMDRM\_ContentID</span></span>                        | <span data-ttu-id="21fb2-118">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-118">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-119">**DRM \_ DRMHeader \_ ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="21fb2-119">**DRM\_DRMHeader\_ContentDistributor**</span></span>](drm-drmheader-contentdistributor.md)       | <span data-ttu-id="21fb2-120">g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="21fb2-120">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>    | <span data-ttu-id="21fb2-121">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-121">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-122">**DRM \_ DRMHeader \_ ContentID**</span><span class="sxs-lookup"><span data-stu-id="21fb2-122">**DRM\_DRMHeader\_ContentID**</span></span>](drm-drmheader-contentid.md)                         | <span data-ttu-id="21fb2-123">g \_ wszWMDRM \_ DRMHeader \_ ContentID</span><span class="sxs-lookup"><span data-stu-id="21fb2-123">g\_wszWMDRM\_DRMHeader\_ContentID</span></span>             | <span data-ttu-id="21fb2-124">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-124">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-125">**DRM \_ DRMHeader \_ IndividualizedVersion**</span><span class="sxs-lookup"><span data-stu-id="21fb2-125">**DRM\_DRMHeader\_IndividualizedVersion**</span></span>](drm-drmheader-individualizedversion.md) | <span data-ttu-id="21fb2-126">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="21fb2-126">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span> | <span data-ttu-id="21fb2-127">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-127">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-128">**DRM \_ DRMHeader \_ KeyID**</span><span class="sxs-lookup"><span data-stu-id="21fb2-128">**DRM\_DRMHeader\_KeyID**</span></span>](drm-drmheader-keyid.md)                                 | <span data-ttu-id="21fb2-129">g \_ wszWMDRM \_ DRMHeader \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="21fb2-129">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>                 | <span data-ttu-id="21fb2-130">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-130">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-131">**DRM \_ DRMHeader \_ LicenseAcqURL**</span><span class="sxs-lookup"><span data-stu-id="21fb2-131">**DRM\_DRMHeader\_LicenseAcqURL**</span></span>](drm-drmheader-licenseacqurl.md)                 | <span data-ttu-id="21fb2-132">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="21fb2-132">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>         | <span data-ttu-id="21fb2-133">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-133">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-134">**DRM \_ DRMHeader \_ SubscriptionContentID**</span><span class="sxs-lookup"><span data-stu-id="21fb2-134">**DRM\_DRMHeader\_SubscriptionContentID**</span></span>](drm-drmheader-subscriptioncontentid.md) | <span data-ttu-id="21fb2-135">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="21fb2-135">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span> | <span data-ttu-id="21fb2-136">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-136">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-137">**DRM \_ DRMHeader**</span><span class="sxs-lookup"><span data-stu-id="21fb2-137">**DRM\_DRMHeader**</span></span>](drm-drmheader.md)                                              | <span data-ttu-id="21fb2-138">g \_ wszWMDRM \_ DRMHeader</span><span class="sxs-lookup"><span data-stu-id="21fb2-138">g\_wszWMDRM\_DRMHeader</span></span>                        | <span data-ttu-id="21fb2-139">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-139">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-140">**DRM \_ IndividualizedVersion**</span><span class="sxs-lookup"><span data-stu-id="21fb2-140">**DRM\_IndividualizedVersion**</span></span>](drm-individualizedversion.md)                      | <span data-ttu-id="21fb2-141">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="21fb2-141">g\_wszWMDRM\_IndividualizedVersion</span></span>            | <span data-ttu-id="21fb2-142">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-142">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-143">**DRM \_ KeyID**</span><span class="sxs-lookup"><span data-stu-id="21fb2-143">**DRM\_KeyID**</span></span>](drm-keyid.md)                                                      | <span data-ttu-id="21fb2-144">g \_ wszWMDRM \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="21fb2-144">g\_wszWMDRM\_KeyID</span></span>                            | <span data-ttu-id="21fb2-145">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-145">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-146">**DRM \_ LASignatureCert**</span><span class="sxs-lookup"><span data-stu-id="21fb2-146">**DRM\_LASignatureCert**</span></span>](drm-lasignaturecert.md)                                  | <span data-ttu-id="21fb2-147">g \_ wszWMDRM \_ LASignatureCert</span><span class="sxs-lookup"><span data-stu-id="21fb2-147">g\_wszWMDRM\_LASignatureCert</span></span>                  | <span data-ttu-id="21fb2-148">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-148">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-149">**DRM \_ LASignatureLicSrvCert**</span><span class="sxs-lookup"><span data-stu-id="21fb2-149">**DRM\_LASignatureLicSrvCert**</span></span>](drm-lasignaturelicsrvcert.md)                      | <span data-ttu-id="21fb2-150">g \_ wszWMDRM \_ LASignatureLicSrvCert</span><span class="sxs-lookup"><span data-stu-id="21fb2-150">g\_wszWMDRM\_LASignatureLicSrvCert</span></span>            | <span data-ttu-id="21fb2-151">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-151">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-152">**DRM \_ LASignaturePrivKey**</span><span class="sxs-lookup"><span data-stu-id="21fb2-152">**DRM\_LASignaturePrivKey**</span></span>](drm-lasignatureprivkey.md)                            | <span data-ttu-id="21fb2-153">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="21fb2-153">g\_wszWMDRM\_LASignaturePrivKey</span></span>               | <span data-ttu-id="21fb2-154">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-154">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-155">**DRM \_ LASignatureRootCert**</span><span class="sxs-lookup"><span data-stu-id="21fb2-155">**DRM\_LASignatureRootCert**</span></span>](drm-lasignaturerootcert.md)                          | <span data-ttu-id="21fb2-156">g \_ wszWMDRM \_ LASignatureRootCert</span><span class="sxs-lookup"><span data-stu-id="21fb2-156">g\_wszWMDRM\_LASignatureRootCert</span></span>              | <span data-ttu-id="21fb2-157">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-157">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-158">**DRM \_ LicenseAcqURL**</span><span class="sxs-lookup"><span data-stu-id="21fb2-158">**DRM\_LicenseAcqURL**</span></span>](drm-licenseacqurl.md)                                      | <span data-ttu-id="21fb2-159">g \_ wszWMDRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="21fb2-159">g\_wszWMDRM\_LicenseAcqURL</span></span>                    | <span data-ttu-id="21fb2-160">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-160">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="21fb2-161">**DRM \_ V1LicenseAcqURL**</span><span class="sxs-lookup"><span data-stu-id="21fb2-161">**DRM\_V1LicenseAcqURL**</span></span>](drm-v1licenseacqurl.md)                                  | <span data-ttu-id="21fb2-162">g \_ wszWMDRM \_ V1LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="21fb2-162">g\_wszWMDRM\_V1LicenseAcqURL</span></span>                  | <span data-ttu-id="21fb2-163">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="21fb2-163">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="21fb2-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="21fb2-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21fb2-165">**依類型的屬性**</span><span class="sxs-lookup"><span data-stu-id="21fb2-165">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="21fb2-166">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="21fb2-166">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




