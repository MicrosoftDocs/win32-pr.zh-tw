---
description: 取得 TPM 的擁有者授權資訊（如果登錄中有提供的話）。
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: Win32_Tpm：： GetOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a441b07af31758212152b657ccb033d8abdeebbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511151"
---
# <a name="win32_tpmgetownerauth-method"></a>Win32 \_ Tpm：： GetOwnerAuth 方法

取得 TPM 的擁有者授權資訊（如果登錄中有提供的話）。 如果使用預設設定在 Windows 8 中擁有或布建 TPM，TPM 擁有者授權資訊會儲存在登錄中，而且可供此方法使用。

只有本機系統管理員才能存取此方法。

## <a name="syntax"></a>語法


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OwnerAuth* \[擴展\]
</dt> <dd>

TPM 的擁有者授權資訊（如果登錄中有提供的話）。

</dd> </dl>

## <a name="return-value"></a>傳回值

您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。

常見的傳回碼如下所示。



| 傳回碼/值                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                      |
| 命名空間<br/>                | \\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
