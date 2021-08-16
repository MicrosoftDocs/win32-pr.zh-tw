---
title: Win32_TSLicenseServer 類別的 IsTSCGroupPresent 方法
description: IsTSCGroupPresent 不再提供 Windows Server 2012 使用。
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- IsTSCGroupPresent 方法遠端桌面服務
- IsTSCGroupPresent 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsTSCGroupPresent 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4711236541999264a5a6f96066050f709cdcc087a751e0e56ddd6dea1b9103da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351337"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a>Win32 TSLicenseServer 類別的 IsTSCGroupPresent 方法 \_

\[**IsTSCGroupPresent** 不再提供 Windows Server 2012 使用。\]

不支援這個方法。

**Windows server 2008 R2 和 Windows server 2008：** 抓取終端機伺服器電腦本機群組是否存在於遠端桌面授權伺服器上。

## <a name="syntax"></a>語法


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*存在* \[擴展\]
</dt> <dd>

指出終端機伺服器電腦本機群組是否存在的布林值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **\_ \_ 不 \_ 支援的 WBEM E**。

**Windows server 2008 R2 和 Windows server 2008：** 如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 用戶端支援結束<br/>    | 都不支援<br/>                                                                 |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                                                         |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

