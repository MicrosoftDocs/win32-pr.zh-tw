---
description: UsersInPartitionRole 集合-包含與集合相關的角色中每位使用者的物件。
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: UsersInPartitionRole 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: d07c62fc6c6cc871f803b1f752201bd500e2705c3cfca272ff350ffd018f6018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499641"
---
# <a name="usersinpartitionrole-collection"></a>UsersInPartitionRole 集合

針對與集合相關的角色中的每個使用者，各包含一個物件。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**UsersInPartitionRole** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**RolesForPartition**](rolesforpartition.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [使用者](#usersinpartitionrole-collection)

### <a name="user"></a>使用者



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 使用者名稱。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                                             |
| 類型           | String                                                                                                                                                                                |
| 預設值        | [新增使用者]                                                                                                                                                                            |
| 最小系統 | Windows Server 2003                                                                                                                                                                   |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
