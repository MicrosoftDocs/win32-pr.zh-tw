---
title: Win32_TSSessionDirectory 類別
description: 定義 Win32 TSSessionDirectorySetting 類別的遠端桌面連線代理人 (RD 連線代理人) 設定 \_ 。
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectory 類別遠端桌面服務
- Win32_TSSessionDirectory 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934228"
---
# <a name="win32_tssessiondirectory-class"></a>Win32 \_ TSSessionDirectory 類別

定義 [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) 類別的遠端桌面連線代理人 (RD 連線代理人) 設定。

> [!Note]  
> 在 Windows Server 2008 R2 中，終端機服務會話代理人 (TS 會話代理人) 的名稱已變更為 RD 連線代理人。 除非另有說明，否則這些屬性適用于所有支援的作業系統。

 

下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。 如需方法的參考資訊，請參閱本主題稍後的方法表格。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a>成員

**Win32 \_ TSSessionDirectory** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSSessionDirectory** 類別具有這些方法。



| 方法                                                                                                  | 描述                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [**CreateUserDiskTemplate**](createuserdisktemplate-win32-tssessiondirectory.md)                       | 建立使用者磁片範本。<br/>                                                                     |
| [**DisableUserVhd**](disableuservhd-win32-tssessiondirectory.md)                                       | 停用使用者設定檔 VHD。<br/>                                                                      |
| [**EnableUserVhd**](enableuservhd-win32-tssessiondirectory.md)                                         | 在 RDSH 伺服器上啟用使用者設定檔 VHD。<br/>                                                     |
| [**GetCurrentRedirectableAddresses**](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | 取得目前設定的 DNS 合格地址清單和重新導向類型。<br/>        |
| [**GetRedirectableAddresses**](getredirectableaddresses-win32-tssessiondirectory.md)                   | 取得 DNS 合格位址的完整清單。<br/>                                                |
| [**PingSessionDirectory**](pingsessiondirectory-win32-tssessiondirectory.md)                           | 檢查 RD 連線代理人伺服器是否可供使用。<br/>                                      |
| [**SetCurrentRedirectableAddresses**](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | 設定 DNS 合格位址和重新導向類型的已設定清單。<br/>                     |
| [**SetLoadBalancingState**](setloadbalancingstate-win32-tssessiondirectory.md)                         | 設定值，指出伺服器是否將參與 RD 連線代理人負載平衡。<br/> |
| [**SetServerWeight**](setserverweight-win32-tssessiondirectory.md)                                     | 設定 RD 連線代理人負載平衡的伺服器加權值。<br/>                             |
| [**SetSessionDirectoryActive**](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | 停用並啟用 RD 連線代理人。<br/>                                                    |
| [**SetSessionDirectoryExposeServerIP**](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | 設定 **SessionDirectoryExposeServerIP** 屬性。<br/>                                             |
| [**SetSessionDirectoryProperty**](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | 設定 **SessionDirectoryLocation** 屬性或 **SessionDirectoryClusterName** 屬性。<br/>   |
| [**SetTSRedirectorMode**](settsredirectormode-win32-tssessiondirectory.md)                             | 這個方法無法使用。<br/>                                                                     |



 

### <a name="properties"></a>屬性

**Win32 \_ TSSessionDirectory** 類別具有這些屬性。

<dl> <dt>

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

**GetLoadBalancingState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出伺服器是否設定為參與 RD 連線代理人負載平衡。

<dt>

0
</dt> <dd>

伺服器未設定為參與 RD 連線代理人負載平衡。

</dd> <dt>

1
</dt> <dd>

伺服器設定為參與 RD 連線代理人負載平衡。

</dd> </dl>

</dd> <dt>

**GetServerWeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

抓取 RD 連線代理人負載平衡中使用的伺服器加權值。

</dd> <dt>

**GetTSRedirectorMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出伺服器是否已設定為做為遠端桌面服務的重新導向程式。

<dt>

0
</dt> <dd>

伺服器設定為作為遠端桌面服務的重新導向器。

</dd> <dt>

1
</dt> <dd>

伺服器未設定為做為遠端桌面服務的重新導向器。

</dd> </dl>

**Windows Server 2008：** 無法使用這個屬性。

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

**PolicySourceLoadBalancing**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **GetLoadBalancingState** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryActive**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **SessionDirectoryActive** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryClusterName**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **SessionDirectoryClusterName** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryExposeServerIP**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **SessionDirectoryExposeServerIP** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceSessionDirectoryLocation**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **SessionDirectoryLocation** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceTSRedirectorMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

無法使用這個屬性。

**Windows Server 2008 R2：** 指出 **GetTSRedirectorMode** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**SessionDirectoryActive**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

指定遠端桌面服務是否參與 RD 連線代理人。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

RD 連線代理人中的遠端桌面服務參與已停用。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

已啟用遠端桌面服務參與 RD 連線代理人。

</dd> </dl>

</dd> <dt>

**SessionDirectoryClusterName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD 工作階段主機伺服器所屬叢集的虛擬 IP 位址。

</dd> <dt>

**SessionDirectoryExposeServerIP**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否允許抓取 RD 連線代理人的 IP 位址。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

已拒絕抓取。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

允許抓取。

</dd> </dl>

</dd> <dt>

**SessionDirectoryIPAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

會話目錄所使用之 LAN 介面卡的 IP 位址。

</dd> <dt>

**SessionDirectoryLocation**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD 連線代理人服務執行所在之伺服器的網路 DNS 名稱或 IP 位址。

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

</dd> </dl>

## <a name="remarks"></a>備註

若要連接到 \\ \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。 針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。 針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為六。

下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



在 Windows Server 2008 中，終端機服務會話目錄功能的名稱已變更為終端機服務會話代理程式。

在 Windows Server 2008 R2 中，終端機服務會話代理人功能的名稱已變更為遠端桌面連線代理人。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

