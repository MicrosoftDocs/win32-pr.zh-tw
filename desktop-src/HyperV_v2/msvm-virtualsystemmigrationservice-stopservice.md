---
description: Msvm_VirtualSystemMigrationService 類別的 StopService 方法會停止服務。
ms.assetid: cf0dde8d-b6cf-4a52-905f-c686ac41e314
title: Msvm_VirtualSystemMigrationService 類別的 StopService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 14e94f8351c44319de7ce15053e0f29ab70a6f12dd5bba5894c7b9ab1a3eac39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117994161"
---
# <a name="stopservice-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Msvm VirtualSystemMigrationService 類別的 StopService 方法 \_

停止服務。

## <a name="syntax"></a>語法


```mof
uint32 StopService();
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

 

 




