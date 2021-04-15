---
title: Win32_TSLicenseReport 類別的 DeleteReport 方法
description: 刪除遠端桌面授權伺服器上的報表物件。 這不是靜態方法。
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- DeleteReport 方法遠端桌面服務
- DeleteReport 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，DeleteReport 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a96c8626e4ecc1f89d0f2fcefa69845fec4df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508356"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a>Win32 TSLicenseReport 類別的 DeleteReport 方法 \_

刪除遠端桌面授權伺服器上的報表物件。 這不是靜態方法。

## <a name="syntax"></a>語法


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

這不是靜態方法。 您必須從每個使用者授權使用量報表物件呼叫這個方法。

您必須是 Administrators 群組的成員，才能呼叫這個方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

