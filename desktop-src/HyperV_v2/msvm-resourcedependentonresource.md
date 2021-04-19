---
description: 建立 \_ 代表資源配置的 CIM ResourceAllocationSettingData 實例取決於另一個資源配置。
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Msvm_ResourceDependentOnResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980347"
---
# <a name="msvm_resourcedependentonresource-class"></a>Msvm \_ ResourceDependentOnResource 類別

建立代表資源配置的 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 實例取決於另一個資源配置。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ ResourceDependentOnResource** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ResourceDependentOnResource** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ResourceAllocationSettingData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) ，表示此關聯中的獨立資源。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ResourceAllocationSettingData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) ，表示相依于前一項的資源。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](cim-dependency.md)
</dt> </dl>

 

