---
description: 提供完整解密作業系統磁片區之硬體測試的相關狀態資訊。
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Win32_EncryptableVolume 類別的 GetHardwareTestStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979818"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetHardwareTestStatus 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetHardwareTestStatus** 方法提供完整解密作業系統磁片區之硬體測試的相關狀態資訊。

您可以使用此方法來顯示硬體測試是否擱置，以及上次電腦重新開機後完成的硬體測試是否成功或失敗。 若要要求硬體測試，請使用 [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) 方法。

## <a name="syntax"></a>語法


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TestStatus* \[擴展\]
</dt> <dd>

類型： **uint32**

指定硬體測試是否暫止，以及最後一次電腦重新開機時完成的硬體測試是否成功。



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
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </dl></td>
<td>如果已要求測試，則測試會在最後一次電腦重新開機時成功，而且磁片區加密現在正在進行中。 如需加密狀態，請參閱 <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> 方法。 否則，在上一次電腦重新開機時不會執行任何測試，且沒有擱置中的測試。 <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <dt><strong>失敗</strong></dt> <dt>1</dt> </dl></td>
<td>磁片區加密未啟動。 已移除所有金鑰保護裝置。<br/> 若要解決失敗的測試：<br/>
<ul>
<li>請參閱 <em>TestError</em> 參數中的資訊。</li>
<li>新增金鑰保護裝置，並再次使用 <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> 方法。</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <dt><strong>暫</strong></dt>止 <dt>2</dt> </dl></td>
<td>已要求測試，並將在下一次電腦重新開機時執行。<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*TestError* \[擴展\]
</dt> <dd>

類型： **uint32**

指定上次完成的硬體測試錯誤。



| 值                                                                                               | 意義                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                        | 未發生任何錯誤，或未在最後一次電腦重新開機時執行硬體測試。<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt> 2150694972 (0x8031003C) </dt> </dl> | \_ \_ \_ \_ 找不到 FVE E KEYFILE<br/> 找不到具有外部金鑰檔的 USB 快閃磁片磁碟機。 如果此失敗持續發生，電腦將無法在重新開機期間讀取 USB 磁片磁碟機。 在重新開機期間，您可能無法使用外部金鑰來解除鎖定作業系統磁片區。<br/>                                                                |
| <dl> <dt> 2150694973 (0x8031003D) </dt> </dl> | FVE \_ E \_ KEYFILE \_ 無效<br/> USB 快閃磁片磁碟機上的外部金鑰檔已損毀。 請嘗試其他 USB 快閃磁片磁碟機來儲存外部金鑰檔。<br/>                                                                                                                                                                                 |
| <dl> <dt> 2150694975 (0x8031003F) </dt> </dl> | \_ \_ \_ 已停用 FVE E TPM<br/> TPM 已停用或停用，或已停用或停用。 若要開啟 TPM，請使用 [**Win32 \_ tpm**](win32-tpm.md) WMI 提供者，或執行 tpm 管理嵌入式管理單元 (的) 。<br/>                                                                                                            |
| <dl> <dt> 2150694977 (0x80310041) </dt> </dl> | FVE \_ E \_ TPM \_ 不正確 \_ PCR<br/> TPM 偵測到目前平臺驗證設定檔內作業系統重新開機服務的變更。 從電腦移除任何啟動 CD 或 DVD。 如果此失敗持續發生，請檢查是否已安裝最新的固件和 BIOS 升級，以及 TPM 是否正常運作。<br/> |
| <dl> <dt>2150694979 (0x80310043) </dt> </dl>  | FVE \_ E \_ PIN \_ 無效<br/> 提供的 PIN 不正確。<br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

下表列出一些常見的傳回碼。



| 傳回碼/值                                                                                                                                                                  | Description                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法已成功。<br/> |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl> | 磁片區已鎖定。<br/> |



 

## <a name="remarks"></a>備註

若要要求硬體測試，請使用 [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) 方法。

若要在狀態為 [擱置中] 時執行硬體測試，請遵循下列步驟：

1.  將包含外部金鑰檔案的 USB 快閃磁片磁碟機插入電腦。 只有當磁片區具有「外部金鑰」或「TPM 和啟動金鑰」類型的金鑰保護裝置時，才適用此步驟。
2.  重新啟動電腦。 電腦重新開機時，會自動執行硬體測試。

若要取消硬體測試，請使用 [**加密**](encrypt-win32-encryptablevolume.md) 方法。

成功的測試會判斷：

-   如果有 TPM 相關的金鑰保護裝置，TPM 就可以將磁片區解除鎖定。
-   如果磁片區可由外部 (金鑰（包括啟動金鑰) ）解除鎖定，電腦就可以在啟動期間讀取包含外部金鑰檔的 USB 快閃磁片磁碟機。

在轉換任何變更之後或下次電腦重新開機之後，將無法使用硬體測試結果。 檢查系統事件記錄檔，以取得先前在電腦上執行之任何硬體測試的相關資訊。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
