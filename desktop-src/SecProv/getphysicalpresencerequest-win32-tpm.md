---
description: 傳回暫止的 TPM 實體存在性作業。 使用 SetPhysicalPresenceRequest 方法來要求作業。
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Win32_Tpm 類別的 GetPhysicalPresenceRequest 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8d631aabfc1e2df15aa4182b8332091fe503f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975832"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Win32 Tpm 類別的 GetPhysicalPresenceRequest 方法 \_

[**Win32 \_ tpm**](win32-tpm.md)類別的 **GetPhysicalPresenceRequest** 方法會傳回暫止的 tpm 實體存在性作業。 使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法來要求作業。

## <a name="syntax"></a>語法


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*要求* \[擴展\]
</dt> <dd>

類型： **uint32**

值，指定暫止的 TPM 實體存在性作業。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>0</dt> </dl></td>
<td>沒有要求。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1</dt> </dl></td>
<td>啟用 TPM。<br/> 作業2會反轉這項作業。 <br/> 如需詳細資訊，請參閱這些不牽涉實體存在的相關方法：
<ul>
<li><a href="enable-win32-tpm.md"><strong>啟用</strong></a></li>
<li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>2</dt> </dl></td>
<td>停用 TPM。<br/> 作業1會反轉這項作業。 <br/> 如需詳細資訊，請參閱此相關的方法，此方法不牽涉到實體存在： <a href="disable-win32-tpm.md"><strong>停</strong></a>用。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>3</dt> </dl></td>
<td>啟用 TPM。<br/> 作業4會反轉這項作業。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>4</dt> </dl></td>
<td>停用 TPM。<br/> 作業3會反轉這項作業。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>5</dt> </dl></td>
<td>清除 TPM。<br/> 這種作業無法反轉。<br/> 如需詳細資訊，請參閱此相關的方法，此方法不牽涉到實體存在： <a href="clear-win32-tpm.md"><strong>Clear</strong></a>。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>6</dt> </dl></td>
<td>啟用並啟用 TPM。 <br/> 作業7會反轉這項作業。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>7</dt> </dl></td>
<td>停用並停用 TPM。<br/> 作業6會反轉這項作業。 <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>8</dt> </dl></td>
<td>允許安裝 TPM 擁有者。 <br/> 作業9會反轉這項操作。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>9</dt> </dl></td>
<td>防止安裝 TPM 擁有者。<br/> 作業8會反轉這項作業。 <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>10</dt> </dl></td>
<td>啟用、啟用和允許安裝 TPM 擁有者。<br/> 作業11會反轉這項作業。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>rj-11</dt> </dl></td>
<td>停用、停用及防止 TPM 擁有者的安裝。<br/> 作業10會反轉這項作業。<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>延遲的實體 PresenceunownedFieldUpgrade<br/> 實體狀態設定已更新。<br/> <strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>日</dt> </dl></td>
<td>清除、啟用和啟用 TPM。<br/> 這種作業無法反轉。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>長</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> 設定您必須實際存在才能設定 TPM 的布建。<br/> 作業16會反轉這項作業。<br/> <strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>16</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> 設定您不需要實際存在才能設定 TPM 的布建。<br/> 作業15會反轉這項作業。<br/> <strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>至</dt> </dl></td>
<td>SetNoPPIClear_False<br/> 設定您必須實際存在以清除 TPM 的布建。<br/> 作業18會反轉這項操作。<br/> <strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>達</dt> </dl></td>
<td>SetNoPPIClear_True<br/> 設定您不需要實際存在的布建，以清除 TPM。<br/> 作業17會反轉這項作業。<br/> <strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>診斷</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> 設定您必須實際存在以維護 TPM 的布建。<br/> 作業20會反轉這項作業。<br/> <strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>名</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> 設定您必須實際存在以維護 TPM 的布建。<br/> 作業19會反轉這項操作。<br/> <strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>21</dt> </dl></td>
<td>啟用 + 啟用 + 清除<br/> 啟用、啟用和清除 TPM。<br/> <strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>日</dt> </dl></td>
<td>啟用 + 啟用 + 清除 + 啟用 + 啟動<br/> 啟用、啟用和清除 TPM，然後啟用並重新啟動 TPM。<br/> <strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。

下表列出常見的傳回碼。



| 傳回碼/值                                                                                                                                                                      | Description                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                      | 此方法成功。<br/>                                                            |
| <dl> <dt>**TPM \_E \_ PPI \_ ACPI \_ 故障**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | 發生硬體故障。 如需詳細資訊，請洽詢您的電腦製造商。<br/> |



 

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

[**清楚**](clear-win32-tpm.md)
</dt> <dt>

[**停用**](disable-win32-tpm.md)
</dt> <dt>

[**啟用**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
