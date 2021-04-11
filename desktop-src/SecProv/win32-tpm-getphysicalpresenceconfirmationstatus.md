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
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a><span data-ttu-id="6cb94-103">Win32 \_ Tpm：： GetPhysicalPresenceConfirmationStatus 方法</span><span class="sxs-lookup"><span data-stu-id="6cb94-103">Win32\_Tpm::GetPhysicalPresenceConfirmationStatus method</span></span>

<span data-ttu-id="6cb94-104">指出指定的實體目前狀態作業是否需要實際存在的使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6cb94-104">Indicates if confirmation from a physically present user is required for a given physical presence operation.</span></span>

<span data-ttu-id="6cb94-105">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="6cb94-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb94-106">語法</span><span class="sxs-lookup"><span data-stu-id="6cb94-106">Syntax</span></span>


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6cb94-107">參數</span><span class="sxs-lookup"><span data-stu-id="6cb94-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cb94-108">*操作* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6cb94-108">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb94-109">整數值，指定需要實體存在的要求 TPM 作業。</span><span class="sxs-lookup"><span data-stu-id="6cb94-109">An integer value that specifies the requested TPM operation that requires physical presence.</span></span> <span data-ttu-id="6cb94-110">也支援廠商特有的命令。</span><span class="sxs-lookup"><span data-stu-id="6cb94-110">Vendor specific commands are supported as well.</span></span>

<span data-ttu-id="6cb94-111">*Operation* 參數可能包含下列值。</span><span class="sxs-lookup"><span data-stu-id="6cb94-111">The *Operation* parameter may consist of the following values.</span></span>



