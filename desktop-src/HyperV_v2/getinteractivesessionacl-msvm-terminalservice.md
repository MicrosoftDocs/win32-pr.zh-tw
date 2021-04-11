---
description: 抓取 (DACL) 的目前任意存取控制清單，以控制對虛擬機器的互動式會話的存取。
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Msvm_TerminalService 類別的 GetInteractiveSessionACL 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690795"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a>Msvm TerminalService 類別的 GetInteractiveSessionACL 方法 \_

抓取 (DACL) 的目前 *任意存取控制清單* ，以控制對虛擬機器的互動式會話的存取。

## <a name="syntax"></a>語法


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，該類別代表將抓取其 DACL 的虛擬機器。

</dd> <dt>

*AccessControlList* \[擴展\]
</dt> <dd>

字串陣列，其中每個字串都包含 [**Msvm \_ InteractiveSessionACE**](msvm-interactivesessionace.md) 類別的內嵌實例，表示虛擬機器互動式會話 DACL 中 (ACE) 的 *存取控制專案* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**失敗** (2) 
</dt> <dt>

**Timeout** (3) 
</dt> <dt>

**不正確參數** (4) 
</dt> <dt>

**不正確狀態** (5) 
</dt> <dt>

 (6) 的 **參數不相容**
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**方法保留** (4097. 32767) 
</dt> <dt>

**廠商特定** (32768. 65535) 
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

[**Msvm \_ TerminalService**](msvm-terminalservice.md)
</dt> </dl>

 

 




