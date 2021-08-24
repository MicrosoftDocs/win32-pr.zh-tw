---
description: 將邏輯裝置與父系統產生關聯。
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Msvm_SystemDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67c538d82657d1ac07246f21dc2688f968ce969d1bf20238b20eeb4eea6f71cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746568"
---
# <a name="msvm_systemdevice-class"></a>Msvm \_ SystemDevice 類別

邏輯裝置可由系統匯總。 此關聯性是由系統裝置關聯明確進行。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a>成員

**Msvm \_ SystemDevice** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SystemDevice** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ) 
</dt> </dl>

關聯中的父系統。 這個屬性繼承自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

屬於系統元素的邏輯裝置。 這個屬性繼承自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ SystemDevice** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SystemDevice**](cim-systemdevice.md)
</dt> <dt>

[**CIM \_ SystemDevice**](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[虛擬系統類別](virtual-system-classes.md)
</dt> </dl>

 

