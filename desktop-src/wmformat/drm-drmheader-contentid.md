---
title: DRM_DRMHeader_ContentID
description: DRM \_ DRMHeader \_ ContentID 屬性包含內容擁有者所產生的 ContentID。
ms.assetid: fda38778-2fdf-4218-aad2-e4cf351d74e9
keywords:
- DRM_DRMHeader_ContentID windows Media 格式
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66edd858451e5d1a58b2a91f9f2362d4cabe9da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932929"
---
# <a name="drm_drmheader_contentid"></a>DRM \_ DRMHeader \_ ContentID

**DRM \_ DRMHeader \_ ContentID** 屬性包含內容擁有者所產生的 ContentID。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ DRMHeader \_ ContentID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這個屬性只有 DRM 版本7內容存在。 您可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出它。 若要使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 在檔案上設定內容識別碼，您必須使用 [**DRM \_ ContentID**](drm-contentid.md) 屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




