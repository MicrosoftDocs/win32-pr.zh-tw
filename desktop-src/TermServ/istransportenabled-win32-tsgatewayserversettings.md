---
title: Win32_TSGatewayServerSettings 類別的 IsTransportEnabled 方法
description: 判斷指定的傳輸是否已啟用。
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- IsTransportEnabled 方法遠端桌面服務
- IsTransportEnabled 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，IsTransportEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da152499138f6c1aba1ff6477c719aa0e787deee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094471"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Win32 TSGatewayServerSettings 類別的 IsTransportEnabled 方法 \_

判斷指定的傳輸是否已啟用。

## <a name="syntax"></a>語法


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
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

*已啟用* \[擴展\]
</dt> <dd>

**布林** 值，指出是否已啟用傳輸。

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

 

 





