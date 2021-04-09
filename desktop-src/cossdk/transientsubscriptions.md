---
description: 包含每個暫時性訂用帳戶的物件。 您可以針對執行中的物件實例執行暫時的訂閱，並在物件終結時消失。
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: TransientSubscriptions 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847374"
---
# <a name="transientsubscriptions-collection"></a>TransientSubscriptions 集合

包含每個暫時性訂用帳戶的物件。 您可以針對執行中的物件實例執行暫時的訂閱，並在物件終結時消失。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**TransientSubscriptions** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientPublisherProperties**](transientpublisherproperties.md)
-   [**TransientSubscriberProperties**](transientsubscriberproperties.md)

您可以從下列集合流覽至這個集合：

-   [**根**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [說明](#description)
-   [Enabled](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [>filtercriteria](#filtercriteria)
-   [識別碼](#transientsubscriptions-collection)
-   [InterfaceID](#interfaceid)
-   [MethodName](#methodname)
-   [名稱](#methodname)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [SubscriberInterface](#subscriberinterface)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [使用者名稱](#username)

### <a name="description"></a>Description



| 進入 | 值 |
|----------------|-------------------------------------|
| 描述    | 訂用帳戶的描述。 |
| Access         | 讀寫                           |
| 類型           | String                              |
| 預設值        | ""                                  |
| 最小系統 | Windows 2000                        |



 

### <a name="enabled"></a>已啟用



| 進入 | 值 |
|----------------|----------------------------------------------------------|
| 描述    | 指出目前是否已啟用訂用帳戶。 |
| Access         | 讀寫                                                |
| 類型           | Bool                                                     |
| 預設        | 對                                                     |
| 最小系統 | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 訂閱事件類別時，用來代表包含事件類別之資料分割識別碼的 GUID。 訂閱事件類別時，訂閱者可以選擇訂閱相同或不同資料分割中的事件類別。 |
| Access         | 讀寫                                                                                                                                                                                                                                          |
| 類型           | String                                                                                                                                                                                                                                             |
| 預設值        | NULL                                                                                                                                                                                                                                               |
| 最小系統 | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------|
| 描述    | 事件類別的 CLSID。 您可以指定 EventCLSID 或 PublisherID，但不能同時指定兩者。 |
| Access         | WriteOnce                                                                                    |
| 類型           | String                                                                                       |
| 預設值        | N/A                                                                                          |
| 最小系統 | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>>filtercriteria



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出篩選準則的字串。 可以是 [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) 類別的 CLSID。 |
| Access         | 讀寫                                                                                                            |
| 類型           | String                                                                                                               |
| 預設值        | N/A                                                                                                                  |
| 最小系統 | Windows 2000                                                                                                         |



 

### <a name="id"></a>識別碼



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 訂用帳戶的識別碼。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                        |
| 類型           | String                                                                                                                                                           |
| 預設值        | <Generated>                                                                                                                                                |
| 最小系統 | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| 進入 | 值 |
|----------------|----------------------------------|
| 描述    | 已訂閱之介面的 IID。 |
| Access         | WriteOnce                        |
| 類型           | String                           |
| 預設值        | N/A                              |
| 最小系統 | Windows 2000                     |



 

### <a name="methodname"></a>MethodName



| 進入 | 值 |
|----------------|----------------------------------------------|
| 描述    | 要在其上訂閱的介面上的方法。 |
| Access         | 讀寫                                    |
| 類型           | String                                       |
| 預設值        | N/A                                          |
| 最小系統 | Windows 2000                                 |



 

### <a name="name"></a>Name



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 訂用帳戶的名稱。 移除字串開頭和結尾的額外空間。在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | 讀寫                                                                                                                                                                                                                              |
| 類型           | String                                                                                                                                                                                                                                 |
| 預設值        | [新增訂用帳戶]                                                                                                                                                                                                                     |
| 最小系統 | Windows 2000                                                                                                                                                                                                                           |



 

### <a name="peruser"></a>PerUser



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------|
| 描述    | 指出訂閱是否只適用于指定的使用者（以 UserName 屬性工作表示）。 |
| Access         | 讀寫                                                                                               |
| 類型           | Bool                                                                                                    |
| 預設        | 否                                                                                                   |
| 最小系統 | Windows 2000                                                                                            |



 

### <a name="publisherid"></a>PublisherID



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------|
| 描述    | 發行者的識別碼。 您可以指定 EventCLSID 或 PublisherID，但不能同時指定兩者。 |
| Access         | WriteOnce                                                                           |
| 類型           | String                                                                              |
| 預設值        | ""                                                                                  |
| 最小系統 | Windows 2000                                                                        |



 

### <a name="subscriberinterface"></a>SubscriberInterface



| 進入 | 值 |
|----------------|------------------------------------------|
| 描述    | 訂閱者介面的指標。 |
| Access         | 讀寫                                |
| 類型           | Variant                                  |
| 預設        | N/A                                      |
| 最小系統 | Windows 2000                             |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 訂閱相同資料分割中的事件類別時，用來代表訂閱者之資料分割識別碼的 GUID。 訂閱事件類別時，訂閱者可以選擇訂閱相同或不同資料分割中的事件類別。 |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| 類型           | String                                                                                                                                                                                                                                                          |
| 預設值        | <Generated>                                                                                                                                                                                                                                               |
| 最小系統 | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------|
| 描述    | 當 PerUser 為 True 時，訂用帳戶適用的使用者名稱。 |
| Access         | 讀寫                                                               |
| 類型           | String                                                                  |
| 預設值        | N/A                                                                     |
| 最小系統 | Windows 2000                                                            |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
