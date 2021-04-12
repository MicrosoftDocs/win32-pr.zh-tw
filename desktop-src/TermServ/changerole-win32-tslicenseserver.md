---
title: Win32_TSLicenseServer 類別的 ChangeRole 方法
description: 變更遠端桌面授權伺服器的探索領域。 探索領域會決定網路上) 伺服器遠端桌面工作階段主機 (RD 工作階段主機可以自動探索授權伺服器。
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- ChangeRole 方法遠端桌面服務
- ChangeRole 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，ChangeRole 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464693"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a>Win32 TSLicenseServer 類別的 ChangeRole 方法 \_

變更遠端桌面授權伺服器的探索領域。 探索領域會決定網路上) 伺服器遠端桌面工作階段主機 (RD 工作階段主機可以自動探索授權伺服器。

## <a name="syntax"></a>語法


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ServerRole* \[在\]
</dt> <dd>

遠端桌面授權伺服器的探索領域。 您可以設定下列其中一個值。

<dt>

0
</dt> <dd>

相同工作組中的 RD 工作階段主機伺服器可以探索授權伺服器。

</dd> <dt>

1
</dt> <dd>

相同網域中 RD 工作階段主機伺服器可以探索授權伺服器。 您必須以網域系統管理員的身分登入，才能設定此值。

</dd> <dt>

2
</dt> <dd>

相同樹系中的多個網域 RD 工作階段主機伺服器可以探索授權伺服器。 您必須以企業系統管理員的身分登入，才能設定此值。

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

 

