---
description: 抓取適當類型之指定金鑰保護裝置的平臺驗證設定檔。
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Win32_EncryptableVolume 類別的 GetKeyProtectorPlatformValidationProfile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998146"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e4fbc-103">Win32 EncryptableVolume 類別的 GetKeyProtectorPlatformValidationProfile 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e4fbc-103">GetKeyProtectorPlatformValidationProfile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e4fbc-104">**GetKeyProtectorPlatformValidationProfile** 方法會針對適當類型的指定金鑰保護裝置，抓取平臺驗證設定檔。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-104">The **GetKeyProtectorPlatformValidationProfile** method retrieves the platform validation profile for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="e4fbc-105">金鑰保護裝置識別碼必須參考「TPM」、「TPM 和 PIN」、「TPM 和 PIN 和啟動金鑰」或「TPM 和啟動金鑰」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-105">The key protector identifier must refer to a key protector of type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fbc-106">語法</span><span class="sxs-lookup"><span data-stu-id="e4fbc-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a><span data-ttu-id="e4fbc-107">參數</span><span class="sxs-lookup"><span data-stu-id="e4fbc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4fbc-108">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4fbc-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4fbc-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4fbc-109">Type: **string**</span></span>

<span data-ttu-id="e4fbc-110">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="e4fbc-111">*PlatformValidationProfile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e4fbc-111">*PlatformValidationProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4fbc-112">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e4fbc-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="e4fbc-113">整數的陣列，指定可信賴平臺模組如何 (TPM) 電腦的安全性硬體，以保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-113">An array of integers that specifies how the Trusted Platform Module (TPM) Security Hardware of the computer secures the encryption key of the disk volume.</span></span>



| <span data-ttu-id="e4fbc-114">值</span><span class="sxs-lookup"><span data-stu-id="e4fbc-114">Value</span></span>                                                                         | <span data-ttu-id="e4fbc-115">意義</span><span class="sxs-lookup"><span data-stu-id="e4fbc-115">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4fbc-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-116"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-117"> (CRTM) 、BIOS 和平臺擴充的測量核心根信任</span><span class="sxs-lookup"><span data-stu-id="e4fbc-117">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="e4fbc-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-118"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-119">平臺和主機板設定和資料</span><span class="sxs-lookup"><span data-stu-id="e4fbc-119">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="e4fbc-120"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-120"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-121">選項 ROM 代碼</span><span class="sxs-lookup"><span data-stu-id="e4fbc-121">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="e4fbc-122"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-122"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-123">選項 ROM 設定和資料</span><span class="sxs-lookup"><span data-stu-id="e4fbc-123">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="e4fbc-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-124"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-125">主開機記錄 (MBR) 碼</span><span class="sxs-lookup"><span data-stu-id="e4fbc-125">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="e4fbc-126"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-126"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-127">主開機記錄 (MBR) 磁碟分割資料表</span><span class="sxs-lookup"><span data-stu-id="e4fbc-127">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="e4fbc-128"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-128"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-129">狀態轉換和喚醒事件</span><span class="sxs-lookup"><span data-stu-id="e4fbc-129">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="e4fbc-130"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-130"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-131">電腦 Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="e4fbc-131">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="e4fbc-132"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-132"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-133">NTFS 開機磁區</span><span class="sxs-lookup"><span data-stu-id="e4fbc-133">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e4fbc-134"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-134"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="e4fbc-135">NTFS 開機區塊</span><span class="sxs-lookup"><span data-stu-id="e4fbc-135">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="e4fbc-136"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-136"><dt>10</dt></span></span> </dl> | <span data-ttu-id="e4fbc-137">開機管理程式</span><span class="sxs-lookup"><span data-stu-id="e4fbc-137">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="e4fbc-138"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-138"><dt>11</dt></span></span> </dl> | <span data-ttu-id="e4fbc-139">BitLocker 存取控制</span><span class="sxs-lookup"><span data-stu-id="e4fbc-139">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="e4fbc-140"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-140"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e4fbc-141">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="e4fbc-141">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="e4fbc-142"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-142"><dt>13</dt></span></span> </dl> | <span data-ttu-id="e4fbc-143">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="e4fbc-143">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="e4fbc-144"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-144"><dt>14</dt></span></span> </dl> | <span data-ttu-id="e4fbc-145">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="e4fbc-145">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="e4fbc-146"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-146"><dt>15</dt></span></span> </dl> | <span data-ttu-id="e4fbc-147">定義供靜態作業系統使用</span><span class="sxs-lookup"><span data-stu-id="e4fbc-147">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="e4fbc-148"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-148"><dt>16</dt></span></span> </dl> | <span data-ttu-id="e4fbc-149">用於偵錯工具</span><span class="sxs-lookup"><span data-stu-id="e4fbc-149">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="e4fbc-150"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-150"><dt>17</dt></span></span> </dl> | <span data-ttu-id="e4fbc-151">動態 CRTM</span><span class="sxs-lookup"><span data-stu-id="e4fbc-151">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="e4fbc-152"><dt>達</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-152"><dt>18</dt></span></span> </dl> | <span data-ttu-id="e4fbc-153">已定義平臺</span><span class="sxs-lookup"><span data-stu-id="e4fbc-153">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e4fbc-154"><dt>診斷</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-154"><dt>19</dt></span></span> </dl> | <span data-ttu-id="e4fbc-155">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="e4fbc-155">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="e4fbc-156"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-156"><dt>20</dt></span></span> </dl> | <span data-ttu-id="e4fbc-157">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="e4fbc-157">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="e4fbc-158"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-158"><dt>21</dt></span></span> </dl> | <span data-ttu-id="e4fbc-159">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="e4fbc-159">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="e4fbc-160"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-160"><dt>22</dt></span></span> </dl> | <span data-ttu-id="e4fbc-161">由受信任的作業系統使用</span><span class="sxs-lookup"><span data-stu-id="e4fbc-161">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="e4fbc-162"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-162"><dt>23</dt></span></span> </dl> | <span data-ttu-id="e4fbc-163">應用程式支援</span><span class="sxs-lookup"><span data-stu-id="e4fbc-163">Application support</span></span><br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4fbc-164">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4fbc-164">Return value</span></span>

