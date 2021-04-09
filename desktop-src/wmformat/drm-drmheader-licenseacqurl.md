---
title: DRM_DRMHeader_LicenseAcqURL
description: DRM \_ DRMHeader \_ LicenseAcqURL 屬性包含 drm 第7版授權的授權取得 URL。
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL windows Media 格式
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023038"
---
# <a name="drm_drmheader_licenseacqurl"></a><span data-ttu-id="55cfb-104">DRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="55cfb-104">DRM\_DRMHeader\_LicenseAcqURL</span></span>

<span data-ttu-id="55cfb-105">**Drm \_ DRMHeader \_ LICENSEACQURL** 屬性包含 drm 第7版授權的授權取得 URL。</span><span class="sxs-lookup"><span data-stu-id="55cfb-105">The **DRM\_DRMHeader\_LicenseAcqURL** attribute contains the license acquisition URL for a DRM version 7 license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="55cfb-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="55cfb-106">Global Constant</span></span>

<span data-ttu-id="55cfb-107">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="55cfb-107">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="55cfb-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="55cfb-108">Data Type</span></span>

<span data-ttu-id="55cfb-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="55cfb-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="55cfb-110">備註</span><span class="sxs-lookup"><span data-stu-id="55cfb-110">Remarks</span></span>

<span data-ttu-id="55cfb-111">這個屬性只有 DRM 版本7內容存在。</span><span class="sxs-lookup"><span data-stu-id="55cfb-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="55cfb-112">您可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出它。</span><span class="sxs-lookup"><span data-stu-id="55cfb-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="55cfb-113">若要使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 設定檔案的授權取得 URL，您必須使用 [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="55cfb-113">To set the license acquisition URL on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_LicenseAcqURL**](drm-licenseacqurl.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="55cfb-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55cfb-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55cfb-115">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="55cfb-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




