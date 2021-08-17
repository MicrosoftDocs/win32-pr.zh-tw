---
title: Win32_TSGatewayServerSettings 類別的 SetIPAndPort 方法
description: 設定指定傳輸的接聽 IP 位址和埠號碼。
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- SetIPAndPort 方法遠端桌面服務
- SetIPAndPort 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetIPAndPort 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af40c52523869e07268a26d858e0e70b933431a6583998c9d0041f476678d243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137971"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Win32 TSGatewayServerSettings 類別的 SetIPAndPort 方法 \_

設定指定傳輸的接聽 IP 位址和埠號碼。

## <a name="syntax"></a>語法


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TransportType* \[在\]
</dt> <dd>

指定傳輸類型。 這必須是下列值之一。

<dt>

0
</dt> <dd>

RPC over HTTP 傳輸。

</dd> <dt>

1
</dt> <dd>

HTTP 傳輸。

</dd> <dt>

2
</dt> <dd>

UDP 傳輸。

</dd> </dl> </dd> <dt>

*IPAddress* \[在\]
</dt> <dd>

以八位格式指定接聽的 IP 位址 (例如 "192.168.1.1" ) 。

</dd> <dt>

*埠* \[在\]
</dt> <dd>

指定接聽埠號碼。

</dd> <dt>

*OverrideExisting* \[在\]
</dt> <dd>

指出是否要覆寫 HTTP 的現有 IP/埠系結。 只有在 *TransportType* 參數包含 0 (RPC over HTTP) 或 1 (HTTP) 時，才會使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                           |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





