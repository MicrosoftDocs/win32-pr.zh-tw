---
description: 將服務與其主控電腦系統產生關聯。
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Msvm_HostedService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996596"
---
# <a name="msvm_hostedservice-class"></a>Msvm \_ HostedService 類別

將服務與其主控電腦系統產生關聯。 您可以透過與主機之間的關聯，探索 [**Msvm \_ VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) 的實例。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm 的 \_ HostedService** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm 的 \_ HostedService** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

主控電腦系統的參考。 這個屬性繼承自 [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice)。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

所裝載之服務的參考。 這個屬性繼承自 [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice)。

</dd> </dl>

## <a name="remarks"></a>備註

**Msvm \_ HostedService** 類別的存取權可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

請參閱 [查詢網路物件](querying-networking-objects.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> <dt>

[**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[虛擬系統管理類別](virtual-system-management-classes.md)
</dt> </dl>

 

