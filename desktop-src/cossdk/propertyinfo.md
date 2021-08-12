---
description: 抓取指定集合所支援之屬性的相關資訊。
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: PropertyInfo 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf5c354711ec9ca34af1809707a7a869d39a3026ca5cb7ca11d2245c02be049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547573"
---
# <a name="propertyinfo-collection"></a>PropertyInfo 集合

抓取指定集合所支援之屬性的相關資訊。 您可以使用 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)方法，從任何 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件存取 **PropertyInfo** 集合。 **PropertyInfo** 集合會針對原創組合所支援的每個屬性，各包含一個物件。

## <a name="members"></a>成員

**PropertyInfo** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   **PropertyInfo**
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從每個集合流覽至這個集合。

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [名稱](#name)

### <a name="name"></a>名稱



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 屬性的名稱。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                                                         |
| 類型           | String                                                                                                                                                                                           |
| 預設        | None                                                                                                                                                                                             |
| 最小系統 | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
