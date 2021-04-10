---
title: DRM_BaseLicenseAcqURL
description: DRM \_ BaseLicenseAcqURL 屬性包含部分的基底 URL，播放程式應用程式必須流覽此 URL 才能取得內容的授權。
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL windows Media 格式
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092534"
---
# <a name="drm_baselicenseacqurl"></a>DRM \_ BaseLicenseAcqURL

**DRM \_ BaseLicenseAcqURL** 屬性包含部分的基底 URL，播放程式應用程式必須流覽此 URL 才能取得內容的授權。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ BaseLicenseAcqURL

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這是選擇性的讀寫屬性，它是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)設定和取出。 提供此功能的目的是讓授權散發系統在授權取得 URL 屬性中使用相對路徑。

設定這個屬性之後，內容標頭中的所有部分授權取得 Url 都會將基底 URL 新增至部分 URL 的前方，以構成播放程式要流覽的完整 URL。 針對 **DRM \_ BaseLicenseAcqURL** 呼叫 **IWMDRMReader：： GetDRMProperty** 只會在設定的相同會話中運作。 屬性不會儲存在內容標頭中;它是動態的，且只有相對 URL 會儲存在內容中。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




