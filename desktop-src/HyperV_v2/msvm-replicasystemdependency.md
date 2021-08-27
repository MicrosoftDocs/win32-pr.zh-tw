---
description: 代表 CIM 系統類型實例之間的關聯 \_ ，該類別代表虛擬機器複本，以及 \_ 表示測試虛擬機器複本的 cim 系統類型實例。
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Msvm_ReplicaSystemDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f6bb3f4879ee0e1c7babaf8f85b8455716ee1b2e61db4e0764d6b28583efefd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130428"
---
# <a name="msvm_replicasystemdependency-class"></a>Msvm \_ ReplicaSystemDependency 類別

代表 Cim 系統類型實例之間的關聯 [**， \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 該類別代表虛擬機器複本，以及表示測試虛擬機器複本的 **cim \_ 系統類型** 實例。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ ReplicaSystemDependency** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ReplicaSystemDependency** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 未執行
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) 
</dt> </dl>

代表虛擬機器複本之 CIM 系統 [**類型 \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 實例的參考。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 未執行
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) 
</dt> </dl>

[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)系統類型實例的參考，代表 [**Msvm \_ ReplicationService. TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md)方法所建立的測試虛擬機器複本。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

