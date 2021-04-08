---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: DRM \_ ActionAllowed \_ CopyToNonSDMIDevice 屬性會指出是否允許將內容複寫到非 SDMI 裝置。
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice windows Media 格式
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023070"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a>DRM \_ ActionAllowed \_ CopyToNonSDMIDevice

**DRM \_ ActionAllowed \_ CopyToNonSDMIDevice** 屬性會指出是否允許將內容複寫到非 SDMI 裝置

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

Windows Media DRM 10 授權使用複製動作來限制複製到裝置。 您應該檢查 [**DRM \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) 屬性，以判斷是否允許複製。

這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




