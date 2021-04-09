---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 SetResourceGroup 方法
description: 設定資源群組的類型和名稱。
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- SetResourceGroup 方法遠端桌面服務
- SetResourceGroup 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，SetResourceGroup 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843908"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Win32 TSGatewayResourceAuthorizationPolicy 類別的 SetResourceGroup 方法 \_

設定資源群組的類型和名稱。

## <a name="syntax"></a>語法


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ResourceGroupName* \[在\]
</dt> <dd>

資源群組名稱。 這個值會取代現有的 **ResourceGroupName** 屬性。

</dd> <dt>

*ResourceGroupType* \[在\]
</dt> <dd>

識別資源群組的類型。 這個值會取代現有的 **ResourceGroupType** 屬性。

<dt>

RG
</dt> <dd>

資源群組。

</dd> <dt>

CG
</dt> <dd>

電腦群組，儲存在 Active Directory Domain Services 中。

</dd> <dt>

ALL
</dt> <dd>

所有資源。

</dd> </dl> </dd> </dl>

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

