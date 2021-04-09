---
title: 'Win32_TSGatewayConnection 類別的 DisconnectUser 方法 (Tsgauthenticationengine) '
description: 將指定之使用者的所有連接從遠端桌面閘道的 (RD 閘道) 伺服器中斷連線。
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- DisconnectUser 方法遠端桌面服務
- DisconnectUser 方法遠端桌面服務，Win32_TSGatewayConnection 類別
- Win32_TSGatewayConnection 類別遠端桌面服務，DisconnectUser 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e223a2de36ad6c2a6fcabc446fe88cad27dc5da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686070"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a>Win32 TSGatewayConnection 類別的 DisconnectUser 方法 \_

將指定之使用者的所有連接從遠端桌面閘道的 (RD 閘道) 伺服器中斷連線。

## <a name="syntax"></a>語法


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

使用者 *名稱* \[在\]
</dt> <dd>

以 * Domain * UserName 格式的使用者名稱， **\\** 其連接會中斷連線。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                            |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                       |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                             |
| 標頭<br/>                   | <dl> <dt>Tsgauthenticationengine。h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSGateway mof</dt> </dl>             |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> </dl>

 

