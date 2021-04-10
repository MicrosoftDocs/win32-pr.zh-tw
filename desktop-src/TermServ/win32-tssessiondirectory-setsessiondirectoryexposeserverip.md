---
title: Win32_TSSessionDirectory 類別的 SetSessionDirectoryExposeServerIP 方法
description: 設定 SessionDirectoryExposeServerIP 屬性。
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- SetSessionDirectoryExposeServerIP 方法遠端桌面服務
- SetSessionDirectoryExposeServerIP 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，SetSessionDirectoryExposeServerIP 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934230"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a>Win32 TSSessionDirectory 類別的 SetSessionDirectoryExposeServerIP 方法 \_

設定 **SessionDirectoryExposeServerIP** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SessionDirectoryExposeServerIP* \[在\]
</dt> <dd>

類型： **uint32**

旗標停用或啟用 **SessionDirectoryExposeServerIP** 屬性，以允許或拒絕抓取會話目錄的 IP 位址。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

停用屬性。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

啟用屬性。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

