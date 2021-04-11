---
description: 如果可信賴平臺模組 (TPM) 可供使用，這個方法會保護以使用者指定的個人識別碼增強的磁片區加密金鑰。
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: Win32_EncryptableVolume 類別的 ProtectKeyWithTPMAndPIN 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e5a0a7a253723bec84df7a86fa94ab182bd192dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847871"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b292a-103">Win32 EncryptableVolume 類別的 ProtectKeyWithTPMAndPIN 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b292a-103">ProtectKeyWithTPMAndPIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b292a-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithTPMAndPIN** 方法會使用可信賴平臺模組 (TPM) 電腦上的安全性硬體（如果有的話）來保護磁片區的加密金鑰（如果有的話），並在啟動時必須提供給電腦的使用者指定個人識別碼 (PIN) 。</span><span class="sxs-lookup"><span data-stu-id="b292a-104">The **ProtectKeyWithTPMAndPIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by a user-specified personal identification number (PIN) that must be provided to the computer at startup.</span></span>

<span data-ttu-id="b292a-105">TPM 和個人識別碼的輸入都需要驗證，才能存取磁片區的加密金鑰並解除鎖定磁片區內容。</span><span class="sxs-lookup"><span data-stu-id="b292a-105">Both validation by the TPM and input of the personal identification string are necessary to access the volume's encryption key and unlock volume contents.</span></span>

<span data-ttu-id="b292a-106">這個方法僅適用于包含目前正在執行之作業系統的磁片區。</span><span class="sxs-lookup"><span data-stu-id="b292a-106">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="b292a-107">如果磁片區不存在，就會為磁片區建立「TPM 和 PIN」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="b292a-107">A key protector of type "TPM And PIN" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="b292a-108">語法</span><span class="sxs-lookup"><span data-stu-id="b292a-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="b292a-109">參數</span><span class="sxs-lookup"><span data-stu-id="b292a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b292a-110">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b292a-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b292a-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b292a-111">Type: **string**</span></span>

<span data-ttu-id="b292a-112">使用者指派給此金鑰保護裝置的字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="b292a-112">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="b292a-113">如果未指定此參數，則會使用空白值。</span><span class="sxs-lookup"><span data-stu-id="b292a-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="b292a-114">*PlatformValidationProfile* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b292a-114">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b292a-115">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b292a-115">Type: **uint8\[\]**</span></span>

