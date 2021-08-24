---
description: Msvm_TerminalService 類別的 StopService 方法會停止服務。
ms.assetid: c96ca784-c935-41a4-b1aa-8360cf270c9e
title: Msvm_TerminalService 類別的 StopService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5f2d9cdcb52bc90b204b53f0bd408f9bf91842c615d81a0606319094298ebb51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746578"
---
# <a name="stopservice-method-of-the-msvm_terminalservice-class"></a>Msvm TerminalService 類別的 StopService 方法 \_

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

[**Msvm \_ TerminalService**](msvm-terminalservice.md)
</dt> </dl>

 

 




