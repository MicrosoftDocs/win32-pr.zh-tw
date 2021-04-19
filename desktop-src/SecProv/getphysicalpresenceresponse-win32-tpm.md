---
description: 傳回已執行之 TPM 實體存在作業的結果。
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Win32_Tpm 類別的 GetPhysicalPresenceResponse 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 47dfad1491b398b035e40867d10d2d3e46327dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970584"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a><span data-ttu-id="995ee-103">Win32 Tpm 類別的 GetPhysicalPresenceResponse 方法 \_</span><span class="sxs-lookup"><span data-stu-id="995ee-103">GetPhysicalPresenceResponse method of the Win32\_Tpm class</span></span>

<span data-ttu-id="995ee-104">[**Win32 \_ tpm**](win32-tpm.md)類別的 **GetPhysicalPresenceResponse** 方法會傳回已執行之 Tpm 實體存在作業的結果。</span><span class="sxs-lookup"><span data-stu-id="995ee-104">The **GetPhysicalPresenceResponse** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the results from a TPM physical presence operation that was performed.</span></span> <span data-ttu-id="995ee-105">使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法來要求作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-105">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="995ee-106">語法</span><span class="sxs-lookup"><span data-stu-id="995ee-106">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a><span data-ttu-id="995ee-107">參數</span><span class="sxs-lookup"><span data-stu-id="995ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="995ee-108">*要求* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="995ee-108">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="995ee-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="995ee-109">Type: **uint32**</span></span>

