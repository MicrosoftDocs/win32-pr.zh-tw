---
description: Win32 \_ TCPIPPrinterPort&\# 32;WMI 類別代表 TCP/IP 服務存取點。
ms.assetid: b1be18b6-47de-461c-a90b-c7e0537130ef
ms.tgt_platform: multiple
title: Win32_TCPIPPrinterPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TCPIPPrinterPort
- Win32_TCPIPPrinterPort.Caption
- Win32_TCPIPPrinterPort.Description
- Win32_TCPIPPrinterPort.InstallDate
- Win32_TCPIPPrinterPort.Status
- Win32_TCPIPPrinterPort.CreationClassName
- Win32_TCPIPPrinterPort.Name
- Win32_TCPIPPrinterPort.SystemCreationClassName
- Win32_TCPIPPrinterPort.SystemName
- Win32_TCPIPPrinterPort.Type
- Win32_TCPIPPrinterPort.ByteCount
- Win32_TCPIPPrinterPort.HostAddress
- Win32_TCPIPPrinterPort.PortNumber
- Win32_TCPIPPrinterPort.Protocol
- Win32_TCPIPPrinterPort.Queue
- Win32_TCPIPPrinterPort.SNMPCommunity
- Win32_TCPIPPrinterPort.SNMPDevIndex
- Win32_TCPIPPrinterPort.SNMPEnabled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a0b0f0cb73cc60ff117399a636b0ab8542fac6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972347"
---
# <a name="win32_tcpipprinterport-class"></a>Win32 \_ TCPIPPrinterPort 類別

**Win32 \_ TCPIPPrinterPort** [WMI 類別](../wmisdk/retrieving-a-class.md)代表 tcp/ip 服務存取點。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class Win32_TCPIPPrinterPort : CIM_ServiceAccessPoint
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
  boolean  ByteCount;
  string   HostAddress;
  uint32   PortNumber;
  uint32   Protocol;
  string   Queue;
  string   SNMPCommunity;
  uint32   SNMPDevIndex;
  boolean  SNMPEnabled;
};
```

## <a name="members"></a>成員

**Win32 \_ TCPIPPrinterPort** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TCPIPPrinterPort** 類別具有這些屬性。

<dl> <dt>

**ByteCount**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則電腦會先計算檔中的位元組數，然後再將其傳送至印表機，而印表機則會回報實際讀取的位元組數目。 當列印輸出中偵測到遺漏的位元組時，就會使用這項功能進行診斷。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**HostAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置或列印伺服器的位址。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

可唯一識別服務存取點，並提供所管理功能的指示。 此功能在物件的 Description 屬性中有更詳細的說明。

這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

埠監視器用來與裝置通訊的 TCP 埠數目。

</dd> <dt>

**通訊協定**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

使用的列印通訊協定。 某些印表機只支援 LPR。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

RAW

直接列印到裝置或列印伺服器。

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

Lpr

舊版通訊協定，最終會以 RAW 取代。

</dd> </dl>

</dd> <dt>

**佇列**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與 LPR 通訊協定搭配使用時，伺服器上的列印佇列名稱。

</dd> <dt>

**SNMPCommunity**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的安全性層級值。

範例：「公用」

</dd> <dt>

**SNMPDevIndex**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此裝置的 snmp 索引號碼，適用于 SNMP 代理程式。

</dd> <dt>

**SNMPEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則此印表機支援 [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (簡易的網路管理通訊協定) ，而且可以從裝置提供豐富的狀態資訊。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
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

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

範圍系統的建立類別名稱。

這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

範圍系統的名稱。

這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。

</dd> <dt>

**型別**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) 
</dt> </dl>

SAP 的類型，例如 [已連接] 或 [已重新導向]。

這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)。

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**寫入** (1) 


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**閱讀** (2) 


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

重新 **導向** (4) 


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

**Net \_附加** (8) 


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (16) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ TCPIPPrinterPort** 類別衍生自 cim [**\_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ，它衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。

需要有 **SeLoadDriverPrivilege** 許可權，才能刪除這個 WMI 類別的實例。 下列腳本程式碼片段示範如何建立使用此許可權的 WMI 連接。

`Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate, (LoadDriver)}")`

## <a name="examples"></a>範例

下列 PowerShell 範例會移除印表機和相關聯的 TCPIP 印表機埠。


```PowerShell
function Remove-PrinterAndPort{
    Param( $printername )
   $printer=gwmi win32_Printer -filter "name='HPDJ600'"
   $printer.Delete()
   $port=gwmi win32_tcpipprinterport -filter "name='$($printer.portname)'" -enableall
   $port.Delete()
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ 印表機。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
