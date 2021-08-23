---
description: 允許 TPM 擁有者停用或暫停 TPM。
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Disable Win32_Tpm 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a2bd76795cceaf299843b0b47f6f798d4471c67241f7c3fa206db52060bde745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668038"
---
# <a name="disable-method-of-the-win32_tpm-class"></a>Disable Win32 \_ Tpm 類別的方法

[**Win32 \_ tpm**](win32-tpm.md)類別的 **DISABLE** 方法可讓 tpm 擁有者停用或暫停 tpm。 如果呼叫可能會導致需要 BitLocker 修復，此方法會暫停 BitLocker。 布建 TPM 之後，BitLocker 會自動繼續。

## <a name="syntax"></a>語法


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OwnerAuth* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

識別 TPM 擁有者的字串。 此字串必須是 base64 編碼的字串，其中只包含20個位元組的二進位資料。 使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼轉譯為此預期的格式。 如果未提供任何參數，則會從登錄讀取 *OwnerAuth* 參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

下表列出一些常見的傳回碼。



| 傳回碼/值                                                                                                                                                                         | 描述                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                         | 此方法成功。<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | 提供的擁有者授權值無法執行要求。<br/>                                                                                                        |
| <dl> <dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt> </dl> | TPM 會防禦字典攻擊，並在一段時間內進行。 如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。<br/> |



 

## <a name="remarks"></a>備註

若要在沒有 TPM 擁有者授權值的情況下停用 TPM，請使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                      |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
