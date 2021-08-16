---
title: Use_DRM
description: 使用 \_ drm 屬性會指示寫入器物件將 DRM 版本1保護套用至目前的檔案。
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM windows Media 格式
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b802a7bef777fab4ed835aa3a1770169deaa6eeea9a7eddeb802fb2e4b0a9dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845299"
---
# <a name="use_drm"></a>使用 \_ DRM

**使用 \_ drm** 屬性會指示寫入器物件將 DRM 版本1保護套用至目前的檔案。

## <a name="global-constant"></a>全域常數

g \_ wszWMUse \_ DRM

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

建立 DRM 第1版內容時，請使用 [**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) 將此屬性設定為 **TRUE** 。 無法從 reader 物件存取這個屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




