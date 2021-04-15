---
description: Win32 \_ NetworkProtocol&\# 8194;WMI 類別代表 Win32 電腦系統上的通訊協定和其網路特性。
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Win32_NetworkProtocol 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468481"
---
# <a name="win32_networkprotocol-class"></a>Win32 \_ NetworkProtocol 類別

**Win32 \_ NetworkProtocol** [WMI 類別](../wmisdk/retrieving-a-class.md)代表 win32 電腦系統上的通訊協定和其網路特性。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a>成員

**Win32 \_ NetworkProtocol** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ NetworkProtocol** 類別具有這些屬性。

<dl> <dt>

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

**ConnectionlessService**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP1 \_ 無連接」 ) 
</dt> </dl>

通訊協定支援不需連線的服務。 不需連線的 (資料包) 服務會描述通訊協定或傳輸，其中的資料封包會彼此獨立地路由傳送，而且可能會遵循不同的路由，並以與其傳送的不同順序送達。 相反地，連接導向的服務會提供虛擬電路，資料封包會以傳輸的相同順序接收。 如果電腦之間的連接失敗，就會通知應用程式。

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

**GuaranteesDelivery**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 保證 \_ 傳遞」 ) 
</dt> </dl>

通訊協定支援傳遞資料封包。 如果此旗標為 **FALSE**，則不確定傳送的所有資料都會到達預期的目的地。

</dd> <dt>

**GuaranteesSequencing**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 保證 \_ 順序」 ) 
</dt> </dl>

通訊協定可確保資料會依照傳送的順序抵達。 請注意，這個特性不會確保資料的傳遞，而只是其順序。

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

**MaximumAddressSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| iMaxSockAddr」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「字元」 ) 
</dt> </dl>

通訊協定支援的通訊端位址最大長度。 通訊端位址可以是 () 的 URL， `www.microsoft.com` 或 () 的 IP 位址等專案 `130.215.24.1` 。

</dd> <dt>

**MaximumMessageSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwMessageSize」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「字元」 ) 
</dt> </dl>

通訊協定支援的訊息大小上限。 這是可由主機傳送或接收之訊息的大小上限。 對於不支援訊息框架的通訊協定，可傳送至指定位址之訊息的實際大小上限可能會小於此值。

</dd> <dt>

**MessageOriented**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 訊息 \_ 導向」 ) 
</dt> </dl>

通訊協定為訊息導向。 訊息導向的通訊協定會使用資料的封包來傳輸資訊。 相反地，資料流程導向的通訊協定會以連續的位元組資料流程來傳送資料。

</dd> <dt>

**MinimumAddressSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| iMinSockAddr」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「字元」 ) 
</dt> </dl>

通訊協定所支援之通訊端位址的最小長度。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Name" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| lpProtocol" ) 
</dt> </dl>

通訊協定的名稱。

範例： "TCP/IP"

</dd> <dt>

**PseudoStreamOriented**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 虛擬 \_ 資料流程」 ) 
</dt> </dl>

通訊協定是一種訊息導向的通訊協定，可接收所有接收作業的可變長度資料封包或資料流程處理資料。 當應用程式不希望通訊協定框架訊息，而且需要資料流程導向特性時，此選擇性功能就很有用。 若 **為 TRUE**，表示通訊協定為虛擬資料流程導向。

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

**SupportsBroadcasting**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 支援 \_ 廣播」 ) 
</dt> </dl>

通訊協定支援在網路上廣播訊息的機制。

</dd> <dt>

**SupportsConnectData**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ CONNECT \_ 資料」 ) 
</dt> </dl>

通訊協定可讓資料透過網路連接。

</dd> <dt>

**SupportsDisconnectData**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 中斷連接 \_ 資料」 ) 
</dt> </dl>

通訊協定可讓網路上的資料中斷連線。

</dd> <dt>

**SupportsEncryption**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 加密」 ) 
</dt> </dl>

通訊協定支援資料加密。

</dd> <dt>

**SupportsExpeditedData**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 快速 \_ 資料」 ) 
</dt> </dl>

通訊協定支援快速資料 (也稱為網路上) 的緊急資料。 加急資料可以略過流量控制，並優先于一般資料封包。

</dd> <dt>

**SupportsFragmentation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 片段」 ) 
</dt> </dl>

通訊協定支援以片段傳輸資料。 實體網路最大傳輸單位 (MTU) 會從應用程式隱藏。 每個媒體類型都有無法超過的框架大小上限。 連結層會探索 MTU，並將其報告為使用的通訊協定。

</dd> <dt>

**SupportsGracefulClosing**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 正常 \_ 關閉」 ) 
</dt> </dl>

通訊協定支援兩階段關閉作業，也稱為「正常關閉作業」。 如果沒有，通訊協定只支援 abortive 關閉作業。

</dd> <dt>

**SupportsGuaranteedBandwidth**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 頻寬 \_ 配置」 ) 
</dt> </dl>

通訊協定具有建立和維護頻寬的機制。

</dd> <dt>

**SupportsMulticasting**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| 通訊協定 \_ 資訊 \| dwServiceFlags \| XP \_ 支援 \_ 多播」 ) 
</dt> </dl>

通訊協定支援多播。

</dd> <dt>

**SupportsQualityofService**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| Windows 通訊端結構 \| WSAPROTOCOL \_ 資訊 \| dwServiceFlags1 \| XP1 \_ QOS 支援」 \_ ) 
</dt> </dl>

通訊協定可以支援服務品質 (QoS) 由基礎分層服務提供者或傳輸電訊廠商支援。 QoS 是元件的集合，可對透過網路傳輸的資料子集啟用區分和優先處理。 QoS 表示資料子集會在往返網路時取得較高優先順序或保證服務。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ NetworkProtocol** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例示範如何從 **Win32 \_ NetworkProtocol** 的實例中取出執行中服務的清單。


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



下列 Perl 程式碼範例示範如何從 **Win32 \_ NetworkProtocol** 的實例中取出執行中服務的清單。


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
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

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
