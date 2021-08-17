---
description: CIM \_ ApplicationSystemSoftwareFeature 類別代表的關聯會識別組成特定應用程式系統的軟體功能。 軟體功能可以包含在不同的產品中。
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: CIM_ApplicationSystemSoftwareFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d751a4564e8ed7357abd9dae5b4773e7180c66a5d0a89781a40d672715e69b11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322568"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a>CIM \_ ApplicationSystemSoftwareFeature 類別

**CIM \_ ApplicationSystemSoftwareFeature** 類別代表的關聯會識別組成特定應用程式系統的軟體功能。 軟體功能可以包含在不同的產品中。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a>成員

**CIM \_ ApplicationSystemSoftwareFeature** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ApplicationSystemSoftwareFeature** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ApplicationSystem**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 
</dt> </dl>

在關聯中包含父系統的 [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) 。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ SoftwareFeature**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

[**CIM \_ SoftwareFeature**](cim-softwarefeature.md) ，其中包含屬於系統元件的子項目。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ ApplicationSystemSoftwareFeature** 類別衍生自 [**cim \_ SystemComponent**](cim-systemcomponent.md)。

WMI 不會執行這個類別。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

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

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> </dl>

 

