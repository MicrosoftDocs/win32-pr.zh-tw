---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 AddComputerGroupNames 方法
description: 將指定的電腦群組名加入至 ComputerGroupNames 屬性。
ms.assetid: f0c440d6-0cc2-48b4-b656-65f12e652151
ms.tgt_platform: multiple
keywords:
- AddComputerGroupNames 方法遠端桌面服務
- AddComputerGroupNames 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，AddComputerGroupNames 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495eecd7058a2baa854a02d93d05a66510ac5cc38fd897a3310d4acb15e0ef2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757884"
---
# <a name="addcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Win32 TSGatewayConnectionAuthorizationPolicy 類別的 AddComputerGroupNames 方法 \_

將指定的電腦群組名加入至 **ComputerGroupNames** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 AddComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ComputerGroupNames* \[在\]
</dt> <dd>

要加入至 **ComputerGroupNames** 屬性的電腦群組名清單（以分號分隔）。 電腦群組名的格式應為 *網域 \\ ComputerGroupName*。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

如果 *ComputerGroupNames* 參數中有多個電腦群組名，而且其中一個名稱無法處理，則不會處理任何名稱。

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

