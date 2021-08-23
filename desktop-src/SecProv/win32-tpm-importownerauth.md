---
description: 匯入已擁有作業系統登錄之 TPM 的擁有者授權資訊。
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: Win32_Tpm：： ImportOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6e7d96a5cadf77e539d703ed95f428fa91535d49d1e7b5581300467782fce0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004076"
---
# <a name="win32_tpmimportownerauth-method"></a>Win32 \_ Tpm：： ImportOwnerAuth 方法

匯入已擁有作業系統登錄之 TPM 的擁有者授權資訊。 這項作業會先驗證提供的擁有者授權資訊是否正確。 如果正確，方法會將此資訊匯入至登錄。

只有本機系統管理員才能存取此方法。

## <a name="syntax"></a>語法


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OwnerAuth* \[在\]
</dt> <dd>

TPM 的有效擁有者授權資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。

常見的傳回碼如下所示。



| 傳回碼/值                                                                                                                                 | 描述                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

在 TPM 處於「可縮減功能狀態」的情況下，此方法特別有用，而且需要匯入擁有者授權才能完全就緒，或在其中一個作業系統擁有 TPM 的雙重開機案例中，以及在其他作業系統中無法使用 TPM 的擁有者授權資訊。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                      |
| 命名空間<br/>                | \\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
