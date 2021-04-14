---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: DRM \_ ActionAllowed \_ CopyToSDMIDevice 屬性會指出是否允許將內容複寫到 SDMI 裝置。
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice windows Media 格式
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374347"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>DRM \_ ActionAllowed \_ CopyToSDMIDevice

**DRM \_ ActionAllowed \_ CopyToSDMIDevice** 屬性會指出是否允許將內容複寫到 SDMI 裝置。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

Windows Media DRM 10 授權使用複製動作來限制複製到裝置。 您應該檢查 [**DRM \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) 屬性，以判斷是否允許複製。

這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




