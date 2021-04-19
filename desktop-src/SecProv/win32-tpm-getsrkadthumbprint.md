---
description: 取得 TPM 儲存根金鑰公開部分之指定模數的儲存根金鑰指紋。
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: Win32_Tpm：： GetSrkADThumbprint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973240"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>Win32 \_ Tpm：： GetSrkADThumbprint 方法

取得 TPM 儲存根金鑰公開部分之指定模數的儲存根金鑰指紋。 如果透過群組原則設定啟用 TPM 擁有者授權資訊的 Active Directory 備份，則會使用指紋來為 Active Directory 伺服器上的儲存體根金鑰編制索引。

> [!Note]  
> 從 Windows 10 1607 版開始，TPM 擁有者授權永遠不會備份到 Active Directory。

 

只有本機系統管理員才能存取此方法。

## <a name="syntax"></a>語法


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SrkPublicKeyModulus* \[在\]
</dt> <dd>

TPM 儲存根金鑰之公開部分的模數。 您也可以使用 [Win32 \_ TPM](win32-tpm.md)類別的 [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md)方法來取得它。

</dd> <dt>

*SrkADThumbprint* \[擴展\]
</dt> <dd>

傳回20位元組陣列，其中包含給定模數的儲存體根金鑰指紋。

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

 

 
