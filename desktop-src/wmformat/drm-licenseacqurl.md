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
# <a name="drm_licenseacqurl"></a>DRM \_ LicenseAcqURL

**DRM \_ LicenseAcqURL** 屬性包含用戶端應用程式可以流覽至的網頁位址，以取得 DRM 版本7內容的內容授權。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ LicenseAcqURL

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這個屬性可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定，而且可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來抓取。 您可以使用 [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md)來取出相同的檔案屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




