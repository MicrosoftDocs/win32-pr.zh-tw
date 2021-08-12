---
description: 針對安裝在本機電腦上的每個 COM + 應用程式，各包含一個物件。 這些物件所公開的屬性會保存在應用層級所做的所有設定。
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: 應用程式集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 23ce8d7dc343e9cbca9aab642aee99424c5fffdde8ef0f15a52d2959bf492095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549421"
---
# <a name="applications-collection"></a>應用程式集合

針對安裝在本機電腦上的每個 COM + 應用程式，各包含一個物件。 這些物件所公開的屬性會保存在應用層級所做的所有設定。

您可以使用相關 [**元件**](components.md) 集合來設定應用程式中元件的屬性。 您可以使用相關的 [**角色**](roles.md) 集合，將角色指派給應用程式。

若要將元件安裝到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。 若要從檔案安裝應用程式，或關閉或匯出應用程式，也請在 **COMAdminCatalog** 物件上使用方法。 否則，若要建立新的應用程式，您可以將物件加入至 **應用程式** 集合。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**應用程式** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ApplicationInstances**](applicationinstances.md)
-   [**單元**](components.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**LegacyComponents**](legacycomponents.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**角色**](roles.md)

您可以從下列集合流覽至這個集合：

-   [**分割區**](partitions.md)
-   [**Root**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [3GigSupportEnabled](#3gigsupportenabled)
-   [AccessChecksLevel](#accesscheckslevel)
-   [啟動](#recycleactivationlimit)
-   [ApplicationAccessChecksEnabled](#applicationaccesschecksenabled)
-   [ApplicationDirectory](#applicationdirectory)
-   [ApplicationProxy](#applicationproxyservername)
-   [ApplicationProxyServerName](#applicationproxyservername)
-   [AppPartitionID](#apppartitionid)
-   [驗證](#authenticationcapability)
-   [AuthenticationCapability](#authenticationcapability)
-   [多變](#changeable)
-   [CommandLine](#commandline)
-   [ConcurrentApps](#concurrentapps)
-   [CreatedBy](#createdby)
-   [CRMEnabled](#crmenabled)
-   [CRMLogFile](#crmlogfile)
-   [刪除](#deleteable)
-   [說明](#description)
-   [DumpEnabled](#dumpenabled)
-   [DumpOnException](#dumponexception)
-   [DumpOnFailfast](#dumponfailfast)
-   [DumpPath](#dumppath)
-   [EventsEnabled](#eventsenabled)
-   [識別碼](#applications-collection)
-   [身分識別](#identity)
-   [ImpersonationLevel](#impersonationlevel)
-   [IsEnabled](#isenabled)
-   [IsSystem](#issystem)
-   [MaxDumpCount](#maxdumpcount)
-   [名稱](#applicationproxyservername)
-   [密碼](#password)
-   [QCAuthenticateMsgs](#qcauthenticatemsgs)
-   [QCListenerMaxThreads](#qclistenermaxthreads)
-   [QueueListenerEnabled](#queuelistenerenabled)
-   [QueuingEnabled](#queuingenabled)
-   [RecycleActivationLimit](#recycleactivationlimit)
-   [RecycleCallLimit](#recyclecalllimit)
-   [RecycleExpirationTimeout](#recycleexpirationtimeout)
-   [RecycleLifetimeLimit](#recyclelifetimelimit)
-   [RecycleMemoryLimit](#recyclememorylimit)
-   [複製](#replicable)
-   [RunForever](#runforever)
-   [ServiceName](#servicename)
-   [ShutdownAfter](#shutdownafter)
-   [SoapActivated](#soapactivated)
-   [SoapBaseUrl](#soapbaseurl)
-   [SoapMailTo](#soapmailto)
-   [SoapVRoot](#soapvroot)
-   [SRPEnabled](#srpenabled)
-   [SRPTrustLevel](#srptrustlevel)

### <a name="3gigsupportenabled"></a>3GigSupportEnabled



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出應用程式是否可以在其進程中使用 3 GB 的記憶體。 如果未啟用此功能，應用程式只能使用 2 GB 的記憶體。 |
| Access         | 讀寫                                                                                                                                     |
| 類型           | Bool                                                                                                                                          |
| 預設        | 否                                                                                                                                         |
| 最小系統 | Windows 2000                                                                                                                                  |



 

### <a name="accesscheckslevel"></a>AccessChecksLevel



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出是否只在進程層級執行存取檢查，或在進程和元件層級執行存取檢查。 建議您在列舉中使用常數，而不要使用數值。 |
| Access         | 讀寫                                                                                                                                                                                                       |
| 類型           | 很長可能的值： COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                 |
| 預設        | COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                                                                                |
| 最小系統 | Windows 2000                                                                                                                                                                                                    |



 

### <a name="activation"></a>啟用



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 本機啟用表示應用程式內的物件會在專用本機伺服器進程中執行， (server 應用程式) 。 同進程啟用表示物件會在其建立者的進程中執行， (程式庫應用程式) 。 |
| Access         | 讀寫                                                                                                                                                                                                                           |
| 類型           | 很長可能的值： COMAdminActivationInproc (0) COMAdminActivationLocal (1)                                                                                                                                                         |
| 預設        | COMAdminActivationLocal (1)                                                                                                                                                                                                          |
| 最小系統 | Windows 2000                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a>ApplicationAccessChecksEnabled



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------|
| 描述    | 指出當用戶端對應用程式進行呼叫時，是否對該應用程式執行存取檢查。 |
| Access         | 讀寫                                                                                          |
| 類型           | Bool                                                                                               |
| 預設        | 是                                                                                               |
| 最小系統 | Windows 2000                                                                                       |



 

### <a name="applicationdirectory"></a>ApplicationDirectory



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 應用程式的完整路徑。 當您設定並存 (SxS) 元件時，需要這項資訊。 並存 (SxS) 元件可讓 ASP 應用程式指定要使用的 sxs 支援系統 DLL 版本，例如 msvcrt.lib、MSXML、COMCTL、gdiplus.dll 等等。 例如，如果您的 ASP 應用程式依賴 MSVCRT.LIB 2.0 版，您可以確保即使在將 service pack 套用至伺服器之後，您的應用程式仍會使用 MSVCRT.LIB 2.0 版。 電腦上仍會安裝任何新版的 MSVCRT.LIB，但您的應用程式會保留2.0 版並使用。 SxS 支援的 Dll 儲存在% WINDIR% \\ WinSxS 中。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 類型           | String                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 預設值        | ""                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> 雖然這項功能可在應用層級進行設定，但在任何應用程式集區中只能使用一個系統 DLL 版本。 例如，如果應用程式 App1 使用 MSVCRT.LIB，2.5 版和應用程式 App2 會使用 MSVCRT.LIB、2.4 版，則 App1 和 App2 不應該在相同的應用程式集區中。 如果是，則第一次載入的應用程式會載入其 MSVCRT.LIB 的版本，而其他應用程式則會強制使用它，直到卸載應用程式為止。

 

如需詳細資訊，請參閱 [IIS 6.0 的 COM + 服務變更](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90))中的「並存元件」。

### <a name="applicationproxy"></a>ApplicationProxy



| 進入 | 值 |
|----------------|------------------------------------------------------------|
| 描述    | 指出應用程式是否為應用程式 proxy。 |
| Access         | ReadOnly                                                   |
| 類型           | Bool                                                       |
| 預設        | 否                                                      |
| 最小系統 | Windows 2000                                               |



 

### <a name="applicationproxyservername"></a>ApplicationProxyServerName



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 匯出應用程式 proxy 時使用的遠端伺服器名稱。 它是應用程式 proxy 在用戶端電腦上安裝時所指向的伺服器名稱。 |
| Access         | 讀寫                                                                                                                                                              |
| 類型           | String                                                                                                                                                                 |
| 預設值        | ""                                                                                                                                                                     |
| 最小系統 | Windows 2000                                                                                                                                                           |



 

### <a name="apppartitionid"></a>AppPartitionID



| 進入 | 值 |
|----------------|---------------------------------------------------|
| 描述    | 表示應用程式分割識別碼的 GUID。 |
| Access         | ReadOnly                                          |
| 類型           | String                                            |
| 預設值        | <Generated>                                 |
| 最小系統 | Windows Server 2003                               |



 

### <a name="authentication"></a>驗證



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 設定呼叫的驗證層級，其值會對應至遠端程序呼叫， (RPC) 驗證設定。 選擇 COMAdminAuthenticationDefault 時，會使用 [**LocalComputer**](localcomputer.md) 集合內 DefaultAuthenticationLevel 屬性中的設定。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                             |
| 類型           | 長可能的值： COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                               |
| 預設        | COMAdminAuthenticationPacket (4)                                                                                                                                                                                                                                                                       |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> 針對程式庫 (同進程) 應用程式中，唯一有效的設定是 COMAdminAuthenticationDefault 和 COMAdminAuthenticationNone。 建議您在列舉中使用常數，而不要使用數值。

 

### <a name="authenticationcapability"></a>AuthenticationCapability



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 決定模擬呼叫時所要顯示的身分識別。                                                                                                                                                                      |
| Access         | 讀寫                                                                                                                                                                                                                               |
| 類型           | 較長的可能值： COMAdminAuthenticationCapabilitiesNone (0x0) COMAdminAuthenticationCapabilitiesSecureReference (0x2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)  |
| 預設        | COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)                                                                                                                                                                                 |
| 最小系統 | Windows 2000                                                                                                                                                                                                                            |



 

### <a name="changeable"></a>多變



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 決定是否允許以程式設計方式或透過「元件服務」系統管理工具，來變更應用程式設定或其元件的變更。 |
| Access         | 讀寫                                                                                                                                                                     |
| 類型           | Bool                                                                                                                                                                          |
| 預設        | 是                                                                                                                                                                          |
| 最小系統 | Windows 2000                                                                                                                                                                  |



 

### <a name="commandline"></a>CommandLine



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| 描述    | 用於偵錯工具的命令列字串。 您可以使用指定的命令列，在偵錯工具中啟動應用程式。 |
| Access         | 讀寫                                                                                                                  |
| 類型           | String                                                                                                                     |
| 預設值        | ""                                                                                                                         |
| 最小系統 | Windows 2000                                                                                                               |



 

### <a name="concurrentapps"></a>ConcurrentApps



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------|
| 描述    | 指定可以同時執行之共用應用程式的最大數目。 |
| Access         | 讀寫                                                                        |
| 類型           | Long (1-1048576)                                                                  |
| 預設        | 1                                                                                |
| 最小系統 | Windows XP                                                                       |



 

### <a name="createdby"></a>CreatedBy



| 進入 | 值 |
|----------------|---------------------------------------------------------------|
| 描述    | 說明如何建立應用程式的資訊字串。 |
| Access         | 讀寫                                                     |
| 類型           | String                                                        |
| 預設值        | ""                                                            |
| 最小系統 | Windows 2000                                                  |



 

### <a name="crmenabled"></a>CRMEnabled



| 進入 | 值 |
|----------------|------------------------------------------------------------------|
| 描述    | 判斷是否已啟用補償 Resource Manager。 |
| Access         | 讀寫                                                        |
| 類型           | Bool                                                             |
| 預設        | 否                                                            |
| 最小系統 | Windows 2000                                                     |



 

### <a name="crmlogfile"></a>CRMLogFile



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| 描述    | 用來保存補償資源管理員 (CRM) 記錄檔的檔案名和路徑。 |
| Access         | 讀寫                                                                              |
| 類型           | String                                                                                 |
| 預設值        | ""                                                                                     |
| 最小系統 | Windows 2000                                                                           |



 

### <a name="deleteable"></a>刪除



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| 描述    | 設定是否可透過程式設計方式或透過元件服務管理工具來刪除應用程式。 |
| Access         | 讀寫                                                                                                                   |
| 類型           | Bool                                                                                                                        |
| 預設        | 是                                                                                                                        |
| 最小系統 | Windows 2000                                                                                                                |



 

### <a name="description"></a>描述



| 進入 | 值 |
|----------------|----------------------------|
| 描述    | 描述應用程式。 |
| Access         | 讀寫                  |
| 類型           | String                     |
| 預設值        | ""                         |
| 最小系統 | Windows 2000               |



 

### <a name="dumpenabled"></a>DumpEnabled



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------|
| 描述    | 啟用在指定目錄失敗時，將 COM + 應用程式的狀態傾印。 |
| Access         | 讀寫                                                                                             |
| 類型           | Bool                                                                                                  |
| 預設        | 否                                                                                                 |
| 最小系統 | Windows XP                                                                                            |



 

> [!Note]  
> 從 Windows Server 2003，只有系統管理員具有 com + 傾印檔案的讀取存取許可權。

 

### <a name="dumponexception"></a>DumpOnException



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 當應用程式造成未處理的例外狀況，並由 COM + 執行時間終止時，啟用 COM + 應用程式的狀態傾印。 |
| Access         | 讀寫                                                                                                                                     |
| 類型           | Bool                                                                                                                                          |
| 預設        | 否                                                                                                                                         |
| 最小系統 | Windows XP                                                                                                                                    |



 

### <a name="dumponfailfast"></a>DumpOnFailfast



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------|
| 描述    | 當應用程式失敗時，啟用 COM + 應用程式的狀態傾印。 |
| Access         | 讀寫                                                                       |
| 類型           | Bool                                                                            |
| 預設        | 否                                                                           |
| 最小系統 | Windows XP                                                                      |



 

### <a name="dumppath"></a>DumpPath



| 進入 | 值 |
|----------------|--------------------------------------------------------------|
| 描述    | 儲存傾印檔案之目錄的路徑。 |
| Access         | 讀寫                                                    |
| 類型           | String                                                       |
| 預設值        | "% systemroot% \\ system32 \\ com \\ dmp"                           |
| 最小系統 | Windows XP                                                   |



 

> [!Note]  
> 從 Windows Server 2003，只有系統管理員具有 com + 傾印檔案的讀取存取許可權。

 

### <a name="eventsenabled"></a>EventsEnabled



| 進入 | 值 |
|----------------|-----------------------------------------------------------|
| 描述    | 指出是否已針對應用程式啟用事件。 |
| Access         | 讀寫                                                 |
| 類型           | Bool                                                      |
| 預設        | 是                                                      |
| 最小系統 | Windows 2000                                              |



 

### <a name="id"></a>識別碼



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 表示應用程式的 GUID。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                            |
| 類型           | String                                                                                                                                                               |
| 預設值        | <Generated>                                                                                                                                                    |
| 最小系統 | Windows 2000                                                                                                                                                         |



 

### <a name="identity"></a>身分識別



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 設定應用程式的伺服器進程身分識別。 請指定有效的使用者帳戶或「互動式使用者」，讓應用程式採用目前登入使用者的身分識別。 您也可以指定 "nt 授權 \\ localservice"、"nt 授權單位 \\ networkservice" 和 "nt 授權單位 \\ 系統" 字串。 這三個帳戶的預設密碼為 "" (空白字串) 。 |
| Access         |                                                                                                                                                                                                                                                                                                                                                                                    |
| 類型           |                                                                                                                                                                                                                                                                                                                                                                                    |
| 預設        |                                                                                                                                                                                                                                                                                                                                                                                    |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                                                                       |



 

未針對在用戶端進程中執行的程式庫應用程式啟用識別屬性。

在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼屬性應該與身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。 如果密碼和身分識別不同步，則在系統管理員重設應用程式之前，無法啟動該應用程式。

### <a name="impersonationlevel"></a>ImpersonationLevel



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 設定用於對其他應用程式進行呼叫的模擬等級。                                                                                           |
| Access         | 讀寫                                                                                                                                                     |
| 類型           | 長可能的值： COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)  |
| 預設        | COMAdminImpersonationImpersonate (3)                                                                                                                           |
| 最小系統 | Windows 2000                                                                                                                                                  |



 

### <a name="isenabled"></a>IsEnabled



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 如果 COM + 應用程式或元件已停用，則 IsEnabled 為 False。 如果已啟用 COM + 應用程式或元件，IsEnabled 為 True。 |
| Access         | 讀寫                                                                                                                                 |
| 類型           | Bool                                                                                                                                      |
| 預設        | 是                                                                                                                                      |
| 最小系統 | Windows XP                                                                                                                                |



 

### <a name="issystem"></a>IsSystem



| 進入 | 值 |
|----------------|--------------------------------------|
| 描述    | 識別 COM + 系統應用程式。 |
| Access         | ReadOnly                             |
| 類型           | Bool                                 |
| 預設        | 否                                |
| 最小系統 | Windows 2000                         |



 

### <a name="maxdumpcount"></a>MaxDumpCount



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------|
| 描述    | 表示覆寫之前要產生的檔案數目上限。 |
| Access         | 讀寫                                                                        |
| 類型           | Long (1-200)                                                                      |
| 預設        | 5                                                                                |
| 最小系統 | Windows XP                                                                       |



 

### <a name="name"></a>名稱



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 應用程式的名稱。 移除字串開頭和結尾的額外空間。在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | 讀寫                                                                                                                                                                                                                            |
| 類型           | String                                                                                                                                                                                                                               |
| 預設值        | 「新增應用程式」                                                                                                                                                                                                                    |
| 最小系統 | Windows 2000                                                                                                                                                                                                                         |



 

> [!Note]  
> 應為應用程式選擇唯一的名稱。 如果使用相同的名稱建立多個應用程式，它可能會干擾依名稱參考應用程式，因而導致無法預期的行為。

 

### <a name="password"></a>密碼



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------|
| 描述    | 設定伺服器進程在身分識別下登入所使用的密碼。 |
| Access         | WriteOnly                                                                  |
| 類型           | String                                                                     |
| 預設值        | ""                                                                         |
| 最小系統 | Windows 2000                                                               |



 

在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼應該與身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。 如果密碼和身分識別不同步，則在系統管理員重設應用程式之前，無法啟動該應用程式。

### <a name="qcauthenticatemsgs"></a>QCAuthenticateMsgs



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出在哪些情況下，會對應用程式的佇列要求進行驗證。                                                 |
| Access         | 讀寫                                                                                                                               |
| 類型           | 很長可能的值： COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2)  |
| 預設        | COMAdminQCMessageAuthenticateSecureApps (0)                                                                                              |
| 最小系統 | Windows XP                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a>QCListenerMaxThreads



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出並行接聽程式執行緒的最大數目。 這個屬性的有效範圍是0到1000。 針對新建立的應用程式，此設定衍生自目前用來判斷接聽程式執行緒預設數目的演算法：伺服器中 Cpu 數目的16倍。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                 |
| 類型           | Long (0-1000)                                                                                                                                                                                                                                                                                              |
| 預設        | 0                                                                                                                                                                                                                                                                                                         |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> 您也可以從 [元件服務] 系統管理工具的 [ **佇列** ] 索引標籤，使用 [讀取/寫入] 功能來取得這個屬性。

 

### <a name="queuelistenerenabled"></a>QueueListenerEnabled



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出是否已針對應用程式啟用佇列元件接聽程式。 若已啟用，則會在應用程式啟動時啟動接聽程式。 只有當 QueuingEnabled 設定為 True 時，這個屬性才會生效。 |
| Access         | 讀寫                                                                                                                                                                                                            |
| 類型           | Bool                                                                                                                                                                                                                 |
| 預設        | 否                                                                                                                                                                                                                |
| 最小系統 | Windows 2000                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a>QueuingEnabled



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| 描述    | 指出是否為應用程式啟用 COM + 佇列元件服務。 |
| Access         | 讀寫                                                                            |
| 類型           | Bool                                                                                 |
| 預設        | 否                                                                                |
| 最小系統 | Windows 2000                                                                         |



 

### <a name="recycleactivationlimit"></a>RecycleActivationLimit



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出回收進程之前，應用程式中所要接受的已設定物件的最大啟用數目。 預設啟用數目為0。 |
| Access         | 讀寫                                                                                                                                                            |
| 類型           | Long (0-1048576)                                                                                                                                                      |
| 預設        | 0                                                                                                                                                                    |
| 最小系統 | Windows XP                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a>RecycleCallLimit



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 表示在回收進程之前，允許應用程式中已設定物件接受的呼叫數目上限。 預設的呼叫數目為0。 |
| Access         | 讀寫                                                                                                                                                      |
| 類型           | Long (0-1048576)                                                                                                                                                |
| 預設        | 0                                                                                                                                                              |
| 最小系統 | Windows XP                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a>RecycleExpirationTimeout



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 表示以分鐘為單位的時間 () ，讓回收的進程在關閉之前執行。 倒數計時會在進程回收之後立即開始。 到期時間上限為1440分鐘 (24 小時) ，預設值為15分鐘。 |
| Access         | 讀寫                                                                                                                                                                                                                                                        |
| 類型           | Long (1-1440)                                                                                                                                                                                                                                                     |
| 預設        | 15                                                                                                                                                                                                                                                               |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a>RecycleLifetimeLimit



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 表示在回收之前允許進程執行的最大分鐘數。 存留期上限為30240分鐘 (21 天) ，預設值為0分鐘。 |
| Access         | 讀寫                                                                                                                                                                   |
| 類型           | Long (0-30240)                                                                                                                                                               |
| 預設        | 0                                                                                                                                                                           |
| 最小系統 | Windows XP                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a>RecycleMemoryLimit



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出記憶體使用量的最大數量 (（以 kb 為單位），) 在回收之前允許進程。 如果進程記憶體使用量超過指定的時間長度超過一分鐘，則會回收進程。 記憶體使用量的預設數量為 0 KB。 |
| Access         | 讀寫                                                                                                                                                                                                                                                              |
| 類型           | Long (0-1048576)                                                                                                                                                                                                                                                        |
| 預設        | 0                                                                                                                                                                                                                                                                      |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a>複製



| 進入 | 值 |
|----------------|------------------------------------------------------|
| 描述    | 指出是否可以複寫應用程式。 |
| Access         | 讀寫                                            |
| 類型           | Bool                                                 |
| 預設        | 是                                                 |
| 最小系統 | Windows XP                                           |



 

### <a name="runforever"></a>RunForever



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 如果應用程式閒置，可讓伺服器進程繼續執行。 如果設定為 True，則當閒置時，不會關閉伺服器進程。 如果設定為 False，則會根據 ShutdownAfter 屬性所設定的值來關閉進程。 RunForever 未啟用程式庫 () 應用程式的程式庫。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                |
| 類型           | Bool                                                                                                                                                                                                                                                                                                     |
| 預設        | 否                                                                                                                                                                                                                                                                                                    |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a>ServiceName



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 對應至設定要執行為服務應用程式之應用程式的服務名稱。 如果這個值為 **Null**，則不會將應用程式設定為以服務方式執行。 否則，您可以使用服務名稱來尋找服務的設定資訊。 |
| Access         | ReadOnly                                                                                                                                                                                                                                                                         |
| 類型           | String                                                                                                                                                                                                                                                                           |
| 預設值        | ""                                                                                                                                                                                                                                                                               |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a>ShutdownAfter



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 設定在伺服器進程變成閒置之後，關閉該進程之前的延遲。 關機延遲的範圍是從0到1440分鐘 (24 小時) 。 如果 RunForever 設定為 True，則會忽略這個屬性。 ShutdownAfter 未啟用程式庫 () 應用程式的程式庫。 |
| Access         | 讀寫                                                                                                                                                                                                                                                          |
| 類型           | Long (0-1440)                                                                                                                                                                                                                                                       |
| 預設        | 3                                                                                                                                                                                                                                                                  |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a>SoapActivated



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| 描述    | 指出此應用程式是否會透過 SOAP 通訊協定公開以供取用。 |
| Access         | 讀寫                                                                            |
| 類型           | Bool                                                                                 |
| 預設        | 否                                                                                |
| 最小系統 | Windows Server 2003                                                                  |



 

### <a name="soapbaseurl"></a>SoapBaseUrl



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------|
| 描述    | 此應用程式透過 SOAP 通訊協定公開的 URL 端點。 |
| Access         | 讀寫                                                                    |
| 類型           | String                                                                       |
| 預設值        | ""                                                                           |
| 最小系統 | Windows Server 2003                                                          |



 

### <a name="soapmailto"></a>SoapMailTo



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------|
| 描述    | 此應用程式透過 SOAP 通訊協定公開的電子郵件地址。 |
| Access         | 讀寫                                                                     |
| 類型           | String                                                                        |
| 預設值        | ""                                                                            |
| 最小系統 | Windows Server 2003                                                           |



 

### <a name="soapvroot"></a>SoapVRoot



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| 描述    | IIS 虛擬根目錄，在此根目錄中會透過 SOAP 通訊協定來公開應用程式的存取腳本。 |
| Access         | 讀寫                                                                                                            |
| 類型           | String                                                                                                               |
| 預設值        | ""                                                                                                                   |
| 最小系統 | Windows Server 2003                                                                                                  |



 

### <a name="srpenabled"></a>SRPEnabled



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 判斷應用程式 (SRP) 的軟體限制原則。 如果設定為 True，則會使用應用程式的 SRPTrustLevel 屬性。 如果設定為 False，則會使用本機安全性設定中的軟體限制原則。 本機安全性設定是透過 Microsoft Management Console 的 [本機安全性原則] 嵌入式管理單元來控制。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                             |
| 類型           | Bool                                                                                                                                                                                                                                                                                                                                                                  |
| 預設        | 否                                                                                                                                                                                                                                                                                                                                                                 |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出軟體限制原則 (SRP) 應用程式信任層級。 只有當 SRPEnabled 屬性設定為 True 時，才會使用這個屬性。 SRP 信任層級是指您願意授與應用程式的信任層級。 不受限制的 SRP 信任層級會對應到更安全的 \_ LEVELID \_ FULLYTRUSTED 列舉值，而不允許的 srp 信任層級則對應到安全性不 \_ 允許的 LEVELID \_ 列舉值。 信任層級的列舉定義于 Winsafer 中。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 類型           | 較長的可能值：更安全的 \_ LEVELID 不 \_ 允許 (0X0) 更安全的 \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 預設        | 更安全的 \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

您願意信任但不受限制存取的應用程式應該附加最嚴格的安全性。 不受限制的應用程式只能載入未受限制的元件，而不允許的應用程式無法執行，因此無法載入任何元件。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
