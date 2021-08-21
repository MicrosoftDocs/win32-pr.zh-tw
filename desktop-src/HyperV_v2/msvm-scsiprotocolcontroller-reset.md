---
description: Msvm_SCSIProtocolController 類別的 reset 方法-要求重設。
ms.assetid: 8de43754-19dc-4865-af6c-badcb5445167
title: Msvm_SCSIProtocolController 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SCSIProtocolController.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cf27d7c0e12ca9f7555aac79555ff69bfc97eb20ecd5131a9245f0ace485e218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147301"
---
# <a name="reset-method-of-the-msvm_scsiprotocolcontroller-class"></a>Msvm SCSIProtocolController 類別的 Reset 方法 \_

要求重設。

## <a name="syntax"></a>語法


```mof
uint32 Reset();
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

[**Msvm \_ SCSIProtocolController**](msvm-scsiprotocolcontroller.md)
</dt> </dl>

 

 




