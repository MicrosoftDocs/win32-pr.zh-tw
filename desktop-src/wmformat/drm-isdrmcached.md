---
title: DRM_IsDRMCached
description: DRM \_ IsDRMCached 屬性會指出是否已在本機電腦上儲存 drm 版本1授權資訊。
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached windows Media 格式
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965832"
---
# <a name="drm_isdrmcached"></a>DRM \_ IsDRMCached

**Drm \_ IsDRMCached** 屬性會指出是否已在本機電腦上儲存 drm 版本1授權資訊。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

這是使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)取出的唯讀屬性。 當授權取得 URL 符合在 DRM 第1版中用來取得本機授權的兩個已知 Url 之一時，即為 **TRUE** 。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




