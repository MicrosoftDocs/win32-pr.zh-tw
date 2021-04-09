---
description: 使用電腦上的可信賴平臺模組 (TPM) 來保護磁片區的加密金鑰（如果有的話），並以使用者指定的個人識別碼 (PIN) 以及必須在啟動時顯示給電腦的外部金鑰來增強。
ms.assetid: 8991c22c-1e36-415e-a82b-c5ddf9c3b24a
title: Win32_EncryptableVolume 類別的 ProtectKeyWithTPMAndPINAndStartupKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPINAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9f315629c810027e18dac3a337c126f4a4a4bcce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693991"
---
# <a name="protectkeywithtpmandpinandstartupkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4c36d-103">Win32 EncryptableVolume 類別的 ProtectKeyWithTPMAndPINAndStartupKey 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4c36d-103">ProtectKeyWithTPMAndPINAndStartupKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4c36d-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithTPMAndPINAndStartupKey** 方法會使用電腦上的可信賴平臺模組 (TPM) 來保護磁片區的加密金鑰（如果有的話），以及使用者指定的個人識別碼 (PIN) 以及必須在啟動時顯示給電腦的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c36d-104">The **ProtectKeyWithTPMAndPINAndStartupKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) on the computer, if available, enhanced by both a user-specified personal identification number (PIN) and by an external key that must be presented to the computer at startup.</span></span>

<span data-ttu-id="4c36d-105">需要驗證的三個因素，才能解除鎖定磁片區的加密內容：</span><span class="sxs-lookup"><span data-stu-id="4c36d-105">Three factors of authentication are needed to unlock the encrypted contents of the volume:</span></span>

1.  <span data-ttu-id="4c36d-106">由 TPM 驗證</span><span class="sxs-lookup"><span data-stu-id="4c36d-106">Validation by the TPM</span></span>
2.  <span data-ttu-id="4c36d-107">輸入4到20位數的 PIN，或者，如果已啟用 [允許啟動的增強式 Pin] 群組原則、4到20個字母、符號、空格或數位</span><span class="sxs-lookup"><span data-stu-id="4c36d-107">Input of a 4 to 20 digit PIN or, if the "Allow enhanced PINs for startup" group policy is enabled, 4 to 20 letters, symbols, spaces, or numbers</span></span>
3.  <span data-ttu-id="4c36d-108">輸入包含外部金鑰的 USB 記憶體裝置</span><span class="sxs-lookup"><span data-stu-id="4c36d-108">Input of a USB memory device that contains the external key</span></span>

<span data-ttu-id="4c36d-109">使用 [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) 方法，將此外部金鑰儲存至 USB 記憶體裝置上的檔案，以做為啟動金鑰使用。</span><span class="sxs-lookup"><span data-stu-id="4c36d-109">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file on a USB memory device for usage as a startup key.</span></span> <span data-ttu-id="4c36d-110">這個方法只適用于作業系統磁片區。</span><span class="sxs-lookup"><span data-stu-id="4c36d-110">This method applies only on the operating system volume.</span></span> <span data-ttu-id="4c36d-111">會建立類型為「TPM 和 PIN 和啟動金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4c36d-111">A key protector of type "TPM And PIN And Startup Key" is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c36d-112">語法</span><span class="sxs-lookup"><span data-stu-id="4c36d-112">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndPINAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile,
  [in]           string PIN,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="4c36d-113">參數</span><span class="sxs-lookup"><span data-stu-id="4c36d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c36d-114">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4c36d-114">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c36d-115">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c36d-115">Type: **string**</span></span>

<span data-ttu-id="4c36d-116">標記此金鑰保護裝置的字串。</span><span class="sxs-lookup"><span data-stu-id="4c36d-116">A string that labels this key protector.</span></span> <span data-ttu-id="4c36d-117">如果未指定此參數，則會使用空白值。</span><span class="sxs-lookup"><span data-stu-id="4c36d-117">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="4c36d-118">*PlatformValidationProfile* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4c36d-118">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c36d-119">類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="4c36d-119">Type: **uint8**</span></span>

