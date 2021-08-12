---
title: Win32_TSLicenseServer 類別的 AddLStoTSLSGroup 方法
description: 將遠端桌面授權伺服器新增至與遠端桌面授權伺服器相同網域中的網域控制站上的遠端桌面連線代理人 (RD 連線代理人) 授權伺服器群組。
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- AddLStoTSLSGroup 方法遠端桌面服務
- AddLStoTSLSGroup 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，AddLStoTSLSGroup 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf3d0464b42159ca1827caf579e21982c08d066495cd664ec1adfcaa883a4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610403"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a>Win32 TSLicenseServer 類別的 AddLStoTSLSGroup 方法 \_

將遠端桌面授權伺服器新增至與遠端桌面授權伺服器相同網域中的網域控制站上的遠端桌面連線代理人 (RD 連線代理人) 授權伺服器群組。

## <a name="syntax"></a>語法


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

您必須是 Domain Admins 群組的成員，才能呼叫這個方法。

如果伺服器設定為使用網域或樹系探索領域，則授權伺服器應該是 [遠端桌面授權伺服器] 群組的成員。

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

[**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

