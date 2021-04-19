---
description: 建立虛擬機器與其匯出設定資料的關聯。
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Msvm_SystemExportSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974011"
---
# <a name="msvm_systemexportsettingdata-class"></a>Msvm \_ SystemExportSettingData 類別

建立虛擬機器與其匯出設定資料的關聯。 在呼叫 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)方法之前，可以使用此關聯來抓取 [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)的實例。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ SystemExportSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SystemExportSettingData** 類別具有這些屬性。

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出參考的設定目前是否在專案的作業中使用，或這項資訊未知。 這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。



| 值                                                                        | 意義                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | 目前<br/>     |
| <dl> <dt>2</dt> </dl> | 非最新<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出參考的設定是否為專案的預設值，或這項資訊未知。 這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。



| 值                                                                        | 意義                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | 預設<br/>     |
| <dl> <dt>2</dt> </dl> | 非預設<br/> |



 

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出參考的設定是否為下一個要套用的設定。 例如，應用程式可能會在重新初始化、重設、重新設定要求上進行。 這可能是永久設定，或是僅使用一次的設定，如旗標所示。 如果是永久設定，則會在每次受控元素重新初始化時套用設定，直到以手動方式重設此旗標為止。 但是，如果是單一使用，則會在套用設定之後自動清除旗標。 此外，如果指定此旗標 (亦即設定為0以外的值 (未知的) ) ，則會優先于任何可能已指定為預設值的設定資料。 例如：如果 managed 元素是電腦系統，且此旗標的值為 1 (下一步) ，則設定會在系統下次重設時生效。 而且，除非此旗標已變更，否則後續的系統重設會保存此旗標。 但是，如果此旗標設定為 3 (下一步是使用) ，則這項設定只會使用一次，且旗標會在之後重設為 2 (不是下一個) 。 因此，在上述範例中，如果系統快速地連續重新開機，則在第二次重新開機時不會使用此設定。

這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。



| 值                                                                        | 意義                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>                |
| <dl> <dt>1</dt> </dl> | 下一步<br/>                |
| <dl> <dt>2</dt> </dl> | 不是下一個<br/>            |
| <dl> <dt>3</dt> </dl> | 下一步是用於單次使用<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_** 未執行](msvm-computersystem.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ElementSettingData 的 ) 
</dt> </dl>

虛擬機器的參考。 這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ElementSettingData ) 
</dt> </dl>

參考虛擬機器的匯出設定資料。 這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ SystemExportSettingData** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