<span data-ttu-id="b292a-116">整數陣列，指定電腦的信賴平臺模組 (TPM) 安全性硬體如何保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b292a-116">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="b292a-117">平臺驗證設定檔包含一組平臺設定暫存器 (PCR) 索引，範圍從0到23（含）。</span><span class="sxs-lookup"><span data-stu-id="b292a-117">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="b292a-118">參數中的重複值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b292a-118">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="b292a-119">每個 PCR 索引都會與作業系統啟動時執行的服務相關聯。</span><span class="sxs-lookup"><span data-stu-id="b292a-119">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="b292a-120">每次電腦啟動時，TPM 都會檢查您在平臺驗證設定檔中指定的服務是否未變更。</span><span class="sxs-lookup"><span data-stu-id="b292a-120">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="b292a-121">如果其中任何一項服務在 BitLocker 磁碟機加密)  (的情況下變更，則 TPM 不會釋出加密金鑰來解除鎖定磁片區，而且電腦會進入修復模式。</span><span class="sxs-lookup"><span data-stu-id="b292a-121">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="b292a-122">如果指定了這個參數，但已啟用對應的群組原則設定，它就必須符合群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="b292a-122">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="b292a-123">如果未指定此參數，則會使用預設值0、2、4、5、8、9、10和11。</span><span class="sxs-lookup"><span data-stu-id="b292a-123">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="b292a-124">預設的平臺驗證設定檔會針對下列元素的變更保護加密金鑰：</span><span class="sxs-lookup"><span data-stu-id="b292a-124">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="b292a-125">度量 (的核心根信任 CRTM) </span><span class="sxs-lookup"><span data-stu-id="b292a-125">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="b292a-126">BIOS</span><span class="sxs-lookup"><span data-stu-id="b292a-126">BIOS</span></span>
-   <span data-ttu-id="b292a-127"> (PCR 0) 的平臺擴充</span><span class="sxs-lookup"><span data-stu-id="b292a-127">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="b292a-128">選項 ROM 代碼 (PCR 2) </span><span class="sxs-lookup"><span data-stu-id="b292a-128">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="b292a-129">主開機記錄 (MBR) 代碼 (PCR 4) </span><span class="sxs-lookup"><span data-stu-id="b292a-129">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="b292a-130">主開機記錄 (MBR) 磁碟分割表格 (PCR 5) </span><span class="sxs-lookup"><span data-stu-id="b292a-130">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="b292a-131"> (PCR 8) 的 NTFS 開機磁區</span><span class="sxs-lookup"><span data-stu-id="b292a-131">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="b292a-132">NTFS 開機區塊 (PCR 9) </span><span class="sxs-lookup"><span data-stu-id="b292a-132">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="b292a-133">開機管理程式 (PCR 10) </span><span class="sxs-lookup"><span data-stu-id="b292a-133">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="b292a-134">BitLocker 存取控制 (PCR 11) </span><span class="sxs-lookup"><span data-stu-id="b292a-134">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="b292a-135">針對電腦的安全性，建議預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="b292a-135">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="b292a-136">若要針對早期啟動設定變更進行額外的保護，請使用 PCRs 0、1、2、3、4、5、8、9、10、11的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b292a-136">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="b292a-137">整合可延伸韌體介面 (UEFI) 型電腦預設不會使用 PCR 5。</span><span class="sxs-lookup"><span data-stu-id="b292a-137">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="b292a-138">變更預設設定檔會影響電腦的安全性與管理性。</span><span class="sxs-lookup"><span data-stu-id="b292a-138">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="b292a-139">BitLocker 對平臺修改的機密性 (惡意或授權的) 會隨著 PCRs 的包含或排除而增加或減少。</span><span class="sxs-lookup"><span data-stu-id="b292a-139">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="b292a-140">若要啟用 BitLocker 保護，平臺驗證設定檔必須包含 PCR 11。</span><span class="sxs-lookup"><span data-stu-id="b292a-140">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="b292a-141">值</span><span class="sxs-lookup"><span data-stu-id="b292a-141">Value</span></span>                                                                         | <span data-ttu-id="b292a-142">意義</span><span class="sxs-lookup"><span data-stu-id="b292a-142">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b292a-143"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-143"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="b292a-144"> (CRTM) 、BIOS 和平臺擴充的測量核心根信任</span><span class="sxs-lookup"><span data-stu-id="b292a-144">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="b292a-145"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-145"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="b292a-146">平臺和主機板設定和資料</span><span class="sxs-lookup"><span data-stu-id="b292a-146">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="b292a-147"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-147"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="b292a-148">選項 ROM 代碼</span><span class="sxs-lookup"><span data-stu-id="b292a-148">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="b292a-149"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-149"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="b292a-150">選項 ROM 設定和資料</span><span class="sxs-lookup"><span data-stu-id="b292a-150">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="b292a-151"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-151"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="b292a-152">主開機記錄 (MBR) 碼</span><span class="sxs-lookup"><span data-stu-id="b292a-152">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="b292a-153"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-153"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="b292a-154">主開機記錄 (MBR) 磁碟分割資料表</span><span class="sxs-lookup"><span data-stu-id="b292a-154">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="b292a-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-155"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="b292a-156">狀態轉換和喚醒事件</span><span class="sxs-lookup"><span data-stu-id="b292a-156">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="b292a-157"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-157"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="b292a-158">電腦 Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="b292a-158">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="b292a-159"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-159"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="b292a-160">NTFS 開機磁區</span><span class="sxs-lookup"><span data-stu-id="b292a-160">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b292a-161"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-161"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="b292a-162">NTFS 開機區塊</span><span class="sxs-lookup"><span data-stu-id="b292a-162">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="b292a-163"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-163"><dt>10</dt></span></span> </dl> | <span data-ttu-id="b292a-164">開機管理程式</span><span class="sxs-lookup"><span data-stu-id="b292a-164">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="b292a-165"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-165"><dt>11</dt></span></span> </dl> | <span data-ttu-id="b292a-166">BitLocker 存取控制</span><span class="sxs-lookup"><span data-stu-id="b292a-166">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="b292a-167"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-167"><dt>12</dt></span></span> </dl> | <span data-ttu-id="b292a-168">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="b292a-168">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="b292a-169"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-169"><dt>13</dt></span></span> </dl> | <span data-ttu-id="b292a-170">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="b292a-170">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="b292a-171"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-171"><dt>14</dt></span></span> </dl> | <span data-ttu-id="b292a-172">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="b292a-172">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="b292a-173"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-173"><dt>15</dt></span></span> </dl> | <span data-ttu-id="b292a-174">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="b292a-174">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="b292a-175"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-175"><dt>16</dt></span></span> </dl> | <span data-ttu-id="b292a-176">用於偵錯工具</span><span class="sxs-lookup"><span data-stu-id="b292a-176">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="b292a-177"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-177"><dt>17</dt></span></span> </dl> | <span data-ttu-id="b292a-178">動態 CRTM</span><span class="sxs-lookup"><span data-stu-id="b292a-178">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="b292a-179"><dt>達</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-179"><dt>18</dt></span></span> </dl> | <span data-ttu-id="b292a-180">已定義平臺</span><span class="sxs-lookup"><span data-stu-id="b292a-180">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b292a-181"><dt>診斷</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-181"><dt>19</dt></span></span> </dl> | <span data-ttu-id="b292a-182">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="b292a-182">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="b292a-183"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-183"><dt>20</dt></span></span> </dl> | <span data-ttu-id="b292a-184">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="b292a-184">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="b292a-185"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-185"><dt>21</dt></span></span> </dl> | <span data-ttu-id="b292a-186">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="b292a-186">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="b292a-187"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-187"><dt>22</dt></span></span> </dl> | <span data-ttu-id="b292a-188">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="b292a-188">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="b292a-189"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-189"><dt>23</dt></span></span> </dl> | <span data-ttu-id="b292a-190">應用程式支援</span><span class="sxs-lookup"><span data-stu-id="b292a-190">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="b292a-191">*PIN* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b292a-191">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b292a-192">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b292a-192">Type: **string**</span></span>

<span data-ttu-id="b292a-193">使用者指定的個人識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="b292a-193">A user-specified personal identification string.</span></span> <span data-ttu-id="b292a-194">此字串必須包含6到20位數的序列，或如果已啟用 [允許啟動的增強式 Pin] 群組原則，則為6到20個字母、符號、空格或數位。</span><span class="sxs-lookup"><span data-stu-id="b292a-194">This string must consist of a sequence of 6 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 6 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> <dt>

<span data-ttu-id="b292a-195">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b292a-195">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b292a-196">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b292a-196">Type: **string**</span></span>

<span data-ttu-id="b292a-197">用來管理加密磁片區金鑰保護裝置的更新唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="b292a-197">The updated unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="b292a-198">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b292a-198">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b292a-199">傳回值</span><span class="sxs-lookup"><span data-stu-id="b292a-199">Return value</span></span>

<span data-ttu-id="b292a-200">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b292a-200">Type: **uint32**</span></span>

<span data-ttu-id="b292a-201">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b292a-201">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b292a-202">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b292a-202">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="b292a-203">Description</span><span class="sxs-lookup"><span data-stu-id="b292a-203">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b292a-204"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-204"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="b292a-205">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="b292a-205">The method was successful.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="b292a-206"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-206"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                        | <span data-ttu-id="b292a-207">已提供 *PlatformValidationProfile* 參數，但其值不在已知範圍內，或者不符合目前作用中的群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="b292a-207">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="b292a-208"><dt>**FVE \_E \_ 可 \_**</dt>開機的 CDDVD <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-208"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="b292a-209">在這部電腦上找到可開機的 CD/DVD。</span><span class="sxs-lookup"><span data-stu-id="b292a-209">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="b292a-210">移除 CD/DVD 並重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="b292a-210">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b292a-211"><dt>**FVE \_E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-211"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>              | <span data-ttu-id="b292a-212">TPM 無法保護磁片區的加密金鑰，因為磁片區未包含目前執行中的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b292a-212">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b292a-213"><dt>**FVE \_E \_ 不正確 \_ PIN \_ 字元**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-213"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="b292a-214">*NewPIN* 參數包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="b292a-214">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="b292a-215">當停用 [允許啟動的增強式 Pin] 群組原則時，只支援數位。</span><span class="sxs-lookup"><span data-stu-id="b292a-215">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>          |
| <dl> <span data-ttu-id="b292a-216"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-216"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="b292a-217">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="b292a-217">The volume is locked.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="b292a-218"><dt>**FVE \_E \_ 原則 \_ 不正確 \_ PIN \_ 長度**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-218"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="b292a-219">提供的 *NewPIN* 參數長度超過20個字元、少於6個字元，或小於群組原則指定的最小長度。</span><span class="sxs-lookup"><span data-stu-id="b292a-219">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 6 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>            |
| <dl> <span data-ttu-id="b292a-220"><dt>**FVE \_E \_ 保護裝置 \_ 存在**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="b292a-221">此類型的金鑰保護裝置已經存在。</span><span class="sxs-lookup"><span data-stu-id="b292a-221">A key protector of this type already exists.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="b292a-222"><dt>**Tb \_E \_ 服務 \_ 未 \_**</dt>執行 <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-222"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="b292a-223">在這部電腦上找不到相容的 TPM。</span><span class="sxs-lookup"><span data-stu-id="b292a-223">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="b292a-224">安全性考量</span><span class="sxs-lookup"><span data-stu-id="b292a-224">Security Considerations</span></span>

<span data-ttu-id="b292a-225">針對電腦的安全性，建議預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="b292a-225">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="b292a-226">若要針對早期啟動程式碼變更進行額外的保護，請使用 PCRs 0、2、4、5、8、9、10和11的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b292a-226">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="b292a-227">若要針對早期啟動設定變更進行額外的保護，請使用 PCRs 0、1、2、3、4、5、8、9、10、11的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b292a-227">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="b292a-228">變更預設設定檔會影響您電腦的安全性或可用性。</span><span class="sxs-lookup"><span data-stu-id="b292a-228">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="b292a-229">備註</span><span class="sxs-lookup"><span data-stu-id="b292a-229">Remarks</span></span>

<span data-ttu-id="b292a-230">磁片區最多隻能有一個類型為「TPM 和 PIN」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="b292a-230">At most one key protector of type "TPM And PIN" can exist for a volume at any time.</span></span> <span data-ttu-id="b292a-231">如果您想要變更現有「TPM 和 PIN」金鑰保護裝置所使用的顯示名稱或平臺驗證設定檔，您必須先移除現有的金鑰保護裝置，然後呼叫 **ProtectKeyWithTPMAndPIN** 來建立新的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="b292a-231">If you want to change the display name or the platform validation profile used by an existing "TPM And PIN" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndPIN** to create a new one.</span></span>

<span data-ttu-id="b292a-232">您應指定額外的金鑰保護裝置，以在無法取得存取磁片區加密金鑰的復原案例中解除鎖定磁片區;例如，TPM 無法成功驗證平臺驗證設定檔或 PIN 遺失時。</span><span class="sxs-lookup"><span data-stu-id="b292a-232">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when the PIN is lost.</span></span>

<span data-ttu-id="b292a-233">使用 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 或 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 來建立一或多個金鑰保護裝置，以復原其他鎖定的磁片區。</span><span class="sxs-lookup"><span data-stu-id="b292a-233">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="b292a-234">雖然可以同時有類型為 "TPM" 的金鑰保護裝置，以及另一種類型為「TPM 和 PIN」的金鑰保護裝置，但「TPM」金鑰保護裝置類型的存在會使其他以 TPM 為基礎的金鑰保護裝置產生的影響。</span><span class="sxs-lookup"><span data-stu-id="b292a-234">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And PIN", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="b292a-235">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b292a-235">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b292a-236">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b292a-236">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b292a-237">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b292a-237">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b292a-238">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="b292a-238">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b292a-239">規格需求</span><span class="sxs-lookup"><span data-stu-id="b292a-239">Requirements</span></span>



| <span data-ttu-id="b292a-240">需求</span><span class="sxs-lookup"><span data-stu-id="b292a-240">Requirement</span></span> | <span data-ttu-id="b292a-241">值</span><span class="sxs-lookup"><span data-stu-id="b292a-241">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b292a-242">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b292a-242">Minimum supported client</span></span><br/> | <span data-ttu-id="b292a-243">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b292a-243">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b292a-244">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b292a-244">Minimum supported server</span></span><br/> | <span data-ttu-id="b292a-245">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b292a-245">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b292a-246">命名空間</span><span class="sxs-lookup"><span data-stu-id="b292a-246">Namespace</span></span><br/>                | <span data-ttu-id="b292a-247">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b292a-247">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b292a-248">MOF</span><span class="sxs-lookup"><span data-stu-id="b292a-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b292a-249"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="b292a-249"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b292a-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b292a-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b292a-251">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="b292a-251">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="b292a-252">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="b292a-252">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
