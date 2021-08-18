---
description: 包含父 TransientSubscriptions 集合之每個暫時性發行者屬性的物件。 您可以針對執行中的物件實例執行暫時的訂閱，並在物件終結時消失。
ms.assetid: 63921caa-5c22-4203-b1a3-f143928f4742
title: TransientPublisherProperties 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientPublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 63799e7c39a87b94dace1fc0a85ca67d18fc7c9a1b0bd407fae52df62344cdeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372688"
---
# <a name="transientpublisherproperties-collection"></a>TransientPublisherProperties 集合

包含父 [**TransientSubscriptions**](transientsubscriptions.md) 集合之每個暫時性發行者屬性的物件。 您可以針對執行中的物件實例執行暫時的訂閱，並在物件終結時消失。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**TransientPublisherProperties** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**TransientSubscriptions**](transientsubscriptions.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [名稱](#name)
-   [ReplTest1](#value)

### <a name="name"></a>名稱



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 屬性的名稱。 移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| 類型           | String                                                                                                                                                                                                                                                                 |
| 預設值        | [新增屬性]                                                                                                                                                                                                                                                         |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>值



| 進入 | 值 |
|----------------|---------------------------|
| 描述    | 屬性的值。 |
| Access         | 讀寫                 |
| 類型           | Variant                   |
| 預設        | N/A                       |
| 最小系統 | Windows 2000              |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