| <span data-ttu-id="6cb94-112">值</span><span class="sxs-lookup"><span data-stu-id="6cb94-112">Value</span></span>                                                                                                                               | <span data-ttu-id="6cb94-113">意義</span><span class="sxs-lookup"><span data-stu-id="6cb94-113">Meaning</span></span>                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="6cb94-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-114"><dt>1</dt></span></span> </dl>                                                        | <span data-ttu-id="6cb94-115">啟用</span><span class="sxs-lookup"><span data-stu-id="6cb94-115">Enable</span></span><br/>                                        |
| <dl> <span data-ttu-id="6cb94-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-116"><dt>2</dt></span></span> </dl>                                                        | <span data-ttu-id="6cb94-117">停用</span><span class="sxs-lookup"><span data-stu-id="6cb94-117">Disable</span></span><br/>                                       |
| <dl> <span data-ttu-id="6cb94-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-118"><dt>3</dt></span></span> </dl>                                                        | <span data-ttu-id="6cb94-119">啟動</span><span class="sxs-lookup"><span data-stu-id="6cb94-119">Activate</span></span><br/>                                      |
| <dl> <span data-ttu-id="6cb94-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-120"><dt>4</dt></span></span> </dl>                                                        | <span data-ttu-id="6cb94-121">停用</span><span class="sxs-lookup"><span data-stu-id="6cb94-121">Deactivate</span></span><br/>                                    |
| <dl> <span data-ttu-id="6cb94-122"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-122"><dt>5</dt></span></span> </dl>                                                        | <span data-ttu-id="6cb94-123">清除</span><span class="sxs-lookup"><span data-stu-id="6cb94-123">Clear</span></span><br/>                                         |
| <dl> <span data-ttu-id="6cb94-124"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-124"><dt>6</dt></span></span> </dl>                                                        | <span data-ttu-id="6cb94-125">啟用 + 啟用</span><span class="sxs-lookup"><span data-stu-id="6cb94-125">Enable + Activate</span></span><br/>                             |
| <dl> <span data-ttu-id="6cb94-126"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-126"><dt>7</dt></span></span> </dl>                                                        | <span data-ttu-id="6cb94-127">停用 + 停用</span><span class="sxs-lookup"><span data-stu-id="6cb94-127">Deactivate + Disable</span></span><br/>                          |
| <dl> <span data-ttu-id="6cb94-128"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-128"><dt>8</dt></span></span> </dl>                                                        | <span data-ttu-id="6cb94-129">SetOwnerInstall \_ True</span><span class="sxs-lookup"><span data-stu-id="6cb94-129">SetOwnerInstall\_True</span></span><br/>                         |
| <dl> <span data-ttu-id="6cb94-130"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-130"><dt>9</dt></span></span> </dl>                                                        | <span data-ttu-id="6cb94-131">SetOwnerInstall \_ False</span><span class="sxs-lookup"><span data-stu-id="6cb94-131">SetOwnerInstall\_False</span></span><br/>                        |
| <dl> <span data-ttu-id="6cb94-132"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-132"><dt>10</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-133">啟用 + 啟用 + SetOwnerInstall \_ True</span><span class="sxs-lookup"><span data-stu-id="6cb94-133">Enable + Activate + SetOwnerInstall\_True</span></span><br/>     |
| <dl> <span data-ttu-id="6cb94-134"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-134"><dt>11</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-135">SetOwnerInstall \_ False + 停用 + 停用</span><span class="sxs-lookup"><span data-stu-id="6cb94-135">SetOwnerInstall\_False + Deactivate + Disable</span></span><br/> |
| <dl> <span data-ttu-id="6cb94-136"><dt></dt><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-136"><dt></dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="6cb94-137">延遲的實體 PresenceunownedFieldUpgrade</span><span class="sxs-lookup"><span data-stu-id="6cb94-137">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> |
| <dl> <span data-ttu-id="6cb94-138"><dt></dt><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-138"><dt></dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="6cb94-139">清除 + 啟用 + 啟用</span><span class="sxs-lookup"><span data-stu-id="6cb94-139">Clear + Enable + Activate</span></span><br/>                     |
| <dl> <span data-ttu-id="6cb94-140"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-140"><dt>15</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-141">SetNoPPIProvision \_ False</span><span class="sxs-lookup"><span data-stu-id="6cb94-141">SetNoPPIProvision\_False</span></span><br/>                      |
| <dl> <span data-ttu-id="6cb94-142"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-142"><dt>16</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-143">SetNoPPIProvision \_ True</span><span class="sxs-lookup"><span data-stu-id="6cb94-143">SetNoPPIProvision\_True</span></span><br/>                       |
| <dl> <span data-ttu-id="6cb94-144"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-144"><dt>17</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-145">SetNoPPIClear \_ False</span><span class="sxs-lookup"><span data-stu-id="6cb94-145">SetNoPPIClear\_False</span></span><br/>                          |
| <dl> <span data-ttu-id="6cb94-146"><dt>達</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-146"><dt>18</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-147">SetNoPPIClear \_ True</span><span class="sxs-lookup"><span data-stu-id="6cb94-147">SetNoPPIClear\_True</span></span><br/>                           |
| <dl> <span data-ttu-id="6cb94-148"><dt>診斷</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-148"><dt>19</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-149">SetNoPPIMaintenance \_ False</span><span class="sxs-lookup"><span data-stu-id="6cb94-149">SetNoPPIMaintenance\_False</span></span><br/>                    |
| <dl> <span data-ttu-id="6cb94-150"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-150"><dt>20</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-151">SetNoPPIMaintenance \_ True</span><span class="sxs-lookup"><span data-stu-id="6cb94-151">SetNoPPIMaintenance\_True</span></span><br/>                     |
| <dl> <span data-ttu-id="6cb94-152"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-152"><dt>21</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-153">啟用 + 啟用 + 清除</span><span class="sxs-lookup"><span data-stu-id="6cb94-153">Enable + Activate + Clear</span></span><br/>                     |
| <dl> <span data-ttu-id="6cb94-154"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-154"><dt>22</dt></span></span> </dl>                                                       | <span data-ttu-id="6cb94-155">啟用 + 啟用 + 清除 + 啟用 + 啟動</span><span class="sxs-lookup"><span data-stu-id="6cb94-155">Enable + Activate + Clear + Enable + Activate</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6cb94-156">*ConfirmationStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6cb94-156">*ConfirmationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb94-157">傳回實體存在性命令的確認狀態。</span><span class="sxs-lookup"><span data-stu-id="6cb94-157">Returns the confirmation status for physical presence command.</span></span>

