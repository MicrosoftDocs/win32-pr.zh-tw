---
description: 針對與集合相關的介面上的每個方法，各包含一個物件。
ms.assetid: e64b007f-e44d-4b6b-97b2-1e017c5a7dbe
title: MethodsForInterface 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MethodsForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6057d06d4a67222095d5bb0b5ae6da0d603fb4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386008"
---
# <a name="methodsforinterface-collection"></a>MethodsForInterface 集合

針對與集合相關的介面上的每個方法，各包含一個物件。

此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**MethodsForInterface** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForMethod**](rolesformethod.md)

您可以從下列集合流覽至這個集合：

-   [**InterfacesForComponent**](interfacesforcomponent.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   ['](#autocomplete)
-   [Clsid](#clsid)
-   [說明](#description)
-   [IID](#iid)
-   [Index](#index)
-   [名稱](#name)

### <a name="autocomplete"></a>自動完成



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 決定當方法完成時，物件是否會自動停用，而不需要呼叫 SetComplete 或 SetAbort。 這只會影響在方法開始時 JIT 啟用「完成」位的預設設定。這個位可以重設 (為方法內的 SetComplete 或 SetAbort) ，以覆寫預設值。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                  |
| 類型           | Bool                                                                                                                                                                                                                                                                                                                                       |
| 預設        | 否                                                                                                                                                                                                                                                                                                                                      |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                               |



 

### <a name="clsid"></a>CLSID



| 進入 | 值 |
|----------------|---------------------------|
| 描述    | 元件的 GUID。 |
| Access         | ReadOnly                  |
| 類型           | String                    |
| 預設值        | N/A                       |
| 最小系統 | Windows 2000              |



 

### <a name="description"></a>Description



| 進入 | 值 |
|----------------|------------------------------|
| 描述    | 方法的描述。 |
| Access         | 讀寫                    |
| 類型           | String                       |
| 預設值        | ""                           |
| 最小系統 | Windows 2000                 |



 

### <a name="iid"></a>IID



| 進入 | 值 |
|----------------|---------------------------|
| 描述    | 介面的 GUID。 |
| Access         | ReadOnly                  |
| 類型           | String                    |
| 預設值        | N/A                       |
| 最小系統 | Windows 2000              |



 

### <a name="index"></a>索引



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 方法分派識別碼。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                        |
| 類型           | **Dword**                                                                                                                                                       |
| 預設        | N/A                                                                                                                                                             |
| 最小系統 | Windows 2000                                                                                                                                                    |



 

### <a name="name"></a>Name



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 方法名稱。 在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                           |
| 類型           | String                                                                                                                                             |
| 預設值        | N/A                                                                                                                                                |
| 最小系統 | Windows 2000                                                                                                                                       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
