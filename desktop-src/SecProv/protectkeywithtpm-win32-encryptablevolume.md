---
description: 如果可信賴平臺模組 (TPM) 可供使用，這個方法會保護磁片區的加密金鑰。
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Win32_EncryptableVolume 類別的 ProtectKeyWithTPM 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994416"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2a5e9-103">Win32 EncryptableVolume 類別的 ProtectKeyWithTPM 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2a5e9-103">ProtectKeyWithTPM method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2a5e9-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithTPM** 方法會使用可信賴平臺模組 (TPM) 電腦上的安全性硬體（如果有的話）來保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-104">The **ProtectKeyWithTPM** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available.</span></span>

<span data-ttu-id="2a5e9-105">如果磁片區不存在，就會為磁片區建立「TPM」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-105">A key protector of type "TPM" is created for the volume, if one does not already exist.</span></span>

<span data-ttu-id="2a5e9-106">此方法僅適用于包含目前正在執行之作業系統的磁片區，以及磁片區上是否還沒有金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-106">This method is only applicable for the volume that contains the currently running operating system, and if a key protector does not already exist on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a5e9-107">語法</span><span class="sxs-lookup"><span data-stu-id="2a5e9-107">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="2a5e9-108">參數</span><span class="sxs-lookup"><span data-stu-id="2a5e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a5e9-109">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2a5e9-109">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a5e9-110">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2a5e9-110">Type: **string**</span></span>

<span data-ttu-id="2a5e9-111">字串，指定此金鑰保護裝置的使用者指派字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-111">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="2a5e9-112">如果未指定此參數，則會使用空白值。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-112">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="2a5e9-113">*PlatformValidationProfile* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2a5e9-113">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a5e9-114">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="2a5e9-114">Type: **uint8\[\]**</span></span>

