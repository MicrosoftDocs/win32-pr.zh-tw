---
description: Win32 Tpm 類別的 IsOwnerClearDisabled 方法 \_ 會指出裝置擁有者是否受到限制而無法清除裝置。
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Win32_Tpm 類別的 IsOwnerClearDisabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 639804b21c97a6e445c0eddc9253c46774a4ccd895d58bfe32289432702cbe03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080628"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 IsOwnerClearDisabled 方法 \_

[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsOwnerClearDisabled** 方法會指出裝置擁有者是否受到限制而無法清除裝置。

## <a name="syntax"></a>語法


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IsOwnerClearDisabled* \[擴展\]
</dt> <dd>

類型： **布林值**

若 **為 true**，則裝置擁有者無法清除裝置。 只有實際存在的使用者可以清除裝置。 如果 **為 false**，則裝置擁有者可以清除裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

常見的傳回碼如下所示。



| 傳回碼/值                                                                                                                                 | 描述                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

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

 

 