<span data-ttu-id="995ee-110">整數值，指定已執行的 TPM 實體存在作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-110">An integer value that specifies the TPM physical presence operation that was performed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="995ee-111">值</span><span class="sxs-lookup"><span data-stu-id="995ee-111">Value</span></span></th>
<th><span data-ttu-id="995ee-112">意義</span><span class="sxs-lookup"><span data-stu-id="995ee-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-113"><dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-113"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-114">沒有要求。</span><span class="sxs-lookup"><span data-stu-id="995ee-114">No request.</span></span><br/> <span data-ttu-id="995ee-115">未執行任何實體存在作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-115">No physical presence operation was performed.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-117">啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-117">Enable the TPM.</span></span><br/> <span data-ttu-id="995ee-118">作業2會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="995ee-119">如需詳細資訊，請參閱這些不牽涉實體存在的相關方法：</span><span class="sxs-lookup"><span data-stu-id="995ee-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="995ee-120"><a href="enable-win32-tpm.md"><strong>啟用</strong></a></span><span class="sxs-lookup"><span data-stu-id="995ee-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="995ee-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="995ee-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-123">停用 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-123">Disable the TPM.</span></span><br/> <span data-ttu-id="995ee-124">作業1會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="995ee-125">如需詳細資訊，請參閱此相關的方法，此方法不牽涉到實體存在： <a href="disable-win32-tpm.md"><strong>停</strong></a>用。</span><span class="sxs-lookup"><span data-stu-id="995ee-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-126"><dt>3</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-127">啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-127">Activate the TPM.</span></span><br/> <span data-ttu-id="995ee-128">作業4會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-129"><dt>4</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-130">停用 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="995ee-131">作業3會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-132"><dt>5</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-133">清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-133">Clear the TPM.</span></span><br/> <span data-ttu-id="995ee-134">這種作業無法反轉。</span><span class="sxs-lookup"><span data-stu-id="995ee-134">This operation cannot be reversed.</span></span> <br/> <span data-ttu-id="995ee-135">如需詳細資訊，請參閱此相關的方法，此方法不牽涉到實體存在： <a href="clear-win32-tpm.md"><strong>Clear</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="995ee-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-136"><dt>6</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-137">啟用並啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-137">Enable and activate the TPM.</span></span><br/> <span data-ttu-id="995ee-138">作業7會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-140">停用並停用 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="995ee-141">作業6會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-142"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-143">允許安裝 TPM 擁有者。</span><span class="sxs-lookup"><span data-stu-id="995ee-143">Allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="995ee-144">作業9會反轉這項操作。</span><span class="sxs-lookup"><span data-stu-id="995ee-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-145"><dt>9</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-146">防止安裝 TPM 擁有者。</span><span class="sxs-lookup"><span data-stu-id="995ee-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="995ee-147">作業8會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-148"><dt>10</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-149">啟用、啟用和允許安裝 TPM 擁有者。</span><span class="sxs-lookup"><span data-stu-id="995ee-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="995ee-150">作業11會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-151"><dt>rj-11</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-152">停用、停用及防止 TPM 擁有者的安裝。</span><span class="sxs-lookup"><span data-stu-id="995ee-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="995ee-153">作業10會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="995ee-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-155">延遲的實體 PresenceunownedFieldUpgrade</span><span class="sxs-lookup"><span data-stu-id="995ee-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="995ee-156">實體狀態設定已更新。</span><span class="sxs-lookup"><span data-stu-id="995ee-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="995ee-157"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="995ee-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-158"><dt>日</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-159">清除、啟用和啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="995ee-160">這種作業無法反轉。</span><span class="sxs-lookup"><span data-stu-id="995ee-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-161"><dt>長</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="995ee-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="995ee-163">設定您必須實際存在才能設定 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="995ee-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="995ee-164">作業16會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="995ee-165"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="995ee-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-166"><dt>16</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="995ee-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="995ee-168">設定您不需要實際存在才能設定 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="995ee-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="995ee-169">作業15會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="995ee-170"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="995ee-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-171"><dt>至</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="995ee-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="995ee-173">設定您必須實際存在以清除 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="995ee-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="995ee-174">作業18會反轉這項操作。</span><span class="sxs-lookup"><span data-stu-id="995ee-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="995ee-175"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="995ee-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-176"><dt>達</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="995ee-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="995ee-178">設定您不需要實際存在的布建，以清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="995ee-179">作業17會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="995ee-180"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="995ee-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-181"><dt>診斷</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="995ee-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="995ee-183">設定您必須實際存在以維護 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="995ee-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="995ee-184">作業20會反轉這項作業。</span><span class="sxs-lookup"><span data-stu-id="995ee-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="995ee-185"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="995ee-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-186"><dt>名</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="995ee-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="995ee-188">設定您必須實際存在以維護 TPM 的布建。</span><span class="sxs-lookup"><span data-stu-id="995ee-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="995ee-189">作業19會反轉這項操作。</span><span class="sxs-lookup"><span data-stu-id="995ee-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="995ee-190"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="995ee-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="995ee-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-192">啟用 + 啟用 + 清除</span><span class="sxs-lookup"><span data-stu-id="995ee-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="995ee-193">啟用、啟用和清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="995ee-194"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="995ee-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="995ee-195"><dt>日</dt> </span><span class="sxs-lookup"><span data-stu-id="995ee-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="995ee-196">啟用 + 啟用 + 清除 + 啟用 + 啟動</span><span class="sxs-lookup"><span data-stu-id="995ee-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="995ee-197">啟用、啟用和清除 TPM，然後啟用並重新啟動 TPM。</span><span class="sxs-lookup"><span data-stu-id="995ee-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="995ee-198"><strong>Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="995ee-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="995ee-199">*回應* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="995ee-199">*Response* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="995ee-200">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="995ee-200">Type: **uint32**</span></span>

<span data-ttu-id="995ee-201">整數值，指定執行 TPM 實體存在作業的結果。</span><span class="sxs-lookup"><span data-stu-id="995ee-201">An integer value that specifies the results of performing the TPM physical presence operation.</span></span>

<span data-ttu-id="995ee-202">如果實際存在的使用者確認作業，而且作業執行時沒有錯誤，則實體存在作業會成功。</span><span class="sxs-lookup"><span data-stu-id="995ee-202">A physical presence operation is successful if a physically present user confirms the operation and if the operation runs without errors.</span></span>

<span data-ttu-id="995ee-203">此值可能包含任何 TPM 錯誤。</span><span class="sxs-lookup"><span data-stu-id="995ee-203">This value may contain any TPM error.</span></span> <span data-ttu-id="995ee-204">下表列出一些常見的錯誤回應。</span><span class="sxs-lookup"><span data-stu-id="995ee-204">The following table lists some of the common error responses.</span></span>



