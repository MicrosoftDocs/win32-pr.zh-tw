---
title: Win32_TSLicenseServer 類別的 IsLSSecGrpGPEnabled 方法
description: 抓取 \ 0034; 授權伺服器安全性群組 \ 0034;遠端桌面授權伺服器上已啟用群組原則設定。
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- IsLSSecGrpGPEnabled 方法遠端桌面服務
- IsLSSecGrpGPEnabled 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsLSSecGrpGPEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104303"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a>Win32 TSLicenseServer 類別的 IsLSSecGrpGPEnabled 方法 \_

抓取是否已在遠端桌面授權伺服器上啟用 [授權伺服器安全性群組] 群組原則設定。

## <a name="syntax"></a>語法


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*已啟用* \[擴展\]
</dt> <dd>

指出是否已啟用 [授權伺服器安全性群組] 原則設定的布林值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

[授權伺服器安全性群組] 原則設定可讓您指定遠端桌面工作階段主機 (RD 工作階段主機) 伺服器，以允許連線到授權伺服器，遠端桌面服務 RDS Cal (取得) 用戶端存取授權。 如果授權伺服器上已啟用此原則設定，則伺服器只會回應電腦帳戶是授權伺服器上終端機伺服器電腦本機群組成員之 RD 工作階段主機伺服器的 RDS CAL 要求。

原則設定位於本機群組原則編輯器的下列節點中：

電腦設定 \\ 系統管理範本 \\ Windows 元件 \\ 終端機服務 \\ TS 授權

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

 

