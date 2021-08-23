---
description: 編輯 VHD 設定檔內的 VHD 快照集專案。 如果已有問題的快照集識別碼，則會以新的專案覆寫現有的快照集專案。 否則，新的專案會新增至 VHD 設定檔案。
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Msvm_ImageManagementService 類別的 SetVHDSnapshotInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: af4adddb2b59da303f558cfffac61003e70e5767c77e381b13ba6089228d6643
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522448"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Msvm ImageManagementService 類別的 SetVHDSnapshotInformation 方法 \_

編輯 VHD 設定檔內的 VHD 快照集專案。 如果已有問題的快照集識別碼，則會以新的專案覆寫現有的快照集專案。 否則，新的專案會新增至 VHD 設定檔案。

## <a name="syntax"></a>語法


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*資訊* \[在\]
</dt> <dd>

要在 VHD 設定檔中變更或新增的 VHD 快照集資訊。 字串是 [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)的內嵌實例。

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
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




