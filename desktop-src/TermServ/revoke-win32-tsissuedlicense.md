---
title: Revoke Win32_TSIssuedLicense 類別的方法
description: 撤銷遠端桌面服務的每一裝置用戶端存取授權 (RDS \ 160;Win32 TSIssuedLicense 物件所代表的每一裝置 Cal) \_ 。 這不是靜態函數。
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Revoke 方法遠端桌面服務
- Revoke 方法遠端桌面服務，Win32_TSIssuedLicense 類別
- Win32_TSIssuedLicense 類別遠端桌面服務、Revoke 方法
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686488"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a>Revoke Win32 \_ TSIssuedLicense 類別的方法

撤銷遠端桌面服務的每一裝置用戶端存取授權 (由 [**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md) 物件所代表的 RDS 每一裝置 cal) 。 這不是靜態函數。

## <a name="syntax"></a>語法


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RevokableCals* \[擴展\]
</dt> <dd>

與可撤銷的目前物件相同類型的 RDS Cal 數目。

</dd> <dt>

*NextRevokeAllowedOn* \[擴展\]
</dt> <dd>

系統管理員可以在下一次嘗試撤銷授權的日期。 當 **revoke** 方法呼叫失敗，因為已達到最大撤銷計數，此參數只會包含有效的資料。

</dd> </dl>

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

只有 RDS 每一裝置的 Cal 可以撤銷。

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

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> </dl>

 

