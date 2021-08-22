---
description: 將 TPM 重設為其原廠預設狀態。
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Win32_Tpm 類別的 Clear 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c9c3185fceb315cf9c36caa7de1e450820ad25ce1b31fefc8135c4d57fd76597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892645"
---
# <a name="clear-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 Clear 方法 \_

[**Win32 \_ tpm**](win32-tpm.md)類別的 **CLEAR** 方法會將 Tpm 重設為其原廠預設狀態。 TPM 擁有者可以使用這個方法來取消 TPM 擁有權，並使前一個擁有者所建立的密碼編譯材質失效。 如果呼叫可能會導致需要 BitLocker 修復，此方法會暫停 BitLocker。 布建 TPM 之後，BitLocker 會自動繼續。

> [!Caution]  
> 藉由清除 TPM，您將會遺失應用程式所建立和使用的所有 TPM 金鑰。 如果使用這些金鑰來將資料加密，請確定您有另一種方式可以在清除 TPM 之前存取資料。

 

## <a name="syntax"></a>語法


```mof
uint32 Clear(
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



| 傳回碼/值                                                                                                                                                                         | Description                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                         | 此方法成功。<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | 提供的擁有者授權值無法執行要求。<br/>                                                                                                        |
| <dl> <dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt> </dl> | TPM 會防禦字典攻擊，並在一段時間內進行。 如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。<br/> |



 

## <a name="remarks"></a>備註

執行此方法可協助準備配備 TPM 的電腦以進行回收。

若要清除 TPM，但不再擁有 TPM 擁有者授權，您需要電腦的實體存取權。 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)方法包含的功能可協助您清除沒有 tpm 擁有者授權的 tpm。

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

 

 
