---
description: 從提供的復原變更追蹤識別碼或 VHDSet 快照集識別碼之後，抓取虛擬磁片指定區域的變更清單。
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Msvm_ImageManagementService 類別的 GetVirtualDiskChanges 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971029"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a>Msvm ImageManagementService 類別的 GetVirtualDiskChanges 方法 \_

從提供的復原變更追蹤識別碼或 VHDSet 快照集識別碼之後，抓取虛擬磁片指定區域的變更清單。

## <a name="syntax"></a>語法


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* \[在\]
</dt> <dd>

指定虛擬硬碟檔案位置的完整路徑。

</dd> <dt>

*LimitId* \[在\]
</dt> <dd>

復原變更追蹤識別碼或 VHD 集的快照集識別碼，表示虛擬磁片中的變更基準。

</dd> <dt>

*TargetSnapshotId* \[在\]
</dt> <dd>

VHDSet 快照集識別碼，指出在判斷虛擬硬碟中的變更時，要與基準比較的快照集。 此參數只對 VHD 設定檔案有效。

</dd> <dt>

*ByteOffset* \[在\]
</dt> <dd>

虛擬磁片中要查詢變更之區域的位元組位移。

</dd> <dt>

*ByteLength* \[在\]
</dt> <dd>

要查詢其變更之虛擬磁片區域的位元組長度。 這必須小於虛擬磁片的大小。

</dd> <dt>

*ProcessedByteLength* \[擴展\]
</dt> <dd>

已處理的位元組長度總計。 這可能等於 ByteLength 或更少。

</dd> <dt>

*ChangedByteOffsets* \[擴展\]
</dt> <dd>

虛擬磁片中的位元組位移清單，指出每個變更範圍的開頭。

</dd> <dt>

*ChangedByteLengths* \[擴展\]
</dt> <dd>

虛擬磁片中已變更範圍的位元組長度清單。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果工作已完成) ，則作業 (的參考可以是 null。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值：

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
</dt> <dt>

**找不到** 檔案 (32779) 
</dt> </dl>

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

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