<span data-ttu-id="6cb94-158">*ConfirmationStatus* 參數可能包含下列值。</span><span class="sxs-lookup"><span data-stu-id="6cb94-158">The *ConfirmationStatus* parameter may consist of the following values.</span></span>



| <span data-ttu-id="6cb94-159">值</span><span class="sxs-lookup"><span data-stu-id="6cb94-159">Value</span></span>                                                                        | <span data-ttu-id="6cb94-160">意義</span><span class="sxs-lookup"><span data-stu-id="6cb94-160">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6cb94-161"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-161"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6cb94-162">未實作</span><span class="sxs-lookup"><span data-stu-id="6cb94-162">Not implemented</span></span><br/>                                             |
| <dl> <span data-ttu-id="6cb94-163"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-163"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6cb94-164">僅限 BIOS。</span><span class="sxs-lookup"><span data-stu-id="6cb94-164">BIOS only.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="6cb94-165"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-165"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6cb94-166">BIOS 設定已封鎖作業系統。</span><span class="sxs-lookup"><span data-stu-id="6cb94-166">Blocked for the operating system by the BIOS configuration.</span></span><br/> |
| <dl> <span data-ttu-id="6cb94-167"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-167"><dt>3</dt></span></span> </dl> | <span data-ttu-id="6cb94-168">允許且實際呈現使用者需求。</span><span class="sxs-lookup"><span data-stu-id="6cb94-168">Allowed and physically present user required.</span></span><br/>               |
| <dl> <span data-ttu-id="6cb94-169"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-169"><dt>4</dt></span></span> </dl> | <span data-ttu-id="6cb94-170">允許且實際呈現使用者不需要</span><span class="sxs-lookup"><span data-stu-id="6cb94-170">Allowed and physically present user not required</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cb94-171">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cb94-171">Return value</span></span>

<span data-ttu-id="6cb94-172">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6cb94-172">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="6cb94-173">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="6cb94-173">Common return codes are listed below.</span></span>



| <span data-ttu-id="6cb94-174">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="6cb94-174">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="6cb94-175">Description</span><span class="sxs-lookup"><span data-stu-id="6cb94-175">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6cb94-176"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-176"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6cb94-177">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="6cb94-177">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6cb94-178">備註</span><span class="sxs-lookup"><span data-stu-id="6cb94-178">Remarks</span></span>

<span data-ttu-id="6cb94-179">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6cb94-179">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6cb94-180">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6cb94-180">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6cb94-181">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6cb94-181">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6cb94-182">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="6cb94-182">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb94-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cb94-183">Requirements</span></span>



| <span data-ttu-id="6cb94-184">需求</span><span class="sxs-lookup"><span data-stu-id="6cb94-184">Requirement</span></span> | <span data-ttu-id="6cb94-185">值</span><span class="sxs-lookup"><span data-stu-id="6cb94-185">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb94-186">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cb94-186">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb94-187">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cb94-187">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6cb94-188">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cb94-188">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb94-189">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cb94-189">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6cb94-190">命名空間</span><span class="sxs-lookup"><span data-stu-id="6cb94-190">Namespace</span></span><br/>                | <span data-ttu-id="6cb94-191">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="6cb94-191">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="6cb94-192">MOF</span><span class="sxs-lookup"><span data-stu-id="6cb94-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cb94-193"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-193"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cb94-194">DLL</span><span class="sxs-lookup"><span data-stu-id="6cb94-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cb94-195"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cb94-195"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cb94-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cb94-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb94-197">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="6cb94-197">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
