---
description: 修改修復伺服器的授權專案。
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Msvm_ReplicationService 類別的 ModifyAuthorizationEntry 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17f5ff1a0e4e1cca95dc5f7764d2f8e2bf9d2c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984626"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a>Msvm ReplicationService 類別的 ModifyAuthorizationEntry 方法 \_

修改修復伺服器的授權專案。

## <a name="syntax"></a>語法


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AuthorizationEntry* \[在\]
</dt> <dd>

[**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md)類別實例的字串表示，定義要修改的授權專案。

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

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AddAuthorizationEntry**](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**RemoveAuthorizationEntry**](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**SetAuthorizationEntry**](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

