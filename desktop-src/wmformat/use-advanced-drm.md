---
title: Use_Advanced_DRM
description: '[使用 \_ Advanced \_ drm] 屬性會指定是否使用 DRM 第7版來保護內容。'
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Use_Advanced_DRM windows Media 格式
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a11731fbe212c8b87cd52300da1885206230c7329491a6512ab3c261923c74e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658218"
---
# <a name="use_advanced_drm"></a>使用 \_ Advanced \_ DRM

[ **使用 \_ Advanced \_ drm** ] 屬性會指定是否使用 DRM 第7版來保護內容。

## <a name="global-constant"></a>全域常數

g \_ wszWMUse \_ Advanced \_ DRM

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

這是讀寫屬性，會使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) 抓取，並使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)進行設定。 無法從 reader 物件存取這個屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




