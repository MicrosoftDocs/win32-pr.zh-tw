---
title: DRM_LicenseID
description: DRM \_ LicenseID 屬性包含從與目前開啟的檔案（可唯一識別該授權）相關聯的授權中取出的字串。
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID windows Media 格式
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314346"
---
# <a name="drm_licenseid"></a>DRM \_ LicenseID

**DRM \_ LicenseID** 屬性包含從與目前開啟的檔案（可唯一識別該授權）相關聯的授權中取出的字串。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ LicenseID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這個屬性只有 DRM 版本7內容存在。 您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。

授權識別碼會儲存在授權中，而不是儲存在 ASF 檔案中。 每個個別授權都有唯一的識別碼，由授權產生器在建立授權時指派。 例如，如果您取得相同內容的兩個授權，每一個授權都會有不同的 LicenseID 屬性。 一般來說，應用程式不需要取得此值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




