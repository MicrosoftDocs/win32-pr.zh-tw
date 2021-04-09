---
description: 管理 Hyper-v 主機上的集合。
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Msvm_CollectionManagementService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695639"
---
# <a name="msvm_collectionmanagementservice-class"></a>Msvm \_ CollectionManagementService 類別

管理 Hyper-v 主機上的集合。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a>成員

**Msvm \_ CollectionManagementService** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**Msvm \_ CollectionManagementService** 類別具有這些方法。



| 方法                                                                          | 描述                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddMember**](msvm-collectionmanagementservice-addmember.md)                 | 將指定的 ManagedElement 加入為指定之 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件的成員。<br/>                                                                                           |
| [**DefineCollection**](msvm-collectionmanagementservice-definecollection.md)   | 建立新的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件。<br/>                                                                                                                                        |
| [**DestroyCollection**](msvm-collectionmanagementservice-destroycollection.md) | 刪除指定的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件。<br/>                                                                                                                                    |
| [**RemoveMember**](msvm-collectionmanagementservice-removemember.md)           | 將指定的 ManagedElement 移除為指定之 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件的成員。<br/>                                                                                        |
| [**RemoveMemberById**](msvm-collectionmanagementservice-removememberbyid.md)   | 使用指定的識別碼，將指定的 ManagedElement 移除為 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 的成員。 即使具有該識別碼的物件不存在，也會成功。<br/> |
| [**RenameCollection**](msvm-collectionmanagementservice-renamecollection.md)   | 更新指定之 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件的 ElementName。<br/>                                                                                                                    |
| [**StartService**](msvm-collectionmanagementservice-startservice.md)           | 啟動服務。<br/>                                                                                                                                                                                                |
| [**StopService**](msvm-collectionmanagementservice-stopservice.md)             | 停止服務。<br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 服務**](cim-service.md)
</dt> </dl>

 

 




