---
title: Win32_TSClientSetting 類別的 ConnectionSettings 方法
description: ConnectionSettings 方法會設定適用于連接和登入程式的會話設定。
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- ConnectionSettings 方法遠端桌面服務
- ConnectionSettings 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，ConnectionSettings 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f48a93959b1e86eb77f6ab0fbfab444444ca1c077835e1c28330d34ed66c87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656168"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Win32 TSClientSetting 類別的 ConnectionSettings 方法 \_

**ConnectionSettings** 方法會設定適用于連接和登入程式的會話設定。

## <a name="syntax"></a>語法


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ConnectClientDrivesAtLogon* \[在\]
</dt> <dd>

旗標：啟用或停用 **ConnectClientDrivesAtLogon** 屬性，指定在登入程式期間是否自動連接用戶端的磁片磁碟機。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

用戶端的磁片磁碟機不會自動連線。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

用戶端的磁片磁碟機會自動連接。

</dd> </dl> </dd> <dt>

*ConnectPrinterAtLogon* \[在\]
</dt> <dd>

旗標：啟用或停用 **ConnectPrinterAtLogon** 屬性，指定在登入程式期間是否會自動連接所有對應的本機用戶端印表機。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

所有對應的本機印表機都不會自動連接。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

所有對應的本機印表機都會自動連接。

</dd> </dl> </dd> <dt>

*DefaultToClientPrinter* \[在\]
</dt> <dd>

旗標：啟用或停用 **DefaultToClientPrinter** 屬性，指定列印工作是否自動傳送至用戶端的本機印表機。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

列印工作不會自動傳送。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

列印工作會自動傳送。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果伺服器已覆寫使用者的連接設定，此方法會傳回錯誤。

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

