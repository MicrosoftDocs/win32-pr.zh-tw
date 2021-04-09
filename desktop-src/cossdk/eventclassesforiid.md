---
description: 捕獲事件類別的相關資訊。
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: EventClassesForIID 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110560"
---
# <a name="eventclassesforiid-collection"></a>EventClassesForIID 集合

捕獲事件類別的相關資訊。

「發行者」與「訂閱者」 (s) 之間的連接，是由 [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) 物件管理，它是一個 com + 元件，其中包含發行者用來引發事件的介面和方法。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**EventClassesForIID** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**根**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [應用程式](#application)
-   [位元](#bitness)
-   [Clsid](#clsid)
-   [說明](#description)
-   [IsPrivateComponent](#isprivatecomponent)
-   [ProgID](#progid)

### <a name="application"></a>應用程式



| 進入 | 值 |
|----------------|----------------------------------------------------------|
| 描述    | 包含事件類別的應用程式 GUID。 |
| Access         | ReadOnly                                                 |
| 類型           | String                                                   |
| 預設值        | N/A                                                      |
| 最小系統 | Windows XP                                               |



 

### <a name="bitness"></a>位元



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 表示事件類別的二進位位數類型。 在使用64位 Windows 的系統上，這個屬性會區分64位元件與32位元件。 |
| Access         | ReadOnly                                                                                                                                                                |
| 類型           | 很長可能的值： COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                            |
| 預設        | N/A                                                                                                                                                                     |
| 最小系統 | Windows XP                                                                                                                                                              |



 

### <a name="clsid"></a>CLSID



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 事件類別的 GUID。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                      |
| 類型           | String                                                                                                                                                        |
| 預設值        | N/A                                                                                                                                                           |
| 最小系統 | Windows XP                                                                                                                                                    |



 

### <a name="description"></a>Description



| 進入 | 值 |
|----------------|----------------------------|
| 描述    | 描述事件類別。 |
| Access         | ReadOnly                   |
| 類型           | String                     |
| 預設值        | ""                         |
| 最小系統 | Windows XP                 |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| 進入 | 值 |
|----------------|---------------------------------------------------------|
| 描述    | 指出事件類別元件是否為私用。 |
| Access         | ReadOnly                                                |
| 類型           | Bool                                                    |
| 預設        | 否                                                   |
| 最小系統 | Windows XP                                              |



 

### <a name="progid"></a>ProgID



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 用來識別事件類別的易記名稱。 在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                                            |
| 類型           | String                                                                                                                                                                              |
| 預設值        | ""                                                                                                                                                                                  |
| 最小系統 | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
