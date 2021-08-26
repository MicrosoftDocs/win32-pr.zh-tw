---
description: Role 集合一律與應用程式集合中的物件相關。 它會針對指派給與其相關聯之應用程式的每個角色保存物件。
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: 角色集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: 133477d82f718b992a628bde8af58f22d8d50a9e4974816c7c8f56be7ba8e33f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029468"
---
# <a name="roles-collection"></a>角色集合

**Role** 集合一律與 [**應用程式**](applications.md)集合中的物件相關。 它會針對指派給與其相關聯之應用程式的每個角色保存物件。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**Roles** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInRole**](usersinrole.md)

您可以從下列集合流覽至這個集合：

-   [**應用程式**](applications.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [描述](#description)
-   [Name](#name)

### <a name="description"></a>描述



| 進入 | 值 |
|----------------|----------------------------|
| 描述    | 角色的描述。 |
| Access         | 讀寫                  |
| 類型           | String                     |
| 預設值        | ""                         |
| 最小系統 | Windows 2000               |



 

### <a name="name"></a>名稱



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 角色名稱。 移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                                                                                                                   |
| 類型           | String                                                                                                                                                                                                                                                      |
| 預設值        | 「新角色」                                                                                                                                                                                                                                                  |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
