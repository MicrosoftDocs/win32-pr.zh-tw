---
title: Win32_TSGatewayResourceGroup 類別的 Update 方法
description: 更新資源群組。
ms.assetid: b5927046-f461-41cd-861b-0fd77f2008e5
ms.tgt_platform: multiple
keywords:
- Update 方法遠端桌面服務
- Update 方法遠端桌面服務，Win32_TSGatewayResourceGroup 類別
- Win32_TSGatewayResourceGroup 類別遠端桌面服務，Update 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c2f32e7f0c06f67ad0d32a7754c701097320564c5c01de3c348b9935b8b702
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423908"
---
# <a name="update-method-of-the-win32_tsgatewayresourcegroup-class"></a>Win32 TSGatewayResourceGroup 類別的 Update 方法 \_

更新資源群組。

## <a name="syntax"></a>語法


```mof
uint32 Update(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

資源群組的名稱。

</dd> <dt>

*描述* \[在\]
</dt> <dd>

資源群組的描述。

</dd> <dt>

*資源* \[在\]
</dt> <dd>

此資源群組中的資源清單（以分號分隔）。 「」 \* 表示所有資源。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

如果 *resources* 參數中有多個資源，而且其中一個資源無法處理，則不會處理任何資源。

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

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

