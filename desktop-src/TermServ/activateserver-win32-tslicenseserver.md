---
title: Win32_TSLicenseServer 類別的 ActivateServer 方法
description: 使用透過電話或網際網路取得的遠端桌面授權伺服器識別碼，啟用遠端桌面授權伺服器。
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- ActivateServer 方法遠端桌面服務
- ActivateServer 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，ActivateServer 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969209"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a>Win32 TSLicenseServer 類別的 ActivateServer 方法 \_

使用透過電話或網際網路取得的遠端桌面授權伺服器識別碼，啟用遠端桌面授權伺服器。

## <a name="syntax"></a>語法


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sLicenseServerId* \[在\]
</dt> <dd>

透過電話或網際網路取得的遠端桌面授權伺服器識別碼。 *SLicenseServerId* 參數是35字元的英數位元字串，不能包含連字號。

</dd> <dt>

*ActivationStatus* \[擴展\]
</dt> <dd>

傳回的啟用狀態可以是下列其中一項。

<dt>

0
</dt> <dd>

啟用遠端桌面授權伺服器。

</dd> <dt>

1
</dt> <dd>

未啟用遠端桌面授權伺服器。

</dd> <dt>

2
</dt> <dd>

發生未知的錯誤。 不知道是否啟用遠端桌面授權伺服器。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

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

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

