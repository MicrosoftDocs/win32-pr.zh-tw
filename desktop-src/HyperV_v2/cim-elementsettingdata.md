---
description: 代表 managed 元素與其相關聯設定資料之間的關聯。 此關聯也會說明這是預設值還是目前的設定。
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: CIM_ElementSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979179"
---
# <a name="cim_elementsettingdata-class"></a>CIM \_ ElementSettingData 類別

代表 managed 元素與其相關聯設定資料之間的關聯。 此關聯也會說明這是預設值還是目前的設定。

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a>成員

**CIM \_ ElementSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ElementSettingData** 類別具有這些屬性。

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出參考的設定目前是否由元素使用中。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

**為目前的** (1) 


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

**不是目前的** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出此設定是否為元素的預設設定。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

**預設** (1) 


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

**不是預設值** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

旗標，指出套用設定的時間和頻率。

例如，您可以在重新初始化、重設、重新設定要求上套用設定。 這可能是永久設定，或是僅使用一次的設定，如旗標所示。 如果是永久設定，則會在每次受控元素重新初始化時套用設定，直到以手動方式重設此旗標為止。 但是，如果是單一使用，則會在套用設定之後自動清除旗標。 此外，如果此旗標設定為0以外的值 (未知的) ，則會優先于設定為 "Default" 的 **SettingData** 屬性。

如果受管理元素是電腦系統，且此旗標的值為「下一步」，則此設定將會在系統下次重設時生效。 而且，除非此旗標已變更，否則後續的系統重設會保存此旗標。 但是，如果此旗標設定為 [單一使用的下一步]，則此設定只會使用一次，而且旗標會在之後重設為 2 (不) 下一次。 因此，在上述範例中，如果系統快速地連續重新開機，則在第二次重新開機時不會使用此設定。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

**接下來** (1) 


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

**不是接下來的** (2) 


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

**下一步是用於單一用途** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Managed 元素。

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ SettingData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

與元素相關聯的設定資料。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

