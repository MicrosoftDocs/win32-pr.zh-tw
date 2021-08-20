---
title: Win32_TSGatewayServerSettings 類別的 RecycleRpcApplicationPools 方法
description: 回收 IIS 中的 RPC 應用程式集區。
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- RecycleRpcApplicationPools 方法遠端桌面服務
- RecycleRpcApplicationPools 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，RecycleRpcApplicationPools 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03be03b67e0e6e5c40c73624a08d8a8898022e73f1c716085eefe456f3623d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127925"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a>Win32 TSGatewayServerSettings 類別的 RecycleRpcApplicationPools 方法 \_

回收 IIS 中的 RPC 應用程式集區。

## <a name="syntax"></a>語法


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **uint32**

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

呼叫這個方法會導致所有現有的連接中斷。

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
</dt> <dt>

[**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 

