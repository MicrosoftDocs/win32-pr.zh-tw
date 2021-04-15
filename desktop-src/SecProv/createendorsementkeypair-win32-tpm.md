---
description: 在 TPM 上建立2048位簽署金鑰組。
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Win32_Tpm 類別的 CreateEndorsementKeyPair 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511159"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 CreateEndorsementKeyPair 方法 \_

[**Win32 \_ tpm**](win32-tpm.md)類別的 **CREATEENDORSEMENTKEYPAIR** 方法會在 Tpm 上建立2048位簽署金鑰組。 簽署金鑰組必須可供 [**TakeOwnership**](takeownership-win32-tpm.md) 方法順利執行。 您可以使用 [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) 方法來偵測簽署金鑰是否已存在於 TPM 中。

## <a name="syntax"></a>語法


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

下表列出一些常見的傳回碼。



| 傳回碼/值                                                                                                                                                                  | Description                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/>                          |
| <dl> <dt> **TPM \_ E \_ 停用的 \_ CMD**</dt> <dt>2150105096 (0x80280008)</dt> </dl> | 此 TPM 上已有簽署金鑰組。<br/> |



 

## <a name="remarks"></a>備註

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

 

 
