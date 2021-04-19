---
description: 將物件路徑中指定的邏輯檔案 (或目錄) 複製到 FileName 參數所指定的位置。
ms.assetid: 534d8b73-fc22-4a42-b8e6-24a54353bb14
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 CopyEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ec7c44ec3fc01074a0f4af70249236aa366d64bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984155"
---
# <a name="copyex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="e9b45-103">CIM LogicalFile 類別的 CopyEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e9b45-103">CopyEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="e9b45-104">**CopyEx** 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到 *FileName* 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="e9b45-104">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="e9b45-105">如果需要覆寫現有的邏輯檔案，則不支援複製。</span><span class="sxs-lookup"><span data-stu-id="e9b45-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="e9b45-106">這個方法是 [**複製**](copy-method-in-class-cim-logicalfile.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="e9b45-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9b45-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e9b45-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e9b45-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e9b45-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e9b45-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="e9b45-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e9b45-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="e9b45-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b45-111">語法</span><span class="sxs-lookup"><span data-stu-id="e9b45-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="e9b45-112">參數</span><span class="sxs-lookup"><span data-stu-id="e9b45-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9b45-113">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9b45-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-114">目的地檔 (或目錄) 的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="e9b45-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="e9b45-115">範例： "c： \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="e9b45-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-116">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9b45-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-117">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9b45-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="e9b45-118">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="e9b45-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-119">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e9b45-119">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-120">用來將子檔命名 (或目錄) 的字串，做為這個方法的起點。</span><span class="sxs-lookup"><span data-stu-id="e9b45-120">String that names the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="e9b45-121">一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="e9b45-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="e9b45-122">如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="e9b45-122">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-123">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e9b45-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-124">若為 TRUE，則此方法也會以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="e9b45-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="e9b45-125">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="e9b45-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9b45-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9b45-126">Return value</span></span>

<span data-ttu-id="e9b45-127">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="e9b45-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e9b45-128">「成功」</span><span class="sxs-lookup"><span data-stu-id="e9b45-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-129">0</span><span class="sxs-lookup"><span data-stu-id="e9b45-129">0</span></span>

<span data-ttu-id="e9b45-130">成功。</span><span class="sxs-lookup"><span data-stu-id="e9b45-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-131">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="e9b45-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-132">2</span><span class="sxs-lookup"><span data-stu-id="e9b45-132">2</span></span>

<span data-ttu-id="e9b45-133">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="e9b45-133">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-134">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="e9b45-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-135">8</span><span class="sxs-lookup"><span data-stu-id="e9b45-135">8</span></span>

<span data-ttu-id="e9b45-136">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="e9b45-136">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-137">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="e9b45-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-138">9</span><span class="sxs-lookup"><span data-stu-id="e9b45-138">9</span></span>

<span data-ttu-id="e9b45-139">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="e9b45-139">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-140">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="e9b45-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-141">10</span><span class="sxs-lookup"><span data-stu-id="e9b45-141">10</span></span>

<span data-ttu-id="e9b45-142">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="e9b45-142">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-143">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="e9b45-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-144">11</span><span class="sxs-lookup"><span data-stu-id="e9b45-144">11</span></span>

<span data-ttu-id="e9b45-145">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="e9b45-145">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-146">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="e9b45-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-147">12</span><span class="sxs-lookup"><span data-stu-id="e9b45-147">12</span></span>

<span data-ttu-id="e9b45-148">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="e9b45-148">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-149">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="e9b45-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-150">13</span><span class="sxs-lookup"><span data-stu-id="e9b45-150">13</span></span>

<span data-ttu-id="e9b45-151">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="e9b45-151">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-152">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="e9b45-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-153">14</span><span class="sxs-lookup"><span data-stu-id="e9b45-153">14</span></span>

<span data-ttu-id="e9b45-154">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="e9b45-154">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-155">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="e9b45-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-156">15</span><span class="sxs-lookup"><span data-stu-id="e9b45-156">15</span></span>

<span data-ttu-id="e9b45-157">共用違規。</span><span class="sxs-lookup"><span data-stu-id="e9b45-157">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-158">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="e9b45-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-159">16</span><span class="sxs-lookup"><span data-stu-id="e9b45-159">16</span></span>

<span data-ttu-id="e9b45-160">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="e9b45-160">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-161">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="e9b45-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-162">17</span><span class="sxs-lookup"><span data-stu-id="e9b45-162">17</span></span>

<span data-ttu-id="e9b45-163">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="e9b45-163">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="e9b45-164">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="e9b45-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e9b45-165">21</span><span class="sxs-lookup"><span data-stu-id="e9b45-165">21</span></span>

<span data-ttu-id="e9b45-166">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="e9b45-166">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9b45-167">備註</span><span class="sxs-lookup"><span data-stu-id="e9b45-167">Remarks</span></span>

<span data-ttu-id="e9b45-168">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="e9b45-168">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e9b45-169">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="e9b45-169">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e9b45-170">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e9b45-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e9b45-171">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e9b45-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b45-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9b45-172">Requirements</span></span>



| <span data-ttu-id="e9b45-173">需求</span><span class="sxs-lookup"><span data-stu-id="e9b45-173">Requirement</span></span> | <span data-ttu-id="e9b45-174">值</span><span class="sxs-lookup"><span data-stu-id="e9b45-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b45-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9b45-175">Minimum supported client</span></span><br/> | <span data-ttu-id="e9b45-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9b45-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9b45-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9b45-177">Minimum supported server</span></span><br/> | <span data-ttu-id="e9b45-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9b45-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9b45-179">命名空間</span><span class="sxs-lookup"><span data-stu-id="e9b45-179">Namespace</span></span><br/>                | <span data-ttu-id="e9b45-180">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e9b45-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9b45-181">MOF</span><span class="sxs-lookup"><span data-stu-id="e9b45-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9b45-182"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9b45-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9b45-183">DLL</span><span class="sxs-lookup"><span data-stu-id="e9b45-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9b45-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9b45-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b45-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9b45-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b45-186">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="e9b45-186">CIM\_LogicalFile</span></span>](copyex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="e9b45-187">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="e9b45-187">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

