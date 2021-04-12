---
title: Win32_TSGatewayServerSettings 類別的 GetIPAndPort 方法
description: 取得指定傳輸的接聽 IP 位址和埠號碼。
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- GetIPAndPort 方法遠端桌面服務
- GetIPAndPort 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，GetIPAndPort 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317160"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Win32 TSGatewayServerSettings 類別的 GetIPAndPort 方法 \_

取得指定傳輸的接聽 IP 位址和埠號碼。

## <a name="syntax"></a>語法


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
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

*IPAddress* \[擴展\]
</dt> <dd>

接收接聽 IP 位址的字串，以八位格式 (例如 "192.168.1.1" ) 。

</dd> <dt>

*埠* \[擴展\]
</dt> <dd>

指定接聽埠號碼。

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

 

 





