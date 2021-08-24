---
title: Win32_TSLicenseServer 類別的 ReactivateServerAutomatic 方法
description: 使用自動連線至網際網路，重新開機遠端桌面授權伺服器。
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- ReactivateServerAutomatic 方法遠端桌面服務
- ReactivateServerAutomatic 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，ReactivateServerAutomatic 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e822c441410ae3757f7cdb0a4a714b435facbb20e171646c889e2ea53ec82b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866038"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Win32 TSLicenseServer 類別的 ReactivateServerAutomatic 方法 \_

使用自動連線至網際網路，重新開機遠端桌面授權伺服器。

## <a name="syntax"></a>語法


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*原因* \[在\]
</dt> <dd>

啟用的原因。 它可以是下列值之一。

<dt>

0
</dt> <dd>

伺服器已重新部署。

</dd> <dt>

1
</dt> <dd>

憑證已損毀。

</dd> <dt>

2
</dt> <dd>

私密金鑰遭到盜用。

</dd> <dt>

3
</dt> <dd>

啟用金鑰已過期。

</dd> <dt>

4
</dt> <dd>

伺服器已升級。

</dd> </dl> </dd> <dt>

*ActivationStatus* \[擴展\]
</dt> <dd>

傳回的啟用狀態可以是下列其中一個值。

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

 

