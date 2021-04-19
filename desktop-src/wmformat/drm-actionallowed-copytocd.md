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
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106969091"
---
# <a name="drm_actionallowed_copytocd"></a>DRM \_ ActionAllowed \_ CopyToCD

**DRM \_ ActionAllowed \_ CopyToCD** 屬性會指出是否允許將內容複寫到 CD。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

Windows Media DRM 10 授權使用複製動作來限制複製到 CD。 您應該檢查 [**DRM \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) 屬性，以判斷是否允許複製。

這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




