---
title: DRM_ActionAllowed_CopyToCD
description: DRM \_ ActionAllowed \_ CopyToCD 屬性會指出是否允許將內容複寫到 CD。
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD windows Media 格式
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d44a4c812aed0d2f188b5ab18e9b74a1813bd9605bf348ca23b96b72f7d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809408"
---
# <a name="drm_actionallowed_copytocd"></a>DRM \_ ActionAllowed \_ CopyToCD

**DRM \_ ActionAllowed \_ CopyToCD** 屬性會指出是否允許將內容複寫到 CD。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

WindowsMedia DRM 10 授權使用複製動作來限制複製到 CD。 您應該檢查 [**DRM \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) 屬性，以判斷是否允許複製。

這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




