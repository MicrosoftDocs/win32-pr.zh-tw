---
description: Win32 Tpm 類別的 IsEnabled 方法 \_ 會指出是否已啟用裝置。 此值可由 Enable 和 Disable 方法變更。
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Win32_Tpm 類別的 IsEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 1d61c96d9c80ae77f9869261905fb93461530b452deaf7a4709b394623a3dfab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667498"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 IsEnabled 方法 \_

[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsEnabled** 方法會指出是否已啟用裝置。 此值可由 [**Enable**](enable-win32-tpm.md) 和 [**Disable**](disable-win32-tpm.md) 方法變更。

## <a name="syntax"></a>語法


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IsEnabled* \[擴展\]
</dt> <dd>

類型： **布林值**

若 **為 true**，則會啟用裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

常見的傳回碼如下所示。



| 傳回碼/值                                                                                                                                 | 描述                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

根據受信任的運算群組 (TCG) 1.2 規格，只有在裝置處於停用狀態時，才能使用下列命令。

-   TPM \_ ContinueSelfTest
-   TPM \_ DSAP
-   TPM \_ FlushSpecific
-   TPM \_ GetCapability
-   TPM \_ GetTestResult
-   TPM \_ 初始化
-   TPM \_ OIAP
-   TPM \_ OSAP
-   TPM \_ OwnerSetDisable
-   TPM \_ PCR \_ 重設
-   TPM \_ PhysicalDisable
-   TPM \_ PhysicalEnable
-   TPM \_ PhysicalSetDeactivated
-   TPM \_ 重設
-   TPM \_ SaveState
-   TPM \_ SelfTestFull
-   TPM \_ SetCapability
-   TPM \_ SHA1Complete
-   TPM \_ SHA1Start
-   TPM \_ SHA1Update
-   TPM \_ 啟動
-   TPM \_ TakeOwnership
-   TPM \_ 終止 \_ 控制碼

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

[**停用**](disable-win32-tpm.md)
</dt> <dt>

[**啟用**](enable-win32-tpm.md)
</dt> </dl>

 

 
