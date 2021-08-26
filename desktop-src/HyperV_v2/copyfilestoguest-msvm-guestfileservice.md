---
description: 將檔案從 Hyper-v 主機複製到虛擬機器。
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: Msvm_GuestFileService：： CopyFilesToGuest 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e027d71faf8dda5769962d3c71d1fcfb5958c61c91993cf17fbf472d93aff50f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980478"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a>Msvm \_ GuestFileService：： CopyFilesToGuest 方法

將檔案從 Hyper-v 主機複製到虛擬機器。

## <a name="syntax"></a>語法


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CopyFileToGuestSettings* \[在\]
</dt> <dd>

[**Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)類別的實例陣列，代表「來賓檔案」服務作業。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。 如果作業是以非同步方式執行，則傳回值為4096。

> [!Note]  
> 此參數已在 Windows 10 中新增。

 

</dd> <dt>

*ParentPools* \[out、optional\]
</dt> <dd>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)參考的選擇性陣列，可用來監視作業的進度。 如果 **CopyFilesToGuest** 無法同步執行，則會使用 *ParentPools* 。 如果作業以非同步方式執行，則傳回值為4096。

> [!Note]  
> 此參數已在 Windows 10 中移除。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，會傳回 0;否則，會傳回錯誤值。

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
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | \\\\根 \\ 虛擬化 \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ GuestFileService**](msvm-guestfileservice.md)
</dt> </dl>

 

 




