---
description: 表示轉送 (篩選與透明橋接服務相關聯) 資料庫中的專案。
ms.assetid: 3C9FAE99-9543-4A6A-B578-3F4626598DB3
title: Msvm_DynamicForwardingEntry 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DynamicForwardingEntry
- Msvm_DynamicForwardingEntry.InstanceID
- Msvm_DynamicForwardingEntry.Caption
- Msvm_DynamicForwardingEntry.Description
- Msvm_DynamicForwardingEntry.ElementName
- Msvm_DynamicForwardingEntry.InstallDate
- Msvm_DynamicForwardingEntry.Name
- Msvm_DynamicForwardingEntry.OperationalStatus
- Msvm_DynamicForwardingEntry.StatusDescriptions
- Msvm_DynamicForwardingEntry.Status
- Msvm_DynamicForwardingEntry.HealthState
- Msvm_DynamicForwardingEntry.CommunicationStatus
- Msvm_DynamicForwardingEntry.DetailedStatus
- Msvm_DynamicForwardingEntry.OperatingStatus
- Msvm_DynamicForwardingEntry.PrimaryStatus
- Msvm_DynamicForwardingEntry.SystemCreationClassName
- Msvm_DynamicForwardingEntry.SystemName
- Msvm_DynamicForwardingEntry.ServiceCreationClassName
- Msvm_DynamicForwardingEntry.ServiceName
- Msvm_DynamicForwardingEntry.CreationClassName
- Msvm_DynamicForwardingEntry.MACAddress
- Msvm_DynamicForwardingEntry.DynamicStatus
- Msvm_DynamicForwardingEntry.VlanId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04fef4c5e55be6a5e955c51102620dbda24b264fead6b74d1bf2148eb1db7505
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525298"
---
# <a name="msvm_dynamicforwardingentry-class"></a>Msvm \_ DynamicForwardingEntry 類別

表示轉送 (篩選與透明橋接服務相關聯) 資料庫中的專案。 專案是服務的弱式，如 [**Msvm \_ TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md)所指定。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DynamicForwardingEntry : CIM_DynamicForwardingEntry
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   SystemCreationClassName;
  string   SystemName;
  string   ServiceCreationClassName;
  string   ServiceName;
  string   CreationClassName;
  string   MACAddress;
  uint16   DynamicStatus;
  uint16   VlanId;
};
```

## <a name="members"></a>成員

**Msvm \_ DynamicForwardingEntry** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ DynamicForwardingEntry** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與基礎受管理元素通訊的能力。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配這個類別的其他重要屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。 這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**DynamicStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的狀態。 這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**無效** 的 (2) 
</dt> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**學習** (3) 
</dt> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4) 
</dt> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**管理** (5) 
</dt> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

元素的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 ( 「確定」 ) 。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當虛擬機器建立時自動填入。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (12) 
</dt> </dl>

透明橋接服務具有轉送和篩選資訊的單播 MAC 位址。 MAC 位址的格式為十二個十六進位數位 (例如 "010203040506" ) ，其中每一組代表根據 RFC 2469 以「標準」位順序表示的其中六個 MAC 位址八位。 這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已知物件的標籤。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不受支援。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**ServiceCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

範圍服務的 **CreationClassName**。 這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

範圍服務的名稱。 這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不受支援。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

範圍系統的 **CreationClassName**。 這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

範圍系統的名稱。 這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。

</dd> <dt>

**VlanId**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

與此專案相關聯的虛擬 LAN 識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ DynamicForwardingEntry** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

請參閱 [查詢網路物件](querying-networking-objects.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md)
</dt> <dt>

[**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))
</dt> </dl>

 

