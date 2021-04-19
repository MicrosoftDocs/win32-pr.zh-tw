---
description: 包含每個資料分割使用者的物件。
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: PartitionUsers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989900"
---
# <a name="partitionusers-collection"></a>PartitionUsers 集合

包含每個資料分割使用者的物件。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**PartitionUsers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**根**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [AccountName](#accountname)
-   [DefaultPartitionID](#defaultpartitionid)

### <a name="accountname"></a>AccountName



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 分割區使用者帳戶的名稱。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                                                                    |
| 類型           | String                                                                                                                                                                                                       |
| 預設值        | [新增使用者]                                                                                                                                                                                                   |
| 最小系統 | Windows Server 2003                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a>DefaultPartitionID



| 進入 | 值 |
|----------------|--------------------------------------------------------------------|
| 描述    | 基底應用程式分割區的全域唯一識別碼。 |
| Access         | 讀寫                                                          |
| 類型           | String                                                             |
| 預設值        | {41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}                             |
| 最小系統 | Windows Server 2003                                                |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
