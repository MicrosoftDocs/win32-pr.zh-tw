---
description: 包含應用程式集合中每個未配置元件的物件。 未配置的元件無法利用 COM + 服務。 這些物件所公開的屬性會保存在元件層級所做的設定。
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: LegacyComponents 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0815c9124020ff08e7033f7d1f18f8d9c5b6736763d401a3564bbdd8c6ffdf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120398"
---
# <a name="legacycomponents-collection"></a>LegacyComponents 集合

包含應用程式集合中每個未配置元件的物件。 未配置的元件無法利用 COM + 服務。 這些物件所公開的屬性會保存在元件層級所做的設定。

此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，但不支援 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法。 若要安裝或匯入元件到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。

## <a name="members"></a>成員

**LegacyComponents** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**應用程式**](applications.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [Accesspermissions.list](#accesspermissions)
-   [ActivateAtStorage](#activateatstorage)
-   [AppID](#appid)
-   [AppName](#appname)
-   [AuthenticationLevel](#authenticationlevel)
-   [位元](#bitness)
-   [ClassName](#classname)
-   [CLSID](#clsid)
-   [DllSurrogate](#dllsurrogate)
-   [InprocHandler32](#inprochandler32)
-   [InprocServer32](#inprocserver32)
-   [IsEnabled](#isenabled)
-   [LaunchPermissions](#launchpermissions)
-   [LocalServer32](#localserver32)
-   [LocalService](#localservice)
-   [密碼](#password)
-   [ProgID](#progid)
-   [RemoteServer](#remoteserver)
-   [Runas.exe](#runas)
-   [ServiceParameter](#serviceparameter)
-   [SRPTrustLevel](#srptrustlevel)
-   [ThreadingModel](#threadingmodel)

### <a name="accesspermissions"></a>Accesspermissions.list



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------|
| 描述    | 指定允許或拒絕存取元件的使用者帳戶。 |
| Access         | 讀寫                                                                       |
| 類型           | String                                                                          |
| 預設值        | N/A                                                                             |
| 最小系統 | Windows XP                                                                      |



 

### <a name="activateatstorage"></a>ActivateAtStorage



| 進入 | 值 |
|----------------|------------------------------------------------------------------|
| 描述    | 指定是否要在資料儲存體電腦上執行伺服器。 |
| Access         | 讀寫                                                        |
| 類型           | 字串可能的值： "N" "Y"                                    |
| 預設        | "N"                                                              |
| 最小系統 | Windows XP                                                       |



 

### <a name="appid"></a>AppID



| 進入 | 值 |
|----------------|---------------------|
| 描述    | 應用程式識別碼。 |
| Access         | ReadOnly            |
| 類型           | String              |
| 預設值        | N/A                 |
| 最小系統 | Windows XP          |



 

### <a name="appname"></a>AppName



| 進入 | 值 |
|----------------|------------------------------|
| 描述    | 應用程式的名稱。 |
| Access         | ReadOnly                     |
| 類型           | String                       |
| 預設值        | N/A                          |
| 最小系統 | Windows XP                   |



 

### <a name="authenticationlevel"></a>AuthenticationLevel



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 設定呼叫的驗證層級，其值會對應至遠端程序呼叫， (RPC) 驗證設定。 選擇 COMAdminAuthenticationDefault 時，會使用 [**LocalComputer**](localcomputer.md) 集合內 DefaultAuthenticationLevel 屬性中的設定。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                             |
| 類型           | 長可能的值： COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                               |
| 預設        | COMAdminAuthenticationDefault (0)                                                                                                                                                                                                                                                                      |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> 建議您在列舉中使用常數，而不要使用數值。

 

### <a name="bitness"></a>位元



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 表示元件的二進位位數類型。 在使用64位 Windows 的系統上，這個屬性會區分64位元件與32位元件。 |
| Access         | ReadOnly                                                                                                                                                              |
| 類型           | 很長可能的值： COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                          |
| 預設        | N/A                                                                                                                                                                   |
| 最小系統 | Windows XP                                                                                                                                                            |



 

### <a name="classname"></a>ClassName



| 進入 | 值 |
|----------------|------------------------|
| 描述    | 類別的名稱。 |
| Access         | ReadOnly               |
| 類型           | String                 |
| 預設值        | N/A                    |
| 最小系統 | Windows XP             |



 

### <a name="clsid"></a>CLSID



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 元件的 GUID。 當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                                                  |
| 類型           | String                                                                                                                                                    |
| 預設值        | N/A                                                                                                                                                       |
| 最小系統 | Windows XP                                                                                                                                                |



 

### <a name="dllsurrogate"></a>DllSurrogate



| 進入 | 值 |
|----------------|------------------------------------------------------------|
| 描述    | 指定 surragate 伺服器應用程式的完整路徑。 |
| Access         | 讀寫                                                  |
| 類型           | String                                                     |
| 預設值        | N/A                                                        |
| 最小系統 | Windows XP                                                 |



 

### <a name="inprochandler32"></a>InprocHandler32



| 進入 | 值 |
|----------------|--------------------------------------------------------------------|
| 描述    | 指定32位同進程自訂處理常式 DLL 的完整路徑。 |
| Access         | 讀寫                                                          |
| 類型           | String                                                             |
| 預設值        | N/A                                                                |
| 最小系統 | Windows XP                                                         |



 

### <a name="inprocserver32"></a>InprocServer32



| 進入 | 值 |
|----------------|------------------------------------------------------------|
| 描述    | 指定32位同進程伺服器 DLL 的完整路徑。 |
| Access         | 讀寫                                                  |
| 類型           | String                                                     |
| 預設值        | N/A                                                        |
| 最小系統 | Windows XP                                                 |



 

### <a name="isenabled"></a>IsEnabled



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 如果 COM + 應用程式或元件已停用，則 IsEnabled 為 False。 如果已啟用 COM + 應用程式或元件，IsEnabled 為 True。 |
| Access         | 讀寫                                                                                                                                 |
| 類型           | Bool                                                                                                                                      |
| 預設        | 是                                                                                                                                      |
| 最小系統 | Windows XP                                                                                                                                |



 

### <a name="launchpermissions"></a>LaunchPermissions



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| 描述    | 指定允許或拒絕啟動此元件之許可權的使用者帳戶。 |
| Access         | 讀寫                                                                              |
| 類型           | String                                                                                 |
| 預設值        | N/A                                                                                    |
| 最小系統 | Windows XP                                                                             |



 

### <a name="localserver32"></a>LocalServer32



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指定32位本機伺服器應用程式的完整路徑。 若要協助保護系統安全性，請在路徑中使用加上引號的字串，以指出可執行檔尾和引數的開始位置。 例如，" \\ " C： \\ Program Files \\ Company files \\Application.exe\\ "param1 param2"。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                   |
| 類型           | String                                                                                                                                                                                                                                                                                      |
| 預設值        | N/A                                                                                                                                                                                                                                                                                         |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a>LocalService



| 進入 | 值 |
|----------------|-----------------------------------------------------|
| 描述    | 指定服務應用程式的完整路徑。 |
| Access         | 讀寫                                           |
| 類型           | String                                              |
| 預設值        | N/A                                                 |
| 最小系統 | Windows XP                                          |



 

### <a name="password"></a>密碼



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 設定伺服器進程在指定的 RunAs 身分識別下登入所使用的密碼。 在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼應該與 RunAs 身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。 如果密碼和身分識別不同步，則必須等到系統管理員重設元件之後，才能啟動該元件。 |
| Access         | WriteOnly                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 類型           | String                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 預設值        | NULL                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a>ProgID



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 識別元件的名稱。 在這個集合的物件上呼叫 Name 屬性方法時，就會傳回這個屬性。 |
| Access         | ReadOnly                                                                                                                             |
| 類型           | String                                                                                                                               |
| 預設值        | N/A                                                                                                                                  |
| 最小系統 | Windows XP                                                                                                                           |



 

### <a name="remoteserver"></a>RemoteServer



| 進入 | 值 |
|----------------|---------------------------------------|
| 描述    | 指定遠端伺服器電腦。 |
| Access         | 讀寫                             |
| 類型           | String                                |
| 預設值        | N/A                                   |
| 最小系統 | Windows XP                            |



 

### <a name="runas"></a>RunAs



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指定要在其上執行元件之身分識別的使用者。 在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼應該與 RunAs 身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。 如果密碼和身分識別不同步，則必須等到系統管理員重設元件之後，才能啟動該元件。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                         |
| 類型           | String                                                                                                                                                                                                                                                                                                                                                                                            |
| 預設值        | N/A                                                                                                                                                                                                                                                                                                                                                                                               |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a>ServiceParameter



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------|
| 描述    | 指定當叫用為服務應用程式時，傳遞給應用程式的參數。 |
| Access         | 讀寫                                                                                 |
| 類型           | String                                                                                    |
| 預設值        | N/A                                                                                       |
| 最小系統 | Windows XP                                                                                |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出元件 (SRP) 信任層級的軟體限制原則。 SRP 信任層級是指您願意提供給元件的信任層級。 不受限制的 SRP 信任層級會對應到更安全的 \_ LEVELID \_ FULLYTRUSTED 列舉值，而不允許的 srp 信任層級則對應到安全性不 \_ 允許的 LEVELID \_ 列舉值。 信任層級的列舉定義于 Winsafer 中。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 類型           | 較長的可能值：更安全的 \_ LEVELID 不 \_ 允許 (0X0) 更安全的 \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                          |
| 預設        | 更安全的 \_ LEVELID \_ FULLYTRUSTED                                                                                                                                                                                                                                                                                                                                                                                                        |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

您願意信任但不受限制存取的元件應該附加最嚴格的安全性。 不受限制的應用程式只能載入未受限制的元件，而不允許的應用程式無法執行，因此無法載入任何元件。

### <a name="threadingmodel"></a>ThreadingModel



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 決定如何將元件的實例指派給方法執行的執行緒。 值會對應至 COM 執行緒模型。                                                  |
| Access         | ReadOnly                                                                                                                                                                            |
| 類型           | 長可能的值： COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4)  |
| 預設        | N/A                                                                                                                                                                                 |
| 最小系統 | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
