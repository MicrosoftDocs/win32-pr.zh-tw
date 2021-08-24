---
description: 代表可建立、套用及刪除虛擬系統快照集的服務。
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: CIM_VirtualSystemSnapshotService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5546c7381eb0830d820af20d7efa03e5d7441a712b872a3ae2167b3e441354d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682688"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a>CIM \_ VirtualSystemSnapshotService 類別

代表可建立、套用及刪除虛擬系統快照集的服務。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>成員

**CIM \_ VirtualSystemSnapshotService** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**CIM \_ VirtualSystemSnapshotService** 類別具有這些方法。



| 方法                                                                      | 描述                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ApplySnapshot**](cim-virtualsystemsnapshotservice-applysnapshot.md)     | 將虛擬系統快照集套用至虛擬系統，以進行來源虛擬系統。<br/> |
| [**>icloudblob.createsnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md)   | 建立虛擬系統的快照集。<br/>                                               |
| [**DestroySnapshot**](cim-virtualsystemsnapshotservice-destroysnapshot.md) | 刪除虛擬系統快照集。<br/>                                                    |



 

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

 

 