<span data-ttu-id="4c36d-120">整數陣列，指定電腦的 TPM 如何保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c36d-120">An array of integers that specifies how the computer's TPM secures the volume's encryption key.</span></span> <span data-ttu-id="4c36d-121">平臺驗證設定檔包含一組平臺設定暫存器 (PCR) 索引，範圍從0到23（含）。</span><span class="sxs-lookup"><span data-stu-id="4c36d-121">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="4c36d-122">參數中的重複值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="4c36d-122">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="4c36d-123">每個 PCR 索引都會與作業系統啟動時執行的服務相關聯。</span><span class="sxs-lookup"><span data-stu-id="4c36d-123">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="4c36d-124">每次電腦啟動時，TPM 都會檢查您在平臺驗證設定檔中指定的服務是否未變更。</span><span class="sxs-lookup"><span data-stu-id="4c36d-124">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="4c36d-125">如果其中任何一項服務在 BitLocker 保護保持開啟時變更，TPM 將不會釋出加密金鑰來解除鎖定磁片區，而且電腦會進入修復模式。</span><span class="sxs-lookup"><span data-stu-id="4c36d-125">If any of these services change while BitLocker protection remains on, the TPM will not release the encryption key to unlock the volume and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="4c36d-126">如果未指定此參數，則會使用預設索引0、2、4、5、8、9、10和11。</span><span class="sxs-lookup"><span data-stu-id="4c36d-126">If this parameter is not specified, the default indices of 0, 2, 4, 5, 8, 9, 10, and 11 are used.</span></span> <span data-ttu-id="4c36d-127">預設的平臺驗證設定檔可保護加密金鑰，以避免對 (CRTM) 、BIOS、和平臺擴充功能 (PCR 0) 、選項 ROM 程式碼 (PCR 2) 、主開機記錄 (MBR) 程式碼 (PCR 4) 、主要開機記錄 (MBR) 磁碟分割資料表 (PCR 5) 、NTFS 開機磁區 (pcr 9) 、開機管理程式 (pcr 10) ，以及 BitLocker 存取控制 (PCR 11) 。</span><span class="sxs-lookup"><span data-stu-id="4c36d-127">The default platform validation profile secures the encryption key against changes to the Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions (PCR 0), Option ROM Code (PCR 2), Master Boot Record (MBR) Code (PCR 4), Master Boot Record (MBR) Partition Table (PCR 5), the NTFS Boot Sector (PCR 8), the NTFS Boot Block (PCR 9), the Boot Manager (PCR 10), and the BitLocker Access Control (PCR 11).</span></span> <span data-ttu-id="4c36d-128">整合可延伸韌體介面 (UEFI) 型電腦預設不會使用 PCR 5。</span><span class="sxs-lookup"><span data-stu-id="4c36d-128">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="4c36d-129">建議使用預設的平臺驗證設定檔。</span><span class="sxs-lookup"><span data-stu-id="4c36d-129">The default platform validation profile is recommended.</span></span> <span data-ttu-id="4c36d-130">若要針對早期啟動設定變更進行額外的保護，請使用 PCRs 0、1、2、3、4、5、8、9、10、11的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4c36d-130">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="4c36d-131">變更預設設定檔會影響電腦的安全性與管理性。</span><span class="sxs-lookup"><span data-stu-id="4c36d-131">Changing the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="4c36d-132">BitLocker 對平臺修改的機密性 (惡意或授權的) 會隨著 PCRs 的包含或排除而增加或減少。</span><span class="sxs-lookup"><span data-stu-id="4c36d-132">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="4c36d-133">若要啟用 BitLocker 保護，平臺驗證設定檔必須包含 PCR 11。</span><span class="sxs-lookup"><span data-stu-id="4c36d-133">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="4c36d-134">值</span><span class="sxs-lookup"><span data-stu-id="4c36d-134">Value</span></span>                                                                         | <span data-ttu-id="4c36d-135">意義</span><span class="sxs-lookup"><span data-stu-id="4c36d-135">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c36d-136"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-136"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="4c36d-137"> (CRTM) 、BIOS 和平臺擴充的測量核心根信任</span><span class="sxs-lookup"><span data-stu-id="4c36d-137">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="4c36d-138"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-138"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="4c36d-139">平臺和主機板設定和資料</span><span class="sxs-lookup"><span data-stu-id="4c36d-139">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="4c36d-140"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-140"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="4c36d-141">選項 ROM 代碼</span><span class="sxs-lookup"><span data-stu-id="4c36d-141">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="4c36d-142"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-142"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="4c36d-143">選項 ROM 設定和資料</span><span class="sxs-lookup"><span data-stu-id="4c36d-143">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="4c36d-144"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-144"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="4c36d-145">主開機記錄 (MBR) 碼</span><span class="sxs-lookup"><span data-stu-id="4c36d-145">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="4c36d-146"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-146"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="4c36d-147">主開機記錄 (MBR) 磁碟分割資料表</span><span class="sxs-lookup"><span data-stu-id="4c36d-147">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="4c36d-148"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-148"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="4c36d-149">狀態轉換和喚醒事件</span><span class="sxs-lookup"><span data-stu-id="4c36d-149">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="4c36d-150"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-150"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="4c36d-151">電腦 Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="4c36d-151">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="4c36d-152"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-152"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="4c36d-153">NTFS 開機磁區</span><span class="sxs-lookup"><span data-stu-id="4c36d-153">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4c36d-154"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-154"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="4c36d-155">NTFS 開機區塊</span><span class="sxs-lookup"><span data-stu-id="4c36d-155">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="4c36d-156"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-156"><dt>10</dt></span></span> </dl> | <span data-ttu-id="4c36d-157">開機管理程式</span><span class="sxs-lookup"><span data-stu-id="4c36d-157">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="4c36d-158"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-158"><dt>11</dt></span></span> </dl> | <span data-ttu-id="4c36d-159">BitLocker 存取控制</span><span class="sxs-lookup"><span data-stu-id="4c36d-159">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="4c36d-160"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-160"><dt>12</dt></span></span> </dl> | <span data-ttu-id="4c36d-161">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="4c36d-161">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4c36d-162"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-162"><dt>13</dt></span></span> </dl> | <span data-ttu-id="4c36d-163">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="4c36d-163">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4c36d-164"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-164"><dt>14</dt></span></span> </dl> | <span data-ttu-id="4c36d-165">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="4c36d-165">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4c36d-166"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-166"><dt>15</dt></span></span> </dl> | <span data-ttu-id="4c36d-167">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="4c36d-167">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4c36d-168"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-168"><dt>16</dt></span></span> </dl> | <span data-ttu-id="4c36d-169">用於偵錯工具</span><span class="sxs-lookup"><span data-stu-id="4c36d-169">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="4c36d-170"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-170"><dt>17</dt></span></span> </dl> | <span data-ttu-id="4c36d-171">動態 CRTM</span><span class="sxs-lookup"><span data-stu-id="4c36d-171">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="4c36d-172"><dt>達</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-172"><dt>18</dt></span></span> </dl> | <span data-ttu-id="4c36d-173">已定義平臺</span><span class="sxs-lookup"><span data-stu-id="4c36d-173">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4c36d-174"><dt>診斷</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-174"><dt>19</dt></span></span> </dl> | <span data-ttu-id="4c36d-175">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="4c36d-175">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4c36d-176"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-176"><dt>20</dt></span></span> </dl> | <span data-ttu-id="4c36d-177">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="4c36d-177">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4c36d-178"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-178"><dt>21</dt></span></span> </dl> | <span data-ttu-id="4c36d-179">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="4c36d-179">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4c36d-180"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-180"><dt>22</dt></span></span> </dl> | <span data-ttu-id="4c36d-181">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="4c36d-181">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4c36d-182"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-182"><dt>23</dt></span></span> </dl> | <span data-ttu-id="4c36d-183">應用程式支援</span><span class="sxs-lookup"><span data-stu-id="4c36d-183">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="4c36d-184">*PIN* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c36d-184">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c36d-185">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c36d-185">Type: **string**</span></span>

