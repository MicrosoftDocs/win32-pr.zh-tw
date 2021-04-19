---
description: 將已配置資源的實例與從中配置資源的資源集區產生關聯。
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Msvm_ElementAllocatedFromPool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987246"
---
# <a name="msvm_elementallocatedfrompool-class"></a>Msvm \_ ElementAllocatedFromPool 類別

將已配置資源的實例與從中配置資源的資源集區產生關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ ElementAllocatedFromPool** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ElementAllocatedFromPool** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 **寫**、 **最大** (1) 
</dt> </dl>

資源集區。 這個屬性繼承自 [**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

配置的資源。 這個屬性繼承自 [**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ ElementAllocatedFromPool** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ ElementAllocatedFromPool**](cim-elementallocatedfrompool.md)
</dt> <dt>

[**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))
</dt> <dt>

[**Msvm \_ ElementAllocatedFromPool (V1)**](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[資源管理類別](resource-management-classes.md)
</dt> </dl>

 

