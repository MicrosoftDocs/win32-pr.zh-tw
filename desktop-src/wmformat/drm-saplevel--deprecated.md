---
title: 'DRM_SAPLEVEL (已淘汰) '
description: 指定應用程式支援的 (SAP) 層級的安全音訊路徑。
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (已淘汰) windows Media 格式
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80b43cfcf0c89283237f8ff2d3e4f8612050296d7462f54890c3efa908fa9be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930888"
---
# <a name="drm_saplevel-deprecated"></a>DRM \_ SAPLEVEL (已淘汰) 

\[**DRM \_SAPLEVEL** 不再適用于 Windows Vista 的使用。 相反地，請在媒體基礎程式庫中使用受保護的使用者模式音訊 (PUMA) 。 \]

**DRM \_ SAPLEVEL** 屬性會指定您的應用程式所支援的 (SAP) 層級的安全音訊路徑。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ SAPLEVEL

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這是透過呼叫 [**IWMDRMReader：： SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty)所設定的僅限寫入屬性。 此值是 SAP 層級的寬字元字串標記法，例如 L "200"。 目前支援的值為200和300。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|--------------------------------|
| 用戶端支援結束<br/> | Windows XP<br/>          |
| 伺服器支援結束<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 





