---
description: 設定虛擬機器的複寫授權專案。
ms.assetid: 39b6b0c4-5515-4863-9038-4c37421abe65
title: Msvm_ReplicationService 類別的 SetAuthorizationEntry 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ce51997399a7ea028f39156e31a67144f415f37d4d028694d674f8aff8fe522
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913928"
---
# <a name="setauthorizationentry-method-of-the-msvm_replicationservice-class"></a>Msvm ReplicationService 類別的 SetAuthorizationEntry 方法 \_

設定虛擬機器的複寫授權專案。

## <a name="syntax"></a>語法


```mof
uint32 SetAuthorizationEntry(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 AuthorizationEntry,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要設定其授權專案的虛擬機器。

</dd> <dt>

*AuthorizationEntry* \[在\]
</dt> <dd>

[**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md)類別實例的字串表示，定義要用於虛擬機器的授權專案。

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

[**RemoveAuthorizationEntry**](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

