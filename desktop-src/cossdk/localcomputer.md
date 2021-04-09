---
description: 包含單一物件，該物件對應至您要存取其目錄的電腦。 此物件會保存電腦層級的設定資訊。
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: LocalComputer 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689176"
---
# <a name="localcomputer-collection"></a>LocalComputer 集合

包含單一物件，該物件對應至您要存取其目錄的電腦。 此物件會保存電腦層級的設定資訊。 如果您在從 [**COMAdminCatalog**](comadmincatalog.md)類別建立的物件上呼叫 [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect)方法， **LocalComputer** 集合中的物件將會包含您要存取其目錄之遠端電腦的相關資訊。

此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。

## <a name="members"></a>成員

**LocalComputer** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="related-collections"></a>相關集合

您可以從這個集合流覽至下列任何集合：

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

您可以從下列集合流覽至這個集合：

-   [**根**](root.md)

## <a name="properties"></a>屬性

集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：

-   [ApplicationProxyRSN](#applicationproxyrsn)
-   [CISEnabled](#cisenabled)
-   [DCOMEnabled](#dcomenabled)
-   [DefaultAuthenticationLevel](#defaultauthenticationlevel)
-   [DefaultImpersonationLevel](#defaultimpersonationlevel)
-   [DefaultToInternetPorts](#defaulttointernetports)
-   [說明](#description)
-   [DSPartitionLookupEnabled](#dspartitionlookupenabled)
-   [InternetPortsListed](#internetportslisted)
-   [IsRouter](#isrouter)
-   [LoadBalancingCLSID](#loadbalancingclsid)
-   [LocalPartitionLookupEnabled](#localpartitionlookupenabled)
-   [名稱](#name)
-   [OperatingSystem](#operatingsystem)
-   [PartitionsEnabled](#partitionsenabled)
-   [連接埠](#defaulttointernetports)
-   [ResourcePoolingEnabled](#resourcepoolingenabled)
-   [RPCProxyEnabled](#rpcproxyenabled)
-   [SecureReferencesEnabled](#securereferencesenabled)
-   [SecurityTrackingEnabled](#securitytrackingenabled)
-   [SRPActivateAsActivatorChecks](#srpactivateasactivatorchecks)
-   [SRPRunningObjectChecks](#srprunningobjectchecks)
-   [TransactionTimeout](#transactiontimeout)

### <a name="applicationproxyrsn"></a>ApplicationProxyRSN



| 進入 | 值 |
|----------------|------------------------------------------------------------|
| 描述    | 依預設，應用程式 proxy 所使用的遠端伺服器名稱。 |
| Access         | 讀寫                                                  |
| 類型           | String                                                     |
| 預設值        | ""                                                         |
| 最小系統 | Windows 2000                                               |



 

### <a name="cisenabled"></a>CISEnabled



| 進入 | 值 |
|----------------|-----------------------------------------------------|
| 描述    | 指出是否啟用 COM 網際網路服務。 |
| Access         | 讀寫                                           |
| 類型           | Bool                                                |
| 預設        | 否                                               |
| 最小系統 | Windows 2000                                        |



 

### <a name="dcomenabled"></a>DCOMEnabled



| 進入 | 值 |
|----------------|---------------------------------------------|
| 描述    | 設定為 True 可在電腦上啟用 DCOM。 |
| Access         | 讀寫                                   |
| 類型           | Bool                                        |
| 預設        | 對                                        |
| 最小系統 | Windows 2000                                |



 

### <a name="defaultauthenticationlevel"></a>DefaultAuthenticationLevel



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 將驗證設定為預設的應用程式所使用的驗證層級。 值會對應至遠端程序呼叫， (RPC) 驗證設定。                                                                                         |
| Access         | 讀寫                                                                                                                                                                                                                                                |
| 類型           | 長可能的值： COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)  |
| 預設        | COMAdminAuthenticationConnect (2)                                                                                                                                                                                                                         |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                             |



 

> [!Note]  
> 當 COM 呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時，COMAdminAuthenticationDefault 會對應至 COMAdminAuthenticationConnect。 建議您在列舉中使用常數，而不要使用數值。

 

### <a name="defaultimpersonationlevel"></a>DefaultImpersonationLevel



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 如果未設定，則為允許的模擬層級。                                                                                                               |
| Access         | 讀寫                                                                                                                                                     |
| 類型           | 長可能的值： COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)  |
| 預設        | COMAdminImpersonationIdentify (2)                                                                                                                              |
| 最小系統 | Windows 2000                                                                                                                                                  |



 

> [!Note]  
> 建議您在列舉中使用常數，而不是數值。

 

### <a name="defaulttointernetports"></a>DefaultToInternetPorts



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------|
| 描述    | 判斷提供的埠預設類型是否應該是 Internet (True) 或內部網路 (False) 。 |
| Access         | 讀寫                                                                                           |
| 類型           | Bool                                                                                                |
| 預設        | 否                                                                                               |
| 最小系統 | Windows 2000                                                                                        |



 

### <a name="description"></a>Description



| 進入 | 值 |
|----------------|--------------------------------|
| 描述    | 電腦的描述。 |
| Access         | 讀寫                      |
| 類型           | String                         |
| 預設值        | ""                             |
| 最小系統 | Windows 2000                   |



 

### <a name="dspartitionlookupenabled"></a>DSPartitionLookupEnabled



| 進入 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| 描述    | 指出是否將分割區對應的使用者簽入網域存放區。 |
| Access         | 讀寫                                                                              |
| 類型           | Bool                                                                                   |
| 預設        | 對                                                                                   |
| 最小系統 | Windows Server 2003                                                                    |



 

### <a name="internetportslisted"></a>InternetPortsListed



| 進入 | 值 |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| 描述    | 判斷 [埠] 屬性中所列的埠是否要用於網際網路 (True) 或內部網路 (False) 。 |
| Access         | 讀寫                                                                                                             |
| 類型           | Bool                                                                                                                  |
| 預設        | 否                                                                                                                 |
| 最小系統 | Windows 2000                                                                                                          |



 

### <a name="isrouter"></a>IsRouter



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 如果電腦是 (CLB) 服務的元件負載平衡的路由器，請設定為 True。 只有當元件負載平衡服務目前已安裝在電腦上時，才能將這個屬性設定為 True。否則，COMADMIN E 的錯誤 \_ \_ 需要 \_ 不同的 \_ 平臺。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                           |
| 類型           | Bool                                                                                                                                                                                                                                                                                |
| 預設        | 否                                                                                                                                                                                                                                                                               |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                        |



 

如果此屬性設定為 True，則會設定 CLB 伺服器，並在啟動時啟動。 如果伺服器尚未存在，便會將伺服器加入至 ApplicationCluster 集合。

### <a name="loadbalancingclsid"></a>LoadBalancingCLSID



| 進入 | 值 |
|----------------|-------------------------------------|
| 描述    | 要平衡的物件 CLSID。 |
| Access         | 讀寫                           |
| 類型           | String                              |
| 預設值        | NULL                                |
| 最小系統 | Windows XP                          |



 

### <a name="localpartitionlookupenabled"></a>LocalPartitionLookupEnabled



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| 描述    | 指出是否將分割區對應的使用者簽入本機存放區。 |
| Access         | 讀寫                                                                             |
| 類型           | Bool                                                                                  |
| 預設        | 對                                                                                  |
| 最小系統 | Windows Server 2003                                                                   |



 

### <a name="name"></a>Name



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 電腦的名稱。 移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。 |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| 類型           | String                                                                                                                                                                                                                                                                 |
| 預設值        | "我的電腦"                                                                                                                                                                                                                                                          |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a>OperatingSystem



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 安裝在本機電腦上的作業系統。                                                                                                                                                                                                                                                                                                                                                                                                |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 類型           | 可能的最大值： COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16)  |
| 預設        | COMAdminOSNotInitialized (0)                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a>PartitionsEnabled



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 指出是否可以在本機電腦上使用 COM + 分割。 如果這個屬性為 False，任何使用 COM + 分割的嘗試都會產生錯誤。 |
| Access         | 讀寫                                                                                                                                               |
| 類型           | Bool                                                                                                                                                    |
| 預設        | 否                                                                                                                                                   |
| 最小系統 | Windows Server 2003                                                                                                                                     |



 

### <a name="ports"></a>連接埠



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 字串，描述針對網際網路或內部網路使用的埠，視 InternetPortsListed 屬性而定;例如 "500-599: 600-800"。 |
| Access         | 讀寫                                                                                                                                               |
| 類型           | String                                                                                                                                                  |
| 預設值        | ""                                                                                                                                                      |
| 最小系統 | Windows 2000                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a>ResourcePoolingEnabled



| 進入 | 值 |
|----------------|-------------------------------------|
| 描述    | 可使用資源機。 |
| Access         | 讀寫                           |
| 類型           | Bool                                |
| 預設        | 對                                |
| 最小系統 | Windows 2000                        |



 

### <a name="rpcproxyenabled"></a>RPCProxyEnabled



| 進入 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 控制是否啟用 RPC IIS proxy。 RPC IIS proxy 是與 IIS 搭配使用，以便從 IIS 轉寄對 RPC 機制的呼叫，並且是 COM 網際網路服務的其中一個核心，也就是藉由將 CISEnabled 設定為 True 來啟用。 如需 RPCProxyEnabled 的詳細資訊，請參閱 [HTTP RPC 安全性](/windows/desktop/Rpc/rpc-over-http-security)。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                             |
| 類型           | Bool                                                                                                                                                                                                                                                                                                                                                  |
| 預設        | 否                                                                                                                                                                                                                                                                                                                                                 |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a>SecureReferencesEnabled



| 進入 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 在 DCOM 電腦中強制 [**執行對 IUnknown：： AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 和 [**Iunknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法的跨進程呼叫會受到保護。 |
| Access         | 讀寫                                                                                                                                                                 |
| 類型           | Bool                                                                                                                                                                      |
| 預設        | 否                                                                                                                                                                     |
| 最小系統 | Windows 2000                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a>SecurityTrackingEnabled



| 進入 | 值 |
|----------------|---------------------------------------------------------|
| 描述    | 如果在物件上啟用安全性追蹤，則設定為 True。 |
| Access         | 讀寫                                               |
| 類型           | Bool                                                    |
| 預設        | 對                                                    |
| 最小系統 | Windows 2000                                            |



 

### <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 決定軟體限制原則 (SRP) 如何處理啟動為啟動的連接。 如果設定為 True，則會將為伺服器物件設定的 SRP 信任層級與用戶端物件的 SRP 信任層級進行比較，並使用較高 (更嚴格的) 信任層級來執行伺服器物件。 如果設定為 False，則不論伺服器設定所在的 SRP 信任層級為何，伺服器物件都會以用戶端物件的 SRP 信任層級執行。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 類型           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 預設        | 對                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks



| 進入 | 值 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 判斷軟體限制原則 (SRP) 如何處理與現有進程的已嘗試連接。 如果設定為 False，則不會檢查是否有適當的 SRP 信任層級來連接至執行中的物件。 如果設定為 True，則執行中的物件必須有相等或更高的 (比用戶端物件更嚴格的) SRP 信任層級。 例如，具有不受限制之 SRP 信任層級的用戶端物件，無法連接到具有不允許之 SRP 信任層級的執行中物件。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 類型           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 預設        | 對                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 最小系統 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a>TransactionTimeout



| 進入 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述    | 如果您要在交易內執行許多作業，則應該設定為足夠的值（以秒為單位）。 預設的超時期限為60秒，而最大超時期限為3600秒 (1 小時) 。 將這個屬性設定為0會停用交易超時。 您可以使用 [**元件**](components.md) 集合的 ComponentTransactionTimeout 屬性，以個別元件覆寫這個屬性。 |
| Access         | 讀寫                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 類型           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 預設        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 最小系統 | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a>範例

下列 Microsoft Visual Basic 範例示範如何連接到遠端電腦，並使用遠端電腦的 **LocalComputer** 集合來取得其 SecurityTrackingEnabled 屬性。 若要使用此範例，請新增 COM + 系統管理員類型程式庫做為您 Visual Basic 專案的參考。


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



若要使用函數，請提供遠端電腦名稱稱的字串值。 下列 Visual Basic 程式碼示範如何連接到名為 "RemoteComputerName" 的電腦。


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM + 系統管理集合](com--administration-collections.md)
</dt> </dl>

 

 
