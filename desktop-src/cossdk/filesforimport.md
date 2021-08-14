---
description: 抓取匯入之應用程式的資訊。
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: FilesForImport 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3b6351edd58691db3a499a6c0512e76fe87167f888289b8a2d2a947fe1304cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307325"
---
# <a name="filesforimport-collection"></a>FilesForImport 集合

抓取匯入之應用程式的資訊。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**FilesForImport** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**Root**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [ApplicationFileName](#applicationfilename)
-   [ApplicationName](#applicationname)
-   [說明](#partitiondescription)
-   [FileName](#applicationfilename)
-   [HasUsers](#hasusers)
-   [IsProxy](#isproxy)
-   [IsService](#isservice)
-   [PartitionDescription](#partitiondescription)
-   [PartitionID](#partitionid)
-   [PartitionName](#partitionname)

### <a name="applicationfilename"></a>ApplicationFileName



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------|
| 描述    | 包含可匯入之應用程式的 MSI 檔案名。 |
| Access         | ReadOnly                                                                     |
| 類型           | String                                                                       |
| 預設值        | N/A                                                                          |
| 最小系統 | Windows XP                                                                   |



 

### <a name="applicationname"></a>ApplicationName



| 進入 | 值 |
|----------------|------------------------------|
| 描述    | 應用程式的名稱。 |
| Access         | ReadOnly                     |
| 類型           | String                       |
| 預設值        | ""                           |
| 最小系統 | Windows XP                   |



 

### <a name="description"></a>Description



| 進入 | 值 |
|----------------|-----------------------------------|
| 描述    | 應用程式的描述。 |
| Access         | ReadOnly                          |
| 類型           | String                            |
| 預設值        | ""                                |
| 最小系統 | Windows XP                        |



 

### <a name="filename"></a>FileName



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 包含應用程式的 DLL 或 EXE 檔案名。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                                                                                              |
| 類型           | String                                                                                                                                                                                                                                |
| 預設值        | ""                                                                                                                                                                                                                                    |
| 最小系統 | Windows XP                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a>HasUsers



| 進入 | 值 |
|----------------|--------------------------------------------------|
| 描述    | 指出應用程式是否有任何使用者。 |
| Access         | ReadOnly                                         |
| 類型           | Bool                                             |
| 預設        | 否                                            |
| 最小系統 | Windows XP                                       |



 

### <a name="isproxy"></a>IsProxy



| 進入 | 值 |
|----------------|-----------------------------------------------|
| 描述    | 指出應用程式是否為 proxy。 |
| Access         | ReadOnly                                      |
| 類型           | Bool                                          |
| 預設        | 否                                         |
| 最小系統 | Windows XP                                    |



 

### <a name="isservice"></a>IsService



| 進入 | 值 |
|----------------|-------------------------------------------------|
| 描述    | 指出應用程式是否為服務。 |
| Access         | ReadOnly                                        |
| 類型           | Bool                                            |
| 預設        | 否                                           |
| 最小系統 | Windows XP                                      |



 

### <a name="partitiondescription"></a>PartitionDescription



| 進入 | 值 |
|----------------|-----------------------------------------------|
| 描述    | 應用程式分割區的描述。 |
| Access         | ReadOnly                                      |
| 類型           | String                                        |
| 預設值        | ""                                            |
| 最小系統 | Windows Server 2003                           |



 

### <a name="partitionid"></a>PartitionID



| 進入 | 值 |
|----------------|------------------------------------------|
| 描述    | 應用程式磁碟分割的 GUID。 |
| Access         | ReadOnly                                 |
| 類型           | String                                   |
| 預設值        | ""                                       |
| 最小系統 | Windows Server 2003                      |



 

### <a name="partitionname"></a>PartitionName



| 進入 | 值 |
|----------------|------------------------------------------|
| 描述    | 應用程式的資料分割名稱。 |
| Access         | ReadOnly                                 |
| 類型           | String                                   |
| 預設值        | ""                                       |
| 最小系統 | Windows Server 2003                      |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