<span data-ttu-id="2a5e9-115">整數陣列，指定電腦的信賴平臺模組 (TPM) 安全性硬體如何保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-115">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="2a5e9-116">平臺驗證設定檔包含一組平臺設定暫存器 (PCR) 索引，範圍從0到23（含）。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-116">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="2a5e9-117">參數中的重複值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-117">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="2a5e9-118">每個 PCR 索引都會與作業系統啟動時執行的服務相關聯。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-118">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="2a5e9-119">每次電腦啟動時，TPM 都會檢查您在平臺驗證設定檔中指定的服務是否未變更。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-119">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="2a5e9-120">如果其中任何一項服務在 BitLocker 磁碟機加密)  (的情況下變更，則 TPM 不會釋出加密金鑰來解除鎖定磁片區，而且電腦會進入修復模式。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-120">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="2a5e9-121">如果指定了這個參數，但已啟用對應的群組原則設定，它就必須符合群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-121">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="2a5e9-122">如果未指定此參數，則會使用預設值0、2、4、5、8、9、10和11。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-122">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="2a5e9-123">預設的平臺驗證設定檔可保護加密金鑰，以避免 (CRTM) 、BIOS 和平臺擴充 (PCR 0) 、選項 ROM 程式碼 (PCR 2) 、主開機記錄 (MBR) 程式碼 (PCR 4) 、主開機記錄 (MBR) 磁碟分割資料表 (PCR 5) 、NTFS 開機磁區 (pcr 8) 、NTFS 開機程式碼 (pcr 9) 、開機管理程式 (pcr 10) 和 BitLocker 磁碟機加密存取控制 (PCR 11) 。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-123">The default platform validation profile secures the encryption key against changes to the Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions (PCR 0), Option ROM Code (PCR 2), the Master Boot Record (MBR) Code (PCR 4), the Master Boot Record (MBR) Partition Table (PCR 5), the NTFS Boot Sector (PCR 8), the NTFS Boot Code (PCR 9), the Boot Manager (PCR 10), and the BitLocker Drive Encryption Access Control (PCR 11).</span></span> <span data-ttu-id="2a5e9-124">針對電腦的安全性，建議預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-124">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="2a5e9-125">整合可延伸韌體介面 (UEFI) 型電腦預設不會使用 PCR 5。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-125">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span> <span data-ttu-id="2a5e9-126">若要針對早期啟動設定變更進行額外的保護，請使用 PCRs 0、1、2、3、4、5、8、9、10、11的設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-126">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="2a5e9-127">變更預設設定檔會影響電腦的安全性與管理性。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-127">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="2a5e9-128">BitLocker 對平臺修改的機密性 (惡意或授權的) 會隨著 PCRs 的包含或排除而增加或減少。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-128">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="2a5e9-129">若要啟用 BitLocker 保護，平臺驗證設定檔必須包含 PCR 11。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-129">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="2a5e9-130">值</span><span class="sxs-lookup"><span data-stu-id="2a5e9-130">Value</span></span>                                                                         | <span data-ttu-id="2a5e9-131">意義</span><span class="sxs-lookup"><span data-stu-id="2a5e9-131">Meaning</span></span>                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a5e9-132"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-132"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-133"> () 、BIOS 和平臺擴充的測量核心的核心信任。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-133">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions.</span></span><br/> |
| <dl> <span data-ttu-id="2a5e9-134"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-134"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-135">平臺和主機板設定和資料</span><span class="sxs-lookup"><span data-stu-id="2a5e9-135">Platform and Motherboard Configuration and Data</span></span><br/>                          |
| <dl> <span data-ttu-id="2a5e9-136"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-136"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-137">選項 ROM 代碼</span><span class="sxs-lookup"><span data-stu-id="2a5e9-137">Option ROM Code</span></span><br/>                                                          |
| <dl> <span data-ttu-id="2a5e9-138"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-138"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-139">選項 ROM 設定和資料</span><span class="sxs-lookup"><span data-stu-id="2a5e9-139">Option ROM Configuration and Data</span></span><br/>                                        |
| <dl> <span data-ttu-id="2a5e9-140"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-140"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-141">主開機記錄 (MBR) 碼</span><span class="sxs-lookup"><span data-stu-id="2a5e9-141">Master Boot Record (MBR) Code</span></span><br/>                                            |
| <dl> <span data-ttu-id="2a5e9-142"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-142"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-143">主開機記錄 (MBR) 磁碟分割資料表</span><span class="sxs-lookup"><span data-stu-id="2a5e9-143">Master Boot Record (MBR) Partition Table</span></span><br/>                                 |
| <dl> <span data-ttu-id="2a5e9-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-144"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-145">狀態轉換和喚醒事件</span><span class="sxs-lookup"><span data-stu-id="2a5e9-145">State Transition and Wake Events</span></span><br/>                                         |
| <dl> <span data-ttu-id="2a5e9-146"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-146"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-147">電腦 Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="2a5e9-147">Computer Manufacturer-Specific</span></span><br/>                                           |
| <dl> <span data-ttu-id="2a5e9-148"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-148"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-149">NTFS 開機磁區</span><span class="sxs-lookup"><span data-stu-id="2a5e9-149">NTFS Boot Sector</span></span><br/>                                                         |
| <dl> <span data-ttu-id="2a5e9-150"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-150"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="2a5e9-151">NTFS 開機碼</span><span class="sxs-lookup"><span data-stu-id="2a5e9-151">NTFS Boot Code</span></span><br/>                                                           |
| <dl> <span data-ttu-id="2a5e9-152"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-152"><dt>10</dt></span></span> </dl> | <span data-ttu-id="2a5e9-153">開機管理程式</span><span class="sxs-lookup"><span data-stu-id="2a5e9-153">Boot Manager</span></span><br/>                                                             |
| <dl> <span data-ttu-id="2a5e9-154"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-154"><dt>11</dt></span></span> </dl> | <span data-ttu-id="2a5e9-155">BitLocker 磁碟機加密存取控制</span><span class="sxs-lookup"><span data-stu-id="2a5e9-155">BitLocker Drive Encryption Access Control</span></span><br/>                                |
| <dl> <span data-ttu-id="2a5e9-156"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-156"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2a5e9-157">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="2a5e9-157">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="2a5e9-158"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-158"><dt>13</dt></span></span> </dl> | <span data-ttu-id="2a5e9-159">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="2a5e9-159">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="2a5e9-160"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-160"><dt>14</dt></span></span> </dl> | <span data-ttu-id="2a5e9-161">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="2a5e9-161">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="2a5e9-162"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-162"><dt>15</dt></span></span> </dl> | <span data-ttu-id="2a5e9-163">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="2a5e9-163">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="2a5e9-164"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-164"><dt>16</dt></span></span> </dl> | <span data-ttu-id="2a5e9-165">用於偵錯工具</span><span class="sxs-lookup"><span data-stu-id="2a5e9-165">Used for debugging</span></span><br/>                                                       |
| <dl> <span data-ttu-id="2a5e9-166"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-166"><dt>17</dt></span></span> </dl> | <span data-ttu-id="2a5e9-167">動態 CRTM</span><span class="sxs-lookup"><span data-stu-id="2a5e9-167">Dynamic CRTM</span></span><br/>                                                             |
| <dl> <span data-ttu-id="2a5e9-168"><dt>達</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-168"><dt>18</dt></span></span> </dl> | <span data-ttu-id="2a5e9-169">已定義平臺</span><span class="sxs-lookup"><span data-stu-id="2a5e9-169">Platform defined</span></span><br/>                                                         |
| <dl> <span data-ttu-id="2a5e9-170"><dt>診斷</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-170"><dt>19</dt></span></span> </dl> | <span data-ttu-id="2a5e9-171">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="2a5e9-171">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="2a5e9-172"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-172"><dt>20</dt></span></span> </dl> | <span data-ttu-id="2a5e9-173">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="2a5e9-173">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="2a5e9-174"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-174"><dt>21</dt></span></span> </dl> | <span data-ttu-id="2a5e9-175">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="2a5e9-175">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="2a5e9-176"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-176"><dt>22</dt></span></span> </dl> | <span data-ttu-id="2a5e9-177">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="2a5e9-177">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="2a5e9-178"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-178"><dt>23</dt></span></span> </dl> | <span data-ttu-id="2a5e9-179">應用程式支援</span><span class="sxs-lookup"><span data-stu-id="2a5e9-179">Application support</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="2a5e9-180">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2a5e9-180">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a5e9-181">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2a5e9-181">Type: **string**</span></span>

