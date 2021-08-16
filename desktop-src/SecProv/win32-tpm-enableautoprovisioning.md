---
description: 啟用 TPM 的自動布建（如果目前已停用）。
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: Win32_Tpm：： EnableAutoProvisioning 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 111073fc6f1a8c047182a33240c1cf1e7f3ed29260e9f7b1a390360dc6538c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891011"
---
# <a name="win32_tpmenableautoprovisioning-method"></a>Win32 \_ Tpm：： EnableAutoProvisioning 方法

啟用 TPM 的自動布建（如果目前已停用）。 如果已啟用自動布建，則作業沒有任何作用。 預設會啟用 Windows 8 和 Windows Server 2012 的自動布建。

只有本機系統管理員才能存取此方法。

## <a name="syntax"></a>語法


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                      |
| 命名空間<br/>                | \\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
