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
ms.openlocfilehash: 6fcb010855ac4660792a7c579556001d5d7c4c96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507784"
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

 

 




