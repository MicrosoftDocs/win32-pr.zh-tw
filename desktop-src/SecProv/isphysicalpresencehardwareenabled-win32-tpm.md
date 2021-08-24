---
description: Win32 Tpm 類別的 IsPhysicalPresenceHardwareEnabled 方法會 \_ 指出是否可以使用硬體信號來設定平臺上的實體存在。
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Win32_Tpm 類別的 IsPhysicalPresenceHardwareEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 499ec39741b23583b599407ef43696ab82164f365626c8042586b6b6e4b56deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797038"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 IsPhysicalPresenceHardwareEnabled 方法 \_

[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsPhysicalPresenceHardwareEnabled** 方法會指出是否可以使用硬體信號來設定平臺上的實體存在。 此值是由平臺製造商根據平臺設計來設定。 平臺製造商提供的檔可能會提供其他資訊。

## <a name="syntax"></a>語法


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IsPhysicalPresenceHardwareEnabled* \[擴展\]
</dt> <dd>

類型： **布林值**

若 **為 true**，則平臺上的實體存在可以使用硬體信號來設定。

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

 

 
