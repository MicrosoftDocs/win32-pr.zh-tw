---
description: 如果可信賴平臺模組 (TPM) 可供使用，這個方法會保護由外部金鑰增強的磁片區加密金鑰。
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Win32_EncryptableVolume 類別的 ProtectKeyWithTPMAndStartupKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 06ab2b9474b3564a567374490d9aeb70448338be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973622"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="239df-103">Win32 EncryptableVolume 類別的 ProtectKeyWithTPMAndStartupKey 方法 \_</span><span class="sxs-lookup"><span data-stu-id="239df-103">ProtectKeyWithTPMAndStartupKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="239df-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithTPMAndStartupKey** 方法會使用可信賴平臺模組 (TPM) 電腦上的安全性硬體（如果有的話）來保護磁片區的加密金鑰（如果有的話），並以必須在啟動時向電腦呈現的外部金鑰增強。</span><span class="sxs-lookup"><span data-stu-id="239df-104">The **ProtectKeyWithTPMAndStartupKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by an external key that must be presented to the computer at startup.</span></span>

<span data-ttu-id="239df-105">您必須透過 TPM 驗證以及包含外部金鑰的 USB 記憶體裝置輸入，才能存取磁片區的加密金鑰，並將磁片區內容解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="239df-105">Both validation by the TPM and input of a USB memory device that contains the external key are necessary to access the volume's encryption key and unlock the volume contents.</span></span> <span data-ttu-id="239df-106">使用 [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) 方法，將此外部金鑰儲存至 USB 記憶體裝置上的檔案，以做為啟動金鑰使用。</span><span class="sxs-lookup"><span data-stu-id="239df-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file on a USB memory device for usage as a startup key.</span></span>

<span data-ttu-id="239df-107">這個方法僅適用于包含目前正在執行之作業系統的磁片區。</span><span class="sxs-lookup"><span data-stu-id="239df-107">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="239df-108">如果磁片區不存在，就會為磁片區建立類型為「TPM 和啟動金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="239df-108">A key protector of type "TPM And Startup Key" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="239df-109">語法</span><span class="sxs-lookup"><span data-stu-id="239df-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="239df-110">參數</span><span class="sxs-lookup"><span data-stu-id="239df-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="239df-111">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="239df-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="239df-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="239df-112">Type: **string**</span></span>

<span data-ttu-id="239df-113">使用者指派給此金鑰保護裝置的字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="239df-113">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="239df-114">如果未指定此參數，則會使用空白值。</span><span class="sxs-lookup"><span data-stu-id="239df-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="239df-115">*PlatformValidationProfile* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="239df-115">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="239df-116">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="239df-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="239df-117">整數陣列，指定電腦的信賴平臺模組 (TPM) 安全性硬體如何保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="239df-117">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the encryption key of the disk volume.</span></span>

