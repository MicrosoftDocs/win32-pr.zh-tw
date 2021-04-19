---
title: Win32_TSLicenseServer 類別的 IsLSinTSLSGroup 方法
description: 抓取遠端桌面授權伺服器是否為指定網域中網域控制站上的遠端桌面授權伺服器群組的成員。
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- IsLSinTSLSGroup 方法遠端桌面服務
- IsLSinTSLSGroup 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsLSinTSLSGroup 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106993748"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a>Win32 TSLicenseServer 類別的 IsLSinTSLSGroup 方法 \_

抓取遠端桌面授權伺服器是否為指定網域中網域控制站上的遠端桌面授權伺服器群組的成員。

## <a name="syntax"></a>語法


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*網域* \[在\]
</dt> <dd>

網域名稱。

</dd> <dt>

*IsMember* \[擴展\]
</dt> <dd>

布林值，指出授權伺服器是否為網域中的遠端桌面授權伺服器群組的成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

如果未提供功能變數名稱，則會查詢授權伺服器所在網域中的網域控制站。

如果伺服器設定為使用網域或樹系探索領域，則授權伺服器應為遠端桌面授權伺服器群組的成員。 如果授權伺服器不是此群組的成員，則每位使用者的授權追蹤和報告將無法運作。

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
</dt> <dt>

[**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

