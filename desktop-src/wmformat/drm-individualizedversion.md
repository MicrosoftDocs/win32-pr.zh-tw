---
title: DRM_IndividualizedVersion
description: DRM \_ IndividualizedVersion 屬性會儲存在 drm 標頭中，並包含存取內容所需的最小個別版本。
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion windows Media 格式
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d7c9f64a7d4d00e95f8e877e7f33c9e6a8177977eff3b523c25cc1432ac57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704680"
---
# <a name="drm_individualizedversion"></a>DRM \_ IndividualizedVersion

**Drm \_ IndividualizedVersion** 屬性會儲存在 drm 標頭中，並包含存取內容所需的最小個別版本。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ IndividualizedVersion

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這個屬性只有 DRM 版本7內容存在。 您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。 您可以使用 [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md)來取出相同的檔案屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




