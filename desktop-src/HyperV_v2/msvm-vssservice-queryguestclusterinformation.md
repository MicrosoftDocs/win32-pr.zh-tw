---
description: 查詢從 Hyper-v 主機到來賓的叢集資訊。
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Msvm_VssService 類別的 QueryGuestClusterInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c3b58aefb5d821eec114010ea5f878d407d3b7474778b12ca74250bf5f757a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117993776"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a>Msvm VssService 類別的 QueryGuestClusterInformation 方法 \_

查詢從 Hyper-v 主機到來賓的叢集資訊。

## <a name="syntax"></a>語法


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*GuestClusterInformation* \[擴展\]
</dt> <dd>

成功時，會包含描述來賓叢集的 [**Msvm \_ GuestClusterInformation**](msvm-guestclusterinformation.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，會傳回 0 (完成，沒有錯誤) ，或 4096 (作業已啟動) ;否則，會傳回錯誤。

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

**系統正在使用中** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VssService**](msvm-vssservice.md)
</dt> </dl>

 

 