<span data-ttu-id="2a5e9-182">此字串可唯一識別已建立的保護裝置，並可用於管理金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-182">A string that uniquely identifies the created protector and which can be used to manage the key protector.</span></span>

<span data-ttu-id="2a5e9-183">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-183">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a5e9-184">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a5e9-184">Return value</span></span>

<span data-ttu-id="2a5e9-185">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2a5e9-185">Type: **uint32**</span></span>

<span data-ttu-id="2a5e9-186">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-186">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2a5e9-187">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="2a5e9-187">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="2a5e9-188">Description</span><span class="sxs-lookup"><span data-stu-id="2a5e9-188">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a5e9-189"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-189"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="2a5e9-190">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-190">The method was successful.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="2a5e9-191"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-191"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="2a5e9-192">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-192">The volume is locked.</span></span><br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="2a5e9-193"><dt>**Tb \_E \_ 服務 \_ 未 \_**</dt>執行 <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-193"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="2a5e9-194">在這部電腦上找不到相容的 TPM。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-194">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="2a5e9-195"><dt>**FVE \_E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-195"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="2a5e9-196">TPM 無法保護磁片區的加密金鑰，因為磁片區未包含目前執行中的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-196">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                           |
| <dl> <span data-ttu-id="2a5e9-197"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-197"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="2a5e9-198">提供 *PlatformValidationProfile* 參數，但其值不在已知範圍內，或者不符合目前作用中的群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-198">The *PlatformValidationProfile* parameter is provided but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="2a5e9-199"><dt>**FVE \_E \_ 保護裝置 \_ 存在**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-199"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="2a5e9-200">此類型的金鑰保護裝置已經存在。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-200">A key protector of this type already exists.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="2a5e9-201">安全性考量</span><span class="sxs-lookup"><span data-stu-id="2a5e9-201">Security Considerations</span></span>

