---
description: CompressEx 方法會將邏輯檔案壓縮 (或在物件路徑中指定的目錄) 。 這個方法是壓縮方法的擴充版本。
ms.assetid: 7d119865-c246-4cb5-9de4-48a4c42efd90
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 CompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7570cbe3ebc00708023a18da42ef35ff3306d3b0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847090"
---
# <a name="compressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="73289-104">CIM LogicalFile 類別的 CompressEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="73289-104">CompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="73289-105">**CompressEx** 方法會將邏輯檔案壓縮 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="73289-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="73289-106">這個方法是 [**壓縮**](compress-method-in-class-cim-logicalfile.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="73289-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73289-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="73289-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="73289-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="73289-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="73289-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="73289-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="73289-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="73289-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="73289-111">語法</span><span class="sxs-lookup"><span data-stu-id="73289-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="73289-112">參數</span><span class="sxs-lookup"><span data-stu-id="73289-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73289-113">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="73289-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73289-114">方法失敗 (或目錄) 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="73289-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="73289-115">如果方法成功，則此參數為 null。</span><span class="sxs-lookup"><span data-stu-id="73289-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="73289-116">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73289-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73289-117">要做為方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="73289-117">Child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="73289-118">一般而言，此參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="73289-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="73289-119">如果這個參數是 null，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="73289-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="73289-120">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73289-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73289-121">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="73289-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="73289-122">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="73289-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73289-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="73289-123">Return value</span></span>

<span data-ttu-id="73289-124">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="73289-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="73289-125">「成功」</span><span class="sxs-lookup"><span data-stu-id="73289-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="73289-126">0</span><span class="sxs-lookup"><span data-stu-id="73289-126">0</span></span>

<span data-ttu-id="73289-127">成功。</span><span class="sxs-lookup"><span data-stu-id="73289-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="73289-128">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="73289-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="73289-129">2</span><span class="sxs-lookup"><span data-stu-id="73289-129">2</span></span>

<span data-ttu-id="73289-130">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="73289-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="73289-131">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="73289-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="73289-132">8</span><span class="sxs-lookup"><span data-stu-id="73289-132">8</span></span>

<span data-ttu-id="73289-133">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="73289-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="73289-134">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="73289-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="73289-135">9</span><span class="sxs-lookup"><span data-stu-id="73289-135">9</span></span>

<span data-ttu-id="73289-136">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="73289-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="73289-137">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="73289-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="73289-138">10</span><span class="sxs-lookup"><span data-stu-id="73289-138">10</span></span>

<span data-ttu-id="73289-139">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="73289-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="73289-140">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="73289-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="73289-141">11</span><span class="sxs-lookup"><span data-stu-id="73289-141">11</span></span>

<span data-ttu-id="73289-142">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="73289-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="73289-143">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="73289-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="73289-144">12</span><span class="sxs-lookup"><span data-stu-id="73289-144">12</span></span>

<span data-ttu-id="73289-145">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="73289-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="73289-146">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="73289-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="73289-147">13</span><span class="sxs-lookup"><span data-stu-id="73289-147">13</span></span>

<span data-ttu-id="73289-148">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="73289-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="73289-149">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="73289-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="73289-150">14</span><span class="sxs-lookup"><span data-stu-id="73289-150">14</span></span>

<span data-ttu-id="73289-151">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="73289-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="73289-152">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="73289-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="73289-153">15</span><span class="sxs-lookup"><span data-stu-id="73289-153">15</span></span>

<span data-ttu-id="73289-154">共用違規。</span><span class="sxs-lookup"><span data-stu-id="73289-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="73289-155">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="73289-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="73289-156">16</span><span class="sxs-lookup"><span data-stu-id="73289-156">16</span></span>

<span data-ttu-id="73289-157">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="73289-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="73289-158">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="73289-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="73289-159">17</span><span class="sxs-lookup"><span data-stu-id="73289-159">17</span></span>

<span data-ttu-id="73289-160">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="73289-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="73289-161">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="73289-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="73289-162">21</span><span class="sxs-lookup"><span data-stu-id="73289-162">21</span></span>

<span data-ttu-id="73289-163">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="73289-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73289-164">備註</span><span class="sxs-lookup"><span data-stu-id="73289-164">Remarks</span></span>

<span data-ttu-id="73289-165">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="73289-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="73289-166">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="73289-166">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="73289-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="73289-167">Requirements</span></span>



| <span data-ttu-id="73289-168">需求</span><span class="sxs-lookup"><span data-stu-id="73289-168">Requirement</span></span> | <span data-ttu-id="73289-169">值</span><span class="sxs-lookup"><span data-stu-id="73289-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73289-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73289-170">Minimum supported client</span></span><br/> | <span data-ttu-id="73289-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73289-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73289-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73289-172">Minimum supported server</span></span><br/> | <span data-ttu-id="73289-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73289-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73289-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="73289-174">Namespace</span></span><br/>                | <span data-ttu-id="73289-175">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="73289-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="73289-176">MOF</span><span class="sxs-lookup"><span data-stu-id="73289-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73289-177"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="73289-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="73289-178">DLL</span><span class="sxs-lookup"><span data-stu-id="73289-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73289-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73289-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73289-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73289-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73289-181">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="73289-181">CIM\_LogicalFile</span></span>](compressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="73289-182">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="73289-182">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

