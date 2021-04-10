---
description: Win32 Tpm 類別的 IsEndorsementKeyPairPresent 方法 \_ 指出簽署金鑰組是否存在於裝置上。
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Win32_Tpm 類別的 IsEndorsementKeyPairPresent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115872"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 IsEndorsementKeyPairPresent 方法 \_

[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsEndorsementKeyPairPresent** 方法指出簽署金鑰組是否存在於裝置上。 必須要有簽署金鑰組，才可擁有裝置。 [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)方法可以建立這個金鑰組。

必須啟用並啟用裝置，此方法才能成功。 若要啟用和啟用無人擁有的裝置，請參閱 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法。

## <a name="syntax"></a>語法


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IsEndorsementKeyPairPresent* \[擴展\]
</dt> <dd>

類型： **布林值**

若 **為 true**，表示簽署金鑰組存在於裝置上。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

常見的傳回碼如下所示。



| 傳回碼/值                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

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
</dt> <dt>

[**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
