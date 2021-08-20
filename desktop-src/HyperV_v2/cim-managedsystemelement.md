---
description: CIM \_ ManagedSystemElement 是 system 元素階層的基類。 系統可能會以這個類別或其子類別來表示系統的任何元件。
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: 'CIM_ManagedSystemElement 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0056aa172827bde2967c20c1f8b8922c2bfcb5165adc4e03d94c98f30748157e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812015"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a>CIM_ManagedSystemElement 類別 (Hyper-v 管理) 

**CIM \_ManagedSystemElement** 是系統元素階層的基類。 系統可能會以這個類別或其子類別來表示系統的任何元件。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
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
};
```

## <a name="members"></a>成員

**CIM \_ ManagedSystemElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ManagedSystemElement** 類別具有這些屬性。

<dl> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與此元素通訊的能力。 **Null** 值表示檢測不支援這個屬性。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

 (1) **無法使用**


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

**通訊正常** (2) 


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

**遺失通訊** (3) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** (4) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (0x8000。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**"，"**CIM \_ ManagedSystemElement**.**HealthState**") 
</dt> </dl>

指出補充 **PrimaryStatus** 屬性的其他狀態詳細資料。 **Null** 值表示檢測不支援這個屬性。

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

 (0) **無法使用**


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

**沒有其他資訊** (1) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** (2) 


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

**預測性失敗** (3) 


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

**無法復原的錯誤** (4) 


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

**錯誤中的支援實體** (5) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (0x8000。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示專案目前的健康情況。 這個屬性會表示這個專案的健康情況，但不一定是其子元件的健全狀況。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**確定** (5) 


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

**降級/警告** (10) 


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

**次要失敗** (15) 


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

**重大失敗** (20) 


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

**嚴重失敗** (25) 


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

**無法復原的錯誤** (30) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) 
</dt> </dl>

已知物件的標籤。 子類別化時， **Name** 屬性可以覆寫為索引鍵屬性。

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**") 
</dt> </dl>

表示專案目前的操作條件。 這個屬性可以用來提供關於 **EnabledState** 屬性值的更多詳細資料。 **Null** 值表示檢測不支援這個屬性。

「未知」表示

「無」表示

于

入門

從而

「已停止」和「已中止」很類似，雖然前者

「休眠」表示

「已完成」表示 t

遷移

"Immigrating"

"Emigrating"

「正在關機」

「測試中」

轉變

「服務中」

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

實作為一般能夠傳回這個屬性，但目前無法這麼做。

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**


</dt> <dd>

執行 (提供者) 能夠傳回這個屬性的值，但不是針對此特定硬體/軟體的部分，或是刻意未使用屬性的情況，因為它不會加入任何有意義的資訊 (例如，將其他資訊新增至另一個屬性) 時所使用的屬性。

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) 


</dt> <dd>

描述要設定、維護、清除或以其他方式管理的元素。

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) 


</dt> <dd>

描述正在初始化的元素。

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) 


</dt> <dd>

描述要帶到有條理之停止的元素。

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) 


</dt> <dd>

發生乾淨且有條理的停止。

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) 


</dt> <dd>

發生突然停止，其中元素的狀態和設定可能需要更新。

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) 


</dt> <dd>

元素為非使用中或已停止。

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) 


</dt> <dd>

元素已完成其作業。 此值應該與 PrimaryStatus 中的 [確定]、[錯誤] 或 [已降級]，讓用戶端能夠判斷完成的作業是否已完成，但有「確定」 (通過) 、已完成，但 (失敗) 或已完成，但作業已完成，但未完成，或未報告錯誤 (。

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) 


</dt> <dd>

專案正在主控制項之間移動。

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) 


</dt> <dd>

正在將專案從主控制項移開。

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) 


</dt> <dd>

正在將元素移至新的主項目目。

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) 


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) 


</dt> <dd>

描述進入突然停止的元素。

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) 


</dt> <dd>

元素正在執行測試函數。

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) 


</dt> <dd>

描述狀態之間的專案，也就是它在先前的狀態或下一個狀態下並未完全可用。 如果其他表示轉換為特定狀態的值不適用，則應使用此值。

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) 


</dt> <dd>

描述服務中和操作中的元素。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (0x8000。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ManagedSystemElement**。**StatusDescriptions**") 
</dt> </dl>

包含元素目前狀態的指標。 **OperationalStatus** 屬性的第一個值應該包含元素的主要狀態。

> [!Note]  
> **OperationalStatus** 屬性會取代已被取代的 **Status** 屬性。 由於在管理應用程式中廣泛使用現有的 **Status** 屬性，因此強烈建議提供者或檢測提供 **狀態** 和 **OperationalStatus** 屬性。 當已檢測的 **狀態**，因為它是單一值屬性，所以也應該提供元素的主要狀態。

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**確定** (2) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (3) **降級**


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span> (4) 的 **壓力**


</dt> <dd>

元素運作正常，但需要注意。 「壓力」狀態的範例有多載、針對過熱等等。

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (5) 


</dt> <dd>

元素正在運作名義上，但在不久的未來預測失敗。

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (6) 


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (7) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (8) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (9) 


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (10) 


</dt> <dd>

發生有條理的停止。

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (11) 


</dt> <dd>

要設定、維護、清除或以其他方式管理的元素。

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (12) 


</dt> <dd>

監視系統有此專案的知識，但是從未能夠與其建立通訊。

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (13) 


</dt> <dd>

已知 ManagedSystem 元素存在，而且已在過去成功聯繫，但目前無法連線。

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (14) 


</dt> <dd>

突然停止，其中專案的狀態和設定可能需要更新的位置發生。

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (15) 


</dt> <dd>

元素為非使用中或已停止。

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>錯誤 (16) **中支援的實體**


</dt> <dd>

這個元素可能是「確定」，但另一個相依的元素（相依）發生錯誤。 例如，因為較低層的網路問題而無法運作的網路服務或端點。

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (17) 


</dt> <dd>

元素已完成其作業。

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**電源模式** (18) 


</dt> <dd>

專案具有相關聯 PowerManagementService 關聯中包含的額外電源模型資訊。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (0x8000。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ManagedSystemElement**.**DetailedStatus**"，"**CIM \_ ManagedSystemElement**.**HealthState**") 
</dt> </dl>

表示高階狀態值。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**確定** (1) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

 (2) **降級**


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** (3) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (0x8000。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「**CIM \_ ManagedSystemElement**。**OperationalStatus**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) 
</dt> </dl>

指出物件的主要狀態。

> [!Note]  
> 此屬性已被取代。 它會由 **OperationalStatus** 屬性取代。 如果您選擇使用 **Status** 屬性來提供回溯相容性，它應該是 [ **OperationalStatus** ] 屬性的 [次要]。

 

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


</dt> <dd></dd> <dt>



  ( 「壓力」 ) 


</dt> <dd></dd> <dt>



  ( "NonRecover" ) 


</dt> <dd></dd> <dt>



  ( "No Contact" ) 


</dt> <dd></dd> <dt>



  ( 「遺失通訊」 ) 


</dt> <dd></dd> <dt>



  ( 「已停止」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ManagedSystemElement**。**OperationalStatus**") 
</dt> </dl>

指出 **OperationalStatus** 陣列中對應值的描述。 例如，如果 [ **OperationalStatus** ] 屬性中的專案包含 [ **正在停止**] 值，則在這個屬性中相同陣列索引處的專案可能會包含物件停止原因的說明。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

