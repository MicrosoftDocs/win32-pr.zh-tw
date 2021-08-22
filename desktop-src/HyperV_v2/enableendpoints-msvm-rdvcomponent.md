---
description: 要求遠端桌面服務的虛擬裝置啟動與虛擬機器的管道連接。
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Msvm_RdvComponent 類別的 EnableEndPoints 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8a23f39ee46cb41c5941be3d9632fbe15901dfffd35078e680ebe61d46fdb131
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532528"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a>Msvm RdvComponent 類別的 EnableEndPoints 方法 \_

要求遠端桌面服務的虛擬裝置啟動與虛擬機器的管道連接。

## <a name="syntax"></a>語法


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**記憶體不足** (32774) 
</dt> <dt>

**找不到** 檔案 (32775) 
</dt> <dt>

  (32776) 
</dt> <dt>

  (32777) 
</dt> <dt>

  (32778) 
</dt> <dt>

  (32779) 
</dt> <dt>

  (32780) 
</dt> <dt>

  (32781) 
</dt> <dt>

  (32782) 
</dt> </dl>

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

[**Msvm \_ RdvComponent**](msvm-rdvcomponent.md)
</dt> </dl>

 

 