| <span data-ttu-id="995ee-205">值</span><span class="sxs-lookup"><span data-stu-id="995ee-205">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="995ee-206">意義</span><span class="sxs-lookup"><span data-stu-id="995ee-206">Meaning</span></span>                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="995ee-207"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="995ee-207"><dt>0</dt></span></span> </dl>                                                                                                                                                                                             | <span data-ttu-id="995ee-208">要求的 TPM 操作成功。</span><span class="sxs-lookup"><span data-stu-id="995ee-208">The requested TPM operation was successful.</span></span><br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <span data-ttu-id="995ee-209"><dt>**TPM \_E \_ PPI \_ USER \_ ABORT**</dt> <dt>2150171393 (0x80290301)</dt></span><span class="sxs-lookup"><span data-stu-id="995ee-209"><dt>**TPM\_E\_PPI\_USER\_ABORT**</dt> <dt>2150171393 (0x80290301)</dt></span></span> </dl>       | <span data-ttu-id="995ee-210">使用者已拒絕要求的 TPM 操作。</span><span class="sxs-lookup"><span data-stu-id="995ee-210">The user rejected the requested TPM operation.</span></span><br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <span data-ttu-id="995ee-211"><dt>**TPM \_E \_ PPI \_ BIOS \_ 失敗**</dt> <dt>2150171394 (0x80290302)</dt></span><span class="sxs-lookup"><span data-stu-id="995ee-211"><dt>**TPM\_E\_PPI\_BIOS\_FAILURE**</dt> <dt>2150171394 (0x80290302)</dt></span></span> </dl> | <span data-ttu-id="995ee-212">執行 TPM 操作時發生 BIOS 失敗。</span><span class="sxs-lookup"><span data-stu-id="995ee-212">A BIOS failure occurred while running the TPM operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="995ee-213">傳回值</span><span class="sxs-lookup"><span data-stu-id="995ee-213">Return value</span></span>

<span data-ttu-id="995ee-214">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="995ee-214">Type: **uint32**</span></span>

<span data-ttu-id="995ee-215">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="995ee-215">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="995ee-216">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="995ee-216">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="995ee-217">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="995ee-217">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="995ee-218">Description</span><span class="sxs-lookup"><span data-stu-id="995ee-218">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="995ee-219"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="995ee-219"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="995ee-220">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="995ee-220">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="995ee-221"><dt>**TPM \_E \_ PPI \_ ACPI \_ 故障**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="995ee-221"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="995ee-222">發生硬體故障。</span><span class="sxs-lookup"><span data-stu-id="995ee-222">A hardware failure occurred.</span></span> <span data-ttu-id="995ee-223">如需詳細資訊，請洽詢您的電腦製造商。</span><span class="sxs-lookup"><span data-stu-id="995ee-223">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="995ee-224">備註</span><span class="sxs-lookup"><span data-stu-id="995ee-224">Remarks</span></span>

<span data-ttu-id="995ee-225">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="995ee-225">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="995ee-226">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="995ee-226">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="995ee-227">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="995ee-227">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="995ee-228">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="995ee-228">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="995ee-229">規格需求</span><span class="sxs-lookup"><span data-stu-id="995ee-229">Requirements</span></span>



| <span data-ttu-id="995ee-230">需求</span><span class="sxs-lookup"><span data-stu-id="995ee-230">Requirement</span></span> | <span data-ttu-id="995ee-231">值</span><span class="sxs-lookup"><span data-stu-id="995ee-231">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="995ee-232">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="995ee-232">Minimum supported client</span></span><br/> | <span data-ttu-id="995ee-233">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="995ee-233">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="995ee-234">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="995ee-234">Minimum supported server</span></span><br/> | <span data-ttu-id="995ee-235">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="995ee-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="995ee-236">命名空間</span><span class="sxs-lookup"><span data-stu-id="995ee-236">Namespace</span></span><br/>                | <span data-ttu-id="995ee-237">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="995ee-237">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="995ee-238">MOF</span><span class="sxs-lookup"><span data-stu-id="995ee-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="995ee-239"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="995ee-239"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="995ee-240">DLL</span><span class="sxs-lookup"><span data-stu-id="995ee-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="995ee-241"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="995ee-241"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="995ee-242">另請參閱</span><span class="sxs-lookup"><span data-stu-id="995ee-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="995ee-243">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="995ee-243">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="995ee-244">**清楚**</span><span class="sxs-lookup"><span data-stu-id="995ee-244">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="995ee-245">**停用**</span><span class="sxs-lookup"><span data-stu-id="995ee-245">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="995ee-246">**啟用**</span><span class="sxs-lookup"><span data-stu-id="995ee-246">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="995ee-247">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="995ee-247">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> </dl>

 

 
