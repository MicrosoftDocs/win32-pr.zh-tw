---
title: Win32_TSLicenseServer 類別的 UnpublishLS 方法
description: 從 Active Directory Domain Services Unpublishes 遠端桌面授權伺服器。
ms.assetid: 275854e2-85f6-4142-8bce-8d633bfcff7d
ms.tgt_platform: multiple
keywords:
- UnpublishLS 方法遠端桌面服務
- UnpublishLS 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，UnpublishLS 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnpublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ec183b5be8055dc30add5bc00a7eb537cd20f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508732"
---
# <a name="unpublishls-method-of-the-win32_tslicenseserver-class"></a>Win32 TSLicenseServer 類別的 UnpublishLS 方法 \_

從 Active Directory Domain Services Unpublishes 遠端桌面授權伺服器。

## <a name="syntax"></a>語法


```mof
uint32 UnpublishLS();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

若要呼叫這個方法，您必須以企業系統管理員的身分登入授權伺服器為其成員的樹系。

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

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

