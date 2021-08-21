---
description: 變更 TPM 擁有者授權值。
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Win32_Tpm 類別的 ChangeOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 02ca13049df20c57eeb5cc594bde1b247df0eb3829c757b64b8bd31f87e3796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004676"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 ChangeOwnerAuth 方法 \_

[**Win32 \_ tpm**](win32-tpm.md)類別的 **CHANGEOWNERAUTH** 方法會變更 Tpm 擁有者授權值。

## <a name="syntax"></a>語法


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OldOwnerAuth* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

為裝置的目前 TPM 擁有者授權值命名的字串。 使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將密碼轉譯為此授權值。 未提供 *OldOwnerAuth* 參數或提供空字串，這個方法會從登錄中取得值（如果有的話）。

</dd> <dt>

*NewOwnerAuth* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

為新的 TPM 擁有者授權值命名的字串。 使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將密碼轉譯為此授權值。 *NewOwnerAuth* 參數不可為空白或 **Null。**

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

下表列出一些常見的傳回碼。



| 傳回碼/值                                                                                                                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                              | 此方法成功。<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**TPM \_E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | 目前的 TPM 擁有者授權值不正確。<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt> </dl>      | TPM 會防禦字典攻擊，並在一段時間內進行。 如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。<br/>                                                                                                                                                                                                             |
| <dl> <dt>**FVE \_E \_ AD \_ 架構 \_ 未 \_ 安裝**</dt> <dt>2150694922 (0x8031000A)</dt> </dl> | 無法將修復資訊儲存到網路。 電腦已設定為將修復資訊儲存至 Active Directory Domain Services。 如需有關如何設定 Active Directory 的指示，請參閱 [BitLocker 磁碟機加密設定指南：將 BitLocker 和 TPM 修復資訊備份至 Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10))。<br/> |
| <dl> <dt>**連接失敗**</dt> <dt>2147943755 (0x8007054B)</dt> </dl>                  | 無法將修復資訊儲存到網路。 電腦已設定為將修復資訊儲存至 Active Directory Domain Services。 需要網路連接才能繼續。<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>備註

如果已設定適當的群組原則設定， **ChangeOwnerAuth** 方法會將新的 TPM 擁有者授權備份至 Active Directory Domain Services。

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

 

 
