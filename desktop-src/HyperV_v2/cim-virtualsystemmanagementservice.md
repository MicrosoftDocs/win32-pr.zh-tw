---
description: 表示管理虛擬系統的服務。
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: CIM_VirtualSystemManagementService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979110"
---
# <a name="cim_virtualsystemmanagementservice-class"></a>CIM \_ VirtualSystemManagementService 類別

表示管理虛擬系統的服務。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a>成員

**CIM \_ VirtualSystemManagementService** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**CIM \_ VirtualSystemManagementService** 類別具有這些方法。



| 方法                                                                                      | 描述                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResourceSettings**](cim-virtualsystemmanagementservice-addresourcesettings.md)       | 將資源新增至虛擬系統設定。<br/>                          |
| [**DefineSystem**](cim-virtualsystemmanagementservice-definesystem.md)                     | 定義虛擬系統。<br/>                                                  |
| [**DestroySystem**](cim-virtualsystemmanagementservice-destroysystem.md)                   | 刪除虛擬系統。<br/>                                                  |
| [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | 修改虛擬系統組態的虛擬資源設定。<br/> |
| [**ModifySystemSettings**](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | 修改虛擬系統設定。<br/>                                          |
| [**RemoveResourceSettings**](cim-virtualsystemmanagementservice-removeresourcesettings.md) | 從虛擬系統組態移除虛擬資源設定。<br/>     |



 

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

[**CIM \_ 服務**](cim-service.md)
</dt> </dl>

 

 




