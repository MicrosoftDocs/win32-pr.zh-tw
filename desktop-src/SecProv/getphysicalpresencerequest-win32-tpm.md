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
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a><span data-ttu-id="e3a9a-104">Win32 Tpm 類別的 GetPhysicalPresenceRequest 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e3a9a-104">GetPhysicalPresenceRequest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="e3a9a-105">[**Win32 \_ tpm**](win32-tpm.md)類別的 **GetPhysicalPresenceRequest** 方法會傳回暫止的 tpm 實體存在性作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-105">The **GetPhysicalPresenceRequest** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="e3a9a-106">使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法來要求作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a9a-107">語法</span><span class="sxs-lookup"><span data-stu-id="e3a9a-107">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a><span data-ttu-id="e3a9a-108">參數</span><span class="sxs-lookup"><span data-stu-id="e3a9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a9a-109">*要求* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e3a9a-109">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a9a-110">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e3a9a-110">Type: **uint32**</span></span>

<span data-ttu-id="e3a9a-111">值，指定暫止的 TPM 實體存在性作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-111">A value that specifies the pending TPM physical presence operation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3a9a-112">值</span><span class="sxs-lookup"><span data-stu-id="e3a9a-112">Value</span></span></th>
<th><span data-ttu-id="e3a9a-113">意義</span><span class="sxs-lookup"><span data-stu-id="e3a9a-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-114"><dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-114"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-115">沒有要求。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-115">No request.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-117">啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-117">Enable the TPM.</span></span><br/> <span data-ttu-id="e3a9a-118">作業2會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="e3a9a-119">如需詳細資訊，請參閱這些不牽涉實體存在的相關方法：</span><span class="sxs-lookup"><span data-stu-id="e3a9a-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="e3a9a-120"><a href="enable-win32-tpm.md"><strong>啟用</strong></a></span><span class="sxs-lookup"><span data-stu-id="e3a9a-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="e3a9a-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="e3a9a-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-123">停用 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-123">Disable the TPM.</span></span><br/> <span data-ttu-id="e3a9a-124">作業1會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="e3a9a-125">如需詳細資訊，請參閱此相關的方法，此方法不牽涉到實體存在： <a href="disable-win32-tpm.md"><strong>停</strong></a>用。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-126"><dt>3</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-127">啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-127">Activate the TPM.</span></span><br/> <span data-ttu-id="e3a9a-128">作業4會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-129"><dt>4</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-130">停用 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="e3a9a-131">作業3會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-132"><dt>5</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-133">清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-133">Clear the TPM.</span></span><br/> <span data-ttu-id="e3a9a-134">這種作業無法反轉。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-134">This operation cannot be reversed.</span></span><br/> <span data-ttu-id="e3a9a-135">如需詳細資訊，請參閱此相關的方法，此方法不牽涉到實體存在： <a href="clear-win32-tpm.md"><strong>Clear</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-136"><dt>6</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-137">啟用並啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-137">Enable and activate the TPM.</span></span> <br/> <span data-ttu-id="e3a9a-138">作業7會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-140">停用並停用 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="e3a9a-141">作業6會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-142"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-143">允許安裝 TPM 擁有者。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-143">Allow the installation of a TPM owner.</span></span> <br/> <span data-ttu-id="e3a9a-144">作業9會反轉這項操作。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-145"><dt>9</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-146">防止安裝 TPM 擁有者。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="e3a9a-147">作業8會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-148"><dt>10</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-149">啟用、啟用和允許安裝 TPM 擁有者。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="e3a9a-150">作業11會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-151"><dt>rj-11</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-152">停用、停用及防止 TPM 擁有者的安裝。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="e3a9a-153">作業10會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="e3a9a-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-155">延遲的實體 PresenceunownedFieldUpgrade</span><span class="sxs-lookup"><span data-stu-id="e3a9a-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="e3a9a-156">實體狀態設定已更新。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="e3a9a-157"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-158"><dt>日</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-159">清除、啟用和啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="e3a9a-160">這種作業無法反轉。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-161"><dt>長</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="e3a9a-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="e3a9a-163">設定您必須實際存在才能設定 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="e3a9a-164">作業16會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="e3a9a-165"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-166"><dt>16</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="e3a9a-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="e3a9a-168">設定您不需要實際存在才能設定 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="e3a9a-169">作業15會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="e3a9a-170"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-171"><dt>至</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="e3a9a-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="e3a9a-173">設定您必須實際存在以清除 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="e3a9a-174">作業18會反轉這項操作。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="e3a9a-175"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-176"><dt>達</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="e3a9a-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="e3a9a-178">設定您不需要實際存在的布建，以清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="e3a9a-179">作業17會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="e3a9a-180"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-181"><dt>診斷</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="e3a9a-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="e3a9a-183">設定您必須實際存在以維護 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="e3a9a-184">作業20會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="e3a9a-185"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-186"><dt>名</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="e3a9a-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="e3a9a-188">設定您必須實際存在以維護 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="e3a9a-189">作業19會反轉這項操作。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="e3a9a-190"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e3a9a-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-192">啟用 + 啟用 + 清除</span><span class="sxs-lookup"><span data-stu-id="e3a9a-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="e3a9a-193">啟用、啟用和清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="e3a9a-194"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e3a9a-195"><dt>日</dt> </span><span class="sxs-lookup"><span data-stu-id="e3a9a-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="e3a9a-196">啟用 + 啟用 + 清除 + 啟用 + 啟動</span><span class="sxs-lookup"><span data-stu-id="e3a9a-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="e3a9a-197">啟用、啟用和清除 TPM，然後啟用並重新啟動 TPM。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="e3a9a-198"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a9a-199">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3a9a-199">Return value</span></span>

