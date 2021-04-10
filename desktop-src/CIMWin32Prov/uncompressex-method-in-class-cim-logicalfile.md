---
description: Uncompresses 邏輯檔案 (或在物件路徑中指定的目錄) 。 這個方法是解壓縮方法的擴充版本。
ms.assetid: 383475ba-77d4-4bfb-a241-9c37aa594a1e
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 UncompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c514939425625c15f3b683e4dc10bd5e05cb511
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689144"
---
# <a name="uncompressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="a4f2f-104">CIM LogicalFile 類別的 UncompressEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a4f2f-104">UncompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="a4f2f-105">**UncompressEx** 方法會 uncompresses 物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-105">The **UncompressEx** method uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a4f2f-106">這個方法是 [**解壓縮**](uncompress-method-in-class-cim-logicalfile.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4f2f-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a4f2f-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a4f2f-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a4f2f-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f2f-111">語法</span><span class="sxs-lookup"><span data-stu-id="a4f2f-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="a4f2f-112">參數</span><span class="sxs-lookup"><span data-stu-id="a4f2f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f2f-113">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4f2f-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-114">方法失敗 (或目錄) 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="a4f2f-115">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-116">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a4f2f-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-117">要做為方法起點的子檔案名稱 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-117">Name of the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="a4f2f-118">一般而言，此參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="a4f2f-119">如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-119">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-120">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a4f2f-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-121">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="a4f2f-122">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f2f-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4f2f-123">Return value</span></span>

<span data-ttu-id="a4f2f-124">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a4f2f-125">「成功」</span><span class="sxs-lookup"><span data-stu-id="a4f2f-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-126">0</span><span class="sxs-lookup"><span data-stu-id="a4f2f-126">0</span></span>

<span data-ttu-id="a4f2f-127">成功。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-128">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-129">2</span><span class="sxs-lookup"><span data-stu-id="a4f2f-129">2</span></span>

<span data-ttu-id="a4f2f-130">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-131">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-132">8</span><span class="sxs-lookup"><span data-stu-id="a4f2f-132">8</span></span>

<span data-ttu-id="a4f2f-133">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-134">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-135">9</span><span class="sxs-lookup"><span data-stu-id="a4f2f-135">9</span></span>

<span data-ttu-id="a4f2f-136">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-137">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-138">10</span><span class="sxs-lookup"><span data-stu-id="a4f2f-138">10</span></span>

<span data-ttu-id="a4f2f-139">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-140">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-141">11</span><span class="sxs-lookup"><span data-stu-id="a4f2f-141">11</span></span>

<span data-ttu-id="a4f2f-142">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-143">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-144">12</span><span class="sxs-lookup"><span data-stu-id="a4f2f-144">12</span></span>

<span data-ttu-id="a4f2f-145">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-146">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-147">13</span><span class="sxs-lookup"><span data-stu-id="a4f2f-147">13</span></span>

<span data-ttu-id="a4f2f-148">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-149">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-150">14</span><span class="sxs-lookup"><span data-stu-id="a4f2f-150">14</span></span>

<span data-ttu-id="a4f2f-151">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-152">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-153">15</span><span class="sxs-lookup"><span data-stu-id="a4f2f-153">15</span></span>

<span data-ttu-id="a4f2f-154">共用違規。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-155">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-156">16</span><span class="sxs-lookup"><span data-stu-id="a4f2f-156">16</span></span>

<span data-ttu-id="a4f2f-157">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-158">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-159">17</span><span class="sxs-lookup"><span data-stu-id="a4f2f-159">17</span></span>

<span data-ttu-id="a4f2f-160">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="a4f2f-161">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a4f2f-162">21</span><span class="sxs-lookup"><span data-stu-id="a4f2f-162">21</span></span>

<span data-ttu-id="a4f2f-163">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4f2f-164">備註</span><span class="sxs-lookup"><span data-stu-id="a4f2f-164">Remarks</span></span>

<span data-ttu-id="a4f2f-165">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a4f2f-166">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-166">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a4f2f-167">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-167">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a4f2f-168">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a4f2f-168">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f2f-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4f2f-169">Requirements</span></span>



| <span data-ttu-id="a4f2f-170">需求</span><span class="sxs-lookup"><span data-stu-id="a4f2f-170">Requirement</span></span> | <span data-ttu-id="a4f2f-171">值</span><span class="sxs-lookup"><span data-stu-id="a4f2f-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f2f-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4f2f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f2f-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4f2f-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4f2f-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4f2f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f2f-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4f2f-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4f2f-176">命名空間</span><span class="sxs-lookup"><span data-stu-id="a4f2f-176">Namespace</span></span><br/>                | <span data-ttu-id="a4f2f-177">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a4f2f-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4f2f-178">MOF</span><span class="sxs-lookup"><span data-stu-id="a4f2f-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4f2f-179"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4f2f-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4f2f-180">DLL</span><span class="sxs-lookup"><span data-stu-id="a4f2f-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4f2f-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4f2f-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f2f-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4f2f-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f2f-183">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="a4f2f-183">CIM\_LogicalFile</span></span>](uncompressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="a4f2f-184">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="a4f2f-184">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

