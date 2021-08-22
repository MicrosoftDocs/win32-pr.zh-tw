---
title: DRM_DRMHeader_ContentDistributor
description: DRM \_ DRMHeader \_ ContentDistributor 屬性包含 identifiying 內容散發者的字串。
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor windows Media 格式
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a82e570c43acbe065ec20e1d7296cff701853591759e9187e2b9329ffed8efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586458"
---
# <a name="drm_drmheader_contentdistributor"></a>DRM \_ DRMHeader \_ ContentDistributor

**DRM \_ DRMHeader \_ ContentDistributor** 屬性包含 identifiying 內容散發者的字串。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

內容識別碼是選擇性的，只由內容建立者決定。 寫入器物件不會對此屬性執行任何動作。 這個屬性只有 DRM 版本7內容存在。 您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




