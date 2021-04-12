---
title: Win32_TSGatewayServerSettings 類別的 SetSslBridging 方法
description: 設定遠端桌面閘道 (RD 閘道) 伺服器所使用的 SSL 橋接類型。
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- SetSslBridging 方法遠端桌面服務
- SetSslBridging 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetSslBridging 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384866"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a>Win32 TSGatewayServerSettings 類別的 SetSslBridging 方法 \_

設定遠端桌面閘道 (RD 閘道) 伺服器所使用的 SSL 橋接類型。 此值會儲存在 **SslBridging** 屬性中。

> [!IMPORTANT]
> 使用這個方法變更 SSL 橋接類型時，必須重新開機 RD 閘道服務，才能讓此變更生效。

 

## <a name="syntax"></a>語法


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SslBridging* \[在\]
</dt> <dd>

類型： **uint32**

指定新的 SSL 橋接值。 這可以是下列其中一個值。

<dt>

0
</dt> <dd>

無 SSL 橋接。

</dd> <dt>

1
</dt> <dd>

HTTPS 至 HTTP 橋接。

</dd> <dt>

2
</dt> <dd>

HTTPS 至 HTTPS 橋接。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                        |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

