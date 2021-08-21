---
description: 要求需要實體存在的 TPM 操作。
ms.assetid: e71eb6ab-b6ab-4586-8999-0a464f11047a
title: Win32_Tpm 類別的 SetPhysicalPresenceRequest 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9c1b1e2760ed5015b6b682b94bd364e469edb4ed519adc371e2c348a0bf8c607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891353"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 SetPhysicalPresenceRequest 方法 \_

[**Win32 \_ tpm**](win32-tpm.md)類別的 **SetPhysicalPresenceRequest** 方法會要求需要實體存在的 Tpm 操作。 當您使用這個方法來提交要求之後，請套用 [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) 方法中指出的下一個步驟。 最後，使用 [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) 方法來檢查作業是否順利執行。 如果呼叫可能會導致需要 BitLocker 修復，此方法會暫停 BitLocker。 布建 TPM 之後，BitLocker 會自動繼續。

這些步驟都是必要的，因為只有在電腦偵測到實際存在的使用者之後，才可執行實體目前狀態作業。

## <a name="syntax"></a>語法


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*要求* \[在\]
</dt> <dd>

類型： **uint32**

整數值，指定需要實體存在的要求 TPM 作業。



| 值                                                                                                                               | 意義                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | 沒有要求。<br/> 使用此值可清除暫止的要求。<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | 啟用 TPM。<br/> 作業2會反轉這項作業。<br/> 如需詳細資訊，請參閱下列不涉及實體存在的相關方法： [**啟用**](enable-win32-tpm.md) 和 [**IsEnabled**](isenabled-win32-tpm.md)。<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | 停用 TPM。<br/> 作業1會反轉這項作業。<br/> 如需詳細資訊，請參閱下列不牽涉到實體存在： [**停**](disable-win32-tpm.md)用的相關方法。<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | 啟用 TPM。<br/> 作業4會反轉這項作業。<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | 停用 TPM。<br/> 作業3會反轉這項作業。<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | 清除 TPM。<br/> 這種作業無法反轉。<br/> 如需詳細資訊，請參閱下列未涉及實體存在的相關方法： [**清除**](clear-win32-tpm.md)。<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | 啟用並啟用 TPM。<br/> 作業7會反轉這項作業。<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | 停用並停用 TPM。<br/> 作業6會反轉這項作業。<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | 允許安裝 TPM 擁有者。<br/> 作業9會反轉這項操作。<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | 防止安裝 TPM 擁有者。<br/> 作業8會反轉這項作業。 <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | 啟用、啟用和允許安裝 TPM 擁有者。<br/> 作業11會反轉這項作業。<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | 停用、停用及防止 TPM 擁有者的安裝。<br/> 作業10會反轉這項作業。<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | 延遲的實體 PresenceunownedFieldUpgrade<br/> 實體狀態設定已更新。<br/> **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 不支援這個值。<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | 清除、啟用和啟用 TPM。<br/> 這種作業無法反轉。<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ False<br/> 設定您必須實際存在才能設定 TPM 的布建。<br/> 作業16會反轉這項作業。<br/> **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 不支援這個值。<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ True<br/> 設定您不需要實際存在才能設定 TPM 的布建。<br/> 作業15會反轉這項作業。<br/> **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 不支援這個值。<br/> |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ False<br/> 設定您必須實際存在以清除 TPM 的布建。<br/> 作業18會反轉這項操作。<br/> **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 不支援這個值。<br/>           |
| <dl> <dt>達</dt> </dl>                                                       | SetNoPPIClear \_ True<br/> 設定您不需要實際存在的布建，以清除 TPM。<br/> 作業17會反轉這項作業。<br/> **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 不支援這個值。<br/>   |
| <dl> <dt>診斷</dt> </dl>                                                       | SetNoPPIMaintenance \_ False<br/> 設定您必須實際存在以維護 TPM 的布建。<br/> 作業20會反轉這項作業。<br/> **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 不支援這個值。<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ True<br/> 設定您不需要實際存在以維護 TPM 的布建。<br/> 作業19會反轉這項操作。<br/> **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 不支援這個值。<br/>   |
| <dl> <dt>21</dt> </dl>                                                       | 啟用 + 啟用 + 清除<br/> 啟用、啟用和清除 TPM。<br/> **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 不支援這個值。<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | 啟用 + 啟用 + 清除 + 啟用 + 啟動<br/> 啟用、啟用和清除 TPM，然後啟用並重新啟動 TPM。<br/> **Windows 7、Windows server 2008 R2、Windows Vista 和 Windows Server 2008：** 不支援這個值。<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。



| 傳回碼/值                                                                                                                                                                       | Description                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                       | 此方法成功。<br/> 使用 [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) 方法來判斷所需的下一個步驟。<br/>                                                  |
| <dl> <dt>**TPM \_E \_ PPI \_ 不 \_ 支援**</dt> <dt>2150171395 (0x80290303)</dt> </dl> | 電腦不支援使用此方法的 TPM 實體目前狀態作業。<br/> 如需詳細資訊，請洽詢您的電腦製造商。 電腦的 BIOS 可能會有設定 TPM 的替代支援。<br/> |
| <dl> <dt>**TPM \_E \_ PPI \_ ACPI \_ 故障**</dt> <dt>2150171392 (0x80290300)</dt> </dl>  | 發生硬體故障。<br/> 如需詳細資訊，請洽詢您的電腦製造商。<br/>                                                                                                                                  |



 

## <a name="remarks"></a>備註

TPM 實體存在作業不需要 TPM 擁有者授權。 不過，他們確實需要額外的步驟，以協助防止未經授權的 TPM 變更。

支援 TPM 實體目前狀態作業的電腦會在執行作業之前，嘗試偵測實際存在的使用者。 雖然電腦在執行此偵測時可能會有所不同，但其構想是讓實際存在的使用者或系統管理員授權作業。

例如，電腦可能會要求使用者重新開機電腦。 電腦重新開機之後，電腦可以顯示 BIOS 確認對話方塊，讓使用者使用鍵盤來確認操作。

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

[**啟用**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**停用**](disable-win32-tpm.md)
</dt> <dt>

[**清除**](clear-win32-tpm.md)
</dt> </dl>

 

 
