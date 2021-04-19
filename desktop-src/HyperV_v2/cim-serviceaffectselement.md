---
description: 代表服務與受管理元素之間的關聯，可能會受到其執行影響。
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: CIM_ServiceAffectsElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991755"
---
# <a name="cim_serviceaffectselement-class"></a>CIM \_ ServiceAffectsElement 類別

代表服務與受管理元素之間的關聯，可能會受到其執行影響。

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>成員

**CIM \_ ServiceAffectsElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ServiceAffectsElement** 類別具有這些屬性。

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

受服務影響的 managed 元素。

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 服務**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

影響受管理元素的服務。

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ServiceAffectsElement**。**OtherElementEffectsDescriptions**") 
</dt> </dl>

Managed 元素的效果。 這個陣列對應于 **OtherElementEffectsDescriptions** 陣列。

\- 獨佔使用 (2) ：沒有其他服務可能會與元素有此關聯。

\- 效能影響 (3) ：已淘汰以使用「取用」、「增強效能」或「降低效能」。 執行服務可能會增強或降低元素的效能。 這可能是執行的副作用，也可能是服務所提供之方法的預期結果。

\- 專案完整性 (4) ：已淘汰以使用「取用」、「增強完整性」或「降低完整性」。 執行服務可能會增強或降低元素的完整性。 這可能是執行的副作用，也可能是服務所提供之方法的預期結果。

\- 管理 (5) ：服務會管理元素。

\- 取用 (6) ：服務執行會取用部分或所有相關聯的專案，作為執行服務的結果。 例如，服務可能會耗用 CPU 迴圈，這可能會影響效能，或可能影響效能和完整性的儲存體。  (比方說，缺乏可用的儲存體可能會降低儲存狀態的能力，而降低完整性。 「取用」 ) 可單獨使用或與其他值搭配使用，尤其是「降低效能」和「降級完整性」。

「管理」但不應該使用「取用」來反映服務可能提供的佈建服務。

\- 增強完整性 (7) ：此服務可能會增強相關元素的完整性。

\- 降低 (8) 的完整性：服務可能會降低相關元素的完整性。

\- 增強效能 (9) ：此服務可能會增強相關元素的效能。

\- 降低效能 (10) ：服務可能會降低相關元素的效能。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

**專屬用途** (2) 


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

**效能影響** (3) 


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

**元素完整性** (4) 


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

**管理** (5) 


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

**耗用** (6) 


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

**增強完整性** (7) 


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

**降低完整性** (8) 


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

 (9) **增強效能**


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

**降低效能** (10) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (0x8000。0xFFFF) 


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ServiceAffectsElement**。**ElementEffects**") 
</dt> </dl>

陣列中的每個專案都會針對 **ElementEffects** 陣列中的對應專案提供額外的資訊。 **ElementEffects** 陣列中設定為 **其他** ( "1" ) 的任何專案都需要描述。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

