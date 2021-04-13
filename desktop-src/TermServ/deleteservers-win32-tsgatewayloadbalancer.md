---
title: Win32_TSGatewayLoadBalancer 類別的 DeleteServers 方法
description: 從伺服器屬性刪除伺服器。
ms.assetid: 5ef44725-82b6-464a-abab-a68cc8799669
ms.tgt_platform: multiple
keywords:
- DeleteServers 方法遠端桌面服務
- DeleteServers 方法遠端桌面服務，Win32_TSGatewayLoadBalancer 類別
- Win32_TSGatewayLoadBalancer 類別遠端桌面服務，DeleteServers 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b889f37b783853fbca0b9cb399a83959e2522d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384066"
---
# <a name="deleteservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Win32 TSGatewayLoadBalancer 類別的 DeleteServers 方法 \_

從 **伺服器** 屬性刪除伺服器。

## <a name="syntax"></a>語法


```mof
uint32 DeleteServers(
  [in] string Servers
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*伺服器* \[在\]
</dt> <dd>

要從 [ **伺服器** ] 屬性中刪除的 RD 閘道負載平衡伺服器清單（以分號分隔）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

如果 *伺服器* 參數中有多部伺服器，而且其中一個伺服器無法處理，則不會處理任何伺服器。

您必須是 Administrators 群組的成員，才能呼叫這個方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

