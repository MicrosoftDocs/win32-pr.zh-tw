---
description: 代表 (TPM) 的可信賴平臺模組，這是為電腦系統提供根信任的硬體安全晶片。
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Win32_Tpm 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 53fbe055e469dc4327ae747ab3e20873724923980f1e765d266a5f8143b545c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004016"
---
# <a name="win32_tpm-class"></a>Win32 \_ Tpm 類別

**Win32 \_ tpm** 類別代表 (Tpm) 的可信賴平臺模組，這是為電腦系統提供根信任的硬體安全晶片。

## <a name="syntax"></a>語法

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a>成員

**Win32 \_ Tpm** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ Tpm** 類別具有這些方法。



| 方法                                                                                   | 描述                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBlockedCommand**](addblockedcommand-win32-tpm.md)                                 | 將 TPM 命令新增至 Windows 上封鎖的本機命令清單。<br/>                                                                                                             |
| [**ChangeOwnerAuth**](changeownerauth-win32-tpm.md)                                     | 變更 TPM 擁有者授權值。<br/>                                                                                                                                       |
| [**清除**](clear-win32-tpm.md)                                                         | 將 TPM 重設為其原廠預設狀態。<br/>                                                                                                                                     |
| [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md)                               | 將使用者提供的複雜密碼轉換成20位元組的擁有者授權值，可用來與 TPM 互動。<br/>                                                            |
| [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)                   | 在 TPM 上建立2048位簽署金鑰組。<br/>                                                                                                                              |
| [**停用**](disable-win32-tpm.md)                                                     | 允許 TPM 擁有者停用 TPM。<br/>                                                                                                                                         |
| [**啟用**](enable-win32-tpm.md)                                                       | 允許 TPM 擁有者啟用 TPM。<br/>                                                                                                                                          |
| [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md)               | 取得並傳回暫止的 TPM 實體存在性作業。 使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法來要求作業。<br/> |
| [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md)             | 取得並傳回已執行之 TPM 實體存在作業的結果。<br/>                                                                                          |
| [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)         | 指出執行 TPM 實體目前狀態作業所需的使用者動作。<br/>                                                                                           |
| [**IsActivated**](isactivated-win32-tpm.md)                                             | 指出是否啟用 TPM。<br/>                                                                                                                                          |
| [**IsCommandBlocked**](iscommandblocked-win32-tpm.md)                                   | 指出 TPM 命令是否可在此作業系統上執行。<br/>                                                                                                              |
| [**IsCommandPresent**](iscommandpresent-win32-tpm.md)                                   | 指出此電腦是否支援 TPM 命令。<br/>                                                                                                                   |
| [**IsEnabled**](isenabled-win32-tpm.md)                                                 | 指出是否已啟用 TPM。<br/>                                                                                                                                            |
| [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md)             | 指出 TPM 是否有簽署金鑰組。<br/>                                                                                                                           |
| [**IsOwned**](isowned-win32-tpm.md)                                                     | 指出 TPM 是否有擁有者。<br/>                                                                                                                                          |
| [**IsOwnerClearDisabled**](isownercleardisabled-win32-tpm.md)                           | 指出 TPM 擁有者是否可以清除 TPM。<br/>                                                                                                                               |
| [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)                               | 指出是否可以安裝 TPM 擁有者。<br/>                                                                                                                                  |
| [**IsPhysicalClearDisabled**](isphysicalcleardisabled-win32-tpm.md)                     | 指出 TPM 實體存在作業是否可以清除 TPM。<br/>                                                                                                           |
| [**IsPhysicalPresenceHardwareEnabled**](isphysicalpresencehardwareenabled-win32-tpm.md) | 指出此電腦是否支援專用硬體路徑來表示實體存在。<br/>                                                                                  |
| [**IsSrkAuthCompatible**](issrkauthcompatible-win32-tpm.md)                             | 指出儲存體根金鑰 (SRK) 授權是否與 Windows 相容。<br/>                                                                                           |
| [**RemoveBlockedCommand**](removeblockedcommand-win32-tpm.md)                           | 從 Windows 封鎖的本機命令清單中移除 TPM 命令。<br/>                                                                                                        |
| [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md)                                   | 重設 TPM 製造商所實行的超時時間或其他機制，以防止 TPM 上的字典攻擊。<br/>                                                 |
| [**ResetSrkAuth**](resetsrkauth-win32-tpm.md)                                           | 重設儲存體根金鑰 (SRK) 授權值，以與 Windows 相容。<br/>                                                                                             |
| [**SelfTest**](selftest-win32-tpm.md)                                                   | 執行 TPM 的自我測試，並傳回結果。<br/>                                                                                                                          |
| [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)               | 要求執行 TPM 實體存在作業。<br/>                                                                                                                               |
| [**TakeOwnership**](takeownership-win32-tpm.md)                                         | 安裝 TPM 的擁有者。<br/>                                                                                                                                                   |



 

