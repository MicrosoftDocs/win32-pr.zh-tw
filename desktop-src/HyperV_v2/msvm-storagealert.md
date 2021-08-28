---
description: 代表每次 Msvm \_ ResourcePool 或 Msvm LogicalDisk 類別的 OperationalStatus 屬性變更時引發的事件 \_ 。
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Msvm_StorageAlert 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 41af5f29f54dc0b5c7e63203c43160539bcaa870
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886587"
---
# <a name="msvm_storagealert-class"></a>Msvm \_ StorageAlert 類別

代表每次 [**Msvm \_ ResourcePool**](msvm-resourcepool.md)或 [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)類別的 **OperationalStatus** 屬性變更時引發的事件。

下列語法已從 MOF 程式碼簡化，並包含這些屬性。

## <a name="syntax"></a>語法

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a>成員

**Msvm \_ StorageAlert** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ StorageAlert** 類別具有這些屬性。

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **ModelCorrespondence** ( "cim \_ AlertIndication. AlertingManagedElement"，"Cim \_ AlertIndication. OtherAlertingElementFormat" ) 
</dt> </dl>

指定 **AlertingManagedElement** 屬性的格式。 格式為 CIMObjectPath，格式為 *&lt; NamespacePath &gt; ： &lt; ClassName &gt; 。 &lt;Prop1 &gt; = \\ " &lt; Value1 &gt; \\ "、" &lt; this.prop2 &gt; = \\ " &lt; Value2 &gt; \\ "*，以指定 CIM 架構中的實例。

這個屬性繼承自 **CIM \_ AlertIndication** 類別。

可能的值包括：

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2) 
</dt> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

產生警示之實例的 WMI 路徑。

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定警示的主要分類。 這個屬性的可能值為：

<dl> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**服務品質警示** (3) 
</dt> </dl>

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

偵測到基礎事件的日期和時間。

</dd> <dt>

**訊息**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

藉由將 **MessageArguments** 屬性中所指定之部分或全部動態元素與 **OwningEntity** 屬性相關聯的其他目錄中的 **MessageID** 屬性唯一識別的靜態元素組合在一起所建立的格式化訊息。

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

陣列，其中包含訊息的動態內容。 如果 **MessageID** 的值為32930，則位置為0的引數就是產生警示之 [**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md)實例的 **PoolID** 。

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在 **OwningEntity** 屬性的範圍內唯一識別 **訊息** 屬性的格式。 這個屬性的可能值為：

32930 ( 「儲存體集區 QoS 不足的輸送量訊息」 ) 

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

為 **AlertingManagedElement** 定義「其他」值的字串。 當 **AlertingManagedElement** 設定為 1 ( "Other" ) 的值時，此值必須設定為非 Null 值。 對於 **AlertingManagedElement** 的所有其他值，此字串的值必須設定為 Null。

這個屬性繼承自 **CIM \_ AlertIndication** 類別。

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一識別擁有此實例中所描述之 **訊息** 格式定義的實體。 這個屬性的值一律是 "Microsoft Windows-hyper-v"。

"Microsoft-Windows-hyper-v"

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述警示指示的嚴重性。 這個屬性的可能值為：

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**資訊** (2) 
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**降級/警告** (3) 
</dt> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述導致警示表示之情況的可能原因。

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**儲存體容量問題** (50) 
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**先前的警示已清除** (59) 
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對應于 **ProbableCause** 屬性值的文字描述。

</dd> </dl>

## <a name="remarks"></a>備註

Hyper-v WMI 提供者不會引發個別虛擬磁片的事件，以避免在基礎儲存系統發生大規模故障時，對用戶端發出事件。

當用戶端收到 **Msvm \_ StorageAlert** 事件時，如果 **ProbableCause** 屬性的值為 50 ( 儲存體容量問題 ) ，用戶端就可以使用下列其中一個程式，來探索哪些虛擬磁片在其 QoS 原則之外運作：

-   查詢從產生事件的資源集區配置的所有 [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md) 實例。 這些 **Msvm \_ LogicalDisk** 實例會透過 [**Msvm \_ ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) 關聯與資源集區相關聯。
-   選取 [OperationalStatus] 包含 [輸送量不足] 的實例，以篩選結果清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ AlertIndication**](cim-alertindication.md)
</dt> <dt>

[**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> <dt>

[**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




