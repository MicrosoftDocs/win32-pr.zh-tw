---
description: 重設 TPM 製造商所實行的超時時間或其他機制，以防止對 TPM 授權值的字典攻擊。
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Win32_Tpm 類別的 ResetAuthLockOut 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 779ae7e8578019215e0bab1091512c64d68a84675d702ea7a0d8a5c37e8f081f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906298"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 ResetAuthLockOut 方法 \_

[**Win32 \_ tpm**](win32-tpm.md)類別的 **ResetAuthLockOut** 方法會重設 tpm 製造商所實行的超時時間或其他機制，以防止對 tpm 授權值的字典攻擊。 在字典攻擊中，攻擊者會嘗試透過徹底嘗試所有可能的值，來猜測正確的 TPM 授權值。

如果 TPM 因為輸入擁有者授權或其他授權值的錯誤嘗試太多次而遭到鎖定，請使用此方法。 當 TPM 被鎖定時，發出至 TPM 的部分或所有命令將會傳回錯誤，也就是執行 \_ \_ \_ \_ (0x80280803) 的 tpm E 防護鎖定。

> [!Note]  
> 此方法只能在 TPM 被鎖定時使用一次。如果提供給這個方法的擁有者授權不正確，TPM 將會鎖定整個超時期間，而重設鎖定的其他嘗試將會失敗。

 

## <a name="syntax"></a>語法


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OwnerAuth* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

識別 TPM 擁有者的字串。

此字串必須是 base64 編碼的 null 終止字串，其中包含剛好20個位元組的二進位資料。 使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼轉譯為此預期的格式。 如果未提供任何參數，則會從登錄讀取 *OwnerAuth* 參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。 下表列出一些常見的傳回值。



| 傳回碼/值                                                                                                                                                            | 描述                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                            | 此方法成功。<br/>                                                                                                                                                                                                                                     |
| <dl> <dt>**TPM \_E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl> | 提供的擁有者授權值不正確。 重設鎖定的其他嘗試將會失敗，並出現相同的錯誤。 請等到超時時間或其他製造商專屬的機制過期，再重試鎖定的 TPM 命令。<br/> |



 

## <a name="remarks"></a>備註

這個方法會 \_ 在 tpm 上呼叫 tpm ResetLockValue 命令。 這種方法的確切行為會因 TPM 製造商而異。 電腦或 TPM 製造商提供的檔，可能會提供反字典攻擊機制的執行其他資訊。

一般情況下，製造商可以藉由追蹤失敗的驗證來偵測字典攻擊。 如果失敗的數目或頻率很高，TPM 將會在一段時間內鎖定更多命令。 一般來說，最初的超時期間會很短，讓合法的使用者有機會修正此情況。 如果失敗持續發生，每個後續超時期間的持續時間可能會快速增加。

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
</dt> </dl>

 

 
