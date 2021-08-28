---
description: 從復原伺服器移除授權專案。
ms.assetid: 1647b35d-1c2f-4fb5-84c0-10b357326abf
title: Msvm_ReplicationService 類別的 RemoveAuthorizationEntry 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12276ded5e9021fb775ee6f6be4eb2e5a92c4375a5bce9e3debca7972df2ee86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980068"
---
# <a name="removeauthorizationentry-method-of-the-msvm_replicationservice-class"></a>Msvm ReplicationService 類別的 RemoveAuthorizationEntry 方法 \_

從復原伺服器移除授權專案。

## <a name="syntax"></a>語法


```mof
uint32 RemoveAuthorizationEntry(
  [in]  string              AllowedPrimaryHostSystem,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AllowedPrimaryHostSystem* \[在\]
</dt> <dd>

將從伺服器移除其授權專案的主伺服器。 這與 [**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md)類別的 **AllowedPrimaryHostSystem** 屬性相同。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

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

**System 使用** (32774) 
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

## <a name="remarks"></a>備註

移除授權專案將會停止所有以該專案授權之虛擬機器的複寫。

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

[**AddAuthorizationEntry**](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**ModifyAuthorizationEntry**](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**SetAuthorizationEntry**](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

