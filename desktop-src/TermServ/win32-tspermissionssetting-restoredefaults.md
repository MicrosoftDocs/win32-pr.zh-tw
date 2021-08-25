---
title: 'Win32_TSPermissionsSetting 類別的 RestoreDefaults 方法 (Netfw) '
description: 還原終端機的預設許可權集合值。
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- RestoreDefaults 方法遠端桌面服務
- RestoreDefaults 方法遠端桌面服務，Win32_TSPermissionsSetting 類別
- Win32_TSPermissionsSetting 類別遠端桌面服務，RestoreDefaults 方法
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef81f4b3008f68129026a90d1b2e98e8c13c298537952175e116c9c8e02c4f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769448"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Win32 TSPermissionsSetting 類別的 RestoreDefaults 方法 \_

**RestoreDefaults** 方法會還原終端機的預設許可權集合值。

## <a name="syntax"></a>語法


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

成功時傳回成功，否則失敗。

## <a name="remarks"></a>備註

預設許可權如下：

-   [系統管理員]、[系統] 和 [遠端桌面] 說明小幫手帳戶都具有 [遠端桌面服務許可權](terminal-services-permissions.md)。
-   [遠端桌面使用者] 帳戶具有 [登入]、[連線]、[查詢資訊] 和 [傳送訊息] 許可權。
-   本機服務和網路服務帳戶具有查詢資訊和傳送訊息許可權。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Netfw。h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

