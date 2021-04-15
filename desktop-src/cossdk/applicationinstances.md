---
description: 抓取有關執行中應用程式的資訊。
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: ApplicationInstances 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468168"
---
# <a name="applicationinstances-collection"></a>ApplicationInstances 集合

抓取有關執行中應用程式的資訊。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**ApplicationInstances** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**應用程式**](applications.md)
-   [**根**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [應用程式](#applicationinstances-collection)
-   [HasRecycled](#hasrecycled)
-   [InstanceID](#instanceid)
-   [IsPaused](#ispaused)
-   [PartitionID](#partitionid)
-   [ProcessID](#processid)

### <a name="application"></a>應用程式



| 進入 | 值 |
|----------------|-------------------------------------|
| 描述    | 正在執行之應用程式的識別碼。 |
| Access         | ReadOnly                            |
| 類型           | String                              |
| 預設值        | N/A                                 |
| 最小系統 | Windows XP                          |



 

### <a name="hasrecycled"></a>HasRecycled



| 進入 | 值 |
|----------------|---------------------------------------------------------------|
| 描述    | 指出是否已回收應用程式實例。 |
| Access         | ReadOnly                                                      |
| 類型           | Bool                                                          |
| 預設        | 否                                                         |
| 最小系統 | Windows XP                                                    |



 

### <a name="instanceid"></a>InstanceID



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 應用程式實例的全域唯一識別碼。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                                                                                            |
| 類型           | String                                                                                                                                                                                                                              |
| 預設值        | N/A                                                                                                                                                                                                                                 |
| 最小系統 | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>IsPaused



| 進入 | 值 |
|----------------|-----------------------------------------------------------------|
| 描述    | 指出應用程式實例是否目前已暫停。 |
| Access         | ReadOnly                                                        |
| 類型           | Bool                                                            |
| 預設        | 否                                                           |
| 最小系統 | Windows XP                                                      |



 

### <a name="partitionid"></a>PartitionID



| 進入 | 值 |
|----------------|-------------------------------------------------|
| 描述    | 應用程式所使用的資料分割識別碼。 |
| Access         | ReadOnly                                        |
| 類型           | String                                          |
| 預設值        | N/A                                             |
| 最小系統 | Windows XP                                      |



 

### <a name="processid"></a>ProcessID



| 進入 | 值 |
|----------------|---------------------------------------------|
| 描述    | 應用程式例項的處理程序識別碼。 |
| Access         | ReadOnly                                    |
| 類型           | String                                      |
| 預設值        | N/A                                         |
| 最小系統 | Windows XP                                  |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
