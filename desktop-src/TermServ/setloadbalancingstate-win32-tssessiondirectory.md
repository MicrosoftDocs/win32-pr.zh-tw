---
title: Win32_TSSessionDirectory 類別的 SetLoadBalancingState 方法
description: 設定值，指出伺服器是否將參與遠端桌面連線代理人 (RD 連線代理人) 負載平衡。
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- SetLoadBalancingState 方法遠端桌面服務
- SetLoadBalancingState 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，SetLoadBalancingState 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d539f07c97e4e5b92152190a7bb38a8132d31a73daf08de8f140a39f67efdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987948"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>Win32 TSSessionDirectory 類別的 SetLoadBalancingState 方法 \_

設定值，指出伺服器是否將參與遠端桌面連線代理人 (RD 連線代理人) 負載平衡。

## <a name="syntax"></a>語法


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StateValue* \[在\]
</dt> <dd>

類型： **uint32**

指出伺服器是否將參與 RD 連線代理人負載平衡。

<dt>

0
</dt> <dd>

伺服器將不會參與 RD 連線代理人負載平衡。

</dd> <dt>

1
</dt> <dd>

伺服器將參與 RD 連線代理人負載平衡。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

伺服器必須加入 RD 連線代理人中的伺服器陣列。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

