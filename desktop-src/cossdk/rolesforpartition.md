---
description: RolesForPartition 集合一律與分割區集合中的物件相關。 它會針對每個指派給與其相關之分割區的角色保存物件。
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: RolesForPartition 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110389"
---
# <a name="rolesforpartition-collection"></a>RolesForPartition 集合

**RolesForPartition** 集合一律與分割 [**區集合中的物件**](partitions.md)相關。 它會針對每個指派給與其相關之分割區的角色保存物件。

此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**RolesForPartition** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInPartitionRole**](usersinpartitionrole.md)

您可以從下列集合流覽至這個集合：

-   [**分區**](partitions.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [描述](#description)
-   [Name](#name)

### <a name="description"></a>Description



| 進入 | 值 |
|----------------|----------------------------|
| 描述    | 角色的描述。 |
| Access         | ReadOnly                   |
| 類型           | String                     |
| 預設值        | ""                         |
| 最小系統 | Windows Server 2003        |



 

### <a name="name"></a>Name



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 角色名稱。 移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                                                                                                                    |
| 類型           | String                                                                                                                                                                                                                                                      |
| 預設值        | ""                                                                                                                                                                                                                                                          |
| 最小系統 | Windows Server 2003                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
