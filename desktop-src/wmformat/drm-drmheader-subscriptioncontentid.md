---
title: DRM_DRMHeader_SubscriptionContentID
description: DRM \_ DRMHeader \_ SubscriptionContentID 屬性包含訂用帳戶內容識別碼。
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID windows Media 格式
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b273cf95d2bbb271b055eeff3da80a788a38c88bb2e87db37f5a73e6e918e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086148"
---
# <a name="drm_drmheader_subscriptioncontentid"></a>DRM \_ DRMHeader \_ SubscriptionContentID

**DRM \_ DRMHeader \_ SubscriptionContentID** 屬性包含訂用帳戶內容識別碼。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這個屬性只有 DRM 版本7內容存在。 訂用帳戶內容識別碼是選擇性的，只由內容建立者決定。 寫入器物件不會對此屬性執行任何動作。 您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




