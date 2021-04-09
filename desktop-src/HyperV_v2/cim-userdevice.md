---
description: 代表可讓使用者輸入、查看或聆聽電腦系統上資料的邏輯裝置。
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: 'CIM_UserDevice 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848787"
---
# <a name="cim_userdevice-class-hyper-v-management"></a>CIM_UserDevice 類別 (Hyper-v 管理) 

代表可讓使用者輸入、查看或聆聽電腦系統上資料的邏輯裝置。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a>成員

**CIM \_ UserDevice** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ UserDevice** 類別具有這些屬性。

<dl> <dt>

**IsLocked**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果裝置已鎖定，防止使用者輸入或輸出，則 **為 true** 。否則 **為 false**。

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

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




