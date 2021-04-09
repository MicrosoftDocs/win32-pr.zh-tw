---
title: Win32_TSVirtualIP 類別
description: 定義遠端桌面工作階段主機 (RD 工作階段主機) 伺服器 (IP) 虛擬化設定的網際網路通訊協定。
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIP 類別遠端桌面服務
- Win32_TSVirtualIP 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f87db04d61dda0c6034b536544362ec09e0aaa66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685578"
---
# <a name="win32_tsvirtualip-class"></a>Win32 \_ TSVirtualIP 類別

定義遠端桌面工作階段主機 (RD 工作階段主機) 伺服器 (IP) 虛擬化設定的網際網路通訊協定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a>成員

**Win32 \_ TSVirtualIP** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSVirtualIP** 類別具有這些方法。



| 方法                                                                                                   | 描述                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProgram**](addprogram-win32-tsvirtualip.md)                                                       | 將程式新增至使用 IP 虛擬化的程式清單。<br/>                                                                                                |
| [**RemoveProgram**](removeprogram-win32-tsvirtualip.md)                                                 | 從使用 IP 虛擬化的程式清單中移除程式。<br/>                                                                                           |
| [**SelectNetworkAdapter**](selectnetworkadapter-win32-tsvirtualip.md)                                   | 設定要用於 IP 虛擬化之網路介面卡的 MAC 位址。<br/>                                                                                         |
| [**SetProgramList**](setprogramlist-win32-tsvirtualip.md)                                               | 覆寫使用 IP 虛擬化的程式清單。<br/>                                                                                                       |
| [**SetVirtualIPActive**](setvirtualipactive-win32-tsvirtualip.md)                                       | 設定 **VirtualIPActive** 屬性值。<br/>                                                                                                                      |
| [**SetVirtualIPMode**](setvirtualipmode-win32-tsvirtualip.md)                                           | 設定 **VirtualIPMode** 屬性值。<br/>                                                                                                                        |
| [**SetVirtualizeLoopbackAddressesEnabled**](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | 設定 **VirtualizeLoopbackAddressesEnabled** 屬性值。<br/> **Windows Server 2008 R2：** 此方法在 Windows Server 2012 之前無法使用。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ TSVirtualIP** 類別具有這些屬性。

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

**NetworkAdapterDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

網路介面卡的描述。

</dd> <dt>

**NetworkAdapterDescriptionList**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可用實體網路介面卡的描述清單。

</dd> <dt>

**NetworkAdapterMacAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

網路介面卡的 MAC 位址。

</dd> <dt>

**NetworkAdapterMacList**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可用實體網路介面卡的 MAC 地址清單。

</dd> <dt>

**PolicySourceNetworkAdapter**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出網路介面卡是否由伺服器或群組原則設定。

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

**PolicySourceProgramList**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **ProgramList** 屬性是由伺服器或群組原則設定。

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

**PolicySourceVirtualIPActive**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **VirtualIPActive** 屬性是由伺服器或群組原則設定。

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

**PolicySourceVirtualIPMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **VirtualIPMode** 屬性是由伺服器或群組原則設定。

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

**ProgramList**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定設定為使用 IP 虛擬化的程式。 這可能是程式名稱或完整路徑。

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

**VirtualIPActive**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

指定伺服器上的 IP 虛擬化是否為作用中狀態。 這可以是下列其中一個值。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

IP 虛擬化未啟用。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

IP 虛擬化處於作用中狀態。

</dd> </dl>

</dd> <dt>

**VirtualIPMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定要在伺服器上使用的 IP 虛擬化模式。 這可以是下列其中一個值。

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**每個會話** (0) 


</dt> <dd>

IP 虛擬化模式為每個會話。

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**每一程式** (1) 


</dt> <dd>

IP 虛擬化模式為每位使用者。

</dd> </dl>

</dd> <dt>

**VirtualizeLoopbackAddressesEnabled**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否啟用回送位址虛擬化。

**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

未啟用

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

已啟用

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                       |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 

