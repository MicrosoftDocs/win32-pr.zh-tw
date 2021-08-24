---
title: Win32_TSSessionSetting 類別
description: 定義 Win32 終端機類別的設定 \_ ，例如時間限制以及中斷連線和重新連接動作。
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionSetting 類別遠端桌面服務
- Win32_TSSessionSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5139b53917f3d54b95fd153ac39fab176f047ba4bb9ec6df5d1c7c9b6e2d2f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769148"
---
# <a name="win32_tssessionsetting-class"></a>Win32 \_ TSSessionSetting 類別

**Win32 \_ TSSessionSetting** WMI 類別會定義 [**win32 \_ 終端**](win32-terminal.md)機類別的設定，例如時間限制以及中斷連線和重新連接動作。

下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。 如需方法的參考資訊，請參閱本主題稍後的方法表格。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a>成員

**Win32 \_ TSSessionSetting** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSSessionSetting** 類別具有這些方法。



| 方法                                                              | 描述                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**BrokenConnection**](win32-tssessionsetting-brokenconnection.md) | 設定包含在此類別中的中斷連接屬性。<br/> |
| [**TimeLimit**](win32-tssessionsetting-timelimit.md)               | 設定這個類別中包含的時間限制屬性。<br/>        |



 

### <a name="properties"></a>屬性

**Win32 \_ TSSessionSetting** 類別具有這些屬性。

<dl> <dt>

**ActiveSessionLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

配置給作用中會話的最大時間量（以毫秒為單位）。 值為0會指定無限的時間量。

</dd> <dt>

**BrokenConnectionAction**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當連線因為網路遺失或超過時間限制而中斷時，伺服器在會話上所採取的動作。

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**中斷** (0) 


</dt> <dd>

使用者已與會話中斷連線。

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (1) 


</dt> <dd>

從伺服器中永久刪除會話。

</dd> </dl>

</dd> <dt>

**BrokenConnectionPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

伺服器用來判斷何時中斷連線，因為網路遺失或超過時間限制的原則。

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**伺服器-覆寫** (1) 


</dt> <dd>

伺服器會覆寫使用者的中斷連接原則設定。

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (0) 


</dt> <dd>

使用者的中斷連線原則設定有效。

</dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

簡短描述 (物件的單行字串) 。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**DisconnectedSessionLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

中斷連線的會話終止的時間間隔（以毫秒為單位）。 值為0會指定無限的時間量。

</dd> <dt>

**EnableTimeoutWarning**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

啟用超時警告。

**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 無法使用這個屬性。

</dd> <dt>

**IdleSessionLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

閒置會話終止的時間間隔（以毫秒為單位）。 值為0會指定無限的時間量。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") 
</dt> </dl>

物件的安裝日期。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的名稱。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**PolicySourceActiveSessionLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **ActiveSessionLimit** 屬性是由伺服器、群組原則或預設設定。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> <dt>

2
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceBrokenConnectionAction**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **BrokenConnectionAction** 屬性是由伺服器、群組原則或預設設定。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> <dt>

2
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceDisconnectedSessionLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **DisconnectedSessionLimit** 屬性是由伺服器、群組原則或預設設定。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> <dt>

2
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceIdleSessionLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **IdleSessionLimit** 屬性是由伺服器、群組原則或預設設定。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> <dt>

2
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**PolicySourceReconnectionPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **ReconnectPolicy** 屬性是由伺服器、群組原則或預設設定。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則

</dd> <dt>

2
</dt> <dd>

預設

</dd> </dl>

</dd> <dt>

**ReconnectionPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定使用者是否必須使用先前的用戶端重新連線至已中斷連線的會話。

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**任何用戶端** (0) 


</dt> <dd>

任何用戶端都將用來重新連接。

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**先前的用戶端** (1) 


</dt> <dd>

連接中使用的先前用戶端會用來重新連接。

</dd> </dl>

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

<dt>



  ( [確定] ) 


</dt> <dd></dd> <dt>



  ( 「錯誤」 ) 


</dt> <dd></dd> <dt>



  ( 「降級」 ) 


</dt> <dd></dd> <dt>



  ( 「未知」 ) 


</dt> <dd></dd> <dt>



  ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>



  ( 「開始」 ) 


</dt> <dd></dd> <dt>



  ( 「正在停止」 ) 


</dt> <dd></dd> <dt>



  ( "Service" ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

終端機的名稱。

這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。

</dd> <dt>

**TimeLimitPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

伺服器用來判斷使用者會話時間限制的原則。

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (0) 


</dt> <dd>

使用者的時間限制原則設定生效。

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**伺服器覆寫** (1) 


</dt> <dd>

伺服器會覆寫使用者的時間限制原則設定。

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

請注意，與主控台會話相關聯的 Winstations 無法存取此類別的方法和屬性。 如果嘗試將 "Console" 指定為 TerminalName 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。 如果視窗工作站嘗試呼叫此物件的方法，以新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，則也會傳回此錯誤碼。

若要連接到「根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway」命名空間，驗證層級必須包含封包隱私權。 針對 C/c + + 呼叫，這會是 **RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 隱私權** 的驗證層級。 針對 Visual Basic 和腳本呼叫，這會是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。 下列 Visual Basic 腳本撰寫版 (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dt>

[**CIM \_ 設定**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

