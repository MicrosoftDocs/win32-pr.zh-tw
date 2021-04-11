---
description: 指出指定的實體目前狀態作業是否需要實際存在的使用者確認。
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: Win32_Tpm：： GetPhysicalPresenceConfirmationStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944618"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>Win32 \_ Tpm：： GetPhysicalPresenceConfirmationStatus 方法

指出指定的實體目前狀態作業是否需要實際存在的使用者確認。

只有本機系統管理員才能存取此方法。

## <a name="syntax"></a>語法


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*操作* \[在\]
</dt> <dd>

整數值，指定需要實體存在的要求 TPM 作業。 也支援廠商特有的命令。

*Operation* 參數可能包含下列值。



| 值                                                                                                                               | 意義                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | 啟用<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | 停用<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | 啟動<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | 停用<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | 清除<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | 啟用 + 啟用<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | 停用 + 停用<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | SetOwnerInstall \_ True<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | SetOwnerInstall \_ False<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | 啟用 + 啟用 + SetOwnerInstall \_ True<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | SetOwnerInstall \_ False + 停用 + 停用<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | 延遲的實體 PresenceunownedFieldUpgrade<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | 清除 + 啟用 + 啟用<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ False<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ True<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ False<br/>                          |
| <dl> <dt>達</dt> </dl>                                                       | SetNoPPIClear \_ True<br/>                           |
| <dl> <dt>診斷</dt> </dl>                                                       | SetNoPPIMaintenance \_ False<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ True<br/>                     |
| <dl> <dt>21</dt> </dl>                                                       | 啟用 + 啟用 + 清除<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | 啟用 + 啟用 + 清除 + 啟用 + 啟動<br/> |



 

</dd> <dt>

*ConfirmationStatus* \[擴展\]
</dt> <dd>

傳回實體存在性命令的確認狀態。

*ConfirmationStatus* 參數可能包含下列值。



| 值                                                                        | 意義                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 未實作<br/>                                             |
| <dl> <dt>1</dt> </dl> | 僅限 BIOS。<br/>                                                  |
| <dl> <dt>2</dt> </dl> | BIOS 設定已封鎖作業系統。<br/> |
| <dl> <dt>3</dt> </dl> | 允許且實際呈現使用者需求。<br/>               |
| <dl> <dt>4</dt> </dl> | 允許且實際呈現使用者不需要<br/>            |



 

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

 

 
