---
title: Win32_TSGatewayServerSettings 類別的 EnableTransport 方法
description: 啟用或停用指定的傳輸。
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- EnableTransport 方法遠端桌面服務
- EnableTransport 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，EnableTransport 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08087c4a28b0867f7457bed597a71c5156ea968fb50f3f2509c8da5ef3057fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059596"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a>Win32 TSGatewayServerSettings 類別的 EnableTransport 方法 \_

啟用或停用指定的傳輸。

## <a name="syntax"></a>語法


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
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

*啟用* \[在\]
</dt> <dd>

指定傳輸為啟用或停用。

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

 

 





