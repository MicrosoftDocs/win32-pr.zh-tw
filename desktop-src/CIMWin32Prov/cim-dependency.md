---
description: CIM 相依性 \_ 類別代表在物件之間建立相依性關聯性的關聯。
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: 'CIM_Dependency 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a2c1c568eeb8a3d753479c8663cc04293e76d38c5efb9919ab494b198657efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921938"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a>CIM_Dependency 類別 (CIMWin32 WMI 提供者) 

**CIM 相依 \_** 性類別代表在物件之間建立相依性關聯性的關聯。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a>成員

**CIM 相依 \_** 性類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM 相依 \_** 性類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedSystemElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

參考此關聯中的獨立物件。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedSystemElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

相依于 **Antecedent** 屬性之物件的參考。

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。 如需衍生自 CIM 相依性之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。 **\_**

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