<span data-ttu-id="2a5e9-202">針對電腦的安全性，建議預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-202">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="2a5e9-203">若要針對早期啟動設定變更進行額外的保護，請使用 PCRs 0、1、2、3、4、5、8、9、10、11的設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-203">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="2a5e9-204">變更預設設定檔會影響您電腦的安全性或可用性。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-204">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a5e9-205">備註</span><span class="sxs-lookup"><span data-stu-id="2a5e9-205">Remarks</span></span>

<span data-ttu-id="2a5e9-206">磁片區最多隻能有一個類型為 "TPM" 的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-206">At most one key protector of type "TPM" can exist for a volume at any time.</span></span> <span data-ttu-id="2a5e9-207">如果您想要變更現有「TPM」金鑰保護裝置所使用的顯示名稱或平臺驗證設定檔，您必須先移除現有的金鑰保護裝置，然後呼叫 **ProtectKeyWithTPM** 來建立新的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-207">If you want to change the display name or the platform validation profile used by an existing "TPM" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPM** to create a new one.</span></span>

<span data-ttu-id="2a5e9-208">若為 PCR 索引0到5，則會使用暫存器中目前的度量來保護加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-208">For PCR indices 0 through 5, the current measurements in the registers are used to protect the encryption key.</span></span> <span data-ttu-id="2a5e9-209">針對 PCR 值8到11，使用的測量值是預期會存在於下一個啟動週期的度量。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-209">For PCR values 8 through 11, the measurements used are the ones expected to exist on the next start cycle.</span></span>

<span data-ttu-id="2a5e9-210">您應指定額外的金鑰保護裝置，以在無法取得存取磁片區加密金鑰的復原案例中解除鎖定磁片區;例如，當 TPM 無法成功驗證平臺驗證設定檔時。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-210">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile.</span></span> <span data-ttu-id="2a5e9-211">使用 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 或 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 來建立一或多個金鑰保護裝置，以復原其他鎖定的磁片區。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-211">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="2a5e9-212">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-212">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2a5e9-213">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-213">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2a5e9-214">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-214">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2a5e9-215">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="2a5e9-215">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a5e9-216">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a5e9-216">Requirements</span></span>



| <span data-ttu-id="2a5e9-217">需求</span><span class="sxs-lookup"><span data-stu-id="2a5e9-217">Requirement</span></span> | <span data-ttu-id="2a5e9-218">值</span><span class="sxs-lookup"><span data-stu-id="2a5e9-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a5e9-219">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a5e9-219">Minimum supported client</span></span><br/> | <span data-ttu-id="2a5e9-220">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a5e9-220">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2a5e9-221">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a5e9-221">Minimum supported server</span></span><br/> | <span data-ttu-id="2a5e9-222">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a5e9-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a5e9-223">命名空間</span><span class="sxs-lookup"><span data-stu-id="2a5e9-223">Namespace</span></span><br/>                | <span data-ttu-id="2a5e9-224">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="2a5e9-224">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2a5e9-225">MOF</span><span class="sxs-lookup"><span data-stu-id="2a5e9-225">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a5e9-226"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e9-226"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a5e9-227">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a5e9-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a5e9-228">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="2a5e9-228">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="2a5e9-229">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="2a5e9-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
