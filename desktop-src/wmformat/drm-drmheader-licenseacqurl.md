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
# <a name="drm_drmheader_licenseacqurl"></a>DRM \_ DRMHeader \_ LicenseAcqURL

**Drm \_ DRMHeader \_ LICENSEACQURL** 屬性包含 drm 第7版授權的授權取得 URL。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這個屬性只有 DRM 版本7內容存在。 您可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出它。 若要使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 設定檔案的授權取得 URL，您必須使用 [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md) 屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