<span data-ttu-id="239df-118">平臺驗證設定檔包含一組平臺設定暫存器 (PCR) 索引，範圍從0到23（含）。</span><span class="sxs-lookup"><span data-stu-id="239df-118">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="239df-119">參數中的重複值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="239df-119">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="239df-120">每個 PCR 索引都會與作業系統啟動時執行的服務相關聯。</span><span class="sxs-lookup"><span data-stu-id="239df-120">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="239df-121">每次電腦啟動時，TPM 都會檢查您在平臺驗證設定檔中指定的服務是否未變更。</span><span class="sxs-lookup"><span data-stu-id="239df-121">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="239df-122">如果其中任何一項服務在 BitLocker 磁碟機加密)  (的情況下變更，則 TPM 不會釋出加密金鑰來解除鎖定磁片區，而且電腦會進入修復模式。</span><span class="sxs-lookup"><span data-stu-id="239df-122">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="239df-123">如果指定了這個參數，但已啟用對應的群組原則設定，它就必須符合群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="239df-123">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="239df-124">如果未指定此參數，則會使用預設值0、2、4、5、8、9、10和11。</span><span class="sxs-lookup"><span data-stu-id="239df-124">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="239df-125">預設的平臺驗證設定檔會針對下列元素的變更保護加密金鑰：</span><span class="sxs-lookup"><span data-stu-id="239df-125">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="239df-126">度量 (的核心根信任 CRTM) </span><span class="sxs-lookup"><span data-stu-id="239df-126">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="239df-127">BIOS</span><span class="sxs-lookup"><span data-stu-id="239df-127">BIOS</span></span>
-   <span data-ttu-id="239df-128"> (PCR 0) 的平臺擴充</span><span class="sxs-lookup"><span data-stu-id="239df-128">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="239df-129">選項 ROM 代碼 (PCR 2) </span><span class="sxs-lookup"><span data-stu-id="239df-129">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="239df-130">主開機記錄 (MBR) 代碼 (PCR 4) </span><span class="sxs-lookup"><span data-stu-id="239df-130">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="239df-131">主開機記錄 (MBR) 磁碟分割表格 (PCR 5) </span><span class="sxs-lookup"><span data-stu-id="239df-131">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="239df-132"> (PCR 8) 的 NTFS 開機磁區</span><span class="sxs-lookup"><span data-stu-id="239df-132">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="239df-133">NTFS 開機區塊 (PCR 9) </span><span class="sxs-lookup"><span data-stu-id="239df-133">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="239df-134">開機管理程式 (PCR 10) </span><span class="sxs-lookup"><span data-stu-id="239df-134">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="239df-135">BitLocker 存取控制 (PCR 11) </span><span class="sxs-lookup"><span data-stu-id="239df-135">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="239df-136">針對電腦的安全性，建議預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="239df-136">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="239df-137">若要針對早期啟動設定變更進行額外的保護，請使用 PCRs 0、1、2、3、4、5、8、9、10、11的設定檔。</span><span class="sxs-lookup"><span data-stu-id="239df-137">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="239df-138">整合可延伸韌體介面 (UEFI) 型電腦預設不會使用 PCR 5。</span><span class="sxs-lookup"><span data-stu-id="239df-138">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="239df-139">變更預設設定檔會影響電腦的安全性與管理性。</span><span class="sxs-lookup"><span data-stu-id="239df-139">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="239df-140">BitLocker 對平臺修改的機密性 (惡意或授權的) 會隨著 PCRs 的包含或排除而增加或減少。</span><span class="sxs-lookup"><span data-stu-id="239df-140">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="239df-141">若要啟用 BitLocker 保護，平臺驗證設定檔必須包含 PCR 11。</span><span class="sxs-lookup"><span data-stu-id="239df-141">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="239df-142">值</span><span class="sxs-lookup"><span data-stu-id="239df-142">Value</span></span>                                                                         | <span data-ttu-id="239df-143">意義</span><span class="sxs-lookup"><span data-stu-id="239df-143">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="239df-144"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="239df-144"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="239df-145"> (CRTM) 、BIOS 和平臺擴充的測量核心根信任</span><span class="sxs-lookup"><span data-stu-id="239df-145">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="239df-146"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="239df-146"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="239df-147">平臺和主機板設定和資料</span><span class="sxs-lookup"><span data-stu-id="239df-147">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="239df-148"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="239df-148"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="239df-149">選項 ROM 代碼</span><span class="sxs-lookup"><span data-stu-id="239df-149">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="239df-150"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="239df-150"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="239df-151">選項 ROM 設定和資料</span><span class="sxs-lookup"><span data-stu-id="239df-151">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="239df-152"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="239df-152"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="239df-153">主開機記錄 (MBR) 碼</span><span class="sxs-lookup"><span data-stu-id="239df-153">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="239df-154"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="239df-154"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="239df-155">主開機記錄 (MBR) 磁碟分割資料表</span><span class="sxs-lookup"><span data-stu-id="239df-155">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="239df-156"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="239df-156"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="239df-157">狀態轉換和喚醒事件</span><span class="sxs-lookup"><span data-stu-id="239df-157">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="239df-158"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="239df-158"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="239df-159">電腦 Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="239df-159">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="239df-160"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="239df-160"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="239df-161">NTFS 開機磁區</span><span class="sxs-lookup"><span data-stu-id="239df-161">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="239df-162"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="239df-162"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="239df-163">NTFS 開機區塊</span><span class="sxs-lookup"><span data-stu-id="239df-163">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="239df-164"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="239df-164"><dt>10</dt></span></span> </dl> | <span data-ttu-id="239df-165">開機管理程式</span><span class="sxs-lookup"><span data-stu-id="239df-165">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="239df-166"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="239df-166"><dt>11</dt></span></span> </dl> | <span data-ttu-id="239df-167">BitLocker 存取控制</span><span class="sxs-lookup"><span data-stu-id="239df-167">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="239df-168"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="239df-168"><dt>12</dt></span></span> </dl> | <span data-ttu-id="239df-169">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="239df-169">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="239df-170"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="239df-170"><dt>13</dt></span></span> </dl> | <span data-ttu-id="239df-171">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="239df-171">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="239df-172"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="239df-172"><dt>14</dt></span></span> </dl> | <span data-ttu-id="239df-173">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="239df-173">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="239df-174"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="239df-174"><dt>15</dt></span></span> </dl> | <span data-ttu-id="239df-175">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="239df-175">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="239df-176"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="239df-176"><dt>16</dt></span></span> </dl> | <span data-ttu-id="239df-177">用於偵錯工具</span><span class="sxs-lookup"><span data-stu-id="239df-177">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="239df-178"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="239df-178"><dt>17</dt></span></span> </dl> | <span data-ttu-id="239df-179">動態 CRTM</span><span class="sxs-lookup"><span data-stu-id="239df-179">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="239df-180"><dt>達</dt></span><span class="sxs-lookup"><span data-stu-id="239df-180"><dt>18</dt></span></span> </dl> | <span data-ttu-id="239df-181">已定義平臺</span><span class="sxs-lookup"><span data-stu-id="239df-181">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="239df-182"><dt>診斷</dt></span><span class="sxs-lookup"><span data-stu-id="239df-182"><dt>19</dt></span></span> </dl> | <span data-ttu-id="239df-183">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="239df-183">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="239df-184"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="239df-184"><dt>20</dt></span></span> </dl> | <span data-ttu-id="239df-185">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="239df-185">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="239df-186"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="239df-186"><dt>21</dt></span></span> </dl> | <span data-ttu-id="239df-187">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="239df-187">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="239df-188"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="239df-188"><dt>22</dt></span></span> </dl> | <span data-ttu-id="239df-189">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="239df-189">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="239df-190"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="239df-190"><dt>23</dt></span></span> </dl> | <span data-ttu-id="239df-191">應用程式支援</span><span class="sxs-lookup"><span data-stu-id="239df-191">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="239df-192">*ExternalKey* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="239df-192">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="239df-193">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="239df-193">Type: **uint8\[\]**</span></span>

<span data-ttu-id="239df-194">位元組陣列，指定當電腦啟動時，用來解除鎖定磁片區的256位外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="239df-194">An array of bytes that specifies the 256-bit external key used to unlock the volume when the computer starts.</span></span>

<span data-ttu-id="239df-195">如果未指定外部索引鍵，則會隨機產生一個索引鍵。</span><span class="sxs-lookup"><span data-stu-id="239df-195">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="239df-196">使用 [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) 方法來取得隨機產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="239df-196">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="239df-197">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="239df-197">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="239df-198">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="239df-198">Type: **string**</span></span>

<span data-ttu-id="239df-199">字串，這個字串是與建立的金鑰保護裝置相關聯的唯一識別碼，可用於管理金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="239df-199">A string that is the unique identifier associated with the created key protector that can be used to manage the key protector.</span></span>

<span data-ttu-id="239df-200">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="239df-200">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="239df-201">傳回值</span><span class="sxs-lookup"><span data-stu-id="239df-201">Return value</span></span>

<span data-ttu-id="239df-202">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="239df-202">Type: **uint32**</span></span>

<span data-ttu-id="239df-203">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="239df-203">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="239df-204">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="239df-204">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="239df-205">Description</span><span class="sxs-lookup"><span data-stu-id="239df-205">Description</span></span>                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="239df-206"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="239df-206"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="239df-207">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="239df-207">The method was successful.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="239df-208"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="239df-208"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="239df-209">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="239df-209">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="239df-210"><dt>**Tb \_E \_ 服務 \_ 未 \_**</dt>執行 <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="239df-210"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="239df-211">在這部電腦上找不到相容的 TPM。</span><span class="sxs-lookup"><span data-stu-id="239df-211">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="239df-212"><dt>**FVE \_E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="239df-212"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="239df-213">TPM 無法保護磁片區的加密金鑰，因為磁片區未包含目前執行中的作業系統。</span><span class="sxs-lookup"><span data-stu-id="239df-213">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                                                                                                               |
| <dl> <span data-ttu-id="239df-214"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="239df-214"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="239df-215">已提供 *PlatformValidationProfile* 參數，但其值不在已知範圍內，或者不符合目前作用中的群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="239df-215">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> <span data-ttu-id="239df-216">提供 *ExternalKey* 參數，但不是大小為32的陣列。</span><span class="sxs-lookup"><span data-stu-id="239df-216">The *ExternalKey* parameter is provided but is not an array of size 32.</span></span><br/> |
| <dl> <span data-ttu-id="239df-217"><dt>**FVE \_E \_ 可 \_**</dt>開機的 CDDVD <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="239df-217"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>       | <span data-ttu-id="239df-218">在這部電腦上找到可開機的 CD/DVD。</span><span class="sxs-lookup"><span data-stu-id="239df-218">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="239df-219">移除 CD/DVD 並重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="239df-219">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="239df-220"><dt>**FVE \_E \_ 保護裝置 \_ 存在**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="239df-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>     | <span data-ttu-id="239df-221">此類型的金鑰保護裝置已經存在。</span><span class="sxs-lookup"><span data-stu-id="239df-221">A key protector of this type already exists.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a><span data-ttu-id="239df-222">安全性考量</span><span class="sxs-lookup"><span data-stu-id="239df-222">Security Considerations</span></span>

<span data-ttu-id="239df-223">針對電腦的安全性，建議預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="239df-223">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="239df-224">若要針對早期啟動程式碼變更進行額外的保護，請使用 PCRs 0、2、4、5、8、9、10和11的設定檔。</span><span class="sxs-lookup"><span data-stu-id="239df-224">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="239df-225">若要針對早期啟動設定變更進行額外的保護，請使用 PCRs 0、1、2、3、4、5、8、9、10、11的設定檔。</span><span class="sxs-lookup"><span data-stu-id="239df-225">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="239df-226">變更預設設定檔會影響您電腦的安全性或可用性。</span><span class="sxs-lookup"><span data-stu-id="239df-226">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="239df-227">備註</span><span class="sxs-lookup"><span data-stu-id="239df-227">Remarks</span></span>

<span data-ttu-id="239df-228">磁片區最多隻能有一個類型為「TPM 和啟動金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="239df-228">At most one key protector of type "TPM And Startup Key" can exist for a volume at any time.</span></span> <span data-ttu-id="239df-229">如果您想要變更現有「TPM plus 啟動金鑰」金鑰保護裝置所使用的顯示名稱或平臺驗證設定檔，您必須先移除現有的金鑰保護裝置，然後呼叫 **ProtectKeyWithTPMAndStartupKey** 來建立新的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="239df-229">If you want to change the display name or the platform validation profile used by an existing "TPM plus Startup Key" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndStartupKey** to create a new one.</span></span> <span data-ttu-id="239df-230">您應指定額外的金鑰保護裝置，以在無法取得存取磁片區加密金鑰的復原案例中解除鎖定磁片區;例如，當 TPM 無法成功驗證平臺驗證設定檔，或包含外部金鑰的 USB 記憶體遺失時。</span><span class="sxs-lookup"><span data-stu-id="239df-230">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when USB memory that contains the external key is lost.</span></span>

<span data-ttu-id="239df-231">使用 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 或 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 來建立一或多個金鑰保護裝置，以復原其他鎖定的磁片區。</span><span class="sxs-lookup"><span data-stu-id="239df-231">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="239df-232">雖然可以同時有類型為 "TPM" 的金鑰保護裝置，以及另一種類型為「TPM 和啟動金鑰」的金鑰保護裝置，但「TPM」金鑰保護裝置類型的存在會使其他以 TPM 為基礎的金鑰保護裝置產生的影響不會影響。</span><span class="sxs-lookup"><span data-stu-id="239df-232">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And Startup Key", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="239df-233">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="239df-233">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="239df-234">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="239df-234">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="239df-235">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="239df-235">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="239df-236">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="239df-236">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="239df-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="239df-237">Requirements</span></span>



| <span data-ttu-id="239df-238">需求</span><span class="sxs-lookup"><span data-stu-id="239df-238">Requirement</span></span> | <span data-ttu-id="239df-239">值</span><span class="sxs-lookup"><span data-stu-id="239df-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239df-240">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="239df-240">Minimum supported client</span></span><br/> | <span data-ttu-id="239df-241">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="239df-241">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="239df-242">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="239df-242">Minimum supported server</span></span><br/> | <span data-ttu-id="239df-243">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="239df-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="239df-244">命名空間</span><span class="sxs-lookup"><span data-stu-id="239df-244">Namespace</span></span><br/>                | <span data-ttu-id="239df-245">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="239df-245">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="239df-246">MOF</span><span class="sxs-lookup"><span data-stu-id="239df-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="239df-247"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="239df-247"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239df-248">另請參閱</span><span class="sxs-lookup"><span data-stu-id="239df-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239df-249">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="239df-249">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="239df-250">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="239df-250">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
