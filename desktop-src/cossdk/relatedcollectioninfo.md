---
description: 抓取與所呼叫之集合相關的其他集合相關資訊。
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: RelatedCollectionInfo 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 45e9e0f0e251bc9b0772d5def40fec148d541964d34e4f1dda954825f456468b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637088"
---
# <a name="relatedcollectioninfo-collection"></a>RelatedCollectionInfo 集合

抓取與所呼叫之集合相關的其他集合相關資訊。 您可以使用 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)方法，從任何 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件存取 **RelatedCollectionInfo** 集合。 **RelatedCollectionInfo** 集合針對可從原創組合存取的每個集合，各包含一個物件。 相關的集合會遵循「元件服務」系統管理工具集合階層。

此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**RelatedCollectionInfo** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**PropertyInfo**](propertyinfo.md)
-   **RelatedCollectionInfo**

您可以從每個集合流覽至這個集合。

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [名稱](#name)

### <a name="name"></a>名稱



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 相關集合的名稱。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                                                                   |
| 類型           | String                                                                                                                                                                                                     |
| 預設        | None                                                                                                                                                                                                       |
| 最小系統 | Windows 2000                                                                                                                                                                                               |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
