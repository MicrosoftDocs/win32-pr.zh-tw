---
title: Win32_TSGatewayServerSettings 類別的 EnableCentralCAP 方法
description: 控制 CentralCAPEnabled 屬性，此屬性會控制 (RD \ 160; 的遠端桌面服務連線授權原則。遠端桌面閘道 (RD 閘道) server 的 Cap) 。
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- EnableCentralCAP 方法遠端桌面服務
- EnableCentralCAP 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，EnableCentralCAP 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53bc180d2f4636ed2fd8d7b32d819a9d953416e4022b5cf4c18a900b15776fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574758"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a>Win32 TSGatewayServerSettings 類別的 EnableCentralCAP 方法 \_

控制 **CentralCAPEnabled** 屬性，此屬性會控制遠端桌面閘道 (RD 閘道) 伺服器的遠端桌面服務連線授權原則 (RD cap) 。

## <a name="syntax"></a>語法


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CentralCAPEnabled* \[在\]
</dt> <dd>

如果設定為 **True**，將會使用來自中央 RD CAP 伺服器的 RD cap。 如果設定為 **False**，則只會使用來自本機伺服器的原則。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

