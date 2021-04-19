---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 DisablePrinters 方法
description: 設定 PrintersDisabled 屬性。 如果 DeviceRedirectionType 屬性的值為 \ 0034; 2 \ 0034;，則 PrintersDisabled 屬性會控制透過遠端桌面閘道 (RD 閘道) 伺服器所建立之會話的印表機重新導向。
ms.assetid: bf58d226-e3de-4c2b-aaa9-9e7ddbf49d31
ms.tgt_platform: multiple
keywords:
- DisablePrinters 方法遠端桌面服務
- DisablePrinters 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，DisablePrinters 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePrinters
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625425170bd5e29b953db8299048261e9351bff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106993742"
---
# <a name="disableprinters-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Win32 TSGatewayConnectionAuthorizationPolicy 類別的 DisablePrinters 方法 \_

設定 **PrintersDisabled** 屬性。 如果 **DeviceRedirectionType** 屬性的值為 "2"， **PrintersDisabled** 屬性會控制透過遠端桌面閘道 (RD 閘道) server 所建立之會話的印表機重新導向。

## <a name="syntax"></a>語法


```mof
uint32 DisablePrinters(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*已停用* \[在\]
</dt> <dd>

**PrintersDisabled** 屬性的新值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

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

 

