---
description: 代表 Msvm 的實例（ \_ 代表虛擬機器的實例）與代表虛擬機器之複寫關聯性的 Msvm ReplicationRelationship 實例之間的關聯 \_ 。
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Msvm_SystemReplicationRelationship 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86040e6dc5676f6cd40b223f0a3cbd31864965722de957fda6ff1d140ad94b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810600"
---
# <a name="msvm_systemreplicationrelationship-class"></a>Msvm \_ SystemReplicationRelationship 類別

代表 Msvm 的實例（代表虛擬 [**機 \_**](msvm-computersystem.md) 的實例）與代表虛擬機器之複寫關聯性的 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 實例之間的關聯。 此類別衍生自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency) 性類別。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ SystemReplicationRelationship** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SystemReplicationRelationship** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) 
</dt> </dl>

代表虛擬機器之 Msvm 實例 [**類別 \_**](msvm-computersystem.md) 的實例參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ ReplicationRelationship**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) 
</dt> </dl>

參考 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 類別的實例，代表虛擬系統的複寫關聯性。

</dd> </dl>

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

[**CIM \_ 相依性**](cim-dependency.md)
</dt> <dt>

[**CIM \_ 相依性**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

