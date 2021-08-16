---
description: 指定每個資料分割內包含的應用程式。
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: 分割區集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3badf52755a77557c200569c25610b5918cf8dd599d17a83bdebb5c4ddfa6801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305871"
---
# <a name="partitions-collection"></a>分割區集合

指定每個資料分割內包含的應用程式。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

分割 **區集合繼承** 自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**應用程式**](applications.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForPartition**](rolesforpartition.md)

您可以從下列集合流覽至這個集合：

-   [**Root**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [多變](#changeable)
-   [刪除](#deleteable)
-   [說明](#description)
-   [識別碼](#partitions-collection)
-   [名稱](#name)

### <a name="changeable"></a>多變



| 進入 | 值 |
|----------------|--------------------------------------------------|
| 描述    | 判斷此分割區是否可變更。 |
| Access         | 讀寫                                        |
| 類型           | Bool                                             |
| 預設        | 是                                             |
| 最小系統 | Windows Server 2003                              |



 

### <a name="deleteable"></a>刪除



| 進入 | 值 |
|----------------|---------------------------------------------------|
| 描述    | 判斷此分割區是否可刪除。 |
| Access         | 讀寫                                         |
| 類型           | Bool                                              |
| 預設        | 是                                              |
| 最小系統 | Windows Server 2003                               |



 

### <a name="description"></a>描述



| 進入 | 值 |
|----------------|---------------------------------------------------------------------|
| 描述    | 這個屬性工作表示識別資料分割的描述。 |
| Access         | 讀寫                                                           |
| 類型           | String                                                              |
| 預設值        | ""                                                                  |
| 最小系統 | Windows Server 2003                                                 |



 

### <a name="id"></a>識別碼



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 表示資料分割的 GUID。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                          |
| 類型           | String                                                                                                                                                             |
| 預設值        | <Generated>                                                                                                                                                  |
| 最小系統 | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>名稱



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 表示資料分割名稱。 移除字串開頭和結尾的額外空間。在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | 讀寫                                                                                                                                                                                                                              |
| 類型           | String                                                                                                                                                                                                                                 |
| 預設值        | 「新增分割區」                                                                                                                                                                                                                        |
| 最小系統 | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
