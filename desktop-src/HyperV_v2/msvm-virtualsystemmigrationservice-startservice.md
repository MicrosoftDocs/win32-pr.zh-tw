---
description: Msvm_VirtualSystemMigrationService 類別的 StartService 方法會啟動服務。
ms.assetid: 2803cc6f-64ea-4502-ae5a-075bdd3f8c96
title: Msvm_VirtualSystemMigrationService 類別的 StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f88db5a78044d4382ad4daf1c154fb29b5dd88fe956847dede88bc3d64bcc8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146447"
---
# <a name="startservice-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Msvm VirtualSystemMigrationService 類別的 StartService 方法 \_

啟動服務。

## <a name="syntax"></a>語法


```mof
uint32 StartService();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值：

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