<span data-ttu-id="e3a9a-200">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e3a9a-200">Type: **uint32**</span></span>

<span data-ttu-id="e3a9a-201">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-201">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="e3a9a-202">下表列出常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-202">The following table lists the common return codes.</span></span>



| <span data-ttu-id="e3a9a-203">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="e3a9a-203">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="e3a9a-204">Description</span><span class="sxs-lookup"><span data-stu-id="e3a9a-204">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3a9a-205"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a9a-205"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="e3a9a-206">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-206">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="e3a9a-207"><dt>**TPM \_E \_ PPI \_ ACPI \_ 故障**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a9a-207"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="e3a9a-208">發生硬體故障。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-208">A hardware failure occurred.</span></span> <span data-ttu-id="e3a9a-209">如需詳細資訊，請洽詢您的電腦製造商。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-209">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3a9a-210">備註</span><span class="sxs-lookup"><span data-stu-id="e3a9a-210">Remarks</span></span>

<span data-ttu-id="e3a9a-211">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-211">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e3a9a-212">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-212">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e3a9a-213">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-213">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e3a9a-214">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="e3a9a-214">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a9a-215">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3a9a-215">Requirements</span></span>



| <span data-ttu-id="e3a9a-216">需求</span><span class="sxs-lookup"><span data-stu-id="e3a9a-216">Requirement</span></span> | <span data-ttu-id="e3a9a-217">值</span><span class="sxs-lookup"><span data-stu-id="e3a9a-217">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a9a-218">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3a9a-218">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a9a-219">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3a9a-219">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e3a9a-220">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3a9a-220">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a9a-221">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3a9a-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e3a9a-222">命名空間</span><span class="sxs-lookup"><span data-stu-id="e3a9a-222">Namespace</span></span><br/>                | <span data-ttu-id="e3a9a-223">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="e3a9a-223">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="e3a9a-224">MOF</span><span class="sxs-lookup"><span data-stu-id="e3a9a-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3a9a-225"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3a9a-225"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3a9a-226">DLL</span><span class="sxs-lookup"><span data-stu-id="e3a9a-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3a9a-227"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3a9a-227"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a9a-228">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3a9a-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a9a-229">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="e3a9a-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="e3a9a-230">**清楚**</span><span class="sxs-lookup"><span data-stu-id="e3a9a-230">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="e3a9a-231">**停用**</span><span class="sxs-lookup"><span data-stu-id="e3a9a-231">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="e3a9a-232">**啟用**</span><span class="sxs-lookup"><span data-stu-id="e3a9a-232">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="e3a9a-233">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e3a9a-233">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="e3a9a-234">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="e3a9a-234">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
