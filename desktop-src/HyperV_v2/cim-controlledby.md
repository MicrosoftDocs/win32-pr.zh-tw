---
description: 代表控制器與受控制器管理的邏輯裝置之間的關聯性。
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: 'CIM_ControlledBy 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e6db572177aca7208b9d087fa5eeceab699cf1e1014f736f7150607af8e2805b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813149"
---
# <a name="cim_controlledby-class-hyper-v-management"></a>CIM_ControlledBy 類別 (Hyper-v 管理) 

代表控制器與受控制器管理的邏輯裝置之間的關聯性。

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a>成員

**CIM \_ ControlledBy** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ControlledBy** 類別具有這些屬性。

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此屬性描述裝置透過控制器的存取範圍。

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

**ReadWrite** (2) 


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

**ReadOnly** (3) 


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

**NoAccess** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

透過控制器存取裝置的優先順序。 較低的值表示較高的優先順序。

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出控制器是否正在主動管理裝置。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Active** (1) 


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**非** 使用中 (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 控制器**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

控制器。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalDevice**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

邏輯裝置。

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器內容中相關聯裝置的位址。

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **計數器**
</dt> </dl>

控制器發出的硬重設數目。 硬重設會將裝置傳回到其初始化或啟動狀態，之後所有的內部裝置狀態資訊和資料都會遺失。

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **計數器**
</dt> </dl>

控制器發出的軟重設數目。 軟重設不會清除裝置狀態或資料。

</dd> <dt>

**TimeOfDeviceReset**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器上次重設下游裝置的時間。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ DeviceConnection**](cim-deviceconnection.md)
</dt> </dl>

 