<span data-ttu-id="4c36d-186">包含4到20位數的個人識別碼 (PIN) 或者，如果已啟用 [允許啟動的增強式 Pin] 群組原則、4和20個字母、符號、空格或數位，則為。</span><span class="sxs-lookup"><span data-stu-id="4c36d-186">Contains a 4 to 20-digit personal identification number (PIN) or, if the "Allow enhanced PINs for startup" group policy is enabled, 4 and 20 letters, symbols, spaces, or numbers.</span></span> <span data-ttu-id="4c36d-187">您必須在啟動時將此字串提供給電腦。</span><span class="sxs-lookup"><span data-stu-id="4c36d-187">This string must be provided to the computer at startup.</span></span>

</dd> <dt>

<span data-ttu-id="4c36d-188">*ExternalKey* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4c36d-188">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c36d-189">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="4c36d-189">Type: **uint8\[\]**</span></span>

<span data-ttu-id="4c36d-190">位元組陣列，指定當電腦啟動時，用來解除鎖定磁片區的256位外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c36d-190">An array of bytes that specifies the 256-bit external key used to unlock the volume when the computer starts.</span></span> <span data-ttu-id="4c36d-191">請將此參數保留空白，以隨機產生外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c36d-191">Leave this parameter blank to randomly generate the external key.</span></span> <span data-ttu-id="4c36d-192">使用 [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) 方法來取得隨機產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c36d-192">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="4c36d-193">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4c36d-193">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c36d-194">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c36d-194">Type: **string**</span></span>

