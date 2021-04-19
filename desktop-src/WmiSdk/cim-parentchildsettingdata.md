---
description: CIM VirtualSystemSettingData 的實例 \_ 和 cim VirtualSystemSettingData 實例之間的關聯， \_ 代表這個物件所依據的最新快照集。
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: CIM_ParentChildSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993404"
---
# <a name="cim_parentchildsettingdata-class"></a>CIM \_ ParentChildSettingData 類別

[**Cim \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata)的實例和 **cim \_ VirtualSystemSettingData** 實例之間的關聯，代表這個物件所依據的最新快照集。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a>成員

**CIM \_ ParentChildSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ParentChildSettingData** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedSystemElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

參考此關聯中的獨立物件。

這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**子系**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ VirtualSystemSettingData**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統的設定資料，代表父系的子系。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedSystemElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

相依于 **Antecedent** 屬性之物件的參考。

這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**父系**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ VirtualSystemSettingData**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

子設定資料所依據的快照集設定資料。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------|
| 命名空間<br/> | 根 \\ CIMV2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