### <a name="properties"></a>屬性

**Win32 \_ Tpm** 類別具有這些屬性。

<dl> <dt>

**IsActivated \_ InitialValue**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否啟用 TPM。

如果裝置已啟動 (即為 true，如果 **IsActivated \_ InitialValue** 為 true) ，則為 **true** ，否則為 **false**。

當具現化類別時，會儲存這個值。 TPM 可以在具現化和您檢查此值之間變更狀態。 若要檢查 TPM 是否為即時啟用，請使用 [**IsActivated**](isactivated-win32-tpm.md) 方法。

**Windows Server 2008 和 Windows Vista：** 無法使用這個屬性。

</dd> <dt>

**IsEnabled \_ InitialValue**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否已啟用 TPM。

如果啟用裝置 (即為 true，如果 **IsEnabled \_ InitialValue** 為 true) ，則為 **true** ，否則為 **false**。

當具現化類別時，會儲存這個值。 TPM 可以在具現化和您檢查此值之間變更狀態。 若要檢查是否已即時啟用 TPM，請使用 [**IsEnabled**](isenabled-win32-tpm.md) 方法。

**Windows Server 2008 和 Windows Vista：** 無法使用這個屬性。

</dd> <dt>

**IsOwned \_ InitialValue**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 TPM 是否有擁有者。

如果裝置具有擁有者 (即為 true，如果 **IsOwned \_ InitialValue** 為 true) ，則為 **true** ，否則為 **false**。

當具現化類別時，會儲存這個值。 TPM 可以在具現化和您檢查此值之間變更狀態。 若要檢查 TPM 是否為即時擁有，請使用 [**IsOwned**](isowned-win32-tpm.md) 方法。

**Windows Server 2008 和 Windows Vista：** 無法使用這個屬性。

</dd> <dt>

**ManufacturerId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一為 TPM 製造商命名的識別資訊。

當資料無法使用時，會傳回零。

您可以將每個位元組解讀為 ASCII 字元，以將此整數值轉譯成字串值。 例如，整數值1414548736可以分成4個位元組：0x54、0x50、0x4D 和0x00。 假設字串是由左至右解釋，此整數值會轉譯為 "TPM" 的字串值。

</dd> <dt>

**ManufacturerVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

製造商所指定的 TPM 版本。

當資料無法使用時，會傳回「不支援」。

</dd> <dt>

**ManufacturerVersionInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

TPM 的其他製造商特定版本資訊。

當資料無法使用時，會傳回「不支援」。

</dd> <dt>

**PhysicalPresenceVersionInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

實體存在性介面的版本，這是一種通訊機制，可用來執行電腦支援的裝置作業，該作業需要實體存在。

此介面必須可用來執行 TPM 實體目前狀態作業。 **Win32 \_ Tpm** 方法 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)、 [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md)、 [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)和 [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md)會公開實體狀態介面的功能。

當資料無法使用時，會傳回「不支援」。

</dd> <dt>

**SpecVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

受信任運算群組的版本 (可支援 TPM 的 TCG) 規格。 此值包含主要和次要 TCG 規格版本、規格修訂層級和錯誤修訂層級。 所有值都是十六進位值。 例如，"1.2，2，0" 的版本資訊表示裝置已實作為 TCG 規格1.2 版、修訂層級2，而不含任何勘誤表。

當資料無法使用時，會傳回「不支援」。

</dd> </dl>

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



 

 
