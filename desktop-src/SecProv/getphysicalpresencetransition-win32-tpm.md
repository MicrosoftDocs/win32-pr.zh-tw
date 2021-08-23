---
description: 指出執行可信賴平臺模組 (TPM) 實體目前狀態作業所需的使用者動作。 使用 SetPhysicalPresenceRequest 方法來要求作業。
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Win32_Tpm 類別的 GetPhysicalPresenceTransition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 939f29d923182d3e2b0b9237c49c2a5fc6ff8652d2361f867a7e95af48415654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906338"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 GetPhysicalPresenceTransition 方法 \_

[**Win32 \_ Tpm**](win32-tpm.md)類別的 **GetPhysicalPresenceTransition** 方法表示執行信賴平臺模組所需的使用者動作 (Tpm) 實體目前狀態作業。 使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法來要求作業。 製造時，會為您的電腦設定必要的使用者動作。 通常需要重新開機電腦。

## <a name="syntax"></a>語法


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*轉換* \[擴展\]
</dt> <dd>

類型： **uint32**

整數值，指定執行 TPM 實體存在作業所需的轉換。



| 值                                                                        | 意義                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 不需要採取任何使用者動作，就能執行 TPM 實體目前狀態作業。<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | 若要執行 TPM 實體存在作業，使用者必須關閉電腦，然後使用 [電源] 按鈕將它重新開啟。 使用者必須實際存在於電腦上，才能在 BIOS 提示時接受或拒絕變更。<br/> |
| <dl> <dt>2</dt> </dl> | 若要執行 TPM 實體存在作業，使用者必須使用熱重新開機來重新開機電腦。 使用者必須實際存在於電腦上，才能在 BIOS 提示時接受或拒絕變更。<br/>                              |
| <dl> <dt>3</dt> </dl> | 必要的使用者動作未知。<br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

下表列出一些常見的傳回碼。



| 傳回碼/值                                                                                                                                                                      | 描述                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                      | 此方法成功。<br/>                                                            |
| <dl> <dt>**TPM \_E \_ PPI \_ ACPI \_ 故障**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | 發生硬體故障。 如需詳細資訊，請洽詢您的電腦製造商。<br/> |



 

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
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
