---
description: 針對集合所關聯的元件所公開的每個介面，各包含一個物件。
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: InterfacesForComponent 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 13c0ed22b6d4ee8ffb4a0d6c4d3f6475341192f656c48553ab901206be833b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047446"
---
# <a name="interfacesforcomponent-collection"></a>InterfacesForComponent 集合

針對集合所關聯的元件所公開的每個介面，各包含一個物件。

此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**InterfacesForComponent** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**MethodsForInterface**](methodsforinterface.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForInterface**](rolesforinterface.md)

您可以從下列集合流覽至這個集合：

-   [**單元**](components.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [CLSID](#clsid)
-   [說明](#description)
-   [IID](#iid)
-   [名稱](#name)
-   [QueuingEnabled](#queuingenabled)
-   [QueueingSupported](#queueingsupported)

### <a name="clsid"></a>CLSID



| 進入 | 值 |
|----------------|---------------------------|
| 描述    | 元件的 GUID。 |
| Access         | ReadOnly                  |
| 類型           | String                    |
| 預設值        | N/A                       |
| 最小系統 | Windows 2000              |



 

### <a name="description"></a>描述



| 進入 | 值 |
|----------------|----------------------------------|
| 描述    | 介面的描述。 |
| Access         | 讀寫                        |
| 類型           | String                           |
| 預設值        | ""                               |
| 最小系統 | Windows 2000                     |



 

### <a name="iid"></a>IID



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 介面的 GUID。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                  |
| 類型           | String                                                                                                                                                    |
| 預設值        | N/A                                                                                                                                                       |
| 最小系統 | Windows 2000                                                                                                                                              |



 

### <a name="name"></a>名稱



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 介面的名稱。 在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                    |
| 類型           | String                                                                                                                                                      |
| 預設值        | N/A                                                                                                                                                         |
| 最小系統 | Windows 2000                                                                                                                                                |



 

### <a name="queuingenabled"></a>QueuingEnabled



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 將介面標示為 queuable，而且可以使用管理 SDK 或元件服務系統管理工具來設定。 不過，只有具有 **佇列支援** 旗標集的介面可以設定 **佇列啟用** 旗標。 |
| Access         | 讀寫                                                                                                                                                                                                                          |
| 類型           | Bool                                                                                                                                                                                                                               |
| 預設        | 否                                                                                                                                                                                                                              |
| 最小系統 | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a>QueueingSupported



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 介面支援佇列。 針對支援佇列的介面，所有方法都只能在參數中。 **支援的佇列** 會公開為唯讀屬性。 |
| Access         | ReadOnly                                                                                                                                                               |
| 類型           | Bool                                                                                                                                                                   |
| 預設        | 否                                                                                                                                                                  |
| 最小系統 | Windows 2000                                                                                                                                                           |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
