---
description: 將使用者提供的複雜密碼輸入轉譯為20位元組的擁有者授權，可用來與 TPM 互動。 TakeOwnership 和 ResetAuthLockOut 等方法都需要產生的擁有者授權值。
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Win32_Tpm 類別的 ConvertToOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 88d1b0f2056d6a10ac623421a7fe261acb832657d08c030ab3247f0acf1a0629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004646"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 ConvertToOwnerAuth 方法 \_

[**Win32 \_ Tpm**](win32-tpm.md)類別的 **ConvertToOwnerAuth** 方法會將使用者提供的複雜密碼輸入轉譯為20位元組的擁有者授權，以用來與 Tpm 互動。 [**TakeOwnership**](takeownership-win32-tpm.md)和 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md)等方法都需要產生的擁有者授權值。

轉換程式會遵循來自 [信任運算群組](https://www.trustedcomputinggroup.org/)的規格。

## <a name="syntax"></a>語法


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OwnerPassPhrase* \[在\]
</dt> <dd>

類型： **字串**

要轉換為擁有者授權值的字串。 字串可以包含任何數目的英數位元。

</dd> <dt>

*OwnerAuth* \[擴展\]
</dt> <dd>

類型： **字串**

衍生自 *OwnerPassPhrase* 參數的字串。 這個值是20位元組的二進位值，編碼為28位元組 base64 以 **null** 終止的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

下表列出一些常見的傳回碼。



| 傳回碼/值                                                                                                                                 | 描述                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

Unicode UTF-16LE 編碼的字串會藉由取得字串二進位標記法的 SHA-1 雜湊，轉換成20位元組的 TPM 擁有者授權值。 Unicode 字串的 **null** 終止不包含在雜湊中。 SHA-1 雜湊中未使用 salt。

例如，若要將 TPM 擁有者複雜密碼 "1Sample" 轉換成 TPM 擁有者授權值，則會從下列位元組資料流程取得 SHA-1 雜湊：

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

為了將零長度的複雜密碼轉換成擁有者授權值，會採用 **Null** 位元組資料流程的 sha-1 雜湊。

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

[**TakeOwnership**](takeownership-win32-tpm.md)
</dt> </dl>

 

 