<span data-ttu-id="4c36d-195">用來管理加密磁片區金鑰保護裝置的更新唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c36d-195">The updated unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="4c36d-196">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4c36d-196">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c36d-197">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c36d-197">Return value</span></span>

<span data-ttu-id="4c36d-198">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4c36d-198">Type: **uint32**</span></span>

<span data-ttu-id="4c36d-199">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4c36d-199">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4c36d-200">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4c36d-200">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="4c36d-201">Description</span><span class="sxs-lookup"><span data-stu-id="4c36d-201">Description</span></span>                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c36d-202"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-202"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="4c36d-203">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="4c36d-203">The method was successful.</span></span><br/>                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="4c36d-204"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-204"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                        | <span data-ttu-id="4c36d-205">已提供 *PlatformValidationProfile* 參數，但其值不在已知範圍內，或者不符合目前作用中的群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="4c36d-205">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting that is currently in effect.</span></span><br/> <span data-ttu-id="4c36d-206">提供 *ExternalKey* 參數，但它不是大小為32的陣列。</span><span class="sxs-lookup"><span data-stu-id="4c36d-206">The *ExternalKey* parameter is provided but it is not an array of size 32.</span></span><br/> |
| <dl> <span data-ttu-id="4c36d-207"><dt>**FVE \_E \_ 可 \_**</dt>開機的 CDDVD <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-207"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="4c36d-208">在這部電腦上找到可開機的 CD/DVD。</span><span class="sxs-lookup"><span data-stu-id="4c36d-208">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="4c36d-209">移除 CD/DVD 並重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="4c36d-209">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="4c36d-210"><dt>**FVE \_E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-210"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>              | <span data-ttu-id="4c36d-211">TPM 無法保護磁片區的加密金鑰，因為磁片區未包含目前執行中的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4c36d-211">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="4c36d-212"><dt>**FVE \_E \_ 不正確 \_ PIN \_ 字元**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-212"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="4c36d-213">*NewPIN* 參數包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="4c36d-213">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="4c36d-214">當停用 [允許啟動的增強式 Pin] 群組原則時，只支援數位。</span><span class="sxs-lookup"><span data-stu-id="4c36d-214">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="4c36d-215"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-215"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="4c36d-216">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="4c36d-216">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="4c36d-217"><dt>**FVE \_E \_ 原則 \_ 不正確 \_ PIN \_ 長度**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-217"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="4c36d-218">提供的 *NewPIN* 參數長度超過20個字元、少於4個字元，或小於群組原則指定的最小長度。</span><span class="sxs-lookup"><span data-stu-id="4c36d-218">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 4 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="4c36d-219"><dt>**FVE \_E \_ 保護裝置 \_ 存在**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-219"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="4c36d-220">此類型的金鑰保護裝置已經存在。</span><span class="sxs-lookup"><span data-stu-id="4c36d-220">A key protector of this type already exists.</span></span><br/>                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="4c36d-221"><dt>**Tb \_E \_ 服務 \_ 未 \_**</dt>執行 <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-221"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="4c36d-222">在這部電腦上找不到相容的 TPM。</span><span class="sxs-lookup"><span data-stu-id="4c36d-222">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="4c36d-223">備註</span><span class="sxs-lookup"><span data-stu-id="4c36d-223">Remarks</span></span>