<span data-ttu-id="e4fbc-165">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e4fbc-165">Type: **uint32**</span></span>

<span data-ttu-id="e4fbc-166">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-166">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="e4fbc-167">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="e4fbc-167">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="e4fbc-168">Description</span><span class="sxs-lookup"><span data-stu-id="e4fbc-168">Description</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4fbc-169"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-169"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="e4fbc-170">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-170">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="e4fbc-171"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-171"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="e4fbc-172">*VolumeKeyProtectorID* 參數未參考「tpm」、「TPM 和 pin」、「TPM 和 Pin 和啟動金鑰」或「Tpm 和啟動金鑰」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-172">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="e4fbc-173"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-173"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="e4fbc-174">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-174">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="e4fbc-175">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-175">Add a key protector to enable BitLocker.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="e4fbc-176">備註</span><span class="sxs-lookup"><span data-stu-id="e4fbc-176">Remarks</span></span>

<span data-ttu-id="e4fbc-177">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e4fbc-178">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-178">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e4fbc-179">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e4fbc-180">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="e4fbc-180">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fbc-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4fbc-181">Requirements</span></span>



| <span data-ttu-id="e4fbc-182">需求</span><span class="sxs-lookup"><span data-stu-id="e4fbc-182">Requirement</span></span> | <span data-ttu-id="e4fbc-183">值</span><span class="sxs-lookup"><span data-stu-id="e4fbc-183">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fbc-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4fbc-184">Minimum supported client</span></span><br/> | <span data-ttu-id="e4fbc-185">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4fbc-185">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e4fbc-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4fbc-186">Minimum supported server</span></span><br/> | <span data-ttu-id="e4fbc-187">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4fbc-187">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4fbc-188">命名空間</span><span class="sxs-lookup"><span data-stu-id="e4fbc-188">Namespace</span></span><br/>                | <span data-ttu-id="e4fbc-189">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="e4fbc-189">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e4fbc-190">MOF</span><span class="sxs-lookup"><span data-stu-id="e4fbc-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4fbc-191"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4fbc-191"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4fbc-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4fbc-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fbc-193">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="e4fbc-193">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
