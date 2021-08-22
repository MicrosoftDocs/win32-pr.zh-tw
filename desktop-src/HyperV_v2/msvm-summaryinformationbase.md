---
description: 用於 Msvm VirtualSystemManagementService 類別中的 GetSummaryInformation 方法 \_ ，以快速取得與虛擬系統或快照集相關的一般資訊。
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Msvm_SummaryInformationBase 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d131a2630c0c64e4b4b6bcec371eb901665c989948a1db510b47a41d9159f06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950097"
---
# <a name="msvm_summaryinformationbase-class"></a>Msvm \_ SummaryInformationBase 類別

用於 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別中的 [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)方法，以快速取得與虛擬系統或快照集相關的一般資訊。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a>成員

**Msvm \_ SummaryInformationBase** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SummaryInformationBase** 類別具有這些屬性。

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

資料類型： **DateTime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬系統或快照集的時間。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ManagedElement. ElementName" ) 
</dt> </dl>

虛擬系統或快照的易記名稱。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統或快照的目前狀態。

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出主機是否允許增強模式連線，以及是否允許虛擬機器使用它們（如果有的話）。

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**允許和可用** (2) 


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**不允許** (3) 


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**允許但無法使用** (6) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統目前的健全狀況狀態。 對於代表虛擬系統快照集的 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) 實例而言，這個屬性是不正確。

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝載此虛擬機器的電腦名稱稱。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ManagedElement. InstanceID" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID 是選擇性屬性，可在具現化命名空間的範圍內，用來以不透明和唯一的方式識別此類別的實例。 此類別的各種子類別可覆寫這個屬性，使其成為必要或索引鍵。 這類子類別也可以修改慣用的演算法，以確保以下定義的唯一性。

為確保命名空間中的唯一性，InstanceID 的值應使用下列「慣用」演算法來建立：

<OrgID>:<LocalID>

Where <OrgID> 和 <LocalID> 會以冒號分隔 (： ) ，其中 <OrgID> 必須包含受著作權、商標或其他唯一的名稱，而該名稱是由建立或定義 InstanceID 的商務實體所擁有，或是由可辨識的全域授權單位指派給商務實體的註冊識別碼。  (這項需求類似于 <Schema Name> \_ <Class Name> 架構類別名稱的結構。此外，) 此外，為了確保唯一性， <OrgID> 不能包含冒號 (： ) 。 使用此演算法時，InstanceID 中出現的第一個冒號必須出現在 <OrgID> 和之間 <LocalID> 。

<LocalID> 由商務實體選擇，不應重複使用，以找出不同的基礎 (真實世界) 元素。 如果不是 null，而且未使用上述的「慣用」演算法，則定義實體必須確保產生的 InstanceID 不會在這個實例的命名空間或其他提供者所產生的任何 InstanceIDs 上重複使用。

如果未針對 DMTF 定義的實例將設定為 null，就必須使用「慣用」演算法搭配 <OrgID> 將設定為 CIM。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統或快照的唯一名稱。

</dd> <dt>

**注意事項**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與虛擬系統或快照集相關的附注。

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

配置給虛擬系統或快照集的虛擬處理器總數。

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

專案的目前狀態。

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 null。

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

描述各種 **OperationalStatus** 陣列值的字串。

</dd> <dt>

**99.99**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自虛擬系統上次開機之後的時間量。 對於代表虛擬系統快照集的 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) 實例而言，這個屬性是不正確。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統的版本，格式為「主要. 次要」;例如 "2.0"。

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

列出 VM 所連接之虛擬交換器的易記名稱的字串。

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統的子類型。

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft： hyper-v：子類型： 1** ( "Microsoft： Hyper-v：子類型： 1" ) 


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft： hyper-v：子類型： 2** ( "Microsoft： Hyper-v：子類型： 2" ) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 視圖**](cim-view.md)
</dt> </dl>

 

