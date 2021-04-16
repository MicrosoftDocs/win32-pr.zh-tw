---
description: 包含相關應用程式中每個元件的物件。
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: 元件集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510715"
---
# <a name="components-collection"></a>元件集合

包含相關應用程式中每個元件的物件。 **元件** 集合一律與 [**應用程式**](applications.md)集合中的物件相關。 這些物件所公開的屬性會保存在元件層級所做的設定。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，但不支援 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法。 若要安裝或匯入元件到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。

## <a name="members"></a>成員

**元件** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**InterfacesForComponent**](interfacesforcomponent.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForComponent**](rolesforcomponent.md)
-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

您可以從下列集合流覽至這個集合：

-   [**應用程式**](applications.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [AllowInprocSubscribers](#allowinprocsubscribers)
-   [ApplicationID](#applicationid)
-   [位元](#bitness)
-   [Clsid](#multiinterfacepublisherfilterclsid)
-   [ComponentAccessChecksEnabled](#componentaccesschecksenabled)
-   [ComponentTransactionTimeout](#componenttransactiontimeoutenabled)
-   [ComponentTransactionTimeoutEnabled](#componenttransactiontimeoutenabled)
-   [COMTIIntrinsics](#comtiintrinsics)
-   [ConstructionEnabled](#constructionenabled)
-   [ConstructorString](#constructorstring)
-   [CreationTimeout](#creationtimeout)
-   [說明](#description)
-   [DLL](#dll)
-   [EventTrackingEnabled](#eventtrackingenabled)
-   [ExceptionClass](#exceptionclass)
-   [FireInParallel](#fireinparallel)
-   [IISIntrinsics](#iisintrinsics)
-   [InitializeServerApplication](#initializeserverapplication)
-   [IsEnabled](#isenabled)
-   [IsEventClass](#iseventclass)
-   [IsInstalled](#isinstalled)
-   [IsPrivateComponent](#isprivatecomponent)
-   [JustInTimeActivation](#justintimeactivation)
-   [LoadBalancingSupported](#loadbalancingsupported)
-   [MaxPoolSize](#maxpoolsize)
-   [MinPoolSize](#minpoolsize)
-   [MultiInterfacePublisherFilterCLSID](#multiinterfacepublisherfilterclsid)
-   [MustRunInClientCoNtext](#mustruninclientcontext)
-   [MustRunInDefaultCoNtext](#mustrunindefaultcontext)
-   [ObjectPoolingEnabled](#objectpoolingenabled)
-   [ProgID](#progid)
-   [PublisherID](#publisherid)
-   [SoapAssemblyName](#soapassemblyname)
-   [SoapTypeName](#soaptypename)
-   [同步處理](#synchronization)
-   [ThreadingModel](#threadingmodel)
-   [交易](#componenttransactiontimeout)
-   [TxIsolationLevel](#txisolationlevel)
-   [VersionBuild](#versionbuild)
-   [VersionMajor](#versionmajor)
-   [VersionMinor](#versionminor)
-   [VersionSubBuild](#versionsubbuild)

### <a name="allowinprocsubscribers"></a>AllowInprocSubscribers



| 進入 | 值 |
|----------------|--------------------------------------------------------------------|
| 描述    | 如果元件是事件類別，則在處理訂閱者中啟用。 |
| Access         | 讀寫                                                          |
| 類型           | Bool                                                               |
| 預設        | 對                                                               |
| 最小系統 | Windows 2000                                                       |



 

### <a name="applicationid"></a>ApplicationID



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 包含元件之應用程式的 GUID。 必須是有效的應用程式 GUID，在呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 之前會先進行驗證。 如果此值變更為不同應用程式的 GUID，則元件會移至該應用程式。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                        |
| 類型           | String                                                                                                                                                                                                                                                                                           |
| 預設值        | N/A                                                                                                                                                                                                                                                                                              |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a>位元



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 表示元件的二進位位數類型。 在使用64位 Windows 的系統上，這個屬性會區分64位元件與32位元件。 |
| Access         | ReadOnly                                                                                                                                                            |
| 類型           | 很長可能的值： COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                        |
| 預設        | N/A                                                                                                                                                                 |
| 最小系統 | Windows XP                                                                                                                                                          |



 

### <a name="clsid"></a>CLSID



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 元件的 GUID。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                  |
| 類型           | String                                                                                                                                                    |
| 預設值        | N/A                                                                                                                                                       |
| 最小系統 | Windows 2000                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a>ComponentAccessChecksEnabled



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出是否要對元件的呼叫執行以角色為基礎的存取檢查，並與應用程式上的 AccessChecksLevel 和 ApplicationAccessChecksEnabled 屬性搭配使用。 |
| Access         | 讀寫                                                                                                                                                                                                  |
| 類型           | Bool                                                                                                                                                                                                       |
| 預設        | 否                                                                                                                                                                                                      |
| 最小系統 | Windows 2000                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a>ComponentTransactionTimeout



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 在交易中使用時，會指定此元件造成交易超時的時間週期。預設值為60秒，且不能超過3600秒 (1 小時) 。 超時值可以設定為0，並指定無限的交易超時時間。 若要使用這個屬性，ComponentTransactionTimeoutEnabled 必須是 True。 這個屬性的值會覆寫 [**LocalComputer**](localcomputer.md) 集合的 TransactionTimeout 屬性所指定的全域交易超時時間。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 類型           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 預設        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a>ComponentTransactionTimeoutEnabled



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指定是否啟用此元件的交易超時時間。 依預設，交易超時功能已停用。 當此屬性為 True 時，會使用 ComponentTransactionTimeout 所指定的超時時間。 當這個屬性為 False 時，就會使用 [**LocalComputer**](localcomputer.md) 集合的 TransactionTimeout 屬性所指定的超時時間。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                      |
| 類型           | Bool                                                                                                                                                                                                                                                                                                                                                                                           |
| 預設        | 否                                                                                                                                                                                                                                                                                                                                                                                          |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a>COMTIIntrinsics



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 可從 COM 交易整合器 (COMTI) 將內容屬性傳遞至這個類別的內容。 COMTI 能簡化將大型主機交易和商務邏輯包裝為 COM 元件的工作。 |
| Access         | 讀寫                                                                                                                                                                                                            |
| 類型           | Bool                                                                                                                                                                                                                 |
| 預設        | 否                                                                                                                                                                                                                |
| 最小系統 | Windows 2000                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a>ConstructionEnabled



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------|
| 描述    | 判斷 ConstructorString 是否會在建立時傳遞給物件。 |
| Access         | 讀寫                                                                                |
| 類型           | Bool                                                                                     |
| 預設        | 否                                                                                    |
| 最小系統 | Windows 2000                                                                             |



 

### <a name="constructorstring"></a>ConstructorString



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 元件結構的初始化字串。 您可以使用物件的函式字串，從相同的泛型元件建立不同的物件。 如果 ConstructionEnabled 為 False，則會忽略這個屬性。 |
| Access         | 讀寫                                                                                                                                                                                                          |
| 類型           | String                                                                                                                                                                                                             |
| 預設值        | ""                                                                                                                                                                                                                 |
| 最小系統 | Windows 2000                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a>CreationTimeout



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 在建立物件時，會傳回逾時錯誤之前的毫秒數。 最大超時值為2147483647毫秒 (大約25天) 。 |
| Access         | 讀寫                                                                                                                                              |
| 類型           | Long (0-2147483647)                                                                                                                                     |
| 預設        | 0                                                                                                                                                      |
| 最小系統 | Windows 2000                                                                                                                                           |



 

### <a name="description"></a>Description



| 進入 | 值 |
|----------------|--------------------------|
| 描述    | 描述元件。 |
| Access         | 讀寫                |
| 類型           | String                   |
| 預設值        | ""                       |
| 最小系統 | Windows 2000             |



 

### <a name="dll"></a>DLL



| 進入 | 值 |
|----------------|---------------------------------------------------------|
| 描述    | 包含元件的檔案名和路徑。 |
| Access         | ReadOnly                                                |
| 類型           | String                                                  |
| 預設值        | N/A                                                     |
| 最小系統 | Windows 2000                                            |



 

### <a name="eventtrackingenabled"></a>EventTrackingEnabled



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 判斷是否追蹤事件。 事件包含像是應用程式關閉的動作;物件建立和發行;物件參考、一致性、啟用和停用;方法呼叫、傳回和例外狀況;交易啟動、準備認可和中止;資源配置器連接、配置和回收;執行緒配置和回收。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                     |
| 類型           | Bool                                                                                                                                                                                                                                                                                                                                                                          |
| 預設        | 對                                                                                                                                                                                                                                                                                                                                                                          |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a>ExceptionClass



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | CLSID （可以是 GUID 或標記字串），可在處理重複排入佇列之元件程式的程式期間啟動替代程式。 |
| Access         | 讀寫                                                                                                                                                                 |
| 類型           | String                                                                                                                                                                    |
| 預設值        | ""                                                                                                                                                                        |
| 最小系統 | Windows 2000                                                                                                                                                              |



 

### <a name="fireinparallel"></a>FireInParallel



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------|
| 描述    | 如果元件是事件類別，則可讓事件以平行方式引發。 |
| Access         | 讀寫                                                                  |
| 類型           | Bool                                                                       |
| 預設        | 否                                                                      |
| 最小系統 | Windows 2000                                                               |



 

### <a name="iisintrinsics"></a>IISIntrinsics



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 啟用將 IIS 內容屬性（例如應用程式會話物件或使用者會話物件）傳遞到此類別的內容中。 |
| Access         | 讀寫                                                                                                                                   |
| 類型           | Bool                                                                                                                                        |
| 預設        | 否                                                                                                                                       |
| 最小系統 | Windows 2000                                                                                                                                |



 

### <a name="initializeserverapplication"></a>InitializeServerApplication



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------|
| 描述    | 指出元件是否用來初始化伺服器應用程式。 |
| Access         | 讀寫                                                                   |
| 類型           | Bool                                                                        |
| 預設        | 否                                                                       |
| 最小系統 | Windows Server 2003                                                         |



 

### <a name="isenabled"></a>IsEnabled



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| 描述    | 如果 COM + 應用程式或元件已停用，則為 False。 如果已啟用 COM + 應用程式或元件，IsEnabled 為 True。 |
| Access         | 讀寫                                                                                                                   |
| 類型           | Bool                                                                                                                        |
| 預設        | 對                                                                                                                        |
| 最小系統 | Windows XP                                                                                                                  |



 

### <a name="iseventclass"></a>IsEventClass



| 進入 | 值 |
|----------------|----------------------------------------------------|
| 描述    | 指出元件是否為事件類別。 |
| Access         | ReadOnly                                           |
| 類型           | Bool                                               |
| 預設        | 否                                              |
| 最小系統 | Windows 2000                                       |



 

### <a name="isinstalled"></a>IsInstalled



| 進入 | 值 |
|----------------|-----------------------------------------------------------------|
| 描述    | 指出元件是否安裝在應用程式中。 |
| Access         | ReadOnly                                                        |
| 類型           | Bool                                                            |
| 預設        | 否                                                           |
| 最小系統 | Windows Server 2003                                             |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 判斷伺服器應用程式是否為私用元件。 伺服器應用程式中的私用元件只能從應用程式內啟用。 例如，如果您在私用元件上呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ，它會從跨進程失敗，但會成功進行同進程。 相反地，如果您在公用元件上呼叫 **CoCreateInstance** ，則會成功進行同進程和跨進程。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 類型           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 預設        | 否                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a>JustInTimeActivation



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 判斷是否已啟用元件的 [JIT](enabling-jit-activation-for-a-component.md) 啟用。 當 [交易支援](setting-the-transaction-attribute.md) 設定為必要、需要新增或支援時，這個屬性會設定為 True。 當 JustInTimeActivation 設定為 True 時，必須將 [同步處理支援](setting-the-synchronization-attribute.md) 設定為 [必要] (預設) 或需要新的。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 類型           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 預設        | 否                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a>LoadBalancingSupported



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 如果伺服器上已安裝並啟用元件負載平衡服務，則會判斷元件是否參與負載平衡。 |
| Access         | 讀寫                                                                                                                                        |
| 類型           | Bool                                                                                                                                             |
| 預設        | 否                                                                                                                                            |
| 最小系統 | Windows 2000                                                                                                                                     |



 

### <a name="maxpoolsize"></a>MaxPoolSize



| 進入 | 值 |
|----------------|-----------------------------------|
| 描述    | 集區的最大物件數目。 |
| Access         | 讀寫                         |
| 類型           | Long (1-1048576)                   |
| 預設        | 1048576                           |
| 最小系統 | Windows 2000                      |



 

### <a name="minpoolsize"></a>MinPoolSize



| 進入 | 值 |
|----------------|-----------------------------------|
| 描述    | 共置的物件數目下限。 |
| Access         | 讀寫                         |
| 類型           | Long (0-1048576)                   |
| 預設        | 0                                 |
| 最小系統 | Windows 2000                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a>MultiInterfacePublisherFilterCLSID



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------|
| 描述    | 如果元件是事件類別，則使用發行者篩選器的 CLSID。 |
| Access         | 讀寫                                                               |
| 類型           | String                                                                  |
| 預設值        | N/A                                                                     |
| 最小系統 | Windows 2000                                                            |



 

### <a name="mustruninclientcontext"></a>MustRunInClientCoNtext



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------|
| 描述    | 表示元件必須在其原始呼叫端的內容中啟用。 否則啟用會失敗。 |
| Access         | 讀寫                                                                                                 |
| 類型           | Bool                                                                                                      |
| 預設        | 否                                                                                                     |
| 最小系統 | Windows XP                                                                                                |



 

### <a name="mustrunindefaultcontext"></a>MustRunInDefaultCoNtext



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------|
| 描述    | 指出必須在預設呼叫端的內容中啟用元件。 否則啟用會失敗。 |
| Access         | 讀寫                                                                                                    |
| 類型           | Bool                                                                                                         |
| 預設        | 否                                                                                                        |
| 最小系統 | Windows 2000                                                                                                 |



 

### <a name="objectpoolingenabled"></a>ObjectPoolingEnabled



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------|
| 描述    | 判斷元件是否啟用 [Com + 物件](com--object-pooling.md) 共用。 |
| Access         | 讀寫                                                                                       |
| 類型           | Bool                                                                                            |
| 預設        | 否                                                                                           |
| 最小系統 | Windows 2000                                                                                    |



 

### <a name="progid"></a>ProgID



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 用來識別元件的易記名稱。 在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                                              |
| 類型           | String                                                                                                                                                                                |
| 預設值        | N/A                                                                                                                                                                                   |
| 最小系統 | Windows 2000                                                                                                                                                                          |



 

### <a name="publisherid"></a>PublisherID



| 進入 | 值 |
|----------------|------------------------------------------------------------------------|
| 描述    | 如果元件是事件類別，則為事件發行者的識別碼。 |
| Access         | 讀寫                                                              |
| 類型           | String                                                                 |
| 預設值        | ""                                                                     |
| 最小系統 | Windows 2000                                                           |



 

### <a name="soapassemblyname"></a>SoapAssemblyName



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------|
| 描述    | 識別 GAC 元件的 GUID，該元件會在以 SOAP 服務的形式叫用元件時執行。 |
| Access         | 讀寫                                                                                        |
| 類型           | String                                                                                           |
| 預設值        | NULL                                                                                             |
| 最小系統 | Windows Server 2003                                                                              |



 

### <a name="soaptypename"></a>SoapTypeName



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------|
| 描述    | 可以叫用為 SOAP 服務之元件的 managed 型別名稱。 |
| Access         | 讀寫                                                                    |
| 類型           | String                                                                       |
| 預設值        | NULL                                                                         |
| 最小系統 | Windows Server 2003                                                          |



 

### <a name="synchronization"></a>同步處理



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 判斷元件的呼叫 [同步](setting-the-synchronization-attribute.md) 處理。                                                                                                     |
| Access         | 讀寫                                                                                                                                                                                           |
| 類型           | 長可能的值： COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4)  |
| 預設        | COMAdminSynchronizationIgnored (0)                                                                                                                                                                   |
| 最小系統 | Windows 2000                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a>ThreadingModel



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 決定如何將元件的實例指派給方法執行的執行緒。 值會對應至 COM 執行緒模型。                                                                                        |
| Access         | ReadOnly                                                                                                                                                                                                                  |
| 類型           | 長可能的值： COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5)  |
| 預設        | N/A                                                                                                                                                                                                                       |
| 最小系統 | Windows 2000                                                                                                                                                                                                              |



 

### <a name="transaction"></a>交易



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 決定元件如何支援 [交易](setting-the-transaction-attribute.md)。 建議您在列舉中使用常數，而不要使用數值。 |
| Access         | 讀寫                                                                                                                                                                              |
| 類型           | 長可能的值： COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)         |
| 預設        | COMAdminTransactionNone (1)                                                                                                                                                             |
| 最小系統 | Windows 2000                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a>TxIsolationLevel



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出交易隔離等級。 有五個隔離等級：無、讀取未認可、讀取認可、可重複讀取和序列化。 預設的隔離等級是序列化的。                           |
| Access         | 讀寫                                                                                                                                                                                                                  |
| 類型           | 長可能的值： COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4)  |
| 預設        | COMAdminTxIsolationLevelSerializable (4)                                                                                                                                                                                    |
| 最小系統 | Windows XP                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a>VersionBuild



| 進入 | 值 |
|----------------|---------------------------|
| 描述    | 版本組建識別碼。 |
| Access         | ReadOnly                  |
| 類型           | String                    |
| 預設值        | ""                        |
| 最小系統 | Windows 2000              |



 

### <a name="versionmajor"></a>VersionMajor



| 進入 | 值 |
|----------------|---------------------|
| 描述    | 版本識別碼。 |
| Access         | ReadOnly            |
| 類型           | String              |
| 預設值        | ""                  |
| 最小系統 | Windows 2000        |



 

### <a name="versionminor"></a>VersionMinor



| 進入 | 值 |
|----------------|-------------------------|
| 描述    | 版本子識別碼。 |
| Access         | ReadOnly                |
| 類型           | String                  |
| 預設值        | ""                      |
| 最小系統 | Windows 2000            |



 

### <a name="versionsubbuild"></a>VersionSubBuild



| 進入 | 值 |
|----------------|-------------------------------|
| 描述    | 版本子組建識別碼。 |
| Access         | ReadOnly                      |
| 類型           | String                        |
| 預設值        | ""                            |
| 最小系統 | Windows 2000                  |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
