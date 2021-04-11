---
description: 安裝 TPM 的擁有者。
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Win32_Tpm 類別的 TakeOwnership 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027396"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 TakeOwnership 方法 \_

[**Win32 \_ tpm**](win32-tpm.md)類別的 **TAKEOWNERSHIP** 方法會安裝 Tpm 的擁有者。 TPM 的擁有者可完全使用 TPM 功能。 設定擁有者之後，沒有其他使用者或軟體可以宣告 TPM 的擁有權。

[**IsEnabled**](isenabled-win32-tpm.md)、 [**IsActivated**](isactivated-win32-tpm.md)和 [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)方法都必須是 true，才能成功進行 **TakeOwnership** 方法。

## <a name="syntax"></a>語法


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OwnerAuth* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

識別 TPM 擁有者的字串。 此字串必須是 base64 編碼的 null 終止字串，其中包含剛好20個位元組的二進位資料。 使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼轉譯為此預期的格式。 如果未提供任何參數，則會從登錄讀取 *OwnerAuth* 參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

下表列出一些常見的傳回碼。



| 傳回碼/值                                                                                                                                                                         | Description                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                         | 此方法成功。<br/>                                                                                                                                                                              |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | *OwnerAuth* 參數無效。<br/>                                                                                                                                                                 |
| <dl> <dt>**TPM \_E \_ 擁有者 \_ 設定**</dt> <dt>2150105108 (0x80280014)</dt> </dl>            | TPM 上已有擁有者。<br/>                                                                                                                                                                     |
| <dl> <dt>**TPM \_E \_ NO \_ 背書**</dt> <dt>2150105123 (0x80280023)</dt> </dl>       | 在 TPM 上找不到簽署金鑰。<br/> 若要在 TPM 上建立簽署金鑰組，請參閱 [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) 方法。<br/>             |
| <dl> <dt>**TPM \_E \_ 安裝 \_ 已停用**</dt>的 <dt>2150105099 (0x8028000B)</dt> </dl>     | 無法在此 TPM 上安裝擁有者。<br/> 如需如何允許安裝裝置擁有者的相關資訊，請參閱 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)。<br/> |
| <dl> <dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt> </dl> | TPM 會防禦字典攻擊，並在一段時間內進行。 如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。<br/>                               |



 

## <a name="remarks"></a>備註

[**IsEnabled**](isenabled-win32-tpm.md)、 [**IsActivated**](isactivated-win32-tpm.md)和 [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)方法都必須為 true，才能成功完成 **TakeOwnership** 。

您應該使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼變更為用於 *OwnerAuth* 參數的輸入值。

如果已設定適當的群組原則設定， **TakeOwnership** 方法會將擁有者授權值備份至 Active Directory。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                      |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
