---
description: Msvm_SecurityService 類別的 SetSecurityPolicy 方法：設定虛擬系統的金鑰保護裝置。
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Msvm_SecurityService 類別的 SetSecurityPolicy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3ce4e95fe99eca0616d886ca16fefcb771be50f1a8cc0a46e6780e0411a6ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147092"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a>Msvm SecurityService 類別的 SetSecurityPolicy 方法 \_

設定虛擬系統的金鑰保護裝置。

## <a name="syntax"></a>語法


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SecuritySettingData* \[在\]
</dt> <dd>

字串包含 [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) 類別的內嵌實例，代表虛擬系統的安全性設定。

</dd> <dt>

*SecurityPolicy* \[在\]
</dt> <dd>

原始位元組陣列，包含要設定的安全性原則。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。 如果作業是以非同步方式執行，則傳回值為4096。

</dd> </dl>

## <a name="return-value"></a>傳回值

在上，success 會傳回 0;否則，會傳回錯誤。

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
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 




