---
title: DRM_LicenseAcqURL
description: DRM \_ LicenseAcqURL 屬性包含用戶端應用程式可以流覽至的網頁位址，以取得 DRM 版本7內容的內容授權。
ms.assetid: bee29e39-ded8-439d-9164-fc318cb535c0
keywords:
- DRM_LicenseAcqURL windows Media 格式
topic_type:
- apiref
api_name:
- DRM_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231efc4334a4d893b4bdd1e7545bd50b1bed2a5c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507804"
---
# <a name="drm_licenseacqurl"></a><span data-ttu-id="a3373-104">DRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="a3373-104">DRM\_LicenseAcqURL</span></span>

<span data-ttu-id="a3373-105">**DRM \_ LicenseAcqURL** 屬性包含用戶端應用程式可以流覽至的網頁位址，以取得 DRM 版本7內容的內容授權。</span><span class="sxs-lookup"><span data-stu-id="a3373-105">The **DRM\_LicenseAcqURL** attribute contains the address of a Web page that the client application can navigate to in order to obtain a content license for DRM version 7 content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a3373-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="a3373-106">Global Constant</span></span>

<span data-ttu-id="a3373-107">g \_ wszWMDRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="a3373-107">g\_wszWMDRM\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="a3373-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="a3373-108">Data Type</span></span>

<span data-ttu-id="a3373-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="a3373-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="a3373-110">備註</span><span class="sxs-lookup"><span data-stu-id="a3373-110">Remarks</span></span>

<span data-ttu-id="a3373-111">這個屬性可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定，而且可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來抓取。</span><span class="sxs-lookup"><span data-stu-id="a3373-111">This attribute can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="a3373-112">您可以使用 [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md)來取出相同的檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="a3373-112">The same file attribute can be retrieved using [**DRM\_DRMHeader\_LicenseAcqURL**](drm-drmheader-licenseacqurl.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a3373-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3373-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3373-114">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="a3373-114">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




