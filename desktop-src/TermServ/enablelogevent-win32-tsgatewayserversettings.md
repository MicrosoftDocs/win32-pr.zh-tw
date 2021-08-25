---
title: Win32_TSGatewayServerSettings 類別的 EnableLogEvent 方法
description: 啟用或停用指定事件種類的記錄。
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- EnableLogEvent 方法遠端桌面服務
- EnableLogEvent 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，EnableLogEvent 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd70902649f6fadc66308ad35ce165a6d2fdb4654b73e056c3bc38f1850b3e07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871718"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a>Win32 TSGatewayServerSettings 類別的 EnableLogEvent 方法 \_

啟用或停用指定事件種類的記錄。

## <a name="syntax"></a>語法


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*事件名稱* \[在\]
</dt> <dd>

活動的名稱。 此值應該使用 [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) 方法來抓取。

<dt>

LogChannelDisconnect
</dt> <dd>

使用者已成功與資源中斷連線。

</dd> <dt>

LogFailedChannelConnect
</dt> <dd>

使用者無法連線到資源。

</dd> <dt>

LogFailureNetworkAccessCheck
</dt> <dd>

使用者連接授權失敗。

</dd> <dt>

LogFailureResourceAccessCheck
</dt> <dd>

使用者失敗的資源授權。

</dd> <dt>

LogSuccessChannelConnect
</dt> <dd>

使用者已成功連線至資源。

</dd> <dt>

LogSuccessfulNetworkAccessCheck
</dt> <dd>

使用者成功傳遞連接授權。

</dd> <dt>

LogSuccessfulResourceAccessCheck
</dt> <dd>

使用者已成功傳遞資源授權。

</dd> </dl> </dd> <dt>

*已啟用* \[在\]
</dt> <dd>

指定是否應啟用或停用事件。

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

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

