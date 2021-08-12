---
description: 包含父元件集合之每個訂用帳戶的物件。
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: SubscriptionsForComponent 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: be18f77c4946a5d8a79adc09e97bc9ab35782fdb837f15b82794cbf5f624d59d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546160"
---
# <a name="subscriptionsforcomponent-collection"></a>SubscriptionsForComponent 集合

包含父 [**元件**](components.md) 集合之每個訂用帳戶的物件。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**SubscriptionsForComponent** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**PublisherProperties**](publisherproperties.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**SubscriberProperties**](subscriberproperties.md)

您可以從下列集合流覽至這個集合：

-   [**單元**](components.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [說明](#description)
-   [Enabled](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [>filtercriteria](#filtercriteria)
-   [識別碼](#subscriptionsforcomponent-collection)
-   [InterfaceID](#interfaceid)
-   [MachineName](#machinename)
-   [MethodName](#methodname)
-   [名稱](#machinename)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [已排入佇列](#queued)
-   [SubscriberMoniker](#subscribermoniker)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [使用者名稱](#username)

### <a name="description"></a>描述



| 進入 | 值 |
|----------------|-------------------------------------|
| 描述    | 訂用帳戶的描述。 |
| Access         | 讀寫                           |
| 類型           | String                              |
| 預設值        | ""                                  |
| 最小系統 | Windows 2000                        |



 

### <a name="enabled"></a>啟用



| 進入 | 值 |
|----------------|----------------------------------------------------------|
| 描述    | 指出目前是否已啟用訂用帳戶。 |
| Access         | 讀寫                                                |
| 類型           | Bool                                                     |
| 預設        | 是                                                     |
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
|----------------|------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出篩選準則的字串。 可以是 [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) 類別的 CLSID。 |
| Access         | 讀寫                                                                                                        |
| 類型           | String                                                                                                           |
| 預設值        | N/A                                                                                                              |
| 最小系統 | Windows 2000                                                                                                     |



 

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
|----------------|------------------------------------------|
| 描述    | 已訂閱之介面的 IID。 |
| Access         | 讀寫                                |
| 類型           | String                                   |
| 預設值        | N/A                                      |
| 最小系統 | Windows 2000                             |



 

### <a name="machinename"></a>MachineName



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------|
| 描述    | 遠端電腦上的事件類別訂閱的遠端電腦名稱稱。 |
| Access         | 讀寫                                                                       |
| 類型           | String                                                                          |
| 預設值        | ""                                                                              |
| 最小系統 | Windows 2000                                                                    |



 

### <a name="methodname"></a>MethodName



| 進入 | 值 |
|----------------|----------------------------------------------|
| 描述    | 要在其上訂閱的介面上的方法。 |
| Access         | 讀寫                                    |
| 類型           | String                                       |
| 預設值        | N/A                                          |
| 最小系統 | Windows 2000                                 |



 

### <a name="name"></a>名稱



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 訂用帳戶的名稱。 移除字串開頭和結尾的額外空間。在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | 讀寫                                                                                                                                                                                                                          |
| 類型           | String                                                                                                                                                                                                                             |
| 預設值        | [新增訂用帳戶]                                                                                                                                                                                                                 |
| 最小系統 | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="peruser"></a>PerUser



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------|
| 描述    | 指出訂用帳戶是否只適用于指定的使用者、使用者名稱。 |
| Access         | 讀寫                                                                   |
| 類型           | Bool                                                                        |
| 預設        | 否                                                                       |
| 最小系統 | Windows 2000                                                                |



 

### <a name="publisherid"></a>PublisherID



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| 描述    | 發行者的識別碼。 您可以指定 EventCLSID 或 PublisherID，但不能同時指定兩者。 |
| Access         | WriteOnce                                                                               |
| 類型           | String                                                                                  |
| 預設值        | ""                                                                                      |
| 最小系統 | Windows 2000                                                                            |



 

### <a name="queued"></a>已排入佇列



| 進入 | 值 |
|----------------|-----------------------------------------------|
| 描述    | 指出訂閱是否已排入佇列。 |
| Access         | 讀寫                                     |
| 類型           | Bool                                          |
| 預設        | 否                                         |
| 最小系統 | Windows 2000                                  |



 

### <a name="subscribermoniker"></a>SubscriberMoniker



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| 描述    | 標示為已排入佇列的訂閱者的標記。 當佇列最初設定為 True 時，就會產生預設值。 |
| Access         | 讀寫                                                                                                       |
| 類型           | String                                                                                                          |
| 預設值        | N/A                                                                                                             |
| 最小系統 | Windows 2000                                                                                                    |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 訂閱相同資料分割中的事件類別時，用來代表訂閱者之資料分割識別碼的 GUID。 訂閱事件類別時，訂閱者可以選擇訂閱相同或不同資料分割中的事件類別。 |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| 類型           | String                                                                                                                                                                                                                                                          |
| 預設值        | <Generated>                                                                                                                                                                                                                                               |
| 最小系統 | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>使用者名稱



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------|
| 描述    | 當 PerUser 為 True 時，套用訂用帳戶的使用者名稱。 |
| Access         | 讀寫                                                                |
| 類型           | String                                                                   |
| 預設值        | N/A                                                                      |
| 最小系統 | Windows 2000                                                             |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
