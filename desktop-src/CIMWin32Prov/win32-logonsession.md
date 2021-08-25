---
description: 描述與登入執行 Windows 之電腦系統的使用者相關聯的登入會話或會話。
ms.assetid: d09a115b-95a3-47c7-a04d-c810d044ccc8
ms.tgt_platform: multiple
title: Win32_LogonSession 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSession
- Win32_LogonSession.Caption
- Win32_LogonSession.Description
- Win32_LogonSession.InstallDate
- Win32_LogonSession.Name
- Win32_LogonSession.Status
- Win32_LogonSession.StartTime
- Win32_LogonSession.AuthenticationPackage
- Win32_LogonSession.LogonId
- Win32_LogonSession.LogonType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 85cbc80050fafe887fa99974c41666c7189b2b12c21559aac0255870b2a697d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972979"
---
# <a name="win32_logonsession-class"></a>Win32 \_ LogonSession 類別

**Win32 \_ LogonSession** wmi 類別 (請參閱) 說明如何抓取 [wmi 類別](/windows/desktop/wmisdk/retrieving-a-class)，以描述與登入執行 Windows 之電腦系統的使用者相關聯的登入會話或會話。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{9083C21E-7D58-4e0e-BC30-0BC8922AFB8B}"), AMENDMENT]
class Win32_LogonSession : Win32_Session
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
  string   AuthenticationPackage;
  string   LogonId;
  uint32   LogonType;
};
```

## <a name="members"></a>成員

**Win32 \_ LogonSession** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ LogonSession** 類別具有這些屬性。

<dl> <dt>

**AuthenticationPackage**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來驗證登入會話的子系統名稱。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) 
</dt> </dl>

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**LogonId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

指派給登入會話的識別碼。

</dd> <dt>

**LogonType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出登入會話類型的數值。

<dt>

0
</dt> <dd>

只能由系統帳戶使用。

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**互動式** (2) 


</dt> <dd>

適用于以互動方式使用電腦的使用者，例如由終端機伺服器登入的使用者、遠端 shell 或類似的進程。

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Network** (3) 


</dt> <dd>

適用于可驗證純文字密碼的高效能伺服器。 LogonUser 不會快取此登入類型的認證。

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4) 


</dt> <dd>

適用于批次伺服器，在此情況下可以代表使用者執行處理常式，而不需直接介入;或適用于一次處理許多純文字驗證嘗試的較高效能伺服器，例如郵件或網頁伺服器。 LogonUser 不會快取此登入類型的認證。

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**服務** (5) 


</dt> <dd>

表示服務類型登入。 提供的帳戶必須啟用服務許可權。

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6) 


</dt> <dd>

表示 proxy 型別登入。

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span> (7) **解除鎖定**


</dt> <dd>

這種登入類型適用于以互動方式使用電腦之使用者的 GINA Dll 記錄。 此登入類型允許產生唯一的審核記錄，以顯示工作站解除鎖定的時間。

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8) 


</dt> <dd>

會保留驗證套件中的名稱和密碼，讓伺服器可以在模擬用戶端時，連接到其他網路伺服器。 這可讓伺服器接受來自用戶端的純文字認證、呼叫 LogonUser、驗證使用者是否可透過網路存取系統，並仍與其他伺服器通訊。

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9) 


</dt> <dd>

允許呼叫者複製其目前的權杖，並指定輸出連接的新認證。 新的登入會話具有相同的本機識別，但是針對其他網路連線使用不同的認證。

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10) 


</dt> <dd>

同時為遠端和互動式的終端機服務會話。

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11) 


</dt> <dd>

嘗試快取的認證，而不需要存取網路。

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12) 


</dt> <dd>

與 RemoteInteractive 相同。 這可用於內部審核。

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13) 


</dt> <dd>

工作站登入。

</dd> </dl>

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 
</dt> </dl>

已知物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

會話開始的時間。

這個屬性繼承自 [**Win32 \_ 會話**](win32-session.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

表示物件目前狀態的字串。 您可以定義操作和非運作狀態。 操作狀態可以包含「確定」、「降級」和「Pred 失敗」。 「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。

非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。 「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="examples"></a>範例

[清單登入會話資訊](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3)PowerShell 範例會傳回與目前登入電腦的使用者相關聯之登入會話的相關資訊。

下列 PowerShell 範例會檢查是否有指定使用者的遠端會話開啟。


```PowerShell
$user = "<user name>"
$servers = gci servers.txt 

     foreach ($server in $servers){
     $logons = gwmi win32_loggedonuser -computername $server

          foreach ($logon in $logons){
               if ($logon.antecedent -match $user){
               $logonid = $logon.dependent.split("=")[1] 
               $session =gwmi win32_logonsession |? {$_.logonid -match $logonid}
               if ($session.logontype -eq "10"){
               Write-host "You have an active Terminal Server session on server $($server)"
                }
          }
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 會話**](win32-session.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

