---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 Update 方法
description: 更新目前的遠端桌面資源授權原則 (RD \ 160;RAP) 。
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Update 方法遠端桌面服務
- Update 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，Update 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330bf14759f7cdef129a4c34b32acde1d610619c7f54f7d6ec95789e6bec390f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868918"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Win32 TSGatewayResourceAuthorizationPolicy 類別的 Update 方法 \_

 (RD RAP) 更新目前的遠端桌面資源授權原則。

## <a name="syntax"></a>語法


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

RD RAP 的名稱。

</dd> <dt>

*描述* \[在\]
</dt> <dd>

RD RAP 的描述。

</dd> <dt>

*已啟用* \[在\]
</dt> <dd>

指出是否應該啟用 RD RAP。

</dd> <dt>

*ResourceGroupName* \[在\]
</dt> <dd>

與此 RD RAP 相關聯的資源組名。

</dd> <dt>

*ResourceGroupType* \[在\]
</dt> <dd>

資源群組類型。

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

</dd> </dl> </dd> <dt>

*UserGroupNames* \[在\]
</dt> <dd>

以分號分隔的使用者組名清單。 名稱的格式為 *網域 \\ UserGroupName*。 如果使用者隸屬于這些使用者群組中的任何一項，則會允許存取。

</dd> <dt>

*ProtocolNames* \[在\]
</dt> <dd>

針對此原則啟用的通訊協定名稱清單（以分號分隔）。 名稱必須符合 [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)類別的 [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)方法傳回。

</dd> <dt>

*PortNumbers* \[在\]
</dt> <dd>

針對此原則啟用的埠號碼清單（以分號分隔）。 若要允許任何埠號碼，請設定 " \* "。

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