<span data-ttu-id="4c36d-224">磁片區最多隻能有一個類型為「TPM 和 PIN 和啟動金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4c36d-224">At most one key protector of type "TPM And PIN And Startup Key" can exist for a volume at any time.</span></span> <span data-ttu-id="4c36d-225">如果您想要變更現有「TPM 和 PIN 和啟動金鑰」金鑰保護裝置所使用的顯示名稱或平臺驗證設定檔，您必須先移除現有的金鑰保護裝置，然後呼叫 **ProtectKeyWithTPMAndPINAndStartupKey** 來建立新的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4c36d-225">If you want to change the display name or the platform validation profile used by an existing "TPM And PIN And Startup Key" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndPINAndStartupKey** to create a new one.</span></span>

<span data-ttu-id="4c36d-226">您應指定額外的金鑰保護裝置，以在無法取得存取磁片區加密金鑰的復原案例中解除鎖定磁片區;例如，TPM 無法成功驗證平臺驗證設定檔或 PIN 遺失時。</span><span class="sxs-lookup"><span data-stu-id="4c36d-226">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when the PIN is lost.</span></span> <span data-ttu-id="4c36d-227">使用 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 或 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 來建立一或多個金鑰保護裝置，以復原其他鎖定的磁片區。</span><span class="sxs-lookup"><span data-stu-id="4c36d-227">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="4c36d-228">雖然可以同時有類型為 "TPM" 的金鑰保護裝置，以及另一種類型為「TPM 和 PIN 和啟動金鑰」的金鑰保護裝置，但「TPM」金鑰保護裝置類型的存在會使其他以 TPM 為基礎的金鑰保護裝置產生的影響。</span><span class="sxs-lookup"><span data-stu-id="4c36d-228">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And PIN And Startup Key", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="4c36d-229">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="4c36d-229">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4c36d-230">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4c36d-230">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4c36d-231">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="4c36d-231">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4c36d-232">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="4c36d-232">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c36d-233">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c36d-233">Requirements</span></span>



| <span data-ttu-id="4c36d-234">需求</span><span class="sxs-lookup"><span data-stu-id="4c36d-234">Requirement</span></span> | <span data-ttu-id="4c36d-235">值</span><span class="sxs-lookup"><span data-stu-id="4c36d-235">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c36d-236">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c36d-236">Minimum supported client</span></span><br/> | <span data-ttu-id="4c36d-237">Windows Vista Enterprise 含 SP1、Windows Vista 旗艦版（含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c36d-237">Windows Vista Enterprise with SP1, Windows Vista Ultimate with SP1 \[desktop apps only\]</span></span><br/>     |
| <span data-ttu-id="4c36d-238">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c36d-238">Minimum supported server</span></span><br/> | <span data-ttu-id="4c36d-239">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c36d-239">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c36d-240">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c36d-240">Namespace</span></span><br/>                | <span data-ttu-id="4c36d-241">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="4c36d-241">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4c36d-242">MOF</span><span class="sxs-lookup"><span data-stu-id="4c36d-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c36d-243"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c36d-243"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c36d-244">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c36d-244">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c36d-245">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="4c36d-245">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
